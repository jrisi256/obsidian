---
type: Note
---

* **Creation date**: `= this.file.ctime`
* **Last modified date**: `= this.file.mtime`
* **Tags**: #boox #workflow #device_setup #obsidian #zotero

## Notes

### Handwritten notes

Let's say you are just writing your notes freehand. You can do a few things with this.

1. For starters, you can do nothing. You can just allow the notes to live on your [[Onyx Boox]] device.
2. You can export the note as a [[PDF]]. This will create a copy in `/Storage/note/Name of Note/Name of Note.pdf`. There a few things which should be noted about this PDF.
	1. First, when you open the PDF, it will open with [[NeoReader]] and not the built-in note taking app from Onyx. Notes are there own file format, and they will not show up in your usual file system (I believe they are stored in a [[database]]).
	2. Second, you can delete this PDF, and nothing will happen to your notes. This also holds in the other direction. If you delete your notes, nothing will happen to the PDF (and a bit confusingly you will have the PDF version of your note, but there will be no *notes* in your note app).
	3. Third, the PDF version of the note will show up under the *Documents* folder on the home page of your storage. Documents pulls from a bunch of different folders to show you all of your documents.
	4. Because the PDF versions of my notes get stored in `/Storage/note`, that is where I have my [[DriveSync]] location set up.
3. You can use the built-in AI handwriting recognition tool within the writing app to convert your handwriting into text.
		1. This `.txt` file has a lot of similarities to the PDF file. When you open the `.txt` file, it will open in NeoReader. You can delete this `.txt` file, and nothing will happen to the original note (and vice versa). It will show up under the *Documents* folder in addition to `/Storage/note/Name of Note/Name of Note.txt`.
		2. One feature that is a bit unfortunate (and strange) is that I cannot edit the text in the NeoReader app. I can add more text, and I can even add my own handwriting. The file remains a `.txt` file, though. When the file is synced to my computer, I can only see the original transcribed text from the note (and nothing I added using NeoReader). Happily, I am able to edit it like normal using a text editor on my computer.

### Typed notes

Boox has recently added the ability to type notes rather than hand write them. They function very similarly to handwritten notes:
	1. You can export your note as a `.txt` file.
	2. When they are exported, they will show up under `/Storage/note/Name of Note/Name of Note.txt`. You can delete this exported `.txt` file, and the original note file will still be there (and vice versa).
	3. When you open the exported file, it will open using NeoReader. Any edits you make using NeoReader will not show in a synced `.txt` file on your computer, but you will be able to edit that `.txt` file normally.
	4. It will show up under your `Documents` folder.

TL;DR

* *Notes* are their own, weird thing within the Onyx Boox ecosystem. They only exist within the context of the [[Notes app]], and you cannot find them in the normal Android file system. You can export them as PDF files or as `.txt` files. These exported files are totally separate from their *notes* version which means you can edit them or delete them, and the original *note* will be fine (and vice versa). This exporting feature is how you are able to: make your notes appear within the Android file system and then sync them to your computer for further editing. You are then only able to edit those exported notes within NeoReader (which cannot edit the original text in `.txt` files). All of your exported notes will also appear within the *Documents* folder of your Android file system which goes through a variety of folders so you can see all of your documents in one place.
* For DriveSync, sync `/Storage/note` with Google Drive since this is where all your notes will get sent.
* For writing a diary, I can either:
	* Hand write in my diary, convert to text, sync using DriveSync, then add to [[Obsidian]].
	* Type directly to text, sync using DriveSync, then add to Obsidian.

## Documents

1. Set up [[Zotero]] along with the [[ZotFile]] plugin.
	1. Note that the [[ZotFile]] plugin no longer works as of 2024 due to Zotero updating to version 7. I will have to figure out a new way to sync PDFs to my tablet.
2. Set up [[Google Drive]] set up on your computer.
3. Set up DriveSync on your Onyx Boox device.

The ZotFile plugin allows you to send a copy of your PDF journal article to a specific Google Drive folder (which should be linked to a specific folder on your Onyx Boox device). Using DriveSync, you can then import that PDF article onto your Onyx Boox device. For my workflow, I have it set up that `/Storage/Books` is linked with Google Drive. This is because this is where the Onyx Boox Library app looks for documents to display in your library.

### Editing the document directly

Once you have a sent a PDF journal article to your Onyx Boox device, we can now start editing and marking up the document.

1. You can directly edit the PDF by writing on it or typing on it. If you want your handwritten notes to be transformed into text, you can double tap on the handwritten note, or you can bring up the typing interface and use the keyboard to hand write notes which will then transcribe your handwriting into text.
	1. You can export any pages with notes written or typed in this way. It will be exported to `/Storage/note/Name_of_article/Name_of_article-scribble.pdf`. All pages exported in this way will be exported into one PDF. The previous export will be overwritten with a new export.
		1. You can change the settings so that the scribbled note will be stored in the same folder as the source file (e.g., `/Storage/Books`). I have not decided, yet, which functionality I would prefer. For now, I am sticking with the default which stores it in `/Storage/note`/.
	2. In addition to (or instead of) exporting the pages with notes, you can just keep the notes as part of the PDF. You would sync the file using DriveSync. In Zotero, you would use ZotFile to retrieve the document from the shared folder (after which it is removed from the folder), and then you can see your newly edited PDF document.
	3. You cannot extract the hand writing or the text from the PDF into a separate note. Using this functionality means your notes are becoming a part of the PDF document itself. I will discuss below other ways for you to add notes which can be extracted into text.

### Annotating the document

You do not have to edit the document directly especially if you want to extract your notes at some point. For this use case, annotating might be a good option. There is a lot of nuance when it comes to annotation, though, so below I am going to get particularly into the weeds on this issue. There are also a lot of potential workflows which could result from this process so I will also be trying my best to note this as well.

1. A reasonable first step would be to start annotating your PDF journal article in Zotero on your computer. You can:
	1. Highlight text a variety of colors.
	2. Highlight text and add a note.
	3. Add a note that exists in a rather free form fashion not tied to any text directly.
	4. Draw a box around an image or table you would like to highlight and/or write about (**note** that the image will not be exported into Obsidian using any of the methods highlighted below nor will any tags associated with an annotation).
2. Once you have done these things, you can extract the annotated notes from within Zotero. This will create a new *note* item within Zotero with all of your annotated text as quotes (with a corresponding citation and page number) as well as any accompanying notes you may have written.
3. To add these extracted annotations to Obsidian, you can:
	1. Use the built-in Zotero functionality by right clicking on the *note* item(s) you want, and clicking Export Note. This will turn the note into a [[Markdown]] file which can then be saved in your Obsidian vault. The benefits of this are that the included annotations have links which when clicked on will open the PDF in Zotero to the direct page where the annotation is. The downsides are that this markdown does not have any metadata or any way to easily integrate its metadata into an Obsidian-friendly framework (i.e., tags, links, and [[YAML]]).
	2. Use the [[Mdnotes]] plugin within Zotero.
		1. If you want to add only some notes, right click on the *note* item(s) you want, then click Mdnotes, Export to markdown. Each note will get its own markdown file. It is very similar to the built-in Zotero functionality. One benefit is that Mdnotes preserves the highlight color. The downsides are it no longer links to the original document in Zotero, and it has a bunch of somewhat ugly HTML.
		2. **My preferred method**. My workflow is set up so that I will export all notes, and my set of notes should be unique and up-to-date. Right click on the parent item (of all note, PDF, and other attachments) in the library view and click Mdnotes, Create full export note. This preserves the original highlight color, it provides a rich set of metadata tags, links, and YAML (because of the template I have set up), and it links back to the original PDF journal article in Zotero. Unfortunately, annotations do not link directly to their place in the article.
		3. Note that as of 2024, this plugin no longer works because [[Mdnotes]] does not support Zotero 7.
	3. Use the [[Zotero Integration]] plugin for Obsidian. This allows you to directly import all notes for a particular parent entity directly into whatever note you are writing in Obsidian. The benefits of this approach are that it is arguably the easiest and fastest as you do not even have to leave Obsidian, and  it preserves the link to the original PDF article as well as the location of the annotation. Unfortunately, it does not retain the rich metadata which comes from the Mdnotes approach. It also does not preserve the highlight color. This approach could easily be combined with Mdnotes to get the best of both worlds. In the future, this is what I might do.

Now we will have a brief aside now about the unique quirks of Zotero's annotations. its annotations do not become embedded within the PDF (which is what other PDF editors usually do). The annotations are instead stored internally within Zotero. This approach helps Zotero run more smoothly, and it allows for interesting functionality (e.g., being able to tag annotations). It does have some drawbacks, though, because if one uses another PDF editor to edit the PDF, the annotations one has made in Zotero will not show up.

1. If one wishes to edit a Zotero PDF in another PDF editor while having their Zotero annotations show up, one can do that by going into library view and clicking File, Export PDF on the PDF they want to export.
2. Zotero, though, can read annotations made by another PDF editor. When you import a PDF which has annotations from another PDF editor, those annotations will be locked meaning they cannot be edited (nor can any corresponding notes). You can still extract them, and add them to Obsidian in the ways outlined above. If you want to turn the annotations into Zotero annotations, you can also do that. Open the PDF within Zotero, and then click File, Import Annotations.

I am not sure yet what my preferred workflow option is going to be, but it is nice to know and understand the options.

For more details on how this works and why Zotero decided to do things this way, consult the following official documentation links:

* [Zotero PDF Reader](https://www.zotero.org/support/pdf_reader#adding_annotations_to_notes).
* [Zotero annotations](https://www.zotero.org/support/kb/annotations_in_database).

Let's go back to Onyx Boox. Let's say you have sent the PDF document already to your Onyx Boox device, and you want to start annotating it. Here are the steps to do so.

1. First, open the document, and it will automatically open in NeoReader. A prompt will appear asking what to do with the embedded data. I usually select *Merge* as that seems the safest. Of course, if your document does not have any embedded data, it does not matter what you choose.
	1. I believe *Overwrite* overwrites any embedded data you may have added through NeoReader. I believe *Cancel* causes the embedded data to not be recognized as embedded data at all, and NeoReader will view the embedded data as a part of the PDF instead.
	2. **Note** that NeoReader does not recognize standalone notes as annotations. It will always recognize them as being part of the PDF.
2. As stated above, annotations from Zotero will not show up on NeoReader. Any annotations you made using a different PDF editor will show up, though.
3. Once you have annotated some text, you can add some comments or not. The note has to be handwritten (although you can use the keyboard to write instead of type, and it will recognize your handwriting as text).
	1. You can also share and export the annotation itself by embedding it within a note, but this functionality does really seem all that useful especially since it will not be recognized as text.
4. You then use DriveSync to sync the new PDF file to Google Drive and your computer. Go into Zotero on your computer, right click on the parent entry and click Manage Attachments, Get from Tablet. The new PDF will be pulled into Zotero with the new annotations (and your existing Zotero annotations). If you wish to integrate the Onyx Boox annotations into Zotero, you can do that as well as outlined above.

### Taking notes in Onyx Boox on a PDF article

You can, of course, also take notes that are not embedded in the PDF but are standalone files. The process is pretty simple and straightforward. You open the split screen functionality in NeoReader, and you begin taking notes by hand or by typing. The notes will be associated with your PDF. This means if you stop taking notes, and close the app and later come back to it and start writing again, the same note will appear.

The notes will also appear in the *Notes* app (as reading notes rather than local notes). Remember from the beginning that notes in Onyx Boox devices are there own thing, separate from the rest of the file system. As a result, if you want to sync them to your computer, you first must export them. Thankfully, the process for exporting is the same as outlined above because at the end of the day, they are still notes.

## Conclusion and Workflow

* If I am not working on the Onyx Boox device, the workflow is simple. I add the PDFs to my Zotero. I edit them in Zotero adding any annotations I want. I export my annotation notes to Obsidian using Zotero's built-in functionality, Mdnotes, or the Zotero Integration Obsidian plugin. I continue taking notes in Obsidian not tied to any specific annotations.
	* I think I should keep all my notes in Obsidian so that way I can best leverage the power of Obsidian. This means not taking non-annotation notes in Zotero. I can export them to Obsidian, but it seems like it would get messy in terms of which notes are up-to-date and things like that. It seems cleaner to just do it this way for now.
* For working on my Onyx Boox device, I need to send the PDF to the tablet. I can then annotate and take notes on the Boox device itself. On my computer, I can pretty easily import the annotations from the Boox device into Zotero and export them as notes into Obsidian. Any written or typed notes will have to be more manually added into Obsidian, but it is still not a big lift all things considered.
* For taking notes in my diary, I can type or hand write them as I see fit on my Onyx Boox device. Then, it is pretty easy to sync with a computer, and then import into Obsidian.