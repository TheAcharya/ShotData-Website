---
label: Databases
icon: server
order: -5
---
# Database Settings

![Database Settings](/assets/sd-database-settings.png)

!!!info Info
Delve deeper into the distinctions and parallels between Notion and Airtable [here](/databases/database-platforms).
!!!

## Creating Notion Database Profile

![Create Notion Profile](/assets/sd-database-settings_01.png)

!!!info Info
For Notion Profile, it is imperative to underscore that users are mandated to utilise the provided Notion's [Marker Data Template](/user-guide/databases/#notion-template).
!!!

1. Click on the `+` button to Create Database Profile.
2. Enter a Profile Name.
3. For Notion Platform, click on the `Notion` tab.
4. Click `Save` once values are entered.

==- Notion Workspace

Enter your [Notion Workspace Name](/databases/notion-prerequisite#obtain-your-workspace-name) here.

==- Notion Integration Token

Enter your [Notion Integration Token](/databases/notion-prerequisite#obtain-your-integration-token) here.

==- Notion Database URL

Enter your [Notion Database URL](/databases/notion-prerequisite##obtain-your-database-url) here.

!!!info Info
Users must duplicate the supplied [Marker Data Template](/user-guide/databases/#notion-template). Subsequently, you can acquire the link from your duplicated Notion Template within your Workspace.
!!!

==- Rename Key Column

By [!badge text="Default"] **Marker Data** will designate the Notion's Key Column with the nomenclature of `Marker ID`. However, you retain the flexibility to establish an alternative form of Notion Database by integrating Marker Metadata from Final Cut Pro. To illustrate, you have the capability to designate your Notion's Key Column as, for instance, `Shot Code`. Upon configuring this setting in Notion, you may then input the same corresponding value in this field as `Shot Code`.

!!!warning Warning
Please do not enter `Marker ID` into this field. `Marker ID` is the default key column and cannot be used in this field.
!!!

==- Merge Only

Merge Only offers users selectively merge or update individual columns within a Notion Database. By [!badge text="Default"], the column selection feature of Merge Only remains inactive. The utilisation of Merge Only is only possible when Notion Database URL is provided.

!!!info Info
The utilisation of the 'Merge Only' column feature is presently confined exclusive to the Notion Database Profile.
!!!

===

## Duplicate Database Profile

You have the ability to duplicate any Database Profile by clicking on the `Duplicate` button.

!!!info Info
Through the utilisation of the `Duplicate` button, you can effortlessly generate numerous Database Profiles. The sole prerequisite is the substitution of the Database URL for Notion or the Base ID and Table ID for Airtable, thereby facilitating the quick replication of Database Profiles.
!!!

## Edit Database Profile

You have the ability to edit any Database Profile by clicking on the `Edit` button.

!!!info Info
Upon the expiration of values, such as the `Token`, upon obtaining a renewed set of Tokens, you can update your pre-existing Database Profiles. This task is accomplished by clicking the `Edit` button, followed by `Save` button.
!!!

## Delete Database Profile

1. Click on the `-` button.
2. You will be prompted for confirmation before deletion.

## Open Database Folder in Finder

Select the `Open Database Folder in Finder` link to unveil the Finder directory housing the Database Profile files. You can copy the `.json` files to another location for the purpose of creating backups and restoration of your Database Profile files.

## Notion Template

[![](/assets/template-banner-01.png)](https://soothsayer.notion.site/509f0a7f6eb742579160569a43116227?v=fc1eb1226b4345feb63a43a70c58c99a){target="_blank"}

[!ref icon="paper-airplane" text="Sending to Notion"](/in-action/notion-profile)