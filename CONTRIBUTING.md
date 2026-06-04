# Contributing

Feel free to add new pages of information or modify the front page information. *All pages must be written in `markdown`*. If you're unsure how to use Markdown, just copy one of the existing pages and use that as a template, for additional notes on using Markdown you can checkout [this cheat sheet](https://www.markdownguide.org/cheat-sheet/). If you are curious, Discord uses the same formatting in their chat.

## Branching

Since this is mostly information, unless someone else is applying a change at the same time on the same page, don't worry about working on a separate branch. Feel free to work straight on the `main` branch here.

## Front Page

The front page of the site is the `index.md` page. Don't add any links to this to other pages as they are automatically added by the GH Pages generation once it gets pushed. Use this site purely for introductory information and additional links that aren't already pages on this site.

## New Pages

New pages *must* follow Jekyll's required format for naming. Make sure that the name of your page is sequential in a "date".

Jekyll forces the use of dates because it's made for blogs, so each page is named in `YYYY-MM-DD-title-here.md` format. The format we are using is `0001-01-01-XXX.md`. The pagination will occur just with the last 3 digits so make sure that the "date" preceding it *does not* change.

Inside each page you must also include a `title` for the automatic link to the page.
