# Remote Control API

This document outlines the options in the Quelea Remote Server
that can be utilised in. A few more have been added since this document was
created and will be added here eventually. The full list in the source code can
be found [here](https://github.com/quelea-projection/Quelea/blob/8cb07de3e2df3b29927b01f86babd8c968444cdd/Quelea/src/main/java/org/quelea/server/RemoteControlServer.java#L100-L134).

**Continuous refresh requests** should be constantly refreshed 
for the latest version and their results updated in display. 

**One-way requests** should be fetched without affecting the current page,
and their results should be discarded. 

**Two-way requests** should be used to fetch information
from Quelea to later be used for one-way requests.

---

## Overview

1. [Continuous refresh requests](#continuous-refresh-requests)
    1. [Lyrics](#/lyrics)
    1. [Status](#/status)
    1. [Schedule](#/schedule)
1. [One-way requests](#one-way-requests)
    1. [Logout](#/logout)
    1. [Toggle logo](#/tlogo)
    1. [Toggle black](#/black)
    1. [Toggle clear](#/clear)
    1. [Next slide](#/next)
    1. [Previous slide](#/prev)
    1. [Next item](#/nextitem)
    1. [Previous item](#/previtem)
    1. [Play video](#/play)
    1. [Record](#/record)
    1. [Add a song](#/add)
    1. [Add a Bible passage](#/addbible)
    1. [Select a section](#/section)
1. [Two-way requests](#two-way-requests)
    1. [Database search](#/search)
    1. [Get song information](#/song)
    1. [Get Bible translations](#/translations)
    1. [Get Bible translation books](#/books)
1. [Other requests](#other-requests)
    1. [Root page](#/)
    1. [Song search page](#/songsearch)
    1. [Bible add page](#/passage)

---

## Continuous refresh requests

### /lyrics

**Lyrics Page**

HTML formatted, continuous refresh request of the current live item in
Quelea. All items return a message of `<i>Currently Displaying: {item
name}</i>` followed by HTML depending on the type of item:

##### Song/Bible Passage

List of all lyrics of the item, CSS formatted as such:
```
[outer]
  [inner]Verse 1[/inner]
  [inner current]Verse 2 - Currently selected[/inner]
  [inner]Verse 3[/inner]
[/outer]
```
and HTML formatted as such:
```
<div>
  <div><p class="empty" onclick="section(0)">Verse 1</p></div>
  <div><p class="empty" onclick="section(1)"Verse 2</p></div>
  <div><p class="empty" onclick="section(2)"Verse 3</p></div>
</div>
```
Where section() is a one-way request link to /section (see below)

##### Video HTML

`<button type="button" onclick="play();" id="playbutton">Play</button>`

where play() uses /play (see above)

##### Other

Displays "Empty Lyrics", i.e. `<i>Lyrics will be displayed here</i>`

### /status

**Status Selector**

Continuous refresh. Returns:

```
logo,black,clear,video,record
```

where logo, black, clear and record equal true if they are currently selected,
false if not and video is a string used in the button for `/lyrics` (in
English, it returns "Play" or "Pause")

### /schedule

**Schedule List**

Continuous refresh at reduced speed. Lists the items in the schedule,
HTML formatted as italics for queued item (in the Preview Window), bold
for currently live item (in the Live Panel) and normal for any other
items. The website is formatted the following way:

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
</head>
[Song Title - Song Author]<br/>
<b>[Song Title - Song Author (Live Item)]</b><br/>
<i>[Song Title - Song Author (Preview Item)]</i><br/>
</html>
```

---

## One-way requests

### /logout

**Logout Page**

Visiting this page will log out the current user, removing their IP
address from a list of currently known IP addresses.

This will most likely not be used in any apps.

### /tlogo

**Toggle Logo**

One-way request to toggle whether the logo is on or not.

### /black

**Toggle Black**

One-way request to toggle whether the screen is blacked or not.

### /clear

**Toggle Clear**

One-way request to toggle whether the screen is cleared of lyrics or
not.

### /next

**Next Slide**

One-way request to Quelea to move to the next slide

### /prev

**Previous Slide**

One-way request to Quelea to move to the previous slide

### /nextitem

**Next Item**

One-way request to Quelea to move to the next item in the schedule

### /previtem

**Previous Item**

One-way request to Quelea to move to the next item in the schedule

### /play

**Play Video**

One-way request to Quelea to toggle play/pause on a video

### /record

One-way request to Quelea to start/stop a recording

### /add

**Add Song**
```
/add/[ID]
```
 adds a song to the schedule. Returns `Add Successful` if no
errors occur. Use `/search` below to find a song ID.

### /addbible

**Add Bible Page**

```
/addbible/[Bible Translation]/[Book]/[Chapter]:[Verse]
```
adds a Bible passage
to the schedule. Returns `Add Successful` if no errors occur. Use the two-way
methods below to fetch the `/translations` and `/books`.

### /section

**Section Selector**

One-way request to tell Quelea to change the selected slide to a
specific slide number. Use: `/section0` to go to first slide, `/section1`
goes to second slide, etc. Used in conjunction with `/lyrics` to make the
lyrics hyperlinkable to navigate slide.

---

## Two-way requests

### /search

**Database Search**

```
/search/[search-phrase]
```
returns a website of links to the songs containing
the search phrase. The page is formatted like this:

```
<!DOCTYPE html><html><head><meta charset="UTF-8"></head>
<a href="/song/[ID-int]">[Song title]</a><br/>
...
</html>
```
where `[ID-int]` refers to the integer ID number of the song.
The link directs to the song information below.

### /song

**Song Information**

```
/song/[ID]
```
returns a website containing the title, author and lyrics of a 
song. The page is formatted the following way:

```
<!DOCTYPE html><html><head><meta charset="UTF-8"></head>
[Title]<br/>
[Author]<br/><br/>
[Song Lyrics, including section titles]<br/><br/>
<a href="/add/[ID-int]">Add Song to Schedule</a></html>
```
where `[ID-int]` refers to the integer ID number of the song.
The link directs to the song add page below.

### /translations

**Bible Translations list**

Returns a list of all available Bible translations in plain text, separated
by a line break.

### /books

**Bible Book List**

```
/books/[Translation]
```
returns a list of all available Bible books 
in the selected translation in plain text, separated by a line break.

---

## Other requests

### /

**Root page**

The root page will either show a login screen, or if you have logged in
it will show the main screen used in the web page version.

  - Login screen
    A simple box and button. A POST request to / with the password
    stored in a "password" variable.
  - Main screen
    If the user has been logged in (i.e, their IP address on the network
    is saved into a local list of logged in users) then the main screen
    will show.

This will most likely not be used in any apps.

### /songsearch

**Song Search Page**

A page containing a textbox and button. Button sends the text in the
textbox to `/search/`

Not likely to be used in Apps

### /passage

**Bible Passage List**

A page containing two selectors (for Bible translation and Bible book), 
a textbox and button. Button sends the text in the textbox, along with 
the selections from Bible translation and Bible book to `/add/`

Not likely to be used in Apps

---
