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
