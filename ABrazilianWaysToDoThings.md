# Brazillian Title Install Method

This is an alternative to loadiine. In a nutshell, we will be installing any game of your choosing to the Wii U itself. This means that if you have an external USB HDD formatted to the Wii U's file format, then you will be able to install whatever game to that USB drive and run it. Going online with these titles **will** work, though at this point it's unclear if it's safe to do so.

**Disclaimer:** /r/WiiUHacks does not condone piracy. In this section I will be presenting tools that access Nintendo's servers to download titles in the desired format for this tutorial. This same method displayed can be used to download content illegally; which we are in no way responsible for your actions regardless of what you chose to do.

&nbsp;

## Phase 1: uTikDownloadHelper

We will be grabbing the game of your choice from Nintendo directly in the format it needs to be in for this to work. Thanks to /u/DanTheMan827 for making uTikDownloadHelper!

**Step 1)** Download the latest [uTikDownloadHelper](https://github.com/DanTheMan827/uTikDownloadHelper/releases). 

**Step 2)** Create an empty directory/ folder. (This will be used to download the game.)

**Step 3)** Open 'uTikDownloadHelper.exe'. A window will pop up asking you a question, and you must answer it before uTikDownloadHelper will work.

* **NOTE:** The answer to this question is against the rules to post on this subreddit, however it's an easy one to answer if you search google.

**Step 4)** A list of games will be displayed. On the upper left hand corner, choose the region from the drop down box that matches your Wii U. The list of games will be filtered for that specific region.

**Step 5)** Select the game of your choice and click 'Download Selected'. It will ask you to choose a folder to download the game into. Find and select the folder we made back in **Step 2**. 

* **NOTE:** The directory/ folder you made in **Step 2** must be empty. uTikDownloadHelper will tell you if the folder isn't empty and ask you to select another folder that is.

* **NOTE 2:** The game you pick needs to have been released on the eShop, and also must have seen a retail (physical copy) release. For example, Call of Duty: Ghosts **won't** work because it has never been released on the eShop. Toki Tori 2 **won't** work because it only saw an eShop release. Splatoon **will** work because it saw a physical release and was digitally sold on the eShop.

**Step 6)** A command prompt window will pop up and begin to download your game. Depending on how big the game is, it might take a while. When it's completed the download, the window will disappear. You can now close uTikDownloadHelper.

We've now got the game in the correct format with the modified ticket to use later. You're ready for phase 2.

&nbsp;

## Phase 2: Formatting the USB HDD

If you plan on installing your game onto a USB HDD, then follow these next few steps. We need to format the drive into the specific file system the Wii U wants it to be in. 

* **NOTE:** If you have a USB HDD you already use for **Wii U** games, than it's already in the correct format. You can skip ahead to phase 3.

* **NOTE 2:** You cannot use the same USB HDD for Wii U and hacked vWii purposes. vWii asks for something like a FAT32 partition, when the Wii U wants to take over the whole HDD with it's own proprietary format. No kind of fancy partitioning will help.

* **NOTE 3:** This process **will erase** all the contents of the HDD, and it will become unusable when plugged into a PC.

**Step 1)** Plug your USB HDD into a usb port while your Wii U is turned off.

* **NOTE:** The Wii U can use external HDDs that are bigger than 2TBs, but can only utilize 2TBs of the HDD. For example, I'm using a 3TB external HDD - but the Wii U can only use 2TBs of the 3TBs.

* **NOTE 2:** If you're using an external HDD that does not have it's own power source, then you need a [Y-cable](https://oyendigital.com/images/USB3-y-cable.jpg). Plug both male ends into either the back or in the front two USB ports.

**Step 2)** Turn the Wii U on. You will be prompted to format the detected HDD. Do so now.

* **NOTE:** This **will erase** all the contents of the HDD, and it will become unusable when plugged into a PC.

And that's it! Onto phase 3.

&nbsp;

## Phase 3: Setting up the SD card and Installing our Game

I'm assuming you've already followed the '*Kernel Exploit Prep Work: Setting up Your SD Card*' guide from above.

**Step 1)** Download the latest [Modified WUP Installer](https://github.com/Yardape8000/wupinstaller/releases)

**Step 2)** Set things up in the SD card like this:

* SD:/wiiu/apps/wupinstaller/wupinstaller.elf
* SD:/wiiu/apps/wupinstaller/icon.png
* SD:/wiiu/apps/wupinstaller/meta.xml

**Step 3)** Create a directory in the root of your SD card and call it 'install'

* SD:/install

**Step 4)** Navigate to the folder/ directory we created in **Phase 1, Step 2**. Copy **all** of the contents from this folder into the 'install' folder we just created in the root of the SD card from **Step 3**.

**Step 6)** Put the SD card into the SD Card slot in your Wii U.

**Step 7)** Get into the homebrew launcher with your preferred method.

**Step 8)** Launch 'WUP Installer Mod'

**Step 9)** You'll see a black screen with white text. Pressing A will install your game onto the system memory, and pressing X will install your game to your USB HDD. Read the below note first, and then press one of those buttons depending on what you want to do.

* **NOTE:** To be on the safer side of things, we recommend that you install your game onto the external USB HDD first, and then testing the game to see if it runs before installing it onto the system itself.

**Step 10)** It'll tell you when it's done with the installation. When it is, press the home button. This will bring you back to the homebrew launcher. From here, get back to the Wii U main menu.

If everything went well, you'll see your new game installed on the menu ready to be played! You can make sure it installed into the correct directory by checking where it has installed in 'System Settings' under 'Data Management.'

&nbsp;

## Additional Notes


*These are things you cannot share on this subreddit, doing so will result in a ban, no exceptions*

* Wii U Title Keys (16-digit ID)
* Wii U Common Key (32-character ID)
* Modified or Unmodified Tickets (title.tik)
* WUD files
* Anything downloaded from NUSGrabber/ uTikDownloadHelper
* Websites where they provide these things for you
* Copyrighted content in general


*I get this error in WUP Installer: 0xFFFBF440. What does this mean?*

* The answer to this is unclear at the moment. Modify the originally obtained ticket again, and redownload the game from NUSGrabber. This has been reported to work, even after several attempts.


*The installation process failed without giving me a solid error*

* You may have insufficient space wherever you're trying to install the game to. If you think this happened to you, go into Data Management under System Settings. If you check up on what is installed on your system memory/ USB external drive, it may ask you to delete some unnecessary data. Do that, and restart the install when you believe you have sufficient storage space.


*My external HDD is 4TBs and my Wii U says it only has 2TBs. What's going on?*

* The Wii U can see external USB HDDs that are larger than **2TBs**, but will only utilize **2TBs** of the HDD.


*Can I use the same Wii U formatted external HDD alongside my hacked vWii for USB Loader GX/ Nintendont/ etc?*

* No. When the Wii U formats your external HDD, it formats the whole thing. There is no way to partition it.

*When I enter a title key into UWizard before extracting a WUD, it says it's incorrect. What's going on?*

* Your WUD might be from a different region, or it might just be as simple as copying over the title key again.

*I can't find a WUD file for [XXXXXX] game*

* I'm not helping you with this. However, WUD files only exist for games that have been physically released. eShop games are not in WUDs, therefore it's not possible to install an eshop game via this Brazilian procedure.

*Can I bring my saves over from Loadiine?*

* Absolutely, you must use Saviine. I plan on doing a write-up about this, but in the mean time - there are multiple guides on how to do this around the internet right now.

*Can I update my games?*

* Yes, it's perfectly safe to update your games via the Wii U. Turn on nnupatcher before updating to make it work. In some cases, nnupatcher is not enough. In these cases, remove dualhax, update your games, and then put dualhax back on.

*Can I hold you responsible if my Wii U bricks?*

* No you can't. That's on you.

&nbsp;
