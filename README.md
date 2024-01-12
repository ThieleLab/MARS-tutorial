![MARS Image](images/MARS.png)

# MARS-tutorial
This tutorial guides you through using the MARS Streamlit application

## Table of Contents
1. [User Interface Walkthrough](#user-interface-walkthrough)
2. [Data Input](#data-input)
3. [Using the Application](#using-the-application)
4. [Interpreting Results](#interpreting-results)
5. [Troubleshooting](#troubleshooting)
6. [Appendix](#appendix)

<a name="user-interface-walkthrough"></a>
## User Interface Walkthrough
![Opening Image](images/Opening.png)

### Optional Parameters

**Cutoff Slider**: This slider allows you to set a cutoff value for the relative abundance data. Any taxa with values below this threshold can be ignored or considered as noise.

**Output Format**: Here you can select the desired output file format for your processed data. The options include:

**csv**: A comma-separated values file which is widely used and compatible with most spreadsheet applications.
**txt**: A plain text file.
**xlsx**: An Excel spreadsheet file format.
**Stratification File Upload**: You can drag and drop or browse to upload a stratification file. This file should contain groupings or classifications within your data, which can be useful for downstream analysis.

**Skip ANT Checkbox**: If you want to process your data without using the Automated NCBI Taxonomy (ANT) tool, you can check this box.

### File Upload Sections

There are four main areas where you can upload different types of files:

1. **Upload Taxonomy Table**
Drag and drop or browse to upload your taxonomy table here. The file should be in one of the following formats: CSV, TSV, TXT, XLSX.

2. **Upload Feature Table**
Here you can upload the feature table, which typically includes quantitative data on the features (like OTUs, taxa, or genes) identified in your samples.

3. **Upload Combined Table**
If you have a combined table that includes both taxonomy and feature data, you can upload it in this section.

4. **Upload Resource File (Optional)**
This is an optional upload for your own resource file. Use this if you have a custom resource file that you want to include in the analysis.

Each file upload section has a limit of 200MB per file.

After you've uploaded your files, the application will process the data based on MARS and ANT algorithms, and you'll be able to download the results or view them within the interface.

### Getting Started

To begin using the application:

1. Set your desired optional parameters.
2. Upload the necessary files in their respective sections.
3. If you choose to skip ANT, make sure to check the box.
4. Once all files are uploaded, the application will start processing your data when the `Process Files` button is clicked.
5. After processing, view the results directly in the application or download the output files in your chosen format.

![Middle Image](images/Middle.png)

**Process Files**: This is the button to start the processing of your data.

The Streamlit application will provide real-time updates on the processing status. 

![Middle2 Image](images/Middle2.png)

### Results Summary and Data Download

After the processing is complete, the application displays a summary of the results along with options to download the data. Here's an explanation of each element visible in this section:

**Number of species found in resource**: This indicates the total number of unique species identified in the selected resource from your dataset, which in this case is `313`.

**Number of homosynonyms found in resource**: Displays the count of homosynonymous terms identified, `6` in this case, which helps in understanding the complexity of taxonomic naming in your dataset.

### Results Table
The results table is divided into several columns, each providing valuable information:

**Species in Resource**: Lists the species that were successfully mapped to the resource database from your dataset.
**Homosynonyms in Resource**: Shows if any alternative names (homosynonyms) that correspond to the primary species name were found in the resource.
**NCBI Taxonomic IDs**: Provides the unique identifier assigned to each species by the NCBI Taxonomy database.
**All Found Homosynonyms**: Lists all the homosynonyms or alternative names found for each species.

### Data Download

**Download Species**: This button allows you to download the list of species and related information processed by the application.

![End Image](images/End.png)

Once your data has gone through normalization and the presence checks in the resource, the application will display the outputs as follows:

### Metric Table

The metric table provides a detailed breakdown of the normalized data across different taxonomic levels:

**Normalized**: This column shows the normalized values, indicating the relative abundance or presence of taxa within the sample after normalization.
**Present**: The number of times a taxon appears in the dataset (i.e., is present).
**Absent**: A count of how many taxa expected in the resource were not found in the dataset.
**Metrics**: This is a placeholder that suggests additional metrics may be displayed or available for download.

The table headers (Kingdom, Phylum, Class, Order, Family, Genus, Species) represent different taxonomic classifications of the organisms in your dataset. Each row under these headers shows the corresponding data for each taxon, such as 'Archaea' or 'Bacteria', and their respective normalized values and presence across various taxonomic categories.

**Download Kingdom**: This button allows you to download the information related to the 'Kingdom' taxonomic level. Presumably, similar buttons for other taxonomic levels would allow you to download those specific datasets as well.

<a name="data-input"></a>
## Data Input
See files directory for examples of acceptable input files

<a name="interpreting-results"></a>
## Interpreting Results
See files directory for examples of acceptable input files

<a name="troubleshooting"></a>
## Troubleshooting
See files directory for examples of acceptable input files

<a name="appendix"></a>
## Appendix
See files directory for examples of acceptable input files

