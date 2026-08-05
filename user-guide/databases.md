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

## Creating Airtable Database Profile

![Create Airtable Profile](/assets/sd-database-settings_02.png)

!!!info Info
For Airtable Profile, it is imperative to underscore that users are mandated to utilise the provided Airtable's [Marker Data Template](/user-guide/databases/#airtable-template).
!!!

1. Click on the `+` button to Create Database Profile.
2. Enter a Profile Name.
3. For Airtable Platform, click on the `Airtable` tab.
4. Click `Save` once values are entered.

==- Airtable Token

Enter your [Airtable Token](/databases/airtable-prerequisite#obtain-your-workspace-name) here.

==- Airtable Base ID

Enter your [Airtable Base ID](/databases/airtable-prerequisite#obtain-your-base-id--table-id) here.

!!!info Info
It is strongly advised that you to duplicate the supplied [Marker Data Template](/user-guide/databases/#airtable-template). Subsequently, you can acquire the Base ID from your duplicated Airtable Template within your Workspace.
!!!
 
==- Airtable Table ID

Enter your [Airtable Table ID](/databases/airtable-prerequisite#obtain-your-base-id--table-id) here.

!!!info Info
It is strongly advised that you to duplicate the supplied [Marker Data Template](/user-guide/databases/#airtable-template). Subsequently, you can acquire the Table ID from your duplicated Airtable Template within your Workspace.
!!!

==- Rename Key Column

By [!badge text="Default"] **Marker Data** will designate the Airtable's Key Column with the nomenclature of `Marker ID`. However, you retain the flexibility to establish an alternative form of Airtable Database by integrating Marker Metadata from Final Cut Pro. To illustrate, you have the capability to designate your Airtable's Key Column as, for instance, `Shot Code`. Upon configuring this setting in Notion, you may then input the same corresponding value in this field as `Shot Code`.

!!!warning Warning
Please do not enter `Marker ID` into this field. `Marker ID` is the default key column and cannot be used in this field.
!!!

==- Dropbox App Key

Enter your [Dropbox App Key](/databases/dropbox-prerequisite) here. Setting up Dropbox integration is a one-time process. Whenever you duplicate or create a new Airtable Database Profile, the **Marker Data** feature will automatically utilise the pre-existing Dropbox App Key. If there arises a necessity to modify or refresh your Dropbox App Key, simply input the new value into the Dropbox App Key field and proceed accordingly.

![Dropbox Setup](/assets/sd-database-settings_dropbox.gif)

!!!info Info
It is advisable to ensure prior login to your Dropbox Account has been completed.
!!!

1. Ensure that all prescribed steps [delineated here](/databases/dropbox-prerequisite) have been completed.
2. Copy your App Key.
3. Paste it in the `Dropbox App Key` field.
4. Press `Continue`.
5. **Marker Data** will launch Terminal.
6. There would be small delay before the URL appears. Highlight the full URL, right-click to `Open Link`.
7. Your default browser will be launched with the URL.
8. Click `Continue` and click `Allow`.
9. Copy your unique `Authorisation code`.
10. Return back to the Terminal session, and paste the `Authorisation code`.
11. Press `Enter` on your keyboard.
12. Once `Done` appears on the Terminal session, you can close your Terminal window.
13. You will see `Dropbox configured` text on your Airtable Database Profile window.

!!!info Info
Upon initial utilisation, **Marker Data** will create a directory titled `Marker Data` within the root of your Dropbox and proceed to upload accordingly.
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

[![](/assets/template-banner-02.png)](https://soothsayer.notion.site/25939547200e4cbe85bffe5be9d84c14?v=b36de86c42774f4cb1185b862200b492){target="_blank"}

[!ref icon="paper-airplane" text="Creating Shot Library"](/in-action/creating-shot-library)

## Airtable Template

[![](/assets/template-banner-03.png)](https://www.airtable.com/universe/expzYnCE6yMri18UM/marker-data){target="_blank"}

[!ref icon="paper-airplane" text="Sending to Airtable"](/in-action/airtable-profile)
