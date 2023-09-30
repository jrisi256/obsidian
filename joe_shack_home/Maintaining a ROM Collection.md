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
	   
8. For older ROM sets (think MAME and NES), you may need to edit the hex code for the ROM files. I like [ImHex](https://github.com/WerWolv/ImHex). This [Reddit thread](https://www.reddit.com/r/Roms/comments/16qoexc/missing_some_nes_roms/) was also useful for explaining why some files need to be edited.
   
9. Since ROMs and ISOs take up a lot of space, I need to be as efficient as possible in how I am storing things. The basic workflow is this:
   
	1. Scan my ROM collection.
	   
	2. Create a 1G1R collection (which will separate the ROMs in the 1G1R collection from those that are not).
	   
	3. Move the entire 1G1R and leftover No-Intro/Redump ROMs into cloud storage and delete them from my local storage. I will have to re-download them (and combine them) if I want to scan them again. ClrMAMEPro will not be affected though. It simply takes a snapshot of my ROM collection.
	   
	4. Make copies of the .dat files in cloud storage (keep local copies).
	   
	5. Make copies of the ClrMAMEPro setting files which essentially syncs scans across computers.

### Rebuild

The *Rebuild* option allows one to add new ROMs to your existing ROM set (based on some existing .dat file). Typically, these new ROMs are missing ROMs.

1. Click on *Rebuild*. Select your *Source* folder to be where the new ROMs are being stored. Select your *Destination* folder to be where your existing ROMs are stored.
   
2. You can uncheck *Recompress Files* because they are most likely already compressed. You can also check *Remove Matched Sourcefiles* because there is no need to keep the new ROMs once they have been verified and moved into your existing ROM set.
   
3. Once you have rebuilt your ROM set, you will want to go back into Scanner and *Scan* your ROM set again (no need to do a whole new scan).
   
4. Rebuilder and New Scan are very similar, but it is good practice to use Rebuilder (especially for arcade games) where multiple ROMs are often stored in the same set (i.e., zipped file).
   
5. You could also use Rebuild to share missing ROM files with others. You add a *.dat file* which is the list of ROMs one is missing. You then use *Rebuild* to extract the pertinent ROMs from your collection (into whatever destination folder you want). This ensures only the missing ROMs are extracted. Make sure *Remove Matched Sourcefiles* is not checked.

### WWW Mode

By going through these steps, one can see if one's .dat files are out-of-date. ClrMAMEPro checks the date of your .dat file against the .dat files from the source provided to see if they're out-of-date.

1. On the main page of ClrMAMEPro, click on WWW Mode.
2. Click on add site. 
3. For No-Intro .dat files, go to Dat-o-matic -> Download. On this web page, you will find an xml link which can be used as the site reference to check your dat files against.
4. Redump does not have an XML link which you can check for updates. There is this project, though: [https://github.com/bilakispa/redump-xml-updater](https://github.com/bilakispa/redump-xml-updater)
	1. If that script does not work, you can try this one: [https://github.com/xprism1/Redump-XML-Updater](https://github.com/xprism1/Redump-XML-Updater)

### 1G1R Mode

1G1R stands for *1 Game, 1 ROM*. Given a ROM set, you specify a set of rules for choosing which versions of each ROM to keep.

1. Dat-o-matic -> Download -> P/Clone XML for the system of interest.
   
2. Add the dat file, set the ROM path, and *change the mode to 1G1R*.
   
3. Click on the drop down menu, select Regions. Then select the Regions you want the exclusives of. Make sure you sort the regions by order of importance. For example, I generally want all the USA versions of all ROMs first, then if there is no USA version, give me the European exclusives, and then if there are no USA or European versions, give me the Japanese version. I would select USA, Europe, and Japan. Then, I would make sure USA is first, then Europe, and then Japan.