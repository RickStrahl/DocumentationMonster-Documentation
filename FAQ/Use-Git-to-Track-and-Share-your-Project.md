Git is almost universally supported these days for developer tasks and you can use Git with Documentation Monster to share and safely archive your documentation projects.

## Git Features 
Documentation Monster has a number of Git integration features:

* Interactive Git Commit Dialog
* New Projects automatically create a Git Repo
* Attach to Remote
* Push and Pull from Repo
* Open in external Diff Viewer
* Open in external Git Client


## Interactive Commit Dialog
Probably the most useful Git integration inside of Documentation Monster is the Git Commit dialog which shows you changed files in an existing repository and allows you review changes, commit and push them to the server.

This dialog also provides access to most other Git administration features like Clone, Create and Add Remote which can also be accessed from the **File->Git** menu.

![GitCommitDialog Project](./GitCommitDialog-Project.png)

> #### @icon-info-circle Git Repository must be active
> The Git Commit Dialog only works if you have an active Git repository to start with. If Git is not enabled you will first need to create the repo in the project folder either using the Git Repository support mentioned below (**File->Git** menu) or using the Git command line or an external Git client.

The dialog acts as a control center for all things Git. You can:

* Select Files to Commit
* Commit and Commit & Push
* Push and Pull
* Compare files in an external Diff client <small>*(configurable)*</small>
* Open an external Git Client <small>*(configurable)*</small>
* Open the Remote Web site (ie. GitHub, BitBucket, GitLab etc.)
* Create or Clone a Repository or Attach to a Remote
* Switch Branches

You can of course also use any external Git Client or the Git/GitHub Command Line tools to manage the project. 

> #### @icon-lightbulb Configure a Git Client Application
> In addition to the built-in Git tooling, that's specifically geared to DM's project based tasks, you can also configure a Git Client application in the configuration via the **Git Client Executable** in **Tools -> Settings -> Application Settings** that you can invoke for more complex tasks, like conflict resolution or advanced branch management. When configured the Git Client button on the Git Commit dialog brings up the project's repository in your configured Git Client for quick access. 
> 
> DM automatically detects various common Git Clients if they are installed including GitHub Desktop, SourceTree, SmartGit and GitKraken, if the client is initially unset. But you can override to use any tool of your choice (or open a Terminal).

## Git Repository Support
You can integrate with Git in a couple of ways:

* Create a new Project which creates a Repository
* Clone an exiting DM Project Repository
* Attach to an existing Project via Remote

### New Projects automatically create a Git Repository
When you create a new Documentation Monster project - and you have Git installed locally - DM automatically creates a new Git repository. The repo is created locally, so if you want to publish on GitHub or elsewhere you'll need to connect it to an online repository.

### Clone Repository
If there's an existing Git repo online that you want to use locally you can clone the Repo by going to:

* File Menu -> Git -> Clone Repository

![Git Clone Repository](./GitCloneRepository.png)

> #### @icon-warning No Support for Authentication when Cloning
> There's no support for private repositories at the moment. If you need to clone a private repository please use the Git Command Line or another Git Tool to clone and create your folder.
>
> The recommended target location is at:
> ```text
> ~\Documents\Documentation Monster\YourProject
> ```
>
> However, once you've cloned your repo and the remote has been configured you can push to the private repo just fine from within Documentation Monster.

Assuming the cloning works without error, you can then manually open the project from that folder.

### Connect to a Remote
Although there's no support directly in Documentation Monster to create a new online repository, you can create one online, and then attach to the remote. 

To do this, go to:

* File Menu -> Git -> Attach to Remote

![Git Attach To Remote Repository](./GitAttachToRemoteRepository.png)

Once the remote is attached you can now push and pull from that repo from the Git Commit Dialog.


## Using Git for Collaboration and Syncing
As with any Git repository it's critical to update status frequently to minimize merge conflicts and perform syncing operation in the right order.

The proper sequence for a syncing process is:

* Commit any pending changes
* Push to the Remote Repo (or **Commit and Push**)
* Pull changes from the Remote Repo

If there are merge conflicts, DM does not provide a UI interface to perform the conflict resolution. For this we recommend you use an external Git client or the command line.


