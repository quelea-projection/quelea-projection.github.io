---
title: Installation Instructions
permalink: /Installation_Instructions/
---

System requirements
-------------------

Quelea should run on Windows, Linux or MacOS. The developers all use Windows in their day to day work on Quelea, so that will be the most stable platform by implication, A \`deb\` package is provided for debian based installs (including Ubuntu) but all other platforms, including MacOS, will require the cross platform jar installer (which will require the JRE to be installed first.)

Generally, any modern machine should be ok to run Quelea, but we would recommend at a minimum:

-   4GB RAM
-   5GB free hard drive space
-   Dual display outputs (triple display output required for stage view)
-   SSD (not required, but start up times will be much faster.)

Realistically, any machine purchased or built in the last few years should be fine.

Windows Install
---------------

The .exe file provided on the downloads file should work with most computers, if you have any problems post on the Quelea Discuss Google Groups found [here](https://groups.google.com/forum/#!forum/quelea-discuss).

For videos to work, you must have the latest version of VLC installed as well. It must be \*32-bit\*, even if you are running on a 64 bit machine, since the JRE bundled with Quelea is also 32 bit.

Linux Install
-------------

Quelea 2015.1 for Linux needs Oracle Java 8. For unknown reasons, OpenJDK 8 does not work.

Here's how to install Oracle Java 8 for Ubuntu/Linux Mint systems (tested on Mint 17.1 64 bit):

From the [instructions here](http://tecadmin.net/install-oracle-java-8-jdk-8-ubuntu-via-ppa/) do this in a terminal: $ sudo add-apt-repository ppa:webupd8team/java $ sudo apt-get update $ sudo apt-get install oracle-java8-installer That will take a while, as the download is quite large. To verify the version of Java that your system will use:

$ java -version You should see something like: java version "1.8.0_40" Java(TM) SE Runtime Environment (build 1.8.0_40-b25) Java HotSpot(TM) 64-Bit Server VM (build 25.40-b25, mixed mode) If not, you might have other versions of Java installed. To set the default, do:

$ sudo update-alternatives --config java For example:

There are 3 choices for the alternative java (providing /usr/bin/java).

` Selection    Path                                             Priority   Status`
` 0            /usr/lib/jvm/java-8-oracle/jre/bin/java          1072       auto mode`
` 1            /usr/lib/jvm/java-7-openjdk-amd64/jre/bin/java   1071       manual mode`
` 2            /usr/lib/jvm/java-8-openjdk-amd64/jre/bin/java   1069       manual mode`
` * 3          /usr/lib/jvm/java-8-oracle/jre/bin/java          1072       manual mode`

Press enter to keep the current choice\[\*\], or type selection number:

Choose the number that refers to the Oracle Java. The "\*" indicates the current default.