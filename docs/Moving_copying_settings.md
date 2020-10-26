# Moving or copying your settings
If you are installing Quelea on a second machine, or are swapping to a new one, it is possible to copy (or move) your existing settings and databases.  This will save set up time.  All Quelea's settings are stored in the `.quelea` folder in your user's home area or login profile.  On Linux / Mac the `.quelea` folder will be hidden in your home area.  For Windows it's located under `C:\Users\<username>`, for example `C:\Users\fred\.quelea`.

Ensure Quelea is closed on both the source and destination computer, then simply copy your `.quelea` folder to removable storage (e.g. a USB stick) or to network / cloud storage.  Paste a copy of `.quelea` in the relevant place on the destination machine.  When you start Quelea on the new computer it will have the same settings as on the old one.

**Note:** This will *not* keep the two copies in sync.  Any changes you make on one will have to be replicated on the other.

## Can multiple users on the same computer use the same settings?
Yes, you can use something called a _symlink_ (symbolic link) to achieve this.  Copy your settings to a shared location, that all the users can read and write to.  Then create a symlink from the user's normal `.quelea` folder to point at the shared copy.  Consult your Operating System documentation for instructions on making a symlink.

**Note:** Only one user of the computer will be able to use Quelea at a time.

-----


[← Installation instructions](Installation_Instructions) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[Short introduction to Quelea
→](Short_introduction_to_Quelea)

---
