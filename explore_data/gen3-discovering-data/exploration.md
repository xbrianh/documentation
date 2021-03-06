---
description: An explanation for the Exploration page on Gen3 BioData Catalyst.
---

# Exploration

## Using Exploration

The Exploration page located in the upper right-hand section of the toolbar allows users to search through data and create cohorts. The Exploration portal contains a dynamic summary statistics display, as well as search facets leveraging the DCC Harmonized Variables.

### Data Accessibility

![Data access panel in the Exploration page. ](../../.gitbook/assets/data_access.png)

Users can navigate through data in the Exploration page by selecting any of the three Data Access categories: 

* `Data with Access`: A user can view all of the summary data and associated study information for studies the user has access to, including but not limited to Project ID, file types, and clinical variables.
* `Data without Access`: Users can still search through the available studies but only view summary statistics. Summary information will also be hidden if the select cohort contains fewer than 50 subjects \(example below\). Users can request access to data by visiting the [dbGaP homepage](https://dbgap.ncbi.nlm.nih.gov/). 

![Example: The variable of Ethnicity is hidden once the number of subjects falls below 50.](../../.gitbook/assets/ethnicity_data_access.png)

* `All Data`: Users can view all of the data available in the BioData Catalyst Gen3 platform, including studies with and without access. As a result, studies not available to a user will be locked as demonstrated below.

![](../../.gitbook/assets/restricted_data_set_access.png)

By default, all users visiting the Exploration page will be assigned to `Data with Access`.

### The Data Tab

![Exploration page with Data Access displaying the Data with Access.](../../.gitbook/assets/data_page.png)

Under the "Data" tab, users can leverage the [DCC harmonized variables](https://chs-nhlbi.org/sites/chs-nhlbi.org/files/page/Stilp_topmed_pheno_harmonization_ccc_portland_2017-03-11.pdf) to create custom cohorts. When facets are selected and/or updated to cover a desired range of values, the display will reflect the information relevant to the new applied filter. If no facets have been selected, all of the data accessible to the user will be displayed. At this time, a user can filter based on three categories of clinical information:

* `Medical History`: Standard questionnaire used to collect medical records from patients.
* `Diagnosis`: Data from the investigation, analysis and recognition of the presence and nature of disease, condition, or injury from expressed signs and symptoms; also, the scientific determination of any kind; the concise results of such an investigation.
* `Subject`: The collection of all data related to a specific subject in the context of a specific experiment.

> **NOTE**: The facet filters are based on the DCC Harmonized Variables, which are a selected subset of clinical data that have been transformed for compatibility across the dbGaP studies. TOPMed studies that do not contain harmonized clinical data at this time will be filtered out when a facet is chosen, unless the `no data` option is also selected for certain facets.

### Exporting Data from the Data Tab

After a cohort has been selected, the user will have 3 different option for exporting the data

#### Export

The options for export are as follows:

![Three options offered for data export.](../../.gitbook/assets/export_options.png)

* `Export All to Terra` :  Initiate a [Portable Format for Bioinformatics \(PFB\)](pfb-files.md#what-is-a-portable-format-for-bioinformatics-pfb) export of all clinical data and file GUIDs for the selected cohort to [BioData Catalyst powered by Terra](https://terra.biodatacatalyst.nhlbi.nih.gov/). At this time the max number of subjects that can be exported to Terra is 14,000.
* `Export to PFB` : Initiate a [PFB](./) export of all clinical data and file GUIDs for the selected cohort to your local storage.
* `Export to Workspaces` : Export a manifest to the user's workspace and make the case-associated data files available in the workspace under the `/data` directory.

> **NOTE**: PFB export times can take up to 60 minutes, but often will complete in less than 10 minutes.

### The Files Tab

![The Files Tab page.](../../.gitbook/assets/files_tab.png)

The Files tab displays study files from the facets chosen on the left-side panel \(Project ID, Data Type, and Data Format\). Each time a facet selection is made, the data summary and displays will update to reflect the applied filters.

#### Locating Unharmonized Clinical Data

The Files tab also contains files that are either case-independent or project-level. This is important for files that are part of the `Unharmonized Clinical Data` category under the Data Type field. Unharmonized clinical files are made available in two distinct data formats: 

* `TAR` : Contain a directory of TSV files that are direct downloads of unharmonized clinical data from dbGaP.
* `AVRO`: These files are the same as the unharmonized clinical data from dbGaP, but in a [PFB](pfb-files.md#what-is-a-portable-format-for-bioinformatics-pfb) file.

> **NOTE**: The unharmonized clinical data sets contains all data from the dbGaP study, but it is not cross-compatible across all studies within BioData Catalyst.

### Exporting/Downloading Data from the Files Tab

Once the user has selected a cohort, there are three options for accessing the files: 

![Two button options offered for file download or export. ](../../.gitbook/assets/download_options.png)

* `Download Manifest`: Download the file manifest using the [gen3-client](https://gen3.org/resources/user/gen3-client/). 
* `Export to Workspace`: The files can be exported to a Gen3 workspace.
* `GUID Download File Page`:  Users can download files by first clicking on the link\(s\) under the GUIDs column, followed by the Download button in the file information pages \(see below\).

![Files can be downloaded by first clicking on the link\(s\) located under the GUID column.](../../.gitbook/assets/image%20%2846%29.png)

### File Information Page

A user can visit the File Information Page after clicking on any of the available GUID link\(s\) in the Files tab page. The page will display details such as data format, size, object\_id, the last time it was updated and the md5sum. The page also contains a button to download the file via the browser \(see below\). For files that are 5GB or more, we suggest using the [gen3-client](https://gen3.org/resources/user/gen3-client/).

![An example file information page with the Download button. ](../../.gitbook/assets/file_information_page.png)

