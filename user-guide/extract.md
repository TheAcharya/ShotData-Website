# Extract

![Extract Window](/assets/sd-main.png)

**Shot Data**'s home panel, `Extract`, lets you provide a Final Cut Pro still-image timeline and create a shot list: one PNG per shot plus a Notion or CSV manifest. Optionally upload to Notion when your [Extraction Format](/user-guide/general) is a database profile.

Following the creation of your [Configuration](/user-guide/configurations), choose an `Export Folder` and an `Extraction Format` in the footer, then provide a timeline to Extract. Set `Scene Number` and `Folder Format` under [General → File](/user-guide/general).

## Drag and Drop

![Extract Window](/assets/sd-main-01.gif)

Drag and drop an `.fcpxml` or `.fcpxmld` file onto Extract, or drag a timeline / compound clip directly from Final Cut Pro. You may also use a Finder text clipping that contains FCPXML. The drop overlay reads `Drop to Extract Timeline to Shot List`.

Alternatively, click `Choose File` or press `⌘` `O` to select a file.

Extraction begins as soon as a valid timeline is received, provided an Export Folder is set and Scene Number is not empty.

!!!info Info
**Shot Data** processes one FCPXML timeline per action. If multiple items are offered at once, only the first item is used.
!!!

!!!info Info
Extract is intended for primary-spine still-image timelines. If Final Cut Pro cannot grant access to the source stills, **Shot Data** will ask you to choose a media folder before writing PNGs.
!!!
