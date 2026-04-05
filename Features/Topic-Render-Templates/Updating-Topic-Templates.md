
Documentation Monster ships with a default set of templates that are ready to use as is. The templates are frequently updated and each release of DM provides an updated set of templates.

Even if you use the templates without any customizations, you'll want to update your templates to get the latest features and improvements in those templates to get applied to your project.

You can use the Main Menu to access:

* **Build** -> **Update Output Scripts and Templates**

This operation does two things:

* Makes a backup <small>*(in a `_docmonster-date` folder of your project)*</small>
* Copies the new templates into `_docmonster` folder

> Once you've made sure that your templates are up to date and rendering properly you can delete these backup folders.

## What to check after updating
If you customized your templates you can use a Compare Tool like [Beyond Compare](https://www.scootersoftware.com/home) or the [VS Code](https://visualstudio.microsoft.com/downloads/) Diff editor to compare file changes.

The most common changes are likely to be in `_layout.dmhtml` and `docmonster.css`, so those two are where we suggest you start with comparisons.

If your changes are more complex it might take more work, but we recommend to keep your main templates as close as possible to the originals with the majority of UI layout changes confined to the `_layout.dmhtml` and `docmonster.css` files.