# Installation instructions

## System requirements

Quelea should run on Windows, Linux or MacOS. Most of the developers use
Windows in their day to day work on Quelea, so that will be the most
stable platform by implication. The cross platform jar installer 
(which will require the JRE to be installed first) should work on all
operating systems, but there is also native installers which you can
read about below.

Generally, any modern machine should be ok to run Quelea, but we would
recommend at a minimum:

* 4GB RAM
* 5GB free hard drive space
* Dual display outputs (triple display output required for stage view)
* SSD (not required, but start up times will be much faster.)

Realistically, any machine purchased or built in the last few years
should be fine.

## Windows Install

The `.exe` file provided on the downloads file should work with most
computers, if you have any problems post on the Quelea Discourse Discuss
Group found
[here](https://quelea.discourse.group/).

## Mac Install

Download the `.zip` file and extract it. Then you can drag the icon into
the Applications folder and you should be able to run it as any other
application.

## Linux Install

### Using Snap

The main method to install Quelea on a Linux system is through Snap. 
If you use a Ubuntu-based distribution, it should already be installed. 
If it is not installed, read about how you install it [here](https://snapcraft.io/docs/installing-snapd).

Once Snap is installed, just open a terminal window and enter the following 
line to install Quelea:

```
sudo snap install quelea
```

### Using the cross-platform installer

Quelea for Linux needs Oracle Java 8. (OpenJDK8 can also be used, but only if OpenJFX8 is also installed.)

Here's how to install Oracle Java 8 for Ubuntu/Linux Mint systems
(tested on Mint 17.1 64 bit):

From the [instructions
here](http://tecadmin.net/install-oracle-java-8-jdk-8-ubuntu-via-ppa/)
do this in a terminal:

```text
$ sudo add-apt-repository ppa:webupd8team/java 
$ sudo apt-get update 
$ sudo apt-get install oracle-java8-installer 
```

That will take a while, as the download is quite large. To verify the version
of Java that your system will use:

```text
$ java -version 
```

You should see something like: 

```text
java version "1.8.0_40" Java(TM) SE Runtime Environment (build 1.8.0_40-b25) 
Java HotSpot(TM) 64-Bit Server VM (build 25.40-b25, mixed mode) 
```

If not, you might have other versions of Java installed. To set the default, do:

```text
$ sudo update-alternatives --config java 
```

For example:

There are 3 choices for the alternative java (providing
/usr/bin/java).

| Selection   | Path                                            | Priority  | Status      |
| --- | --- | --- | --- |
| 0           | /usr/lib/jvm/java-8-oracle/jre/bin/java         | 1072      | auto mode   |
| 1           | /usr/lib/jvm/java-7-openjdk-amd64/jre/bin/java  | 1071      | manual mode |
| 2           | /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java  | 1069      | manual mode |
| * 3         | /usr/lib/jvm/java-8-oracle/jre/bin/java         | 1072      | manual mode |

Press enter to keep the current choice [*], or type selection number:

Choose the number that refers to the Oracle Java. The "\*" indicates the current default.

---
