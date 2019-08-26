# FOMC Text Analysis Project
## Authors: Jose Luis Montiel Olea, Oliver Giesecke, Anand Chitale
### Purpose: This repo contains tools to download, extract, and analyze information from the FOMC Website
## Organization:
The Repo is Organized as follows:
All relevant code is contained in the *src* folder

The src folder is broken down into three subfolders:

1. **Collection**: Contains tools for scraping, downloading, and extracting raw text from documents on the FOMC website.

2. **Derivation**: Contains tools for deriving information(such as alternatives and economic indicators) for each meeting from collected data

3. **Analysis**: Contains tools for analyzing the information we have derived on meetings and alternatives and produces figures for publication

Each of which contains the following grouped by programming language:
1. **Data**: Manually downloaded or modified files which must be read in
2. **Scripts**: Programs which produce some output
3. **Output**: Content generated by scripts


## Collection

This folder contains scripts used in order to read and download all documents from the FOMC website.

Key Files:
1. python/scripts/download_raw_doc_metadata.py:
Reads through each page of the FOMC website to meeting dates, docuemnts and links for each year. Produces output file **raw_data.csv**

2. python/scripts/extract_derived_data.py:
Reads in the raw_doc_metadata and produces a derived file derived_data.csv containing the following fields: 
['year', 'start_date', 'end_date', 'event_type','file_name', 'file_size','file_type', 'link', 'grouping','document_class']

3.
python/scripts/perform_collection.sh:
The other files in this folder are responsible for downloading and extracting raw text from specific files, as well as manually downloaded data from the data folder. This shell script executes all downloads and text extractions, execute by typing ./perform_collection.sh

## Derivation

## Analysis
