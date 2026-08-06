# Database Settings

![Database Settings](/assets/sd-database-settings.png)

**Shot Data** stores [Notion](https://www.notion.com/) Database Profiles so you can upload shot-list manifests during extract or later from [Notion Queue](/user-guide/notion-queue). Each profile holds a Profile Name, Integration Token, and Database URL.

## Creating a Notion Database Profile

![Create Notion Profile](/assets/sd-database-settings_01.png)

!!!info Info
Duplicate the [Shot Data Notion Template](#notion-template) first. Your database title (key) column must be named `Shot ID` and must use Notion’s **Title** property type. **Shot Data** will not create that column for you.
!!!

1. Click the `+` button to create a Database Profile.
2. Enter a Profile Name.
3. Enter your Notion Integration Token and Notion Database URL.
4. Click `Save`.

==- Notion Integration Token

Enter your [Notion Integration Token](/database/notion-prerequisite#obtain-your-integration-token) here. The field is secure.

==- Notion Database URL

Enter your [Notion Database URL](/database/notion-prerequisite#obtain-your-database-url) here. The field is secure.

!!!info Info
Duplicate the [Shot Data Notion Template](#notion-template), then copy the link from your duplicated database in Notion.
!!!

===

!!!warning Warning
Upload aborts if the live Notion database has no title property named `Shot ID`. Other manifest fields that are missing from the database schema are skipped (they are not created automatically). `Image Filename` still drives the page image upload even when it is not a database property; `Icon Image` sets the page icon and is not stored as a property.
!!!

## Upload Threads

![Upload Threads](/assets/sd-database-settings_02.png)

Press `Upload Threads` in the Databases toolbar to set how many Notion rows upload in parallel. Choices are `5`, `10`, and `15`. By [!badge text="Default"] the value is `5`.

!!!info Info
Upload Threads is app-wide. It applies to every Database Profile and to both extract-time upload and [Notion Queue](/user-guide/notion-queue). It is not stored on individual profiles.
!!!

## Duplicate Database Profile

You can duplicate any Database Profile with the `Duplicate` button.

!!!info Info
After duplicating, edit the copy and replace the Notion Database URL so each profile points at the correct destination.
!!!

## Edit Database Profile

You can edit any Database Profile with the `Edit` button.

!!!info Info
When a token expires or you rotate credentials, open the profile with `Edit`, update the values, then `Save`.
!!!

## Delete Database Profile

1. Select a profile in the table.
2. Click the `-` button.
3. Confirm deletion when prompted.

## Open Database Profiles in Finder

Select `Open Database Profiles in Finder` to reveal the folder that stores your Database Profile `.json` files. You can copy those files elsewhere for backup and restore.

## Notion Template

[![](/assets/template-banner-01.png)](https://soothsayer.notion.site/509f0a7f6eb742579160569a43116227?v=fc1eb1226b4345feb63a43a70c58c99a){target="_blank"}
