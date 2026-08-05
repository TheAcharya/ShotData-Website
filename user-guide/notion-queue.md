# Notion Queue

![Queue Window](/assets/sd-queue.png)

**Marker Data**'s Queue feature presents a sophisticated solution, empowering users to efficiently manage multiple Data Sets destined for various database and platform endpoints; [Notion](https://www.notion.com/) and/or [Airtable](https://www.airtable.com/). This functionality enables consecutive queuing of Data Sets for seamless uploading, thereby streamlining the process of data dissemination. Notably, users have the flexibility to customise Database Profiles for each individual Data Set, tailoring the upload parameters to suit specific destination requirements. Such nuanced control fosters a refined approach to data management, allowing for optimal organisation and integration within diverse database ecosystems. This level of customisation underscores **Marker Data**’s commitment to facilitating precise and tailored data handling solutions, empowering users to leverage their data effectively across disparate platforms.

**Marker Data**'s Queue functionality accommodates 3 distinct scenarios.

## Scenario 1 - No Initial Upload

When grappling with the complexities of a sizeable timeline, managing multiple timelines can prove to be a daunting task, particularly when faced with the necessity of uploading each timeline individually from Final Cut Pro. In such instances, the utilisation of the `Notion (No Upload)` or `Airtable (No Upload)` profile within the [General Setting](/user-guide/general/#profiles) of **Marker Data** provides an elegant solution. By employing this profile, users can streamline their workflow by pre-extracting all pertinent data to an [Export Destination](/user-guide/general/#export-destination) of their preference, thus alleviating the burden of individual uploads.

This approach seamlessly integrates with **Marker Data**'s Queue system, consolidating all extracted Data Sets within a single, centralised Queue window. Here, users are can assign specific [Database Profiles](/user-guide/databases) to each individual Data Set prior to initiating the upload sequence with the simple click of the `Start Upload` button.

<video controls width="1920">
  <source src="/assets/sd-queue-01.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

<br>

1. Ensure that you have created and setup your desired [Database Profiles](/user-guide/databases).
2. Under [General Setting](/user-guide/general/#profiles), depending on the platform of your choice, select `Notion (No Upload)` or `Airtable (No Upload)`.

!!!info Info
If you happen to utilise both Notion and Airtable platforms, you have the flexibility to switch between `Notion (No Upload)` or `Airtable (No Upload)` prior to dispatching your timeline to **Marker Data**'s designated Share Destination.
!!!

3. Once all of your extraction are completed, the Data Sets will be listed in Queue window.
4. For each of your Data Set, assign your desired [Database Profile](/user-guide/databases) under `Upload Destination` column.
5. Press `Start Upload` to commence upload.

!!!info Info
The upload process adheres to API constraints, necessitating a sequential transfer of individual Data Sets. Consequently, the speed of upload is subject to several variables, including the user's network connection type, geographic location, and the efficiency of the platform's servers.
!!!

## Scenario 2 - Uploading Existing Data Sets

In the scenario where **Marker Data** has been deployed onto additional computers, the duplication of Data Sets from one system to another is easily achievable. These Data Sets may be selectively copied within an existing [Export Destination](/user-guide/general/#export-destination), or alternatively, a new [Configurations](/user-guide/configurations) can be created to accommodate them. **Marker Data** will automatically load and list Data Set in Queue Window.

![Load from Export Destination](/assets/sd-queue-02.gif)

- You have the option to manually load the Data Set by pressing `Load from Export Destination`.
- When `Delete Folder After Upload` is enabled, those Data Set that have been assigned with [Database Profiles](/user-guide/databases), will be deleted upon successful upload. 

## Scenario 3 - Drag & Drop Specific Data Sets

**Marker Data** possesses the capability to discerningly list extracted Data Sets into the Queue window via the intuitive action of Drag & Drop.

![Drag & Drop to Queue Window](/assets/sd-queue-03.gif)
