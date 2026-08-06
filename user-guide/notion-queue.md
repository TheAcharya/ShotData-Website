# Notion Queue

![Notion Queue Window](/assets/sd-notion-queue.png)

**Shot Data**'s Notion Queue lists Notion shot-list extracts that are ready to upload. You can assign a [Database Profile](/user-guide/databases) to each row, then upload in sequence with `Start Upload`.

The table columns are:

| Column | Meaning |
|---|---|
| **Name** | Manifest name. Hover to see `Timeline Name - Date - Shots` from `result.json`. |
| **Shots** | Shot count from `result.json`. |
| **Upload Destination** | The Notion [Database Profile](/user-guide/databases) for that row, or `No Upload`. |
| **Status** | Idle (`-`), uploading (`Upload (n/total)`), Uploaded, or Failed. |

!!!info Info
Only **Notion** extracts appear in Notion Queue. CSV extracts are local only and are not listed.
!!!

**Shot Data**'s Notion Queue accommodates three common scenarios.

## Scenario 1 - Extract First, Upload Later

When you need to extract several timelines before uploading, choose `Notion (No Upload)` under [General → File](/user-guide/general/#extraction-format). Each extract is saved to your [Export Folder](/user-guide/general/#export-folder). Notion Queue then lists those shot lists so you can assign destinations and upload when ready.

<video controls width="1920">
  <source src="/assets/sd-queue-01.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

<br>

1. Create and set up your desired [Database Profiles](/user-guide/databases).
2. Under [General → File](/user-guide/general/#extraction-format), select `Notion (No Upload)`.
3. Extract your timelines on [Extract](/user-guide/extract).
4. Open Notion Queue. For each row, choose an Upload Destination.
5. Press `Start Upload` to begin. Press `Stop` to cancel an upload in progress.

!!!info Info
Uploads run one shot list after another. Within each list, **Shot Data** uploads rows concurrently according to Upload Threads in [Databases](/user-guide/databases). Speed depends on your network and Notion.
!!!

!!!info Info
Your Notion database title (key) column must already be named `Shot ID`. **Shot Data** will not create that column for you. See [Databases](/user-guide/databases) and the [Notion Prerequisite](/databases/notion-prerequisite).
!!!

## Scenario 2 - Load Existing Extracts

If shot-list folders already exist in an Export Destination — for example after copying them to another Mac — press `Load from Export Destination` to scan and list them.

![Load from Export Destination](/assets/sd-queue-02.gif)

- Press `Load from Export Destination` to refresh the list from the current Export Folder.
- When `Delete Folders After Upload` is enabled, folders that upload successfully are moved to the Trash.

## Scenario 3 - Drag and Drop Folders

You can drag specific extraction folders onto Notion Queue to list only those shot lists.

![Drag and Drop to Queue Window](/assets/sd-queue-03.gif)

!!!info Info
Right-click the table and choose `Clear` to empty the Queue list.
!!!
