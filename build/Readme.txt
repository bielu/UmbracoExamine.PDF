
  _    _ __  __ ____  _____           _____ ____  
 | |  | |  \/  |  _ \|  __ \    /\   / ____/ __ \ 
 | |  | | \  / | |_) | |__) |  /  \ | |   | |  | |
 | |  | | |\/| |  _ <|  _  /  / /\ \| |   | |  | |
 | |__| | |  | | |_) | | \ \ / ____ | |___| |__| |
  \____/|_|  |_|____/|_|  \_/_/    \_\_____\____/ 
                                                   
----------------------------------------------------

UmbracoExamine PDF indexer has been installed. 

The installer has added a new Indexer & Searcher to ~/Config/ExamineSettings.config
called: "PDFIndexer" & "PDFSearcher"
and added a new Index Set to ~/Config/ExamineIndex.config called "PDFIndexSet"


**** NOTE: Not all PDFs can have text read from them! ****


This shows the specific configuration options for the "PDFIndexer" and the 
default values applied when they are not specified:

*   extensions = comma seperated list of file extensions that our PDFs have
    the default is ".pdf"
*   umbracoFileProperty = the property of the media type that contains files
	the default is "umbracoFile"

*****************************************************************************
MANUAL INSTALLATION
*****************************************************************************

To add this to your site, drop the files from this zip file in the bin folder.

You'll need to add a new Indexer & Searcher to ~/Config/ExamineSettings.config
called: "PDFIndexer" & "PDFSearcher"

	<add name="PDFIndexer"
           type="UmbracoExamine.PDF.PDFIndexer, UmbracoExamine.PDF"
           extensions=".pdf"
           umbracoFileProperty="umbracoFile" />
  
	<add name="PDFSearcher"
         type="UmbracoExamine.UmbracoExamineSearcher, UmbracoExamine" />

and add a new Index Set to ~/Config/ExamineIndex.config called "PDFIndexSet":

	<IndexSet SetName="PDFIndexSet" IndexPath="~/App_Data/TEMP/ExamineIndexes/PDFs" />

*****************************************************************************
LICENSE
*****************************************************************************

The source code for UmbracoExamine.PDF is licensed under the MIT license. 