---
label: Troubleshooting
icon: tools
order: -95
---
# Troubleshooting

Below, you will find a comprehensive list of common issues users may encounter, accompanied by solutions to resolve them.

## How to access the logs in Marker Data?

To access the logs for **Shot Data**, navigate to the `Help` menu and select `Open Logs`.

## Why is the upload speed to Notion slow?

The slow upload speed to Notion could be attributed to potential issues with Notion's servers or regional server connectivity. Please verify the current [status](https://status.notion.so/) of Notion's servers.

## Final Cut Pro crashes during extraction when the timeline includes Metaburner’s Custom Title.

Metaburner’s Custom Title is a highly complex title effect, leading to an intricate FCPXML structure. This complexity is the primary reason Final Cut Pro encounters stability issues during the extraction process. Additionally, **Marker Data** does not account for Metaburner’s Custom Title, as we do not support third-party custom titles for parsing.

If you need to burn Metaburner’s Title into your clips for image extraction via **Marker Data**, a simple solution is to pre-render the timeline. To do this, render the timeline containing Metaburner’s Title and export it as a new file. Then, create a new timeline with the rendered file and copy-paste the title containing all your markers. This approach allows you to perform extraction tasks seamlessly without encountering any issues.

## I have verified and ensured that all Notion prerequisites are met and entered correctly. However, Marker Data still shows Failed to upload completely.

1. Navigate to the `Help` menu and select `Open Logs`.
2. Open the log file `csv2notion-neo_log.txt`.
3. Scroll down to review the most recent entries.

If you encounter error messages similar to the one displayed, it may indicate that Notion has updated its APIs, requiring an update to Marker Data's Notion module.

```bash
2025-02-15 10:23:02,118 [ERROR   ] Error at division
Traceback (most recent call last):
  File "csv2notion_neo/cli.py", line 58, in cli
  File "csv2notion_neo/cli_steps.py", line 80, in upload_rows
  File "tqdm/std.py", line 1181, in __iter__
  File "csv2notion_neo/utils_threading.py", line 39, in process_iter
  File "csv2notion_neo/utils_threading.py", line 39, in <genexpr>
  File "concurrent/futures/_base.py", line 437, in result
  File "concurrent/futures/_base.py", line 389, in __get_result
  File "concurrent/futures/thread.py", line 57, in run
  File "csv2notion_neo/utils_threading.py", line 27, in worker
  File "csv2notion_neo/notion_uploader.py", line 33, in upload_row
  File "csv2notion_neo/notion_uploader.py", line 50, in _get_db_row
  File "csv2notion_neo/notion_db.py", line 106, in add_row
  File "csv2notion_neo/notion_db_collection.py", line 39, in add_row_block
  File "csv2notion_neo/notion_db_collection.py", line 69, in _add_row_block
  File "csv2notion_neo/notion_row.py", line 46, in icon
  File "csv2notion_neo/notion_row_upload_file.py", line 21, in upload_filetype
  File "csv2notion_neo/notion_row_upload_file.py", line 41, in upload_file
```

Occasionally, **Shot Data**'s Notion module would become non-functional when Notion updates its APIs. This occurs due to the reliance on [unofficial APIs](/faq/#what-rationale-underlies-the-utilisation-of-notion-v2-tokens-in-lieu-of-official-api-provided-by-notion).

If you encounter such an problem, please open an [issue](https://github.com/TheAcharya/ShotData/issues). With time and thorough investigation, we will release an update for **Shot Data**. However, the update may not be immediate, as it depends on our availability to analyse and resolve the issue. We appreciate your patience and understanding.

## Module Status

To streamline our internal testing process, we have implemented an automated weekly validation of Marker Data’s module.

Modules   | Status | Schedule
---    | --- | ---
Notion  | [![notion_image_upload_test](https://github.com/TheAcharya/csv2notion-neo/actions/workflows/notion_image_upload_test.yml/badge.svg)](https://github.com/TheAcharya/csv2notion-neo/actions/workflows/notion_image_upload_test.yml) | Scheduled weekly on Saturdays at 8:00 AM Singapore time

If the badge is green, indicating a successful test, it confirms that our modules are compatible with the supported database platforms. However, if the badge turns red, signalling a failure, an update may be necessary to ensure continued compatibility.