If you cannot find the answer to the problem you are looking for here,
search for your issue in the discussion group:
<https://groups.google.com/forum/#!forum/quelea-discuss>. If you cannot
find any information about your issues there already, feel free to ask a
new question.

## The video background flickers as it repeats

Some users have reported the following to help with this:

1.  Open VLC
2.  Open preference
3.  Find "Video".
4.  Uncheck the box "Accelerated video output (Overlay)

In newer versions, that option doesn't exist, so you'll need to do this:

1.  Open VLC
2.  Open preference
3.  Select "All" under "Show settings" (bottom left)
4.  Select "Video" -\> Output modules
5.  Under Video output module, select DirectDraw.
6.  Select "Video" -\> Output modules -\> DirectDraw
7.  Uncheck "Overlay video output".

## My animations/transitions in a presentation do not appear

Try to use the native [PowerPoint or OpenOffice
support](Presentations_tab.md "Presentations tab") instead. The built-in
presentation feature converts your presentation to a set of images and
will therefore not preserve any transitions or any other effects you
might have added. There is no flawless solution yet due to technical
difficulties, so use the solution you feel best suits your needs or use
a separate software for you presentation needs.

## The font size is too small

The font size is automatically calculated based on how much text there
is per section. Try to split the text into more sections by adding a
blank line/set a [maximum amount of verses per slide for a Bible
passage](Bible_tab.md#layout-of-bible-passages "Bible tab"), change the
[maximum font size](General_tab.md#maximum-font-size "General tab") to a
higher value, lower the [maximum amount of characters per
line](General_tab.md#maximum-characters-per-line "General tab") or uncheck the
[uniform font size](General_tab.md#use-uniform-font-size "General tab") and
see if anything helps you.

## VLC is not found even though it is installed

It is probably because your VLC version is incompatible with Quelea. You
cannot use a 64-bit version of VLC with Quelea if you use the 32-bit
installer of Quelea and vice versa. To check if this is the case for
Windows users, an easy way is to look in your Program Files folder. If
this is the issue you will most likely also find a folder called Program
Files (x86) that contains your 32-bit installations. If you look in the
two Program Files folder, Quelea should in that case be installed in one
of them and VLC in the other. If that is the case, download and install
the corresponding versions of the software.

## I cannot select Output 2 although the projector is connected

First of all, check that you see anything from the computer on the
projector. With Quelea you have to use what usually is called Extended
Desktop, which means that the desktop becomes wider, stretching from
your computer and onto your projector, allowing you to drag a window
past the edge of one screen an onto the next. If you see the same things
on both screens, the screen is cloned and not extended. In that case,
that is probably the problem and you need to change the graphics
settings of your computer for that (often there is a keyboard shortcut
for this, accessible with help of the fn button, or windows key + p). If
you do not see anything on your projector, it is probably that the
computer is set to only use the local screen and you change that setting
the same way as above. 

## I cannot play YouTube videos

Due to video encryption that seems to be added to more and more YouTube
videos today, YouTube support has been removed by default in Quelea
2017.0. A possible work-around would be to use one of the many services
that offers you to download YouTube videos and then add it to the
schedule as a regular video. If you really need this feature, contact
the developers in the discussion forum on how to re-enable it.

-----



[← Previous chapter - Shortcuts and other things that are good to
know](Shortcuts_and_other_things_that_are_good_to_know.md "Shortcuts and other things that are good to know")
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [Chapter 7 - FAQ (Frequently Asked Questions) →](FAQ_(Frequently_Asked_Questions).md "FAQ (Frequently Asked Questions)")

---
