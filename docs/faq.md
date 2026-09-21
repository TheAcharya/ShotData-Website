---
label: FAQ
icon: question
order: -93
---
# Frequently Asked Questions

## What is the purpose of the CSV Extraction Format?

The `CSV` Extraction Format exists to keep **Shot Data** deliberately open-ended. Whilst the Notion manifest is written to mirror the [Shot Data Notion Template](/user-guide/databases/#notion-template) schema, the CSV manifest makes no assumption whatsoever about where your shot list is ultimately destined.

Every CSV extract is written alongside the very same ordered PNG stills produced by any other Extraction Format, with the `Image Filename` column binding each row to its corresponding still. That pairing of a plain, standards-compliant data set with a sequenced set of images is intentionally neutral. It may be imported into a spreadsheet application, ingested by a bespoke production database, parsed by an in-house script, or repurposed entirely by a custom application built around your own pipeline.

In short, Notion is the destination **Shot Data** is built around, whilst `CSV` is the provision for everything else. You are free to take the data set and the stills and reshape them however your workflow demands.

CSV extracts are local only and do not appear in [Notion Queue](/user-guide/notion-queue). Select `Notion` or `Notion (No Upload)` as your [Extraction Format](/user-guide/general/#extraction-format) when you require Queue support.

## Is the exported CSV compatible with spreadsheet applications like Apple Numbers?

Yes. The exported `.csv` manifest follows a standard comma-separated format, so it opens directly in Apple's [Numbers](https://www.apple.com/iwork/index.html), Microsoft Excel, Google Sheets, and other spreadsheet applications that support `.csv` files, without requiring any conversion.

## Is the Notion manifest compatible with csv2notion-neo?

Yes. The Notion JSON manifest written by **Shot Data** is compatible with [CSV2Notion Neo](https://github.com/TheAcharya/csv2notion-neo), which is free and open source. You can upload that Data Set with csv2notion-neo from the command line if you prefer a terminal workflow. **Shot Data** also includes its own in-process Notion upload for the same kind of manifest.

## Why is the JSON file produced by the Notion Extraction Format mostly empty?

This is entirely by design, and is not an indication that the extraction has failed.

The Notion JSON manifest is written to be structurally identical to the [Shot Data Notion Template](/user-guide/databases/#notion-template) database schema. Every column defined in that template is present in the manifest, irrespective of whether **Shot Data** is in a position to populate it.

**Shot Data** writes only those values a still-image timeline can truthfully supply, namely `Shot ID`, `Shot Number`, `Shot Duration`, `Scene Number`, `Icon Image`, and `Image Filename`. The remaining columns, such as `Camera Angle`, `Lens`, `Scene Cast`, `Wardrobe Notes`, and `Lighting Notes`, describe creative and production intent that simply does not exist within FCPXML. Rather than fabricate those values, **Shot Data** leaves them empty for you to complete.

## Why there is no built-in Shot List Editor

It would certainly have been possible to introduce a Shot List Editor between extraction and upload, allowing those fields to be filled locally beforehand. After considerable deliberation, this was not implemented, for two reasons.

Firstly, it would immediately create two competing sources of truth. The moment you amend a shot in Notion, the locally extracted data set becomes outdated, and reconciling the two would introduce far more complexity than it resolves.

Secondly, it would be markedly slower than the alternative. Populating those fields directly within Notion, whether by hand, by way of the [Notion MCP with AI agents](https://www.notion.com/help/notion-mcp), or using [Notion's own built-in AI](https://www.notion.com/help/category/notion-ai), can be accomplished in a matter of minutes, and leaves the Notion database as the single, authoritative source of truth for the production.

The empty columns are nonetheless retained in full, so that the manifest remains faithful to the template schema and **Shot Data** is future-proofed against any expansion of the extracted field set.

## Why is there no PDF Extraction Format?

Storyboards and shot lists have traditionally been exported and circulated as PDF documents, and for a short-form piece that remains perfectly serviceable. On a production of any appreciable scale, however, that approach begins to falter.

Consider a project comprising upwards of a hundred scenes. The result is a proliferation of PDF documents to be juggled on set, tedious to search, awkward to organise, and cumbersome to distribute across departments. A PDF is, by its very nature, a static snapshot. The instant a shot is revised, reordered, or removed, every copy in circulation is rendered obsolete and the document must be regenerated and redistributed in its entirety.

A database removes those shortcomings outright. Within Notion, the same shot list may be filtered, sorted, grouped, and tagged to suit whoever happens to be consulting it, with custom views prepared for each department. Each shot is its own page, carrying its still image alongside any notes, references, or blocks appended to it as the production evolves. Revisions are reflected immediately for everyone, with no reissuing required.

That is the reasoning behind **Shot Data** producing a Shot List Database rather than a document.

## How is the Mac app different from the CLI?

**Shot Data** brings [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit)'s Shot Extraction into a native, graphical macOS interface. Options that are set via command-line flags in the CLI — such as export destination, folder naming, scene number, and Notion or CSV output — are presented as straightforward controls within the app, alongside conveniences like drag-and-drop FCPXML intake, Configurations, Notion Queue, and dual progress for extract plus optional Notion upload.

The CLI remains free and open source for terminal-based workflows and is, in effect, OpenFCPXMLKit itself. As **Shot Data** is built directly on top of this same Shot Extraction engine, the underlying extraction is the same between the two; the choice is simply a matter of interface, with the app adding the polished workflow and in-process Notion upload.

## Is there a trial version of Shot Data?

There is currently no dedicated trial version of **Shot Data**. However, prospective users are welcome to download the latest CLI build from [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit/releases), the open-source engine that powers the application. This allows you to run Shot Extraction directly from the CLI tool on your own FCPXML files, with full [documentation](https://github.com/TheAcharya/OpenFCPXMLKit/blob/main/Documentation/README.md) and usage guidance provided within the repository. If you are satisfied with the results, you can proceed to purchase **Shot Data** with confidence for the graphical workflow and in-app Notion upload.

## I do not wish to purchase Shot Data.

That is entirely understandable. You are welcome to continue using the CLI tool free of charge for as long as it suits your needs.

## I have purchased Shot Data and am not satisfied with it. Can I request a refund?

Apple provides a mechanism for requesting refunds on App Store purchases. Please refer to the steps outlined on Apple's official support [pages](https://support.apple.com/en-us/118223) to submit your request.

## What kind of timelines are supported in Shot Data?

**Shot Data** can take Projects and Compound Clips as FCPXML / FCPXMLD input. Extraction only covers the **primary timeline** (primary spine), and only **still images** on that spine are supported. Video clips, Motion templates, titles/generators, and primary-spine audio are not extracted. Connected and secondary lanes are ignored.

## Why is there no Workflow Extension for Shot Data?

Incorporating a Final Cut Pro Workflow Extension into **Shot Data** would not, in practice, unlock any meaningfully new capability for Shot Extraction. There are two principal reasons for this decision.

Firstly, a Workflow Extension would introduce a considerable degree of additional complexity to the **Shot Data** codebase, requiring ongoing maintenance to remain compatible with Final Cut Pro's own extension framework and any changes Apple may introduce to it over time. This added burden does not correspond to a proportionate benefit for the user.

Secondly, and more fundamentally, the core function of **Shot Data** does not require it. Users are already able to drag and drop their `.fcpxmld` or `.fcpxml` file directly onto **Shot Data**'s Extract panel or its Dock icon, or open a file with `⌘` `O`, achieving effectively the same outcome with no meaningful difference in convenience or speed. A Workflow Extension would, at best, offer a marginally more integrated point of entry from within Final Cut Pro itself, but would not alter the underlying extraction process or the quality of the resulting shot list in any material way.

For these reasons, the existing drag-and-drop approach is considered the most sensible and sustainable path, offering users a straightforward experience without unnecessarily expanding the scope or complexity of the application.

## Does Shot Data support Intel-based Macs?

No. **Shot Data** is built and optimised exclusively for Apple Silicon.

## Why is Shot Data only available on the latest macOS versions?

**Shot Data** requires macOS 26.0 or later, owing to Apple's policy of restricting new software features and frameworks to their most recent operating system releases. Whilst these features may technically function on older systems, Apple provides no official support for such compatibility, which presents considerable challenges for developers who must then choose between implementing extensive workarounds or confining support to older OS versions.

As an independent developer, we have elected to support the current major release of macOS, so as to avoid the complexities and time-consuming nature of such workarounds. This is a matter of practicality and efficiency, and is in no way a reflection of any lack of effort or dedication on our part.

## How is Marker Data different from Shot Data?

[Marker Data](https://markerdata.theacharya.co) and **Shot Data** are two distinct applications, each built to address a different aspect of the Final Cut Pro workflow. **Marker Data** focuses on extracting a timeline's Marker metadata, along with associated PNGs or animated GIFs, and transmitting it into Notion or Airtable, allowing teams to manage VFX shots, shot collections, comments, and edit notes within a shared, dynamic database. **Shot Data**, by contrast, creates a shot list from still-image timelines: one PNG per shot plus a Notion or CSV manifest, with optional in-app Notion upload and Notion Queue.

Put simply, **Marker Data** is oriented towards marker-driven, collaborative database workflows, while **Shot Data** is oriented towards stills-based shot lists. Both applications are built on open-source parsing foundations, and depending on your workflow, they can be used independently or alongside one another.

## How is Production Data different from Shot Data?

[Production Data](https://productiondata.theacharya.co) and **Shot Data** are two distinct applications, each built to address a different aspect of the Final Cut Pro workflow. **Production Data** turns FCPXML into production Excel and PDF reports — roles, sheets, and columns for production paperwork. **Shot Data**, by contrast, creates a Shot List Database from still-image timelines: one PNG per shot plus a Notion or CSV manifest, with optional in-app Notion upload and Notion Queue.

Put simply, **Production Data** is oriented towards production reports, while **Shot Data** is oriented towards stills-based shot lists. Together with [Marker Data](https://markerdata.theacharya.co), they form a trilogy of Final Cut Pro tools and can be used independently or alongside one another.

## Are you affiliated with Notion?

We are not associated with, nor do we have any affiliation with, Notion in any capacity.

## Is it possible to use Shot Data with the free plan of Notion?

**Shot Data** can be used with Notion's free plan. There are no technical constraints imposed by Shot Data on such usage. However, it is important to consider the limitations inherent to Notion's free tier. Specifically, Notion's free plan restricts uploads to a maximum of 5MB per file. **Shot Data** uploads each shot's PNG still (and, where set, a page icon) to Notion, so files larger than that limit may fail to upload even when extraction itself succeeds.

To use [Notion AI](https://www.notion.com/help/category/notion-ai) or the [Notion MCP](https://www.notion.com/help/notion-mcp) with the shot list, a paid Notion account is required.

## Could other database platforms be supported in the foreseeable future?

No. **Shot Data** uploads shot lists to [Notion](https://www.notion.com/) only. Our emphasis remains the steadfast support and enhancement of that Notion integration, a platform already widely embraced by users and companies across the Film and TV industry. Developing a robust in-app uploader, inspired by our very own [CSV2Notion Neo](https://github.com/TheAcharya/csv2notion-neo) project, has demanded a significant investment of time and effort.

Should you need a destination other than Notion, the `CSV` Extraction Format is the provision for that: a local, standards-compliant data set you can take wherever your pipeline requires.

## Was AI and LLMs used in the development of Shot Data?

Yes, though the extent varied across different parts of the application. The underlying engine, [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit), which handles the parsing and shot extracting logic that powers **Shot Data**, was developed with substantial assistance from various large language models throughout its creation.

The user interface, by contrast, has a more traditional origin. It was built upon the interface of [Marker Data](https://markerdata.theacharya.co), which was originally hand-written. AI and LLM tools were subsequently used to re-wire and repurpose this existing interface for **Shot Data**'s specific needs, rather than to author it from scratch.

In short, AI played a meaningful role throughout the development process, though its involvement looked rather different depending on which part of the application you're looking at, more foundational in the engine, and more of a re-wiring aid where existing, hand-written work already existed.

## Why is Shot Data a paid application?

This is a fair and reasonable question. Generating revenue from application development has never been a particular interest or priority; it has always been, first and foremost, a side project undertaken for workflow experimentation. That said, developing software for the Apple ecosystem carries genuine and ongoing costs, not least the annual Apple Developer Programme fee. Given that [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit) is provided entirely free of charge and as open-source software, it seemed only fair to position **Shot Data** as a modest paid application, offering the convenience of a polished graphical interface — including Configurations, Notion Queue, and in-app Notion upload — for those users who would rather not engage with the macOS Terminal or are unfamiliar with it.
