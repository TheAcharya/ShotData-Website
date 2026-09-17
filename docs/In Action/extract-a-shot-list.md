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

<video controls width="1920">
  <source src="/assets/sd-queue-01.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

<br>

1. Drag and drop your `.fcpxml` or `.fcpxmld` file onto [Extract](/user-guide/extract), or drag a timeline / compound clip from Final Cut Pro.
2. **Shot Data** will begin the extraction.
3. **Shot Data** will write one PNG per shot and a Notion or CSV manifest into a uniquely named folder in your Export Destination.
4. When the run finishes, press `Show in Finder` to review the PNGs and manifest.

!!!info Info
If **Shot Data** cannot open the source stills, it will ask you to `Choose Media Folder` before writing PNGs — see [Choose Media Folder](/user-guide/extract#choose-media-folder). To upload a Notion extract later, see [Notion Queue](/in-action/notion-queue).
!!!

## Afterthoughts

Once a Final Cut Pro timeline has been extracted into a meaningful shot list, that shot list no longer sits inert in a folder. It lives inside a Notion database, and in doing so it becomes something a production can genuinely work with.

This is where the extraction stops being an endpoint and starts being a foundation. With the shots, their stills, and their ordering already in place, the full breadth of contemporary AI and LLM workflows becomes available to populate everything that surrounds them. By way of the [Notion MCP](https://www.notion.com/help/notion-mcp), a Notion database can be connected to virtually any AI agent, allowing column data to be drafted, refined, and populated on the fly. `Scene Description`, `Shot Size & Type`, `Camera Movement`, `Lighting Notes`, and the rest may be filled out conversationally against the very stills that were extracted, rather than typed into a spreadsheet by hand.

The practical consequence is delegation. A director need no longer be the sole bottleneck for shot list preparation. Scenes may be handed off to an assistant, who populates the accompanying data with the assistance of an AI agent, whilst the director continues cutting and locking the remaining scenes of the project. Both parties work in parallel, against the same live database, with no files to reconcile and no versions to merge.

That is the intention behind **Shot Data** stopping where it does. It undertakes the one task that cannot be delegated or inferred, namely the faithful translation of a locked stills timeline into an ordered, image-backed shot list, and then hands the production a structure that is ready to be built upon by whichever tools and collaborators suit it best.