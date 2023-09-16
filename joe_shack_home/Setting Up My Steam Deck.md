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
	* AutoSuspend.
	* Emuchievements.
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
## Install Retrodeck

* 
## Install extra video game storefronts and apps

### Apps from the Discover Store

* Spotify
* Discord
	* Make sure *minimize to tray* is deselected because otherwise Discord will crash when exiting in game mode.
* ProtonUp-QT
* Disk Usage Analyzer
* Protontricks
* For those apps I would like to have available in game mode, you can right click on the app and add it to Steam.
* Use SteamGridDB to change the artwork.

### Extra video game storefronts

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

* 