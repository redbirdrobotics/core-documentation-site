# Contributing

Feel free to add new pages of information or modify the front page information. *All pages must be written in `markdown`*. If you're unsure how to use Markdown, just copy one of the existing pages and use that as a template. For additional notes on using Markdown you can check out [this cheat sheet](https://www.markdownguide.org/cheat-sheet/). If you are curious, Discord uses the same formatting in their chat.

## Text Edits and Additions

For small edits, you can do them straight from the GitHub repository using the online editor. If you're adding new pages please make sure they follow the organization structure described below — every page must belong to a directory, have a `nav_order` assigned, and be linked to a parent page.

## Committing Changes

When committing changes from the online editor you will be prompted with the following:

![how to commit the changes on GitHub online]({{site.baseurl}}/assets/images/contribution/commit-changes-to-new-branch.png)

Select **"Create a new branch"** so that your changes can be reviewed by someone before they're submitted to make sure no errors were made and that structure is correct.

> Be sure to use a descriptive "Commit message"

---

## Site Organization

This site uses the [Just-the-Docs](https://just-the-docs.com/) Jekyll theme. Pages are organized into a **parent–child hierarchy** that drives both the left navigation sidebar and the logical grouping of content. Understanding this structure is essential before adding or rearranging pages.

### Directory Layout

All documentation pages *must* live inside the `docs/` folder. Within `docs/`, pages are sorted into **category directories** that mirror the navigation sections. For example, all GitHub-related pages go in `docs/github/`, and all standards-related pages go in `docs/standards/`.

```
docs/
├── github/          ← GitHub category directory
│   ├── github.md    ← parent page (has_children: true)
│   ├── setup.md     ← child page (parent: GitHub)
│   ├── concepts.md  ← child page
│   ├── using-desktop.md
│   └── using-bash.md
└── standards/       ← Standards category directory
    ├── standards.md ← parent page (has_children: true)
    ├── cad.md       ← child page
    ├── coding.md
    ├── electronics.md
    └── git.md
```

**Guidelines for directories:**

- **Do not create a new category directory** unless your document genuinely does not fit into an existing one.
- Keep directory names to a **single word** (e.g. `github`, `standards`).
- If your topic is too broad for any existing category, narrow its scope rather than creating an overly generic directory.
- The directory name should **match** the `title` and `nav_order` of the parent page that represents it.  
  Example: the `docs/github/` directory corresponds to the parent page `docs/github/github.md` with `title: GitHub`.

---

## Parent–Child Hierarchy (Just-the-Docs Navigation)

The Just-the-Docs theme builds the sidebar navigation from two front matter fields: `has_children` (on parent pages) and `parent` (on child pages).

### Parent Pages

A parent page acts as a section heading in the sidebar. It **must**:

1. Live inside its own category directory (e.g. `docs/github/github.md`).
2. Set `has_children: true` in its front matter.
3. Have a `nav_order` value that places it among the top-level navigation items.
4. Provide a brief overview of the section's content.

<details>
<summary>Example: parent page front matter</summary>

```markdown
---
# File: docs/github/github.md
title: GitHub
has_children: true
nav_order: 2
---
```
</details>

The top-level parent pages — visible on the home page and in the root of the sidebar — are defined in the `docs/` directory itself. Currently these are:

| Parent Page | `nav_order` | Category Directory |
|---|---|---|
| `index.md` (home) | 1 | root |
| `docs/github/github.md` — GitHub | 2 | `docs/github/` |
| `docs/standards/standards.md` — Standards | 3 | `docs/standards/` |

### Child Pages

A child page belongs to a parent section. It **must**:

1. Live inside the same category directory as its parent page.
2. Set `parent:` in its front matter to the **exact `title`** of the parent page (case-sensitive).
3. Have a `nav_order` value that determines its position **within** that parent's sub-list.

<details>
<summary>Example: child page front matter</summary>

```markdown
---
# File: docs/github/concepts.md
title: "Git Concepts"
parent: GitHub
nav_order: 3
---
```
</details>

Child page `nav_order` values are scoped to their parent — they only need to be unique within the same parent section.

---

## Navigation Order (`nav_order`)

Every page **must** include a `nav_order` field in its front matter. This field controls the order in which pages and sections appear in the sidebar.

- Top-level pages (those in `docs/` or with `has_children: true`) are ordered against each other by `nav_order`.
- Child pages are ordered relative to their siblings under the same parent.
- Lower numbers appear first. `1`, `2`, `3`, etc.
- **Do not skip numbers** for sibling pages — keep them sequential to avoid accidental gaps.
- If you add a page between two existing pages, renumber the subsequent sibling pages to maintain sequential order.

<details>
<summary>Example: nav_order conventions in the Standards section</summary>

```
Parent page:              standards.md,   nav_order: 3
Child pages:
  cad.md                  nav_order: 2
  coding.md               nav_order: 3
  electronics.md          nav_order: 4
```

If you wanted to add `mechanical.md` between `cad.md` and `coding.md`, you would set it to `nav_order: 3` and bump `coding.md` → `nav_order: 4` and `electronics.md` → `nav_order: 5`.
</details>

---

## Page Front Matter Reference

Every page must include a YAML front matter block at the very top. Below is a complete reference of the fields used:

| Field | Required | Applies To | Description |
|---|---|---|---|
| `title` | ✅ Yes | All pages | Displayed in the sidebar and as the page heading. Keep it short but clear. |
| `nav_order` | ✅ Yes | All pages | Integer that controls the order of pages. Lower numbers appear first. |
| `has_children` | When parent | Parent / section pages | Set to `true` to make this page a collapsible section heading. |
| `parent` | When child | Child pages | Must match the `title` of the parent page exactly (case-sensitive). |
| `layout` | When home | Only `index.md` | Set to `layout: home` for the landing page. |

### Complete file template

Use this template when creating a new page:

#### Parent page

```markdown
---
# File: docs/your-category/your-category.md
title: Your Category
has_children: true
nav_order: 4
---

# Your Category

A brief overview of what this section covers.
```

#### Child page

```markdown
---
# File: docs/your-category/your-page.md
title: "Your Page Title"
parent: Your Category
nav_order: 1
---

# Your Page Title

Content goes here...
```

---

## Writing Standards

- **Conciseness:** Pages must be concise. Avoid rambling or duplicating content that exists elsewhere — link to it instead.
- **Clear titles:** The title of the page must clearly define what the page is about.
- **Break down complex topics:** If a topic is large, split it into multiple child pages under an appropriate parent.
- **Cross-linking:** Use `{{site.baseurl}}/docs/path/to/page.md` when linking between pages on this site. This ensures links work both locally and when published.
- **Images:** All images must be **PNG** files. Place them inside `assets/images/`, ideally in a subdirectory named after the page (e.g. `assets/images/github-setup/` for the setup guide). Reference them using the full Jekyll-compatible format:

  ```markdown
  ![Descriptive alt text]({{site.baseurl}}/assets/images/category/image.png)
  ```

  The `{{site.baseurl}}` prefix is required for the site to render images correctly when deployed on GitHub Pages. When previewing the page **locally** before committing, simply remove `{{site.baseurl}}/` from the path so that the image reference becomes a direct relative path like `assets/images/category/image.png`. This lets your local Markdown viewer display the image while you draft.

---

## Adding a New Section (Category)

If you've determined that a new category is genuinely needed:

1. **Create the category directory** inside `docs/`, e.g. `docs/your-category/`.
2. **Create the parent page** inside that directory (e.g. `docs/your-category/your-category.md`).
3. Give the parent page `has_children: true` and a `nav_order` value that fits among the existing top-level sections.
4. Update the `nav_order` values of any existing top-level pages that need to shift.
5. Add your child pages to the same directory, each referencing the parent by its exact `title`.

> **Important:** Only create a new category if your document doesn't apply to one of the existing ones. Keep category names to a single word.

---

## Adding a Page to an Existing Section

1. Place the `.md` file inside the appropriate category directory under `docs/`.
2. Add front matter with `title`, `parent` (matching the parent page's title exactly), and a `nav_order` that fits sequentially among sibling pages.
3. Adjust the `nav_order` of any subsequent sibling pages so that ordering stays sequential with no gaps.

---

## Quick Checklist

Before submitting a pull request or merging, verify:

- [ ] File is inside `docs/<category>/` directory.
- [ ] Front matter includes `title`, `nav_order`, and either `has_children: true` or `parent:`.
- [ ] `parent:` value (if used) matches an existing parent page's `title` exactly.
- [ ] `nav_order` does not conflict with sibling pages and the sequence has no gaps.
- [ ] Category directory name matches the parent page `title` (lowercase, single word).
- [ ] New category directories (if any) are truly necessary and scoped appropriately.
- [ ] Cross-links use `{{site.baseurl}}` and point to valid paths.
- [ ] Page is written in Markdown with concise, clear content.
