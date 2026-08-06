# Database Platform

**Shot Data** uploads shot lists to [Notion](https://www.notion.com/) only. This page explains what Notion is, and why it was chosen instead of other database platforms such as Airtable.

## What is Notion?

[!embed](https://www.youtube.com/watch?v=gp2yhkVw0z4)

[Notion](https://www.notion.com/) is a single space where you can think, write, and plan. Capture thoughts, manage projects, or even run an entire company — and do it exactly the way you want. Notion provides the building blocks and you can create your own layouts and toolkit to get work done at an affordable cost.

Notion’s workspace allows you to write in a beautiful clean space, build your own personal wiki (with endless layers of content), plan using a kanban view, a calendar or a simple list view and last, but not least, to capture your workflows and record everything by creating databases.

If you are familiar with Final Cut Pro’s [Smart Collections](https://support.apple.com/en-sg/guide/final-cut-pro/ver2833eb5b/mac), you will feel right at home with Notion’s database. Notion’s database allows you to create custom views with specific [filters and sort criteria](https://www.notion.com/help/views-filters-and-sorts).

### Notion’s Databases

[!embed](https://www.youtube.com/watch?v=npaNKlAO7g8)

One feature that sets Notion apart from other databases (for example Airtable) is that every entry or record is its own editable page. The record you enter into your database can be opened as its own Notion page, where you can layer or add in any information or [blocks](https://www.youtube.com/watch?v=BZnR2Ml17sc) you want.

That page model suits a **shot list** particularly well: each shot can carry its still image, optional icon, and further notes or references on the same page, while the database view stays filterable and sortable for the whole production.

## Why Notion for Shot Data?

Other platforms — including [Airtable](https://www.airtable.com) — are excellent databases in their own right. Airtable, for example, leans towards a spreadsheet-like, relational data model with linked tables and automations. That is powerful for complex data modelling, but it is a different shape of tool from a shot list that producers and editors browse as pages.

**Shot Data** selects Notion because:

- **Shot pages, not only rows.** Each shot is a Notion page. You can open it, attach images, and extend it with blocks — closer to how people review and annotate a shot list than a pure grid.
- **Views that feel familiar.** Filters and sorts behave in a way that echoes Final Cut Pro Smart Collections, which fits editorial and VFX review habits.
- **A focused upload surface.** **Shot Data** merges by `Shot ID`, uploads stills as page images, and can set a page icon. Notion’s API and page model map cleanly onto that workflow without a second file-hosting path.
- **Accessibility for creative teams.** Notion’s flexible workspace and pricing make it a practical shared destination for shot lists across small and large productions.
- **Continuity with open tools.** The Notion manifest **Shot Data** writes remains compatible with [csv2notion-neo](https://github.com/TheAcharya/csv2notion-neo) for users who prefer a free, open-source command-line upload.

Supporting every database platform would dilute the product. Notion is the destination **Shot Data** is built around: still-image timelines in, structured shot list in Notion out — with CSV available when you need a local spreadsheet instead.
