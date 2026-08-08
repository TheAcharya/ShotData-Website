---
label: FAQ
icon: question
order: -93
---
# Frequently Asked Questions

## Is the exported CSV compatible with spreadsheet applications like Apple Numbers?

Yes. The exported `.csv` manifest follows a standard comma-separated format, so it opens directly in Apple's [Numbers](https://www.apple.com/iwork/index.html), Microsoft Excel, Google Sheets, and other spreadsheet applications that support `.csv` files, without requiring any conversion.

## Is the Notion manifest compatible with csv2notion-neo?

Yes. The Notion JSON manifest written by **Shot Data** is compatible with [csv2notion-neo](https://github.com/TheAcharya/csv2notion-neo), which is free and open source. You can upload that Data Set with csv2notion-neo from the command line if you prefer a terminal workflow. **Shot Data** also includes its own in-process Notion upload for the same kind of manifest.

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

Secondly, and more fundamentally, the core function of **Shot Data** does not require it. Users are already able to drag and drop their `.fcpxmld` or `.fcpxml` file directly onto **Shot Data**'s Extract panel or its Dock icon, or open a file with `⌘O`, achieving effectively the same outcome with no meaningful difference in convenience or speed. A Workflow Extension would, at best, offer a marginally more integrated point of entry from within Final Cut Pro itself, but would not alter the underlying extraction process or the quality of the resulting shot list in any material way.

For these reasons, the existing drag-and-drop approach is considered the most sensible and sustainable path, offering users a straightforward experience without unnecessarily expanding the scope or complexity of the application.

## Does Shot Data support Intel-based Macs?

No. **Shot Data** is built and optimised exclusively for Apple Silicon.

## Why is Shot Data only available on the latest macOS versions?

**Shot Data** is compatible exclusively with the current and preceding major release of macOS, owing to Apple's policy of restricting new software features and frameworks to their most recent operating system releases. Whilst these features may technically function on older systems, Apple provides no official support for such compatibility, which presents considerable challenges for developers who must then choose between implementing extensive workarounds or confining support to the most current OS versions.

As an independent developer, we have elected to support only the current and immediately preceding major release of macOS, so as to avoid the complexities and time-consuming nature of such workarounds. This is a matter of practicality and efficiency, and is in no way a reflection of any lack of effort or dedication on our part.

## How is Marker Data different from Shot Data?

[Marker Data](https://markerdata.theacharya.co) and **Shot Data** are two distinct applications, each built to address a different aspect of the Final Cut Pro workflow. **Marker Data** focuses on extracting a timeline's Marker metadata, along with associated PNGs or animated GIFs, and transmitting it into Notion or Airtable, allowing teams to manage VFX shots, shot collections, comments, and edit notes within a shared, dynamic database. **Shot Data**, by contrast, creates a shot list from still-image timelines: one PNG per shot plus a Notion or CSV manifest, with optional in-app Notion upload and Notion Queue.

Put simply, **Marker Data** is oriented towards marker-driven, collaborative database workflows, while **Shot Data** is oriented towards stills-based shot lists. Both applications are built on open-source parsing foundations, and depending on your workflow, they can be used independently or alongside one another.

## Was AI and LLMs used in the development of Shot Data?

Yes, though the extent varied across different parts of the application. The underlying engine, [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit), which handles the parsing and shot extracting logic that powers **Shot Data**, was developed with substantial assistance from various large language models throughout its creation.

The user interface, by contrast, has a more traditional origin. It was built upon the interface of [Marker Data](https://markerdata.theacharya.co), which was originally hand-written. AI and LLM tools were subsequently used to re-wire and repurpose this existing interface for **Shot Data**'s specific needs, rather than to author it from scratch.

In short, AI played a meaningful role throughout the development process, though its involvement looked rather different depending on which part of the application you're looking at, more foundational in the engine, and more of a re-wiring aid where existing, hand-written work already existed.

## Why is Shot Data a paid application?

This is a fair and reasonable question. Generating revenue from application development has never been a particular interest or priority; it has always been, first and foremost, a side project undertaken for workflow experimentation. That said, developing software for the Apple ecosystem carries genuine and ongoing costs, not least the annual Apple Developer Programme fee. Given that [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit) is provided entirely free of charge and as open-source software, it seemed only fair to position **Shot Data** as a modest paid application, offering the convenience of a polished graphical interface — including Configurations, Notion Queue, and in-app Notion upload — for those users who would rather not engage with the macOS Terminal or are unfamiliar with it.
