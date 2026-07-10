---
label: Troubleshooting
icon: tools
order: -95
---
# Troubleshooting

Below, you will find a comprehensive list of common issues users may encounter, accompanied by solutions to resolve them.

## How to access the logs in Marker Data?

To access the logs for **Marker Data**, navigate to the `Help` menu and select `Open Logs`.

## Marker Data's Workflow Extension is not functioning. 

To ensure optimal functionality of **Marker Data**, please ensure it is installed within the Applications folder.

## Experiencing slow uploads in Notion

Notion enforces variable rate limits on its API, averaging approximately three requests per second. While brief bursts above this average may occasionally be permitted, they are not guaranteed and should not be relied upon. It is important to note that Notion’s rate limits are subject to change without notice, and we do not have control over these adjustments.

As usage approaches the rate limit, upload performance may gradually degrade, resulting in slower response times. To prevent this and avoid errors such as `500 Server Error` or `HTTP 429 (Too Many Requests)`, users are strongly advised not to upload large Data Set (e.g., 99 images) in a single batch.

Instead, we recommend uploading data in smaller batches of up to 50 items, followed by a short pause before initiating the next batch. This approach helps maintain consistent performance and minimises the risk of triggering rate-limiting errors.

For the most up-to-date information on Notion’s rate limits, please refer to their [official documentation](https://developers.notion.com/reference/request-limits).

The slow upload speed could also be attributed to potential issues with Notion's servers or regional server connectivity. Please verify the current [status](https://status.notion.so/) of Notion's servers.

## Why are there no images in the extract folder?

Please ensure that you are using **Marker Data**'s [Share Destination](/user-guide/share-destination). Images will not be extracted when using **Marker Data**'s [Workflow Extension](/user-guide/workflow-extension).

## Marker Data shows Failed to complete upload.

![Failed to complete upload](/assets/md-failed-to-complete-upload.png)

When **Marker Data** displays a `Failed to complete upload` error, it may be attributed to various underlying causes. If you are utilising a firewall application such as Little Snitch, please ensure that outgoing connections to **Marker Data** are permitted.

### Notion

If you encounter issues uploading to your Notion Database, please follow these steps to troubleshoot:

1. Navigate to the `Help` menu and select `Open Logs`.
2. Open the log file `csv2notion-neo_log.txt`.
3. Scroll down to review the most recent entries.

If you observe the error messages `HTTPError: 401 Client Error: Unauthorized for url` or `Invalid Notion token`, it is likely that either your Notion Database URL is incorrect or your Notion Integration Token is incorrect. For detailed instructions on resolving these issues, please refer to the [Notion Prerequisite](/databases/notion-prerequisite) documentation.

### Airtable

If you encounter issues uploading to your Airtable Database, please follow these steps to troubleshoot:

1. Navigate to the `Help` menu and select `Open Logs`.
2. Open the log file `airlift_log.txt`.
3. Scroll down to review the most recent entries.

If you observe the error messages `Authentication required` or `Invalid permissions, or the requested model was not found.`, it is likely that either your Airtable Token is incorrect or your Airtable Base ID & Table ID is incorrect. For detailed instructions on resolving these issues, please refer to the [Airtable Prerequisite](/databases/airtable-prerequisite) documentation.

If you observe the error message `Error in call to API function "files/create_folder": Your app is not permitted to access this endpoint because it does not have the required scope \'files.content.write\'. The owner of the app can enable the scope for the app using the Permissions tab on the App Console.')`, it is likely that the required scopes for the app utilising the Permissions tab within the Dropbox's App Console is not checked. For detailed instructions on resolving these issues, please refer to the [Dropbox Prerequisite](/databases/dropbox-prerequisite) documentation. After you have checked your and submitted the scopes, you must to re-create and start over your Dropbox refresh token again. For detailed instructions on resolving these issues, please refer to the [Creating Airtable Database Profile](/user-guide/databases/#creating-airtable-database-profile) documentation.

## Marker Data shows Failed to upload completely.

![Failed to upload completely](/assets/md-failed-to-upload-completely.png)

When **Marker Data** displays a `Failed to upload completely` error, it may be due to couple of factors. One potential cause is that you are using an Intel-based Mac, which is not supported by **Marker Data**. Starting with **Marker Data** version 1.1.0, application is exclusively build and optimised for Apple Silicon only. For further information, please refer to this [FAQ](/faq/#does-marker-data-support-intel-based-macs).

If you are utilising a firewall application such as Little Snitch, please ensure that outgoing connections to **Marker Data** are permitted.

## Final Cut Pro crashes during extraction when the timeline includes Metaburner’s Title.

[Metaburner](https://metaburner.pro)’s Title is a highly complex title effect, leading to an intricate FCPXML structure. This complexity is the primary reason Final Cut Pro encounters stability issues during the extraction process. Although image extraction may be feasible on basic timelines using Metaburner’s Title, **Marker Data** does not account for Metaburner’s Title, as we do not support third-party custom titles for parsing. It is best to avoid placing Markers on Metaburner’s Title.

If you need to burn Metaburner’s Title into your clips for image extraction via **Marker Data**, a simple solution is to pre-render the timeline. To do this, render the timeline containing Metaburner’s Title and export it as a new file. Then, create a new timeline with the rendered file and copy-paste the title containing all your markers. This approach allows you to perform extraction tasks seamlessly without encountering any issues.

## I have verified and ensured that all Notion prerequisites are met and entered correctly. However, Marker Data still shows Failed to upload completely.

1. Navigate to the `Help` menu and select `Open Logs`.
2. Open the log file `csv2notion-neo_log.txt`.
3. Scroll down to review the most recent entries.

If you encounter error messages similar to the one displayed, it may indicate that Notion has updated its APIs, requiring an update to Marker Data's Notion module.

==- 500 Server Error: Internal Server Error

```bash
2025-04-17 16:42:40,179 [ERROR   ] Error at division
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
  File "csv2notion_neo/notion_row_upload_file.py", line 38, in upload_file
  File "csv2notion_neo/notion_row_upload_file.py", line 69, in _upload_file
  File "csv2notion_neo/notion/block.py", line 224, in space_info
  File "csv2notion_neo/notion/client.py", line 294, in post
  File "requests/models.py", line 1024, in raise_for_status
requests.exceptions.HTTPError: 500 Server Error: Internal Server Error for url: https://www.notion.so/api/v3/getPublicPageData
```

==- 429 Client Error: Too Many Requests

```bash
ERROR: Error at division
Traceback (most recent call last):
  File "csv2notion_neo/cli.py", line 53, in cli
  File "csv2notion_neo/cli_steps.py", line 58, in convert_csv_to_notion_rows
  File "csv2notion_neo/notion_convert.py", line 53, in convert_to_notion_rows
  File "csv2notion_neo/notion_convert.py", line 68, in _convert_row
  File "csv2notion_neo/notion_convert.py", line 114, in _map_columns
  File "csv2notion_neo/notion_convert.py", line 136, in _map_column
  File "csv2notion_neo/notion_convert.py", line 318, in _map_relation
  File "csv2notion_neo/notion_convert.py", line 331, in _resolve_relation_by_key
  File "csv2notion_neo/notion_db.py", line 48, in rows
  File "csv2notion_neo/notion_db_collection.py", line 23, in get_unique_rows
  File "csv2notion_neo/notion_db_collection.py", line 23, in <lambda>
  File "csv2notion_neo/notion/maps.py", line 44, in fget
  File "csv2notion_neo/notion/records.py", line 108, in get
  File "csv2notion_neo/notion/records.py", line 97, in _get_record_data
  File "csv2notion_neo/notion/client.py", line 189, in get_record_data
  File "csv2notion_neo/notion/store.py", line 184, in get
  File "csv2notion_neo/notion/store.py", line 289, in call_load_page_chunk
  File "csv2notion_neo/notion/client.py", line 316, in post
  File "requests/models.py", line 1024, in raise_for_status requests.exceptions.HTTPError: 429 Client Error: Too Many Requests for url: https://www.notion.so/api/v3/loadPageChunk
```

===

Occasionally, **Marker Data**'s Notion module would become non-functional when Notion updates its APIs.

If you encounter such an problem, please open an [issue](https://github.com/TheAcharya/MarkerData/issues). With time and thorough investigation, we will release an update for **Marker Data**. However, the update may not be immediate, as it depends on our availability to analyse and resolve the issue. We appreciate your patience and understanding.

## Module Status

To streamline our internal testing process, we have implemented an automated weekly validation of Marker Data’s module.

Modules   | Status | Platform Status | Schedule
---    | --- | --- | ---
Notion  | [![notion_image_upload_test](https://github.com/TheAcharya/csv2notion-neo/actions/workflows/notion_image_upload_test.yml/badge.svg)](https://github.com/TheAcharya/csv2notion-neo/actions/workflows/notion_image_upload_test.yml) | [Notion Status](https://www.notion-status.com) | Scheduled daily at 8:00 AM Singapore time
Airtable  | [![airtable_image_upload_test](https://github.com/TheAcharya/Airlift/actions/workflows/airtable_image_upload_test.yml/badge.svg)](https://github.com/TheAcharya/Airlift/actions/workflows/airtable_image_upload_test.yml) | [Airtable Status](https://status.airtable.com) | Scheduled daily at 8:00 AM Singapore time

If the badge is green, indicating a successful test, it confirms that our modules are compatible with the supported database platforms. However, if the badge turns red, signalling a failure, an update may be necessary to ensure continued compatibility. In the event of a failure, we also recommend checking the platform's status page to rule out any ongoing outages or service disruptions.