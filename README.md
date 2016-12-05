# FlimFlam69's 5.5.1 IOSU + Kernel Exploit Guide

**LATEST // EXPLOITABLE // RECOMMENDED FIRMWARE:** 5.5.1 

Your Wii U is in no danger if you decide to run an exploit. This is a very safe procedure, and a relatively simple one at that. Were not soldering anything, or preforming kind of hardware mods; all you need is an **SD card**, your **computer** (with the ability to write to an SD card), the **internet** (with a wireless router), and a **Wii U**.

If you have any other questions, check the [F.A.Q.](https://github.com/FlimFlam69/WiiUTutorial/wiki/7:-Frequently-Asked-Questions) first before you ask in the Q&A thread! I will try my best to answer any questions.

## **Table of Contents**

### 0) [Starter Pack Setup](https://github.com/FlimFlam69/WiiUTutorial/wiki/0:-Starter-Pack)
If you plan on going through the whole guide, this should be your first stop. This section shows you how to setup your SD card correctly, what software to download, and where that software should go on the SD card. It is not required to start here, but I would recommend it. This part of the guide contains the following sections:

* **Guide Prep Work:** *Making Your Own Starter Pack*

### 1) [Blocking Updates From Nintendo](https://github.com/FlimFlam69/WiiUTutorial/wiki/1:-Blocking-Updates-From-Nintendo)

Before we get started exploiting the Wii U, we should set the console up to block updates from Nintendo. If your Wii U goes above the latest firmware (5.5.1), you may lose your ability to get to the homebrew launcher and all the other fun stuff. This part of the guide contains the following sections:

* Dualhax
* Blocking Updates with a Proxy Server  
* Router URL Blocking
* Disable Automatic Software Downloads

### 2) [Preparing & Running the Kernel Exploit](https://github.com/FlimFlam69/WiiUTutorial/wiki/2:-Preparing-&-Running-the-Kernel-Exploit)

This is where the fun begins! In this section, we'll be setting up the SD card so we can run the kernel exploit. There are a couple way to go about doing this and we'll explore some of those options. This part of the guide contains the following sections:
  
* **Kernel Exploit Prep Work:** *Setting up Your SD Card* 
* **Running the Kernel Exploit:** *The Easy Way* 
* **Running the Kernel Exploit:** *The Self-Hosting Way* 
* **Running the Kernel Exploit:** *Self-Hosting and Taking Your Wii U Offline* 

### 3) [Installing Haxchi](https://github.com/FlimFlam69/WiiUTutorial/wiki/3:-Installing-Haxchi)

Now let's get our hands a little dirtier! Now that we can get into the Homebrew Launcher, lets install Haxchi to the System Menu so we don't need any wireless connections anymore to run hacks or homebrew. This part of the guide contains the following sections:
   
   * Installing Haxchi

### 4) [Installing IOSUhax](https://github.com/FlimFlam69/WiiUTutorial/wiki/4:-Installing-IOSUhax)

So now that we have installed Haxchi, it's now much easier to boot whatever homebrew we want (from the system menu). For some people, just having the homebrew launcher accessible through the system menu is enough, but you're here because you want to go a bit deeper down this rabbit hole. Instead of the homebrew channel, let's boot IOSUhax! This part of the guide contains the following sections:
   
   * Choosing Dimok's Patcher or redNAND
   * Modifying Haxchi
* Haxchi for Dimok's Simple Signature Check Patcher
* Haxchi for redNAND
   * Running redNAND from Homebrew Launcher
   * Compiling IOSUhax (optional)

### 5) [Brazilian Title Install Method](https://github.com/FlimFlam69/WiiUTutorial/wiki/5:-Brazilian-Title-Install-Method)

This is an alternative to loadiine. In a nutshell, we will be installing any game of your choosing to the Wii U itself. This means that if you have an external USB HDD formatted to the Wii U's file format, then you will be able to install whatever game to that USB drive and run it. Going online with these titles **will** work.

**Disclaimer:** /r/WiiUHacks does not condone piracy. In this section I will be presenting tools that access Nintendo's servers to download titles in the desired format for this tutorial. This same method displayed can be used to download content illegally; which we are in no way responsible for your actions regardless of what you chose to do.

This part of the guide contains the following sections:

   * **Phase 1:** uTikDownloadHelper
   * **Phase 2:** Formatting the USB HDD
   * **Phase 3:** Setting up the SD card and Installing our Game
   * Additional Notes
   
### 6) [And Other Various Things...](https://github.com/FlimFlam69/WiiUTutorial/wiki/6:-And-Other-Various-Things...)

In this section, we'll be exploring miscellaneous procedures that will either solve some problems, or enhance the overall user experience. This part of the guide contains the following sections:
   
   * nnupatcher: eShop Access with Dualhax/ Router URL Blocking
   * Saviine: Injecting Saves
   * Saviine: Dumping Saves
   * SD Card Mount Failed Error
   * Nintendo DS Virtual Console Injection
   * NES & SNES Virtual Console Injection
   * Games Won't Show up in Loadiine
   * Virtual Console Manual Crash Fix
   * Importing and Exporting DS Saves from VC

### 7) [vWii Modding](https://github.com/FlimFlam69/WiiUTutorial/wiki/7:-vWii-Modding)

vWii translates to *Virtual Wii* which is the Wii U's built in Wii. It is very moddable, and the methods we use today have changed a little bit! It's much more painless than what it used to be from a couple of years ago, and I've written this section to make it as easy as possible! This part of the guide contains the following sections:

* Wuphax - Installing the Homebrew Channel
* Dumping the vWii's NAND
* IOS One-by-One Dumping (Optional)
* cIOS Installation
* Additional Information

### 8) [Frequently Asked Questions](https://github.com/FlimFlam69/WiiUTutorial/wiki/8:-Frequently-Asked-Questions)
