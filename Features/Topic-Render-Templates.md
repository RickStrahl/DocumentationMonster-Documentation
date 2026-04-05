**Documentation Monster Render Templates** render Html based templates (`.dmhtml` files by default) and merge them with a model that contains Topic, Project data and various support functions. 

These templates mix **Html** and **Handlebars** like **C#/.NET** syntax to provide flexible and highly customizable Html rendering of your topics based on an expanive model passed into each template that provides detailed Topic and Project data.

Here's how that works:

{{ Helpers.ChildTopicsList() }}