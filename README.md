# AF_dynamic_vis
**Allele Frequency Dynamics Visualization**    

## Overview

This Python Jupyter Notebook file is designed to visualize genetic data, specifically allele frequency and sequencing depth in RPM (reads per million), for multiple samples of a patient. The script generates a heatmap plot using the provided data and allows for easy interpretation of genetic variations across samples.

## Features

- Calculates allele frequency and sequencing depth in RPM at specified genomic positions for each sample.
- Generates a heatmap plot with two subplots: one for allele frequency and the other for sequencing depth.
- Customizable figure size, subtitles, and file paths.

## Requirements

- Python 3.x (Originally build with Python 3.8)
- Required Python libraries: `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`

## Files and Folder Structure

To maintain an organized structure, please follow these guidelines for storing the genetic data files:
- Place the files containing base frequency and total read counts for each longitudinal sample within a folder named after the patient's ID. Append the sampling ordinal to the patient's ID for each specific sample folder.
- Organize these patient-specific folders within a main directory named after the patient's ID.
- Ensure that the Excel sheet containing sample information (metadata) is located in the same working directory as the patient folders.
- Make sure that the column name for the sample ID, which serves as the key variable in the data sheet, is labeled as 'Sample_No' in the Excel file.

Here's an illustration of the recommended folder structure:
```bash
┌─── AF_dynamic_vis.ipynb
│
└─── data/
        │
        ├─── Sample information.xlsx              # Metadata
        │
        ├─── Patient_A/ 
        │       │
        │       ├─── Patient_A-1/                 # 1st sample from patient A
        │       │        ├─── base.fqy              # base frequency file 
        │       │        └─── alignedReads.txt      # total read counts in the sample library
        │       └─── Patient_A-2/                 # 2nd sample from patient A
        │                ├─── base.fqy
        │                └─── alignedReads.txt
        │
        └─── Patient_B/
                │
                ├─── Patient_B-1/                 # 1st sample from patient B
                │        ├─── base.fqy              # base frequency file 
                │        └─── alignedReads.txt      # total read counts in the sample library
                └─── Patient_B-2/
                         ├─── base.fqy
                         └─── alignedReads.txt
```


## Usage

1. Modify the variables in the Jupyter Notebook file according to your data and preferences.

2. Execute the cells within the Jupyter Notebook file sequentially. 

3. The script will generate a heatmap plot displaying allele frequency and sequencing depth for each sample.

