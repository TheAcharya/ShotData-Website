---
label: Extract
icon: home
order: -2
---
# Extract

![Extract Window](/assets/sd-main.png)

**Shot Data**'s home panel, `Extract`, lets you provide a Final Cut Pro still-image timeline and create a shot list: one PNG per shot plus a Notion or CSV manifest. Optionally upload to Notion when your [Extraction Format](/user-guide/general) is a database profile.

Following the creation of your [Configuration](/user-guide/configurations), choose an `Export Folder` and an `Extraction Format` in the footer, then provide a timeline to Extract. Set `Scene Number` and `Folder Format` under [General → File](/user-guide/general).

## Scene Number

![Extract Window](/assets/sd-main-02.png)

A ruby `Scene` badge sits in the top-right corner of Extract. Click it to open a quick Scene Number editor without leaving the panel.

The value is the same `Scene Number` stored under [General → File](/user-guide/general). Shot IDs use the form `{Scene Number}-{NNN}` — for example `1-001` or `50A-001`.

!!!info Info
Scene Number must not be empty before extraction begins. Alphanumeric values are allowed.
!!!

## Drag and Drop

![Extract Window](/assets/sd-main-01.gif)

Drag and drop an `.fcpxml` or `.fcpxmld` file onto Extract, or drag a timeline / compound clip directly from Final Cut Pro. You may also use a Finder text clipping that contains FCPXML. The drop overlay reads `Drop to Extract Timeline to Shot List`.

Alternatively, click `Choose File` or press `⌘` `O` to select a file.

Extraction begins as soon as a valid timeline is received, provided an Export Folder is set and Scene Number is not empty.

!!!info Info
**Shot Data** processes one FCPXML timeline per action. If multiple items are offered at once, only the first item is used.
!!!

!!!info Info
Extract is intended for primary-spine still-image timelines. If **Shot Data** cannot open the source stills, it will ask you to `Choose Media Folder` before writing PNGs — see [Choose Media Folder](#choose-media-folder).
!!!

## Choose Media Folder

After planning shots, **Shot Data** may show `Choose Media Folder` if it cannot open the source stills — for example after dragging a timeline from Final Cut Pro (staged in Cache), when stills live on another volume, or when stills sit inside a Final Cut Pro library (`.fcpbundle`).

The panel message is `Original media, a Final Cut Pro library, or an enclosing folder.` Select one of those, then press `Grant Access`.

- The folder that holds your original stills
- The Final Cut Pro library (`.fcpbundle`) that contains those stills
- A parent folder that contains the library or the stills

If the first choice does not unlock every still, **Shot Data** offers `Choose Another Folder` or `Cancel Extract`. Closing the panel or pressing `Cancel Extract` stops the extraction cleanly — it is not treated as a hard failure.

!!!info Info
The [Export Folder](/user-guide/general/#export-folder) bookmark does not automatically cover source media. A media-folder grant is session-only for that extract and is not saved under [General](/user-guide/general). If stills remain unreadable, see [Troubleshooting](/troubleshooting#prompted-to-choose-a-media-folder--stills-cannot-be-read).
!!!
