**disc2app** is a tool that allows us to install our physical Wii U discs as digital titles onto our systems. By the end of this tutorial, you'll be playing your physical games off of a connected external harddrives or a system menu in no time! Fortunately it's a very easy and straight forward process, however theres a few things we need to do before we can play our newly converted digital titles.

Before we get to **phase 2**, you should know that you're required to have atleast **25gbs** free on the SD card before the disc can be dumped. 

&nbsp'

## Phase 1: Formatting the USB HDD

If you plan on installing your game onto a USB HDD, then follow these next few steps. We need to format the drive into the specific file system the Wii U wants it to be in. If you plan on installing your game onto the system memory, you can skip ahead to the next phase.

* **NOTE:** If you have a USB HDD you already use for **Wii U** games, than it's already in the correct format. You can skip ahead to phase 3.

* **NOTE 2:** You cannot use the same USB HDD for Wii U and hacked vWii purposes. vWii asks for something like a FAT32 partition, when the Wii U wants to take over the whole HDD with it's own proprietary format. No kind of fancy partitioning will help.

* **NOTE 3:** This process **will erase** all the contents of the HDD, and it will become unusable when plugged into a PC.

**Step 1)** Plug your USB HDD into a usb port while your Wii U is turned off.

* **NOTE:** The Wii U can use external HDDs that are bigger than 2TBs, but can only utilize 2TBs of the HDD. For example, I'm using a 3TB external HDD - but the Wii U can only use 2TBs of the 3TBs.

* **NOTE 2:** If you're using an external HDD that does not have it's own power source, then you need a [Y-cable](https://oyendigital.com/images/USB3-y-cable.jpg). Plug both male ends into either the back or in the front two USB ports.

**Step 2)** Turn the Wii U on. You will be prompted to format the detected HDD. Do so now.

* **NOTE:** This **will erase** all the contents of the HDD, and it will become unusable when plugged into a PC.

&nbsp;

## Phase 2: disc2app

Now we're ready to dump our game. Remember, you need to make sure you have *atleast* **25gb** free on your SD card before you begin the process.

**Step 1)** Download the latest [**Modified WUP Installer**](https://github.com/Yardape8000/wupinstaller/releases)

* **NOTE:** If you have taken the time to setup your SD card as instructed by the [starter pack setup guide](https://github.com/FlimFlam69/WiiUTutorial/wiki/0:-Starter-Pack), then you can skip to **Step 5**
 
**Step 2)** Set things up in the SD card like this:

* SD:/wiiu/apps/wupinstaller/wupinstaller.elf
* SD:/wiiu/apps/wupinstaller/icon.png
* SD:/wiiu/apps/wupinstaller/meta.xml

**Step 3)** Download the latest [**disc2app**](https://github.com/koolkdev/disc2app/releases)

**Step 4)** Set things up in the SD card like this:

* SD:/wiiu/apps/disc2app/disc2app.elf

**Step 5)** Put the SD card into the SD Card slot in your Wii U.

**Step 6)** Remove any disc that currently may be in the Wii U disc drive.

**Step 7)** Get into the homebrew launcher with your preferred method and run **disc2app**.

**Step 8)** Press **'A'** to dump to the SD card.

**Step 9)** After gaining access to the IOSU, It will ask: "Please insert the disc you want to dump now to begin." Do that.

* **NOTE:** This procedure may take a while depending on the size of the game. 

Upon completeing the dump, it will take you back to the system menu. You've successfully dumped your physical Wii U game! Now onto the last phase.

&nbsp;

## Installing the Dumped Game

**Step 1)** Get into the homebrew launcher with your preferred method and run **WUP Installer - Mod Y**.

**Step 2)** You'll see a black screen with white text. Pressing A will install your game onto the system memory, and pressing X will install your game to your USB HDD. Read the below note first, and then press one of those buttons depending on what you want to do.

**Step 3)** It'll tell you when it's done with the installation. When it is, press the home button. This will bring you back to the homebrew launcher. From here, get back to the Wii U main menu.

If everything went well, you'll see your new game installed on the menu ready to be played! You can make sure it installed into the correct directory by checking where it has installed in 'System Settings' under 'Data Management.'
