# FlimFlam69's 5.5.1 Kernel Exploit Guide

**LATEST FIRMWARE:** 5.5.1  //  **LATEST EXPLOITABLE FIRMWARE:** 5.5.1  //  **RECOMMENDED FIRMWARE:** 5.5.1

&nbsp;

Your Wii U is in no danger if you decide to run an exploit. This is a very safe procedure, and a relatively simple one at that. Were not soldering anything, or preforming kind of hardware mods; all you need is your **computer**, the **internet** (with a wireless router), a **Wii U**, and an **SD card**.



&nbsp;
---------------------------------------------------------------------------------------------------------------------------


If you have any other questions, check the FAQ first before you ask! I will try my best to answer any question you have. :)
---------------------------------------------------------------------------------------------------------------------------

Before we get started exploiting the Wii U, we should set the console up to block updates from Nintendo. If your Wii U goes above the latest firmware (5.5.1), you may lose your ability to get to the homebrew launcher and all the other fun stuff.

* Let's block updates!

* Let's just get started with the exploit.
















**[TABLE OF CONTENTS]**

* **[KE01]** Dual hax (Tubehax + Chncdcksn hax)
* **[KE02]** Router URL Blocking
* **[KE03]** Disable Automatic Software Downloads
* **[KE04]** Kernel Exploit Prep Work: *Setting up Your SD Card* 
* **[KE05]** Running the Kernel Exploit: *The Easy Way* 
* **[KE06]** Running the Kernel Exploit: *The Self-Hosting Way* 
* **[KE07]** Running the Kernel Exploit: *Self-Hosting and Taking Your Wii U Offline* 
* **[KE08]** Brazillian Title Install Method 
   * **[KE09]** Phase 1: uTikDownloadHelper
   * **[KE10]** Phase 2: Formatting the USB HDD
   * **[KE11]** Phase 3: Setting up the SD card and Installing our Game
   * **[KE12]** Additional Notes
* **[KE13]** Various Things 
   * **[KE14]** nnupatcher: eShop Access with Dualhax/ Router URL Blocking
   * **[KE15]** Saviine: Injecting Saves
   * **[KE16]** Saviine: Dumping Saves
   * **[KE17]** SD Card Mount Failed Error
   * **[KE18]** Nintendo DS Virtual Console Injection
   * **[KE19]** NES & SNES Virtual Console Injection
   * **[KE20]** Games Won't Show up in Loadiine
   * **[KE21]** Virtual Console Manual Crash Fix
   * **[KE22]** Importing and Exporting DS Saves from VC
* **[KE23]** Frequently Asked Questions 


---------------------------------------------------------------------------------------------------------------------------

&nbsp;

**[Dual hax (Tubehax + Chncdcksn hax)]** [KE01]

Tubehax & chncdcksn hax are two different DNS servers that are used for the purpose of preventing updates through Nintendo. Before we do anything, we need to make sure that your Wii U will remain on 5.5.1 - and this is one of the best/ most popular ways of doing so while still being connected online.

This method sets up both *'Tubehax'* and *'chncdcksn hax'* DNS servers. In the event that Tubehax goes down, the Wii U will automatically use chncdcksn hax instead. (You will not be able to access the eShop through this. If you want eShop access, check out the Various Things section.)

* Turn Auto-Obtain DNS **OFF**
* Set Primary DNS to **107.211.140.065** (*Tubehax*)
* Set Secondary DNS to **104.236.072.203** (*chncdcksn hax*)

**Note:** If you still want YouTube access on your Wii U, set Tubehax as your 'Secondary DNS' and chncdcksn hax as your 'Primary DNS'.

Thanks to /u/chncdcksn for the DNS server. The community absolutely appreciates it!

&nbsp;

**[Router URL Blocking]** [KE02]

If your router has the option to block certain URLs from passing through, that's a way better way of keeping your Wii U safe and connected. After setting this up, I *don't think* you will be able to access the eShop, but you should be able to play games online just fine. (*If you still want eShop access, check out the Various Things section.*) I can't exactly write a guide URL router blocking because everyone's router is different, and more specifically, my router doesn't have that specific function. Here are the URLs to block if you can:

* nus.cdn.c.shop.nintendowifi.net
* nus.cdn.shop.wii.com
* nus.cdn.wup.shop.nintendo.net
* nus.wup.shop.nintendo.net
* nus.c.shop.nintendowifi.net
* c.shop.nintendowifi.net
* cbvc.cdn.nintendo.net
* cbvc.nintendo.net

**Note:** Router URL Blocking will block all things Nintendo. This means that if you have a 3DS of any kind, it will not be able to preform updates either. Other Wii U consoles connected to that router won't be able to update as well.

&nbsp;


**[Disable Automatic Software Downloads]** [KE03]

As an added precaution, you can also do as the header says: disable automatic software downloads. If you go into internet settings, the option to enable/ disable is below the 'View Mac Address' button. (Thanks /u/KingGhidorah01)

* **Note:** Do NOT use this as a substitute for Tubehax, chncdcksn hax, or Router URL Blocking. This is only something you should do IN ADDITION to Tubehax, chncdcksn hax, or Router URL Blocking. 

&nbsp;

---------------------------------------------------------------------------------------------------------------------------

&nbsp;

**[Kernel Exploit Prep Work: *Setting up Your SD Card*]** [KE04]

**Step 1)** [Format your SD card to FAT32.](http://www.wikihow.com/Format-an-SD-Card) If the linked method doesn't work for your OS (or if FAT32 isn't listed as an option), you need additional software. /u/LightPrism suggests [fat32format.](http://www.ridgecrop.demon.co.uk/index.htm?guiformat.htm)

* **Note:** If you can, use 64kb clusters. If that ends up not working, try 32kb clusters. I've gotten them both working on Wii U, but people seem to be saying they have better luck with 64kb clusters.

* **Note 2:** If you have to name your SD card, do not name it "wiiu". It's been reported that this will **not** work for whatever reason. (Thanks /u/unfortunate_timing, I should've added this tidbit a while ago!)

**Step 2)** Download my [Starter Pack](https://drive.google.com/open?id=0BzJAGHWBJ_5saVNnMXhzTkVhR2s)

**Step 3)** Extract the contents of the .zip file to the root of your SD Card (It only should be a wiiu folder).

**Step 4)** Games go into the following directory:

* SD:/wiiu/games/Example Game [GAMEID]

&nbsp;

**[Running the Kernel Exploit: *The Easy Way*]** [KE05]

**Step 1)** Put the SD card into the SD Card slot in your Wii U

**Step 2)** Turn on your Wii U, and go to the Web Browser.

**Step 3)** Go into your internet settings and *Reset your Data.* (If this isn't your first time running the exploit, you can probably get a way with just *Deleting Cookies*.)

**Step 4)** Back out of internet settings and type this into the address bar: http://loadiine.ovh/ 

* **Optional:** Bookmark this address so you don't have to type this in *every time* you want to run this exploit in the future.

**Step 5)** Ensure that the displayed drop down box is displaying "Homebrew Launcher..." and press the **Submit** button.

**Step 6)** Presto! It should have worked, and you should be seeing the Homebrew Launcher menu within seconds. If it freezes on a white screen, then just do a hard reset and go back to **Step 2**.

I hope this helps! It's a pretty simple process. The exploit isn't 100% stable, so it might fail from time to time.

&nbsp;

**[Running the Kernel Exploit: *The Self-Hosting Way*]** [KE06]

* *This guide is written for Windows Operating Systems.*

With this method, you will be self-hosting the Wii U exploit, rather than going to loadiine.ovh every time you want to get into Homebrew Launcher. This is literally using *the same payload* http:/loadiine.ovh uses to exploit your console online, so you should be getting close to a 100% success rate with this.

I have made a package for everyone to download that includes instructions on how to do everything. I've made it as simple and noob friendly as possible, though the guide assumes you have followed the "*Kernel Exploit Prep Work: Setting up Your SD Card*" guide from above. You can download the package below.

**Note:** This is a modified version of [Kafluke's all-in-one package from GBATemp](http://gbatemp.net/threads/5-5-1-5-4-0-5-3-2-self-hosting-package-everything-in-one-zip-file.424679/). Special thanks to Cybernatus (From GBATemp and loadiine.ovh) for making this payload public.

[**Download FlimFlam69's All-In-One Self-Hosting Package**](https://drive.google.com/open?id=0BzJAGHWBJ_5sNmphWWVPSTlNMGM) 117mb v1.1

&nbsp;

**[Running the Kernel Exploit: *Self-Hosting and Taking Your Wii U Offline*]** [KE07]

* *This guide is written for Windows Operating Systems.*

With this method, your Wii U will be completely offline and still be able to access the exploit. This is literally using *the same payload* loadiine.ovh uses to exploit your console online, so you should be getting close to a 100% success rate with this. It will be impossible for Nintendo to update your console, but you will obviously lose the ability to browse the eShop and play games online.

I have made a package for everyone to download that includes instructions on how to do everything. I've made it as simple and noob friendly as possible, though the guide assumes you have followed the "*Kernel Exploit Prep Work: Setting up Your SD Card*" guide from above. You can download the package below.

**Note:** This is a modified version of [Kafluke's all-in-one package from GBATemp](http://gbatemp.net/threads/5-5-1-5-4-0-5-3-2-self-hosting-package-everything-in-one-zip-file.424679/) with incorporating [Seita's idea to use Connectify](http://gbatemp.net/threads/run-kexploit-and-loadiine-offline-using-connectify.425212/) in order to take your Wii U offline completely. Special thanks to Cybernatus (From GBATemp and loadiine.ovh) for making this payload public.

[**Download FlimFlam69's All-In-One Self-Hosting (Offline) Package**](https://drive.google.com/open?id=0BzJAGHWBJ_5sM3cwVmFRRE03WkU) 126mb v1.1

&nbsp;

---------------------------------------------------------------------------------------------------------------------------

&nbsp;

**[Brazillian Title Install Method]** [KE08]

This is an alternative to loadiine. In a nutshell, we will be installing any game of your choosing to the Wii U itself. This means that if you have an external USB HDD formatted to the Wii U's file format, then you will be able to install whatever game to that USB drive and run it. Going online with these titles **will** work, though at this point it's unclear if it's safe to do so.

&nbsp;

---------------------------------------------------------------------------------------------------------------------------

**--Disclaimer--**

/r/WiiUHacks does not condone piracy. In this section I will be presenting tools that access Nintendo's servers to download titles in the desired format for this tutorial. This same method displayed can be used to download content illegally; which we are in no way responsible for your actions regardless of what you chose to do.

---------------------------------------------------------------------------------------------------------------------------

&nbsp;

**[Phase 1: uTikDownloadHelper]** [KE09]

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

**[Phase 2: Formatting the USB HDD]** [KE10]

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

**[Phase 3: Setting up the SD card and Installing our Game]** [KE11]

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

**[Additional Notes]** [KE12]


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

---------------------------------------------------------------------------------------------------------------------------

&nbsp;

**[Various Things]** [KE13]

&nbsp;

**[nnupatcher: eShop Access with Dualhax/ Router URL Blocking]** [KE14]

So, you're looking for eShop access with update blocking procedures on? That's why we have [nnupatcher](https://github.com/dibas/nnupatcher-hbl/releases/tag/0.1)! (Thanks /u/supster131) I will be going through these steps **assuming** you have set your SD card up according to the guide above. 

**Step 1)** Download the latest [nnupatcher](https://github.com/dibas/nnupatcher-hbl/releases/tag/0.1). 

* **Note:** If you've already downloaded my [Starter Pack](https://drive.google.com/open?id=0BzJAGHWBJ_5sOXdIUU9XeF9HUTA) from the *Setting up Your SD Card* section, then you already have nnupatcher. You can skip to Step 4.

**Step 2)** Set things up in the SD card like this:

* SD:/wiiu/apps/nnupatcher/nnupatcher.elf
* SD:/wiiu/apps/nnupatcher/icon.png
* SD:/wiiu/apps/nnupatcher/meta.xml

**Step 3)** Put the SD card back into the SD Card slot

**Step 4)** Get to the Homebrew Launcher using your preferred exploit method. (*The Easy Way* or *The Self-Hosting Way*) 

**Step 5)** If you installed nnupatcher correctly, you'll see it pop up on the Homebrew Launcher on screen. Select it!

**Step 6)** It will bring you back into the Wii U system menu. Click the eShop icon.

**Step 7)** And presto, You're in!

&nbsp;

**[Saviine: Injecting Saves]** [KE15]

You are reading this because you want to inject a loadiine save into a game playable via the Wii U main menu. Whether you actually bought the game, or installed it via the Brazilian method, this is what you want to be reading.

**Step 1)** Download, and extract the latest [Saviine.](https://github.com/Maschell/saviine/releases)

**Step 2)** Copy the 'wiiu' folder to the root of your SD card. When it comes to Saviine, Your apps folder should look like this:

* SD:/wiiu/apps/saviine/saviine.elf
* SD:/wiiu/apps/saviine/icon.png
* SD:/wiiu/apps/saviine/meta.xml

**Step 3)** Run 'dump.bat' in the server folder where you extracted Saviine too. This will create a saviine_root folder. Close 'dump.bat'.

**Step 4)** In saviine_root, create a folder and call it, 'inject'.

**Step 5)** Copy the loadiine saves (you would like to inject) from this directory in the SD card:

* SD:\wiiu\saves

Into the 'inject' folder we made in the last step, **Step 4**

**Step 6)** Rename the loadiine save folder, which looks like, 'Paper Mario Color Splash [XXXXXX]' to the games Title ID.

* **NOTE:** These title keys are against the rules to share/ post/ link to on this subreddit. You can find them by using google. In this case, the folder wants the Title ID hyphenated. It should something like, 'XXXXXXXX-XXXXXXXX'

**Step 7)** There are 2 folders in this save folder. Rename them as such:

* c - common
* u - 80000001

**Step 8)** Find your computer's IPv4 address. Remember this address. It should look like this: **192.168.X.XXX**

* **NOTE:** If you're using one of my self-hosting methods, use the IPv4 that connectify supplies with the wireless signal you created.

**Step 9)** Run 'inject.bat' in the server folder where you extracted Saviine too.

**Step 10)** Put the SD card into the SD Card slot in your Wii U.

**Step 11)** Play the game you want to inject your save to until you can make a save.

**Step 12)** Get to the homebrew launcher through your preferred method and launch Saviine.

**Step 13)** Set your IPv4 address you found in **Step 8**.

**Step 14)** Press X to install Saviine and go back to the Wii U menu.

**Step 15)** Launch the game you want to inject the game save into.

**Step 16)** Look at your PC. The inject.bat that's been running since **Step 9** should have given you a prompt with 2 drop down boxes. On the top drop down, select '**80000001**'. In the second drop down, select '**Inject**.

**Step 17)** inject.bat should start working, and finish within 30 seconds. When the game starts: you'll see that the save injected successfully.

&nbsp;

**[Saviine: Dumping Saves]** [KE16]

You are reading this because you want to dump a save from a title installed on the Wii U. You can either share this save online, or use it on a game loaded via loadiine.

**Step 1)** Download, and extract the latest [Saviine.](https://github.com/Maschell/saviine/releases)

**Step 2)** Copy the 'wiiu' folder to the root of your SD card. When it comes to Saviine, Your apps folder should look like this:

* SD:/wiiu/apps/saviine/saviine.elf
* SD:/wiiu/apps/saviine/icon.png
* SD:/wiiu/apps/saviine/meta.xml

**Step 3)** Run 'dump.bat' in the server folder where you extracted Saviine too. This will create a saviine_root folder. Keep dump.bat running.

**Step 4)** Find your computer's IPv4 address. Remember this address. It should look like this: **192.168.X.XXX**

* **NOTE:** If you're using one of my self-hosting methods, use the IPv4 that connectify supplies with the wireless signal you created.

**Step 5)** Put the SD card into the SD Card slot in your Wii U.

**Step 6)** Get to the homebrew launcher through your preferred method and launch Saviine.

**Step 7)** Set your IPv4 address you found in **Step 4**.

**Step 8)** Press X to install Saviine and go back to the Wii U menu.

**Step 9)** Launch the game you would like to dump the save from.

**Step 10)** Look at your PC. The dump.bat that's been running since **Step 3** should have given you a prompt. Dump everything.

**Step 11)** dump.bat should start working, and finish within 30 seconds. When you look in the saviine_root folder, you'll see a folder called 'Dump'. Your save is in this folder labeled with the game's title ID.

* **NOTE:** These title keys are against the rules to share/ post/ link to on this subreddit. You can find them by using google. In this case, It should be something like, 'XXXXXXXX-XXXXXXXX'

&nbsp;

**[SD Card Mount Failed Error]** [KE17]

If you keep getting this error, something is messed up in your SD card. I've found that, for whatever reason, it's because there is *unallocated data* before the FAT32 partition. Let me try to visualize it for you:

* SD:   ----Unallocated Data---      [--------------FAT32-------------]

When the Wii U sees the *unallocated data first*, it refuses to look any farther than that. So how do we go about fixing this? To describe the process in a nutshell:

**WARNING)** If you're using the same SD card from your 3DS that uses emuNAND/ redNAND, the unallocated data is your emuNAND/ redNAND. If you are following this guide, **YOU WILL** delete your emuNAND/ redNAND. *If you haven't hacked your 3DS and don't know what I'm taking about, this doesn't apply to you*.

**Step 1)** You have to use something like [*Ease US Partition Manager*](http://www.partition-tool.com/). This will allow you to visualize whats going on in your SD card and make the necessary changes in formatting.

**Step 2)** Turn the *unallocated data* into something. Usually, it's only a couple of megabytes of data, so you have to format it into an NTFS, so it'll look like this:

* SD: [---------NTFS--------][--------------FAT32-------------]

**Step 3)** Delete the FAT32 partition:

* SD: [---------NTFS--------]   --------Unallocated--------

**Step 4)**  Resize the NTFS partition all the way to the right:

* SD: [--------------------NTFS--------------------------------]--

**Step 5)** Change the NTFS to a FAT32 and give it 64kb cluster allocation

* SD: [--------------------FAT32-------------------------------]--

**Step 6)** Apply changes. It might take a bit to finish these changes.

And that's the gist of it! This is just a quick write-up on how to generally fix the problem.

* **Note:** I don't know if this is true or not, but I've recently heard that if you simply format your SD card to NTFS first, and then change it to FAT32, everything *should* be fine. This is unconfirmed though, so I'm sorry if that doesn't work.

&nbsp;

**[Nintendo DS Virtual Console Injection]** [KE18]

This method, as far as I know, **ONLY** applies to the DS.

Keep in mind that you will not be able to inject any DS roms over 64mbs. This is because there has been no game released for the DS VC (officially) that exceeds 64mbs in size (as of writing this). Also, you cannot inject a 64mb DS rom into a game for the DS VC that’s only 32mb in size.

Another thing: each DS VC release has a modified emulator by Nintendo specifically for that game. Keep in mind, injecting roms into different official VC releases will yield different results. If your desired game doesn’t work (properly) after injecting, try another DS VC Official release. 

The [GBATemp Wiki also has a compatibility list](http://wiki.gbatemp.net/wiki/WiiU_VC_NDS_injection) for DS injects that people have already tried, so see if the game you want to try is listed!

**Step 1)** Have a/ your desired DS VC base game already formatted for Loadiine. (Don’t ask me where to get one. Use Google, it shouldn’t be that hard to grab a base game.) I’m going to use ‘New Super Mario Bros’ as an example for the sake of this guide.

**Step 2)** Unzip the game (if necessary) and navigate to the following directory:

* New Super Mario Bros [GAMEID]/ content/ 0010/ 

**Step 3)** Extract the only file in ‘rom.zip’. It should be a file called something like, ‘WUP-N-DADE.srl’. 

**Step 4)** Copy *only* ‘WUP-N-DADE’ from the filename and delete both ‘WUP-N-DADE.srl’ and ‘rom.zip’.

**Step 5)** Drag your NDS rom into that folder. (In this example, mine is ‘Ace_Attorney.nds’)

**Step 6)** Rename your NDS rom to ‘WUP-N-DADE’ and change the file extension to ‘srl’. (So, ‘Ace_Attorney.nds’ becomes ‘WUP-N-DADE.srl’)

**Step 7)** Right click the new ‘WUP-N-DADE.srl’, go to ‘Send to’, then click ‘Compressed (zipped) folder’ to zip the file. Call it, ‘rom.zip’.

**Step 8)** Rename the game folder. (For example, New Super Mario Bros [GAMEID] would become Ace Attorney [GAMEID])

**Step 9)** Put it on your SD card, in the games directory:

* SD://wiiu/games/

**Step 10)** Run it in Loadiine! Everything should work (or at the very least, boot). 

**Step 11) Optional:** If you would like to get fancy and edit the Icon/ Banner display in Loadiine (meta stuff) then you can edit them in the ‘…/Ace Attorney [GAMEID]/meta’ directory, with photoshop. The icon is called ‘iconTex.tga’ and the banner is ‘bootTvTex.tga’.

I’m sorry if any of this is unclear, I’ll give it another look as soon as I have the chance!

&nbsp;

**[NES & SNES Virtual Console Injection]** [KE19]

/u/dubyadud has written a tutorial on making NES & SNES VC injections. [Check it out here!](https://www.reddit.com/r/WiiUHacks/comments/4igfgz/injecting_roms_into_vc_games/)

&nbsp;

**[Games Won't Show up in Loadiine]** [KE20]

If a game is not showing up in Loadiine and it's definately on the SD card, double check these things:

* Make sure you have the latest [Loadiine GX2](https://github.com/dimok789/loadiine_gx2/releases)

* Make sure your games are in *SD:/wiiu/games/*

* Make sure your GAME IDs are correct. For example, a EU Pokken Tournament directory should look like this: *SD:/wiiu/games/Pokken Tournament [APKP01]*

If it's not one of these things, your game dump may be missing some vital files for Loadiine to recognize it as a game. Grab another dump and try again.

&nbsp;

**[Virtual Console Manual Crash Fix]** [KE21]

This is a fix for the crash that happens when you exit the manual in a VC Inject game. It literally just breaks that function, so the manual will never initiate in the first place. All the credit goes to /u/zeron88 for this fix!

Instructions in his own words: "You have to put these 2 files into "SD:\wiiu\games\VC DS\content\[numbers]\data\scripts" and overwrite the existing ones."

I've personally tested this fix, and it works flawlessly.

[**Download the fix here**](https://drive.google.com/file/d/0B_0A-iy41haIMC1NOFhRUl9sX00/view?usp=drivesdk)

&nbsp;

**[Importing and Exporting DS Saves from VC]** [KE22]

/u/zeron88 figured out a way to do what the title says. I've personally tested this method with Ace Attorney Investigations 2 with DeSmuMe and it worked for me! (As /u/zeron88 says in the original GBATemp thread, this method may need a little more testing.)

*What this Tutorial is for*

* Importing and exporting saves from the DS VC from or to .sav files. 
* .sav are used by most emulators and flashcards.

*Importing saves to the VC*

1. Start the VC game and save it
2. On your PC, go to the save folder of the VC (ex. SD:\wiiu\saves\DS VC\80000001)
3. Delete all .state files in there
4. You now should have a .save file there. Note down its name and delete it.
5. Take your .sav you want to inject, rename it to the name of the .save (extension included!)
6. Once you boot the game, your save should be there.

*Exporting saves from the VC*

1. On your PC, go to the save folder of the VC (ex. SD:\wiiu\saves\DS VC\80000001)
2. Copy the .save and rename it if you want
3. Change the extension of the copy from .save to .sav.

[Original thread on GBATemp](https://gbatemp.net/threads/tutorial-importing-and-exporting-vc-ds-saves-testing-needed.427167/)

---------------------------------------------------------------------------------------------------------------------------

&nbsp;

**[Frequently Asked Questions]** [KE23]

> I have a Wii U on X.X.X firmware. What can I/ should do with it?*

Update the Wii U to 5.5.1 if it isn't already. The eventual release of the IOSU exploit will be compatible with this firmware, and when Nintendo does release a new firmware - it might be tricky to get to 5.5.1 if you're on a lower firmware. Not a lot of retail discs are known to provide the specific 5.5.1 update, so update via Nintendo's official servers **now** while you can. If you don't believe me, check out these statements from [WulfyStylez](https://gbatemp.net/threads/wii-u-hacking-homebrew-discussion.367489/page-993#post-6601905), [(1)](https://gbatemp.net/threads/wii-u-hacking-homebrew-discussion.367489/page-994#post-6604507) and [shinyquagsire23](https://gbatemp.net/threads/wii-u-hacking-homebrew-discussion.367489/page-993#post-6602696) of Team SALT over on GBATemp.

*What is Homebrew Launcher?*

* Homebrew Launcher finds & allows you to boot different Wii U homebrew apps like Loadiine or nnupatcher.

*What is loadiine?*

* Loadiine gx2 is a backup loader for the Wii U. You can play digital backups of your games through your SD card.

*Can we use external USB Hard Drives to load backups?*

* You can load games via USB when you install games via the **Brazilian Title Install Method**, though you can't load games through USB via loadiine.

*When are we getting an IOSU exploit?*

* We have one! Unfortunately, it's useless until developers start taking advantage of the new functions this new exploit brings. Team SALT is working on there own IOSU exploit with a suite of tools to be released. We have no ETA on it's release, however, please be patient and send positive support in their direction. There are others working in the background as well, though we don't specifically know who is. Smealum did a write up/ released tools for developers on his [IOSUhax research](https://github.com/smealum/iosuhax), naehrwert [put out a write up](https://nwert.wordpress.com/2016/05/03/ioctlvhax/) on how he and Plutoo found an IOSU bug back in September 2015 for possible hacks.

*What kind of SD card can I use?*

* Anything up to 256gb will work. Class 10 SD cards will be fine. Even micro SD cards in SD adapters are good to go.

*Can I play EU backups on US consoles and vice versa?*

* Via loadiine, yes. Loadiine is region free, you're good to go! Though - you may have to edit some files to make things work correctly. For example, something named like 'musicEU.mtv' may need to be changed to 'musicUS.mtv' and so on. (Not all games are like this.)

*XXXXX game won't work/ run correctly in Loadiine. How do I make it work?*

* Some games will just function as is, others work with weird bugs, and others won't boot and will require a bit of work to get running. (Some games will just straight up not work.) Before asking in the subreddit, try checking the [GBATemp Loadiine Compatibility Wiki](http://wiki.gbatemp.net/wiki/Loadiine_compatibility_list) first. You might find your answer there! 

*Can I play backups (games) online?*

* You can play online when you install games via the **Brazilian Title Install Method**, though you can't play games online via loadiine.

*I keep seeing 'FSGetMountSource failed.' after I run the exploit. What went wrong?*

* Most of the time (if not *all* of the time) you either don't have an SD Card in the Wii U, or you've setup the file structure on your SD card incorrectly. Go back to, '*Kernel Exploit Prep Work: Setting up Your SD Card*' near the top of the guide and double check everything.

*Nintendo scheduled maintenance for this time. Does that mean we're getting an update?*

* Consider that Nintendo does this every week. Just because they're doing maintenance, doesn't mean we're getting an update. However, they *have* released updates in this fashion before, more traditionally with 3DS. No one can tell you when an update will be pushed, but as long as you've taken precautions (Dualhax, self-host offline, etc) - you should be fine. 

*My Wii U says it failed to download something/ a system update. Is there one out?*

* No, this means Dualhax is working. The Wii U may think it's trying to update, but in reality it's unsure because it can't talk to Nintendo's servers. 

*How do I mod Super Smash Bros. for Wii U?*

* I'm not going to do any kind of write-ups on this because it doesn't interest me too much. However, someone put together a smash modder's dream website. Check out [Sma4sh Mods!](http://sm4shmods.com/) It's got everything you need to get started (like tutorials).

*How do I mod Splatoon?*

* Again - I don't really care too much about modding, so I don't plan on doing any write-ups. GBATemp has a bunch of threads about it, and I'm sure other people in /r/wiiuhacks will be able to help you out.

&nbsp;

&nbsp;
