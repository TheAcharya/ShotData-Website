---
label: Welcome
description: Shot Data creates a Shot List Database from Final Cut Pro still-image timelines.
icon: home
order: -1
image: /static/shot-data-social-card.png
---

# Shot Data

![](/static/shot-data-social-card.png)

The shot list database creation application crafted for [Final Cut Pro](https://www.apple.com/final-cut-pro/). It serves as a native macOS frontend for storytellers who pre-cut a project as a stills timeline, turning that intention into ordered PNG stills and a shot list before cameras roll, powered by [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit), a free and open-source, experimental FCPXML parsing engine.

## Core Features

- Create a Shot List Database from Final Cut Pro still-image timelines: one PNG per shot plus a structured shot list.
- Built for pre-cut stills timelines on the primary timeline.
- Extract as Notion or CSV, with upload to Notion when you choose a Database Profile.
- Notion Queue for extract first, upload later.
- Scene Number and Folder Format controls, plus a quick Scene Number badge on Extract.
- Drag and drop `.fcpxml` / `.fcpxmld` files, or timelines and compound clips from Final Cut Pro.
- Each extract is saved to a uniquely named folder in your Export Folder.
- Written in Apple Swift and SwiftUI.
- No hidden costs, no subscriptions, no in-app purchases.
- Available on the Mac App Store.

## Available Extraction Formats

- Notion (upload via Database Profile)
- Comma-separated values (CSV)

## Demo

==- Export to Excel

<video controls width="1920">
  <source src="/assets/sd-export-01.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

==- Review Roles

<video controls width="1920">
  <source src="/assets/sd-roles-01.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

===

## Screenshot

![Main Extract Window](/assets/sd-main.png)

![Notion Queue Window](/assets/sd-notion-queue.png)

![General Settings](/assets/sd-general-settings.png)

![Configuration Settings](/assets/sd-configuration-settings.png)

![Database Settings](/assets/sd-database-settings.png)

## System Requirements

macOS 26.0 or later
Final Cut Pro 12.0 (Lifetime / Perpetual Version) or later
Final Cut Pro Creator Studio 12.0 (Subscription Version) or later
Runs only on Apple silicon Macs
Internet connection is necessary for Notion upload

## Use Cases

- Pre-cut shot lists from storyboard stills
- Shot List Database before the shoot
- Director and cinematographer shooting-sequence visualisation
- Scene-locked stills timelines in Final Cut Pro
- Sound-locked timelines for picture and audio alignment before the shoot
- Collaborative Notion databases for locked pre-shoot intention

## Support

There is currently no dedicated trial version of **Shot Data**. However, prospective users are warmly welcome to download the latest CLI build from [OpenFCPXMLKit](https://github.com/TheAcharya/OpenFCPXMLKit), the open-source engine that powers the application, with full documentation provided within the repository. We would encourage you to test your own `.fcpxml` or `.fcpxmld` still-image timelines with the CLI first, and to proceed with purchasing **Shot Data** only once you are happy with the results, for the graphical workflow and in-app Notion upload.

Do note that OpenFCPXMLKit is offered as-is, as an open-source project, and does not come with official support. That said, if you have any questions or run into issues specifically with the downloaded **Shot Data** software, please do not hesitate to reach out. You can contact us [here](https://tech.theacharya.co).