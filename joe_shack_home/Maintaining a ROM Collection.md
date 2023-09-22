---
type: Note
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #roms #device_setup #workflow 

As a general note, anything which I do not understand can usually be found through Google. I will not be making notes of everything I learn, but my main goal is to capture the important steps, and preserve them here so I can replicate this process if need be.

## Useful links

* [Video demonstrating how to maintain your own ROM collection](https://www.youtube.com/watch?v=ZYHS6pnuUiA)
* [Website for obtaining .dat files for cartridge-based systems.](https://datomatic.no-intro.org/index.php?page=search&s=64) 
* [Website for obtaining .dat files for disc-based systems.](http://redump.org/downloads/)
* [Explains what ROM sets are](https://docs.mamedev.org/usingmame/aboutromsets.html)
	* For cartridge-based games, No-Intro ROM sets are considered the gold standard. No-Intro ROM sets only include the best ROMs without errors or changes and which are as close as possible to the original cartridges. No-Intro ROM sets usually have on working version of each for a given country as well as updates to those games.
	* Redump is the No-Intro of disc-based games.
* [Naming conventions for different ROM sets](https://wiki.recalbox.com/en/tutorials/games/generalities/isos-and-roms/differents-groups)
* [Naming convention for individual ROMs](https://wiki.no-intro.org/index.php?title=Naming_Convention)
* [Download link for ROM Manager - ClrMAMEPro](https://mamedev.emulab.it/clrmamepro/#downloads)
	* [Documentation for the website which can be a bit hard to navigate](https://mamedev.emulab.it/clrmamepro/docs/index.htm).
* [Website for downloading full No-Intro and Redump ROM sets and ISO sets](https://r-roms.github.io/). Note that this link is the one provided in the Reddit wiki, and it does not seem up-to-date. [This link](https://archive.org/details/no-intro_romsets) seems much more reliable, but I am not sure why.
* Missing and un-dumped games:
	* https://datomatic.no-intro.org/report_mia.html
	* http://wiki.redump.org/index.php?title=MIA_Lists
	* https://wiki.no-intro.org/index.php?title=Undumped_Games_Lists
	* http://wiki.redump.org/index.php?title=Discs_not_yet_dumped

## .dat files

* They link ROM names to their corresponding hashes.

## Basic workflow

1. Create a .dat file using the website listed above depending on if the system is cartridge-based or disc-based.
   
2. Once you have obtained the .dat file, download the full No-Intro or Redump set for the video game system of interest.
   
3. Make sure you have ClrMAMEPro installed.
   
4. Open up ClrMAMEPro and click on Add DatFile to create an entry for the .dat file you just downloaded.
   
	1. This creates a copy of your .dat file under the *datfiles* folder in ClrMAMEPro.
   
5. We will now adjust the settings for our ROM collection. Double-click on our new profile (if a window does not open automatically) and select Settings.
   
6. Add the ROM-Path which is just the directory path to the ROMs you just downloaded.
   
7. Apply your settings, and then click on Scanner which will scan our ROM-path and compare it to the .dat file profile we just created. Make sure you click on *Fix* for all cases. Then, just click on *New Scan*.

	1. The statistics screen will show us what ROMs we are missing, what ROMs we have, and which were *extra* so to speak (not included in the .dat file). ROMs which were extra get added to the *backup/unknown* folder in ClrMAMEPro.

	2. It is important to remember that despite seeming quite easy to define, there is no official list of every video game every made for a specific video game system. Depending on how one defines entry into that list, one can wind up with vastly different sets of games. Does one only include licensed games? What about homebrew games? Pirated games? Games released after the console had ceased being produced and supported (after market games)?
	   
	3. Quick review of the other options available:
	   
		1. Rebuilder. It does a lot of things. Its primary use cases are to allow you to add new ROMs to your existing ROM set (based on some existing .dat file). It basically allows you to add missing ROMs. You simply select as the *Source* your folder where your new ROMs are held, and then you select where your existing ROMs are stored as your *Destination*. You can also Rebuild to create a fixed .dat file (which is a .dat file which includes the missing ROMs).
		   
			1. You can uncheck *Recompress Files* because they are most likely already compressed. You can also check *Remove Matched Sourcefiles* because there is no need to keep the new ROMs once they have been verified and move into your existing ROM set.
			   
			2. Once you have rebuilt your ROM set, you will want to go back into Scanner and *Scan* your ROM set again (no need to do a whole new scan).
			   
			3. Rebuilder and New Scan are very similar, but it is good practice to use Rebuilder (especially for arcade games) where multiple ROMs are often stored in the same set (i.e., zipped file).
			   
8. 