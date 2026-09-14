---
label: Extract a Shot List
icon: video
order: -1
---
# Extract a Shot List

![](/assets/content-banner-notion.png)

## Configuration Setup

![Create Configuration for Shot List](/assets/sd-extract-a-shot-list-01.gif)

1. [Create Your Configuration](/user-guide/configurations/#add-configuration).
2. Select your desired Export Destination by clicking on the [Folder Icon](/user-guide/general/#export-folder).
3. Select your desired [Extraction Format](/user-guide/general/#extraction-format). `Notion (No Upload)` [!badge text="Default"] writes a local Notion JSON manifest and PNGs. `CSV` writes a local CSV manifest and PNGs.
4. Set [Scene Number](/user-guide/general/#scene-number) and [Folder Format](/user-guide/general/#folder-format) under [General → File](/user-guide/general).
5. Return to Configurations to [Update Active Configuration](/user-guide/configurations/#update-active-configuration).

!!!info Info
By [!badge text="Default"], **Shot Data** uses `Notion (No Upload)`. CSV extracts are local only and do not appear in [Notion Queue](/user-guide/notion-queue). Extraction begins as soon as a valid timeline is received.
!!!

## Final Cut Pro to Shot List

![Extract a Shot List](/assets/sd-main-01.gif)

<br>

1. Drag and drop your `.fcpxml` or `.fcpxmld` file onto [Extract](/user-guide/extract), or drag a timeline / compound clip from Final Cut Pro.
2. **Shot Data** will begin the extraction.
3. **Shot Data** will write one PNG per shot and a Notion or CSV manifest into a uniquely named folder in your Export Destination.
4. When the run finishes, press `Show in Finder` to review the PNGs and manifest.

!!!info Info
If **Shot Data** cannot open the source stills, it will ask you to `Choose Media Folder` before writing PNGs — see [Choose Media Folder](/user-guide/extract#choose-media-folder). To upload a Notion extract later, see [Notion Queue](/in-action/notion-queue).
!!!
