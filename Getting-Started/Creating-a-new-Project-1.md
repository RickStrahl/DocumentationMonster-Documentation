To create a new Project you can use:

* **File -> New Project**
* Use the **@icon-folder-plus New Project Toolbar** button

![New Project Dialog](/Features/NewProjectDialog.png)

The file and folder name are automatically generated for you, although you can explicitly change them if you prefer.

By default projects are stored in:

* My `Documents\Documentation Monster\Your Project`
* Files are created with a `.docmonster` extension

> Documentation Monster project files are JSON files, and you can use any extension you want as long as you can remember them. DM looks for `.docmonster`,`.docs.json`, and `.json` in project dialogs.


## A new Project is generated
Here's what the new project looks like once created:

![New Project Created](/Features/NewProjectCreated.png)

You can now edit this [new topic](dm-topic://_q3p2dafghs). The center pane contains the main topic content, while the pane on the right contains the topic editor where topic meta data is stored:

* Topic Title
* Topic Type (topic, header, classheader, etc.)
* Topic Content Type (markdown, html)
* Keywords
* Notes/Remarks
* See Also
* Slug (relative path with topic id)
* Link (to the content Markdown file on disk)

For certain types of topics like Classes or Databases or Service items there will be additional fields that map to these specific features (ie. Classname, member name etc.) These are typically only used for imports but they become available for specific topic types only in the topic editor.

Any changes you make are immediately applied and saved and you can see them applied in the previewer. As you type into the content pane content is updated.