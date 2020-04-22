# Troubleshooting

If you cannot find the answer to the problem you are looking for here,
search for your issue in the [discussion group](https://quelea.discourse.group). If you cannot
find any information about your issues there already, feel free to ask a
new question.

## The video background flickers as it repeats

Some users have reported the following to help with this:

1.  Open VLC
2.  Open _preferences_
3.  Find _Video_
4.  Uncheck the box _Accelerated video output (Overlay)_

In newer versions, that option doesn't exist, so you'll need to do this:

1.  Open VLC
2.  Open _preferences_
3.  Select _All_ under _Show settings_ (bottom left)
4.  Select _Video_ -&gt; _Output modules_
5.  Under _Video output module_, select _DirectDraw_
6.  Select _Video_ -&gt; _Output modules_ -&gt; _DirectDraw_
7.  Uncheck _Overlay video output_

If you still experience issues, try downgrading VLC to [an older version](http://download.videolan.org/pub/videolan/vlc/2.2.0/win64/vlc-2.2.0-win64.exe) and see if that helps.

## My animations/transitions in a presentation do not appear

Try to use the native [PowerPoint or OpenOffice
support](Presentations_tab "Presentations tab") instead. The built-in
presentation feature converts your presentation to a set of images and
will therefore not preserve any transitions or any other effects you
might have added. There is no flawless solution yet due to technical
difficulties, so use the solution you feel best suits your needs or use
separate software for your presentation needs.

## The font size is too small

The font size is automatically calculated based on how much text there is per section, so these may help:

* Try to split the text into more sections by adding a blank line
* Set a [maximum amount of verses per slide for a Bible passage](Bible_tab#layout-of-bible_passages "Bible tab")
* Change the [maximum font size](General_tab#maximum-font-size "Bible tab") to a higher value
* Lower the [maximum amount of characters per line](General_tab#maximum-characters-per-line "Bible tab")
* Uncheck the [uniform font size](General_tab#use-uniform-font-size "Bible tab")

## VLC is not found even though it is installed

It is probably because your VLC version is incompatible with Quelea. 
You cannot use a 64-bit version of VLC with Quelea if you use the 
32-bit installer of Quelea and vice versa. To check if this is the 
case for Windows users, an easy way is to look in your `Program Files` 
(usually `C:\Program Files`) folder. If this is the issue you will most 
likely also find a folder called `Program Files (x86)` that contains 
your 32-bit installations. 

If Quelea is in one folder (for example `C:\Program Files`) and VLC 
is in the other (for example `C:\Program Files (x86`) you will need to 
download and install the corresponding versions of the software.

## I cannot select Output 2 although the projector is connected

First of all, check that you see anything from the computer on the 
projector. With Quelea you have to use what usually is called 
_Extended Desktop_, which means that the desktop becomes wider, 
stretching from your computer and onto your projector, allowing 
you to drag a window past the edge of one screen an onto the next. 
If you see the same things on both screens, the screen is _cloned_ 
and not extended. In that case, that is probably the problem and you 
need to change the graphics settings of your computer for that 
(often there is a keyboard shortcut for this, accessible with help of 
the _fn_ button, or _windows key + p_). If you do not see anything on 
your projector, it is probably that the computer is set to only use the 
local screen and you change that setting the same way as above. 

## I cannot play YouTube videos

Due to video encryption that seems to be added to more and more YouTube 
videos today, YouTube support has been removed by default as of Quelea 2017.0. 
An option would be to play the videos using the [website feature](Displaying_a_website "Displaying a website") 
(tip: use the "Embed" link). Another possible work-around would be to use 
one of the many services that offers you to download YouTube videos and 
then add it to the schedule as a regular video. If you really need this 
feature and are aware of the fact that most videos will not work, 
contact the developers in the discussion forum on how to re-enable it.

## Recordings does not work

On Mac computers, all software that need access to the microphone must
request permissions to use it. Java (which Quelea is written in) has
currently no way to specifically ask for it. Some users have reported
that they get the permission request when they run the software as administrators.
You could also try seeing if using the cross-platform installation
helps you. If you are experiencing issues with another operating system,
such as Window, feel free to [open an issue for it](https://github.com/quelea-projection/Quelea/issues).

-----



[← Previous chapter - Shortcuts and other things that are good to
know](Shortcuts_and_other_things_that_are_good_to_know "Shortcuts and other things that are good to know")
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Chapter 7 - FAQ (Frequently Asked Questions) →](FAQ_(Frequently_Asked_Questions) "FAQ (Frequently Asked Questions)")

---
