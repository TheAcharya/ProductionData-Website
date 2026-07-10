---
label: Creating VFX Database
icon: file
order: -2
---
# Creating VFX Database

[Josh Beal](https://www.jkbedit.com) provides a compelling analysis, drawing a noteworthy comparison between the workflows of two prominent video editing platforms, namely [Media Composer](https://www.avid.com/media-composer) and [Final Cut Pro](https://www.apple.com/final-cut-pro/), particularly in the context of VFX database creation. Unquestionably, Josh affirms the superiority of Final Cut Pro's methodology, attributing this advantage to the efficacy of FCPXML's metadata handling capabilities.

[!embed](https://www.youtube.com/watch?v=Md-hNTzr5UE)

## Glaring Pain Points

### Batch exporting still frames for thumbnails & frame identification

Within Final Cut Pro, the capability to extract individual still frames is present through the utilisation of the native Save Current Frame preset, which can be seamlessly integrated into the [share destination](https://support.apple.com/en-sg/guide/final-cut-pro/ver9fd008a21/mac) menu. While the software inherently supports the batch exportation of clips, it is noteworthy that, for still frames, the process remains constrained to a one-by-one basis. Nevertheless, a solution lies in the creation of a [Custom Compressor Setting](https://support.apple.com/en-sg/guide/compressor/cpsr52823a16/mac) tailored specifically for the batch export of still frames. It is imperative to acknowledge that despite the implementation of this customised setting, a manual process involving the transfer of desired clips into compound clips and subsequent frame selection is requisite for optimal results.

![Excerpts from Josh Beal’s Video](/assets/jb-batch_export_still_frames.gif)

!!!info Info
Requires too many steps in my textbook. Consider the implications when confronted with the management of 500 visual effects shots.
!!!

### Extracting Marker information & match still’s filename

An application of notable repute, [Producer’s Best Friend](https://intelligentassistance.com/producer-s-best-friend.html), offers a sophisticated utility for Final Cut Pro users. Leveraging the FCPXML file format, this tool facilitates the meticulous extraction of comprehensive metadata from any given timeline, presenting users with the capability to systematically compile this information into a structured spreadsheet. Remarkably adept in its functionality, Producer’s Best Friend stands out as an exceptional resource, particularly for the purpose of generating and extracting targeted reports derived from diverse Final Cut Pro projects.

![Excerpts from Josh Beal’s Video](/assets/jb-extract_metadata.gif)

!!!info Info
Once more, the establishment of a comprehensive dataset correlating with thumbnails demands supplementary application and additional procedural tasks.
!!!

### Sending & Managing VFX Data Set to a Database Application

Josh Beal employs Airtable as the cornerstone for his dataset management. Undoubtedly, Airtable stands as a potent cloud-based database application, boasting a plethora of attributes ranging from automations, scripting, and extensions to robust features for report generation and collaborative efforts. However, it is essential to note that users may incur a considerable expense, particularly with regard to collaborative expansion and the acquisition of additional user licenses, as detailed in the pricing structure [here](https://www.airtable.com/pricing). Furthermore, certain advanced database views and features are restricted to higher-tier paywall access. Consequently, exploring alternative database platforms becomes an advisable consideration for the discerning end user.

![Excerpts from Josh Beal’s Video](/assets/jb-airtable_database.gif)

!!!info Info
The aforementioned illustration demonstrates the amalgamation of image dataset and a `.csv` dataset facilitated by Airtable's [CSV Import Extension](https://support.airtable.com/docs/csv-import-extension). Nevertheless, a modest degree of manual intervention remains necessary for the mapping of data to the respective fields.
!!!

### Creating Burn-In labels

Numerous methodologies exist for generating Burn-In labels on still frames. Josh Beal employs a sophisticated approach by utilising a specialised [Effect Template](https://support.apple.com/en-sg/guide/motion/motn141bbb1f/mac) within Final Cut Pro, derived from Apple Motion. This template serves as a pivotal tool in crafting the desired Burn-In label on individual frames."

![Excerpts from Josh Beal’s Video](/assets/jb-burn-ins.gif)

!!!info Info
The utilisation of an Effect Template originating from Apple Motion constitutes a commendable strategy, its efficacy contingent upon the desired outcome. Possessing a bespoke Effect Template for the integration of Burn-In labels consistently proves to be a valuable asset.
!!!

**Is there room to revamp and enhance this workflow?**