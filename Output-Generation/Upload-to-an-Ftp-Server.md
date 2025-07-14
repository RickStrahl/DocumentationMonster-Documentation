The most likely Publish target of Documentation Output is like a Web site and Documentation Monster lets you quickly upload content to an Ftp server **Publish to Pdf**:

![Publish To Pdf](./PublishToPdf.png)

This dialog configures the Ftp settings to upload to the server.

> Some of these settings are stored as part of the project and can also be edited from the Project Settings Dialog.

> ##### @icon-warning FTP and SFTP only for now
> Currently we only support `ftp://` and `sftp://` protocols. `ftps://` (Ftp over SSH) is currently not supported.

> ##### @icon-lightbulb You can also Upload Individual Topics
> In addition to publishing the entire project you can also quickly update an indidual topic by using the @icon-arrow-up-right-from-square icon in the topic editor which opens this same dialog in single file upload mode.

## Ftp Publish Settings

* **Ftp Host Name or IP Address**  
You need to specify the host name or IP Address to the Ftp server to upload to. Note that this should be **just the hostname or IP address** without a `ftp://` prefix or a complete Url. So, `ftp.example.com` or `123.123.123.123` are valid. You can also specify a custom portname: `ftp.example.com:5621` or `123.123.123.123:5621` as part of the Host name or Ip address field.

* **Server Relative Upload Path**  
This is the server relative Ftp path to upload files to. Make sure you use a root relative that starts with a `/` for the Ftp site root and include the full path. If unsure what the path is use FileZilla or other Ftp client to check what paths you're using and duplicate that path here.

* **Username and Password**  
These days it's unlikely that you'll find a server that doesn't require username and password, so provide them here. The application remembers and stores the username across sessions in the configuration, while the password is remembered for the duration of the Documentation Monster session.


* **Delete Extra Server Files**  
When this option is checked extra files on the server are deleted in folders that are known when the project is published. It's possible that deleted or renamed folders may not be deleted since they won't be referenced from the client any longer.

> For reliable deletion of all files for a 'clean' install, we recommend you delete files on the server directly or with explicitly with an FTP occasionally and then republish. This feature is useful to clean up occasionally renamed or deleted files but it's not meant to be complete cleanup solution.

* **Open Web Site when Complete**  
Once the upload has completed it's useful to view the Web site immediately and this option opens the Web site at the designated Url. The Url is configured in the project configuration based on the Web Site Url and Relative Base Url. 


## Project Publishing is Incremental
The project publishes files **incrementally** meaning that only changed files are uploaded to the server. DM does this by comparing client and server files in all directories and comparing file sizes and approximate dates. 

So uploading a few files often can go very quick, although for large projects the file comparison task may actually be somewhat time consuming.

## The Project Dialog in Non-Modal
Note that the Project Dialog is non-modal so you can leave it open. As you work on a project, DM automatically builds any Html content both for the Previewer and for final Html content in `wwwroot` so the Html content is kept up to date as you work.

> ##### @icon-warning Images are not kept up to date unless you Build
> While Html in the output `wwwroot` folder is kept up to date, any dependencies and specifically images are not automatically updated. So if you add new images or any other non-Html dependencies into your project you have to rebuild to ensure your project is up to date.