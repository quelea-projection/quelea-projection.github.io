This document outlines the current options in the Quelea Remote Server
that can be utilised in

One-way requests should be fetched without affecting the current page,
and their results should be discarded. Continuous refresh requests
should be constantly refreshed for the latest version and their results
updated in display

### /

''' Root page '''

The root page will either show a login screen, or if you have logged in
it will show the main screen used in the webpage version.

  - Login screen
    A simple box and button. A POST request to / with the password
    stored in a "password" variable.
  - Main screen
    If the user has been logged in (i.e, their IP address on the network
    is saved into a local list of logged in users) then the main screen
    will show.

This will most likely not be used in any apps.

### /logout

''' Logout Page '''

Visiting this page will log out the current user, removing their IP
address from a list of currently known IP addresses.

This will most likely not be used in any apps.

### /tlogo

''' Toggle Logo '''

One-way request to toggle whether the logo is on or not.

### /black

''' Toggle Black '''

One-way request to toggle whether the screen is blacked or not.

### /clear

''' Toggle Clear '''

One-way request to toggle whether the screen is cleared of lyrics or
not.

### /next

''' Next Slide '''

One-way request to Quelea to move to the next slide

### /prev

''' Previous Slide '''

One-way request to Quelea to move to the previous slide

### /nextitem

''' Next Item '''

One-way request to Quelea to move to the next item in the schedule

### /previtem

''' Previous Item '''

One-way request to Quelea to move to the next item in the schedule

### /play

''' Play Video '''

One-way request to Quelea to toggle play/pause on a video

### /lyrics

''' Lyrics Page '''

HTML formatted, continuous refresh request of the current live item in
Quelea. All items return a message of "\<i\>Currently Displaying: {item
name}\</i\>" followed by HTML depending on the type of item:

  - Song/Bible Passage
    List of all lyrics of the item, CSS formatted as such:

`[outer]`
`  [inner]Verse 1[/inner]`
`  [inner current]Verse 2 - Currently selected[/inner]`
`  [inner]Verse 3[/inner]`
`[/outer]`

and HTML formatted as such:

`<div>`
`  <div><p class="empty" onclick="section(0)">Verse 1</p></div>`
`  <div><p class="empty" onclick="section(1)"Verse 2</p></div>`
`  <div><p class="empty" onclick="section(2)"Verse 3</p></div>`
`</div>`

Where section() is a one-way request link to /section (see below)

  - Video
    HTML of

<button type="button" onclick="play();" id="playbutton">`Play`</button>

where play() uses /play (see above)

  - Other
    Displays "Empty Lyrics"

### /section

''' Section Selector '''

One-way request to tell Quelea to change the selected slide to a
specific slide number. Use: /section0 to go to first slide, /section1
goes to second slide, etc. Used in conjunction with /lyrics to make the
lyrics hyperlinkable to navigate slide.

### /status

''' Status Selector '''

Continuous refresh. Returns:

`logo,black,clear,video`

where logo, black and clear equal true if they are currently selected,
false if not and video is a string used in the button for /lyrics (in
English, it returns "Play" or "Pause")

### /schedule

''' Schedule List '''

Continuous refresh at reduced speed. Lists the items in the schedule,
HTML formatted as italics for queued item (in the Preview Window), bold
for currently live item (in the Live Panel) and normal for any other
items.

### /songsearch

''' Song Search Page '''

A page containing a textbox and button. Button sends the text in the
textbox to /search/

Not likely to be used in Apps

### /search

''' Database Search '''

### /song

''' Song Information '''

### /add

''' Add Song '''

### /addbible

''' Add Bible Page '''

### /translations

''' Bible Translations list '''

### /books

''' Bible Book List '''

### /passage

''' Bible Passage List '''---

---
