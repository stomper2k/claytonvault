# Using Zotero, Zotfile and Scrivener

[Using Zotero, Zotfile and Scrivener to carry out research, annotate PDFs and extract the annotations as notes. – AN -|- ANCIENT -|- ACADEMIC (an-ancient-academic.com)](https://an-ancient-academic.com/2019/05/22/using-zotero-zotfile-and-scrivener-to-carry-out-research-annotate-pdfs-and-extract-the-annotations-as-notes/)

The purpose of this post is to introduce the way I’m going to use Zotero, Zotfile and Scrivener for my PhD research. It follows from my searches online for hints and tips, so there is nothing really new here but I hope it will save others some time. This is not a technical tutorial (save a few parts) and won’t go into the download and installation of the various elements of the software as there are many good tutorials out there for that purpose.

## About Zotero, Zotfile and Scrivener.

[**Zotero**](https://www.zotero.org/) is very effective research software and is open source. Its features include the ability to automatically sense research on the web and save direct to your Zotero folder, this synchronises with an online account you create so you can access your work anywhere. This can be in many formats including web pages. Zotero is a great organiser. You can sort items into collections and tag them with keywords. When you search by keyword you can save this search and it will automatically fill with relevant materials as you work. Great if you tag items with theory concepts and then create a search to pull them all together. When you save an item to Zotero it will automatically get all the information for referencing and it will create references and bibliographies directly to MS Word via an add-in. It supports every referencing format I’ve ever seen.  
[**Zotfile**](http://zotfile.com/) is a Zotero plugin that manages attachments. It can automatically rename, move, and attach PDFs (or other files) to Zotero items, sync PDFs from your Zotero library to your (mobile) PDF reader (e.g. an iPad, Android tablet, etc.) and, most importantly for me, extract annotations from PDF files. It has the ability to extract annotations that are colour coded and will extract them from notes, highlights or underlined text. It is possible to extract colour coded highlights as separate notes e.g. green highlights, yellow highlights etc, but I found that this didn’t help me as things looked disjointed. I preferred one note that was sequenced as I’d annotated it on the PDF, so that is what I will describe here.  
**[Scrivener](https://www.literatureandlatte.com/scrivener/overview)** is a very powerful writing application. It isn’t free, but at around £40 I think it’s worth the cost. Scrivener features make the planning, organisation and arrangement of long documents much easier to manage and will store both your writing and your research. It works well with Zotero and will export your work in many formats such as Word, e-book etc. It can manage your writing by allowing goals and targets to be set for word counts and deadlines. So, you could break down your 100K word dissertation into a set number of words for each chapter/sub-chapter if you wanted and set dates for completion.

## Setting up File Structures

I do the majority of my editing work on a MacBook Pro and use an iPad Pro for reading and note taking. I work with OneDrive and this is historic rather than a preference. I like the way it stores a local copy of files and synchronises them in the cloud. I tend to work on the local copies of the cloud files, this doesn’t cause any issues but you need a decent internet connection to avoid any latency issues for large files. My local OneDrive looks like this…

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-12.18.12.png)

I set up the structure in Zotero and the research folder in Scrivener in the same vein to keep consistency and help to remember where things were (or should be). In Zotero, right click on ‘My Library’ to create a new collection (e.g. PhD) and right click on this collection to add sub-collections such as ‘Theory’.

![](https://whoareyou999.files.wordpress.com/2019/05/test1.png)

In Scrivener, right click on ‘Research’ and add new folders to get the structure set up…

![](https://whoareyou999.files.wordpress.com/2019/05/test2.png)

## Sharing files between these applications and editing/extracting notes.

Adding items to Zotero is a simple drag/drop operation, however Zotero has a bizarre internal storage system so I opted to link the files to it rather than create copies. The benefit of doing this is that if you update a file on your local drive it is automatically reflected in Zotero. To create a linked file on a Mac, hold command and option when you drag/drop the file. I guess Windows users can use right click and drag/drop. You can select many files at once to drag over, but my experience is that 10 or so at a time is reliable. A successfully linked file will have a chain on its icon. Zotero does a great job at retrieving all the reference information automatically.

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-12.57.43.png?w=656)

Creating a linked file in Scrivener is the same drag/drop process, the linked file has a curved arrow on its icon…

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-13.07.51.png?w=656)

Let’s take some notes on this work that we want to be able to refer to. Because the PDF file is in the OneDrive cloud, I can access it on my iPad and annotate it. There are many apps that can do this, but for information I use PDF Expert – it has good features and is very popular – and my Apple Pencil. You can see I’ve added a note and highlighted the journal text – green for general text and blue for the quote. I avoid highlighting in yellow as notes are added in that colour, but you can choose whatever works for you. On the iPad in PDF Expert…

![](https://whoareyou999.files.wordpress.com/2019/05/test3-1.png)

And here are the annotations automatically shown in Scrivener on the MacBook as the files are linked…

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-13.35.34.png?w=656)

## Extracting the Annotations

Let’s extract these annotations using Zotfile and Zotero. Extracted annotations are saved in Zotero notes, but remember that PDF is a complex file format and the extraction will likely not work if you can’t easily copy & paste text from the file in your PDF software. Firstly, you will have to configure Zotfile to extract the annotations in colour by changing some hidden options in Zotero preferences. This is accessed through the ‘Advanced’ tab in Preferences and under the ‘Advanced Configuration’ – ‘Config Editor’ at the bottom of the window. Note you will get a warning message as you need to take care changing configuration elements!

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-13.56.59-1.png)

Once in the configuration editor, search for ‘PDFExtraction’ which will give you a list of the possible config options. The ones to note and change are below with the configs to copy/paste.

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-14.03.10-1.png)

Make sure you copy the config text below including everything from the 1st < to the last >

**Extensions.zotfile.pdfExtraction.colorNotes:**

Set this to ‘true’ if you want to extract each colour highlight as a separate note. I decided not to do this.

**extensions.zotfile.pdfExtraction.formatAnnotationHighlight:**

```
<div class="highlight" style="background-color:%(color)"><p class="text">%(content)</p><p class="source" style="text-align:right;">%(cite)</p></div>
```

**extensions.zotfile.pdfExtraction.formatAnnotationNote:**

```
<div class="note" style="background-color:%(color)"><p class="text">%(content)</p><p class="source" style="text-align:right;">%(cite)</p></div>
```

**extensions.zotfile.pdfExtraction.formatAnnotationUnderline:**

```
<div class="underline" ><p class="text"><u>%(content)</u></p><p class="source" style="text-align:right;">%(cite)</p></div>
```

**extensions.zotfile.pdfExtraction.formatNoteTitle:**

```
<div class="head"><p class="title">%(title): %(date)</p><p class="date" style="display:none;">%(date)</p></div>
```

Now that Zotfile is configured, we can extract the annotations. To do this, right click on the PDF file in Zotero and choose ‘Manage Attachments’ – ‘Extract Annotations’. You should get a note file called ‘extracted annotations: date/time’ and your annotations in colour in the order you did them.

![](https://whoareyou999.files.wordpress.com/2019/05/test4.png)

We can now add these to Scrivener in the notes panel of the research file by dragging and dropping the Zotero Note into the Scrivener note panel.

![](https://whoareyou999.files.wordpress.com/2019/05/screenshot-2019-05-22-at-14.21.02-1.png)

Of course, there are other ways to create Scrivener notes. You could just copy and paste the text directly from the PDF file, but this method keeps a consistency through your work and will retain the references from Zotero in Scrivener. These references are links that will lead directly to the page referred to in the PDF, but only if the PDF has its page numbering set up and many don’t.

I hope this proves useful, please let me know in the comments below. Remember there are lots of tutorials and YouTube videos available online for Zotero and Scrivener.