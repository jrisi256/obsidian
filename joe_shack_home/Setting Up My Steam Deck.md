---
type: Note
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #steam_deck #device_setup 

## Install the Hard Drive

* [I used this video as my main guide for installing a new hard drive into my Steam Deck](https://www.youtube.com/watch?v=GSvdsic4_dk). I will write up the instructions below as well, but it is probably easiest to just watch the video.
* You will need: Philips #0 Screwdriver, Philips #1 Screwdriver, Tweezers, Opening Tool, Replacement SSD hard drive, Replacement SSD hard drive cover.
* First, discharge the battery to 25%, and set your Steam Deck into battery storage mode.
* Remove your SD card if you have one inserted because it could get damaged.
* Remove your back plate. Do not strip the screwhead.
* Remove the motherboard cover. Make sure you remember you screw the screws into the correct places because the screws from the back plate screw into the motherboard cover.
* Disconnect the battery.
* Remove the [[SSD]] and replace it with your own.
* Reattach the pieces you removed.
### Reinstall [[SteamOS]]

* You will need a 8GB USB stick and some way to plug your USB stick into the [[Steam Deck]] (USA-A to USB-C adapter or some sort of USB hub).
  
* [Link to downloading SteamOS](https://help.steampowered.com/en/faqs/view/1b71-edf2-eb6d-2bb3). Make sure you unzip the file.
  
* You can use [[Rufus]], but it is [[Windows]] only. [Here is the download link](https://rufus.ie/en/).

* For [[Ubuntu]], I used [[balenaEtcher]]. [Click here to go to their homepage](https://etcher.balena.io/). It is very easy to run.
	* **Note** I could not get the Steam Deck to properly use the flashed image on my USB drive when I used balenaEtcher. I am not sure why.
  
* Once you have flashed the USB drive with the SteamOS image, plug it into your Steam deck. Click on Boot Manager, and then select the external drive. You will have to wait a few minutes, but then you should see your desktop. Click on the icon, "Reimage Steam Deck". You will then have to wait a few minutes again. By the end, you will have installed SteamOS onto your new hard drive.
## Format the SD Card

* This is as simple as going into Setting -> System -> Format SD Card.
## First time set-up

### Settings in Game Mode

* Show Battery Percentage indicator.
* Enable developer mode.
* Schedule night mode.
* Hide offline friends in custom categories.
* Hide categorized friends in Online/Offline friends.
* Open advanced settings for performance.
* Set Performance Overlay Level to 1.
* Show Performance Overlay in Steam.

### Settings in Desktop Mode

* Customize the Appearance to suit one's needs.
* Turn on automatic updates.
* Power Management -> Advanced Power Settings -> At the critical level, have the computer shut down.
* Install and log into Firefox.
* Dolphin File Manager Settings
	* Show Hidden files.
	* Add compatdata folder to Place for easy access (/Home/.local/share/Steam/steampps).
	* Add shadercache folder. It has the same path as compadata.
	* Clean up the side panel by removing unnecessary folders.
* Create a Non-Steam Games folder on the SD card and on the internal SSD which can then be symbolically linked to the Proton prefix folders where other video game storefronts are downloaded. This ensures your games are preserved and easily accessible if something happens to the digital storefronts or the prefixes they are installed in.
## Install Decky Loader and Plugins

* The first step is to set a password for sudo privileges. Head to the terminal and type in `passwd`.
* Install [DeckyLoader](https://github.com/SteamDeckHomebrew/decky-loader). The instructions on their website are very straightforward.
* Then I like to install the following Plugins. I have found them to be the most useful:
	* AutoFlatpaks.
	* AutoSuspend.
	* HLTB for Deck.
	* MusicControl.
	* Pause Games.
		* Pause before Suspend.
		* Pause on focus loss.
		* Also on overlay.
	* PowerTools.
	* ProtonDB Badges.
	* SteamGridDB.
	* Storage Cleaner.
## Install Retrodeck/Emudeck

As of the original writing of this guide, Retrodeck still feels like it needs some work before it can reliably be used.

* [Download Emudeck](https://www.emudeck.com/).
* Installation is rather straightforward, truthfully. I will try and document anything I do out of the ordinary.

### Configure Emulators

#### Configure Retroarch

* Settings -> Frame Throttle -> Fast-Forward Rate to 2.0x.
  
* For each Nintendo console, go to Quick Menu -> Controls -> Port 1 Controls (and any subsequent controllers) -> Change buttons to match Steam Deck -> Manage Remap Files -> Save Core Remap File.
## Install extra video game storefronts and apps

### Apps from the Discover Store

* Spotify
* Discord
	* Make sure *minimize to tray* is deselected because otherwise Discord will crash when exiting in game mode.
	* For these two apps (since I plan on using them while in game mode), it can be useful to change the controller setup to *Keyboard (WASD) and Mouse*.
* ProtonUp-QT
* Disk Usage Analyzer
* Protontricks
* For those apps I would like to have available in game mode, you can right click on the app and add it to Steam.
* Use SteamGridDB to change the artwork.

### Extra video game storefronts

Note I am following the [logic from this video](https://www.youtube.com/watch?v=Z_HYcdrYR38).

The basic logic is as follows:

1. Download the installer for each storefront.
   
2. Open Steam (in Desktop Mode), and click on *Add a Non-Steam Game*. We will start by adding the store installer to Steam.
   
3. Click on the Gear Icon for the store installer's entry in Steam. Click on *Compatibility*. Click on *Force the use of a specific Steam Play compatibility tool*. Select *Proton Experimental* from the drop-down menu.
   
4. Click on *Shortcut* on the left-hand side (right above *Compatibility*) and then copy and paste the following command into *Launch Options*: `STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1/ %command%`. This will allow for the storefront to recognize the Steam Deck's SD card.
   
5. You can then launch the installer from Steam, and it will begin the process of installing the storefront. The beauty of [[SteamOS]] is that it leverages the power of [[Proton]]. When installing these storefronts, the installers believe they are installing into a Windows environment. Proton is a compatibility layer that translates Windows-specific commands into their Linux counterparts thus allowing for programs to be run in a Linux environment which were originally designed to run in a Windows environment. Each storefront gets installed into their *Proton prefix* which is a randomly generated series of numbers. These prefixes contain all the essential files necessary to trick the installer into thinking it is within a Windows environment.
   
	1. It is generally recommended to keep each storefront in its own prefix. This is because the storefronts are constantly changing, and each storefront might only run using a specific version of Proton. This necessitates each storefront needing their own unique environment to run in. Of course, if your Steam Deck has a small amount of internal storage, this causes a problem. These prefixes (as far as I understand) must be stored on your Steam Deck. I suppose they could stored on your SD card, but it could severely compromise performance. This leads many people to storing storefronts within the same prefix. This will technically work, but it could cause headaches down the line for the aforementioned reasons. It could also create headaches as one attempts to try to mod games or otherwise attempt idiosyncratic changes to games or their storefronts.
	   
6. Once the installer is done installing, you can use [[Protontricks]] to locate the folder containing the storefront (since it will have a randomly generated number sequence). Navigate to the compatdata folder (path is mentioned above), and then navigate to the folder with the appropriate sequence of random numbers. You will then have to search for the appropriate .exe file which will launch the storefront. Once you have located it, copy the path to that .exe file.
   
	1. While you are in the folder for the storefront, navigate all the way up to the *drive_c* folder. Create a symbolic link to the *Non-Steam Games SSD* folder. This folder (which you should have created on your Steam Deck's internal storage, does not really matter where) will be where the games are stored when installed from non-Steam sources. This ensures that if you need to wipe the prefix containing the storefront, the game installs will still be safe. It also keeps things better organized. You could also install on your SD card.
   
7. Go back to Steam and locate the entry for the installer. Click on the entry and then click on the gear icon on the right hand side. We will now be updating the *Target* and *Start In* entries so they point to the .exe file location (which will launch the storefront). Copy and paste the full path (including the .exe) in *Target* (make sure it is wrapped in quotes). Copy and paste the full path (excluding the .exe) in *Start In*.
   
8. Enter your credentials for logging on to the storefront.
   
9. Adjust settings for each storefront to ensure they run as smoothly as possible on the Steam Deck. This includes things like: making sure the storefront quits rather than minimizes upon exit, turning off any storefront overlays, etc. Also make sure you change the default install path to wherever you want your games to install.
   
10. Next, install the game you want to play.
    
11. The ideal situation is to create a new entry in Steam for this new game. Why? In case we want to create custom controls for this game or we need a specific version of Proton for this game. It also just makes it really nice aesthetically to have an entry on your Steam deck for the game. How do we create an entry for the game on your Steam deck? There are many ways to do it. I will focus on the one way I have found to be easiest.
    
12. Add another entry for the digital storefront to Steam. Click on *Add a Non-Steam game*, navigate to where the .exe file is stored for the digital storefront, and then add it to Steam. You need to run the digital storefront once for the Proton prefix folder to be created. Rename the digital storefront to be for the game you are interested in playing.

13. Now the prefix folder we created for the digital storefront is useless and just wasted space on your drive. We want the game to take advantage of the already existing prefix folder in which the digital storefront is *actually* stored. So take note of the prefix folder number created for this new digital storefront, and then delete that prefix folder. Next create a symbolic link to the prefix folder where the digital storefront is *actually* installed, but rename the folder to be the deleted folder's number.
    
14. This newly created entry is just pointing back to the original storefront. You could theoretically then play any of your installed games from this digital storefront. The Steam entry for the game is illusory. However, it is useful for organizational and aesthetic purposes, but it is also useful in instances where games need custom controls or Proton settings.
    
15. When shifting back to gaming mode, I like to change the controller layout to *Keyboard (WASD) and Mouse*. I find this makes it easiest to interact with the storefront in gaming mode. When I want to play the game, I shift it back to game-pad plus joystick. It is a little annoying, but I am not sure what else can be done. I suppose you could use the touchscreen to navigate and keep the game-pad plus joystick control configuration. The touchscreen on the Steam Deck is pretty bad, though.

I download the following storefronts onto my Steam Deck. The only one that is missing is Riot Games. I chose not to download Riot Games because their games are, in general, not very compatible with Linux.

* Epic Games Store
* Ubisoft Connect
* Battle.net
* EA Launcher
* itch.io
* GOG Galaxy
## Install CryoUtilities

* [This video is a useful and beginner-friendly video for installing and setting up CryoUtilities on your Steam](https://www.youtube.com/watch?v=7RPAxT7HJ7Q).
* [Link to download CryoUtilities](https://github.com/CryoByte33/steam-deck-utilities).
* I will not detail all the steps here because the video and website are super easy to follow in terms of how to get set-up.
## Install Tango

* You can download the Linux version of Tango from the Tango website quite easily.
* You can download the save files from the N1GP discord.
* Make sure you have the controller layout set to game-pad plus joystick. When launching Tango, if you have the layout set to anything other than this, it will not recognize the Steam deck controller as a controller (even if you switch it). When launching the application, it needs to be set to this layout and not switched from. This necessitates using the touchscreen, unfortunately.