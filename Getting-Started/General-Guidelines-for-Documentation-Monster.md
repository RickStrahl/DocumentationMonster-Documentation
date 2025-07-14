Documentation Monster is a documentation generation tool that works in **Project Format**:

* A top level Project
* The Project Contains Topics
* Each Topic can contain Sub-Topics

Topics are split into two types of information:

* The main Topic Content
* Topic Meta Data

The main topic data is shown in the main content area and this is were most user interaction occurs - you're writing your topic content. The main topic text is stored as Markdown files on disk and can also be edited externally without Documentation Monster's UI.

The topic meta data contains additional information about each topic: 

* Title
* Additional Keywords
* Notes/Remarks
* Code Snippets
* Flags like Incomplete, Don't render, Topic is a link etc.
* Topic Type specific fields like Class data f


The topic data is stored in the Project file, which is a JSON document that by default has a `.docmonster` extension.
