# Contributing

Feel free to add new pages of information or modify the front page information. *All pages must be written in `markdown`*. If you're unsure how to use Markdown, just copy one of the existing pages and use that as a template, for additional notes on using Markdown you can checkout [this cheat sheet](https://www.markdownguide.org/cheat-sheet/). If you are curious, Discord uses the same formatting in their chat.

## Text Edits and Additions

For small edits, you can do them straight from the GitHub repository using the onsite editor. If you're adding new pages please make sure that your pages belong to a `nav_category` and have a `nav_order` assigned to them. You can find and create new `nav_categories` in the `_config.yml` file.

## Committing Changes

When committing changes from the online editor you will be prompted with the following:

![how to commit the changes on GitHub online]({{site.baseurl}}/assets/images/contribution/commit-changes-to-new-branch.png)

Select "Create a new branch" so that your changes can be reviewed by someone before they're submitted to make sure no errors were made and that structure is correct.

### Page Location

All pages *must* be in the `docs` folder. Within `docs` make sure that you place your pages in an appropriate category folder. For example, all GitHub related pages go in the `docs/github` directory with the `nav_category: "GitHub"` category related to it. This makes maintaining documents easier as well as maintaining the page order.

Only create a new category if your document doesn't apply to one of the existing ones, and isolate it to a single word. If your category is too broad for the page you are writing you need to narrow it down in scope.

### Writing Standard

Pages must be concise. The title of the page *must* be able to clearly define what the page will be about for the sake of clarity. Complex topics should be broken down into multiple pages.

### Format

Every page must include the following structure:

```docs/examples/doc.md
---
# File: docs/examples/doc.md
title: "Title of the document"
nav_category: "Examples"
nav_order: 1
---

# Title of the Document

Some text...
```

#### Definitions

`# File: path/to/file.md` must be the path starting at docs all the way to the file name. If you're unsure of whether you're typing it correctly look at the existing ones for reference.
`title` is used both for the navigation on the left as well as the top of the page. Keep it short and concise but still clear to the point of the page.
`nav_category` options are defined in the `_config.yml` and are used to encapsulate the page orders. Make sure that your category is appropriate and create new ones if not.
`nav_order` determines the order that the pages are listed in. This order is encapsulated by the
