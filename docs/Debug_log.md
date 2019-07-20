# Locating the debug log

You've probably been sent here because you've been asked to locate your
debug log, probably to send to the developers so they can (hopefully\!)
work out what's causing a problem that you're having.

The file name is **quelea-debuglog.txt**. Note that when sending the
debug log, it's important to start Quelea, reproduce the problem that
you're having, close Quelea and *then* locate and send the debug log -
it gets refreshed each time you launch Quelea, so if you launch it,
don't reproduce the problem then send us the log, we won't be able to
tell much\!

The location of the debug log depends on your OS, in general it is in
the user home area inside a '.quelea' folder.

## Windows

In Windows, it should be in this path:

C:\\users\\USERNAME\\.quelea\\

## Linux

In Ubuntu, it is located in:

/home/USERNAME/.quelea

Other distributions should be similar - the ".quelea" folder will always
be in "~/.quelea", so it should be relatively easy to find this whatever
version of \*nix you're running.

## MacOS

It should be located in:

/Users/USERNAME/.quelea

You can hit "cmd+shift+g" in finder (go to location), then paste this
path in (replacing USERNAME with your username), and you should be able
to see the debug log there.

Alternatively, open a terminal prompt and type:

`open` `~/.quelea`

---
