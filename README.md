# WoRMS_matching
This folder contains scripts from September-December 2019, aimed at cleaning data from the Mariana Back-arc for publication (BCO-DMO, OBIS, GBIF, etc.). Some scripts were used for the actual data cleaning, and some were used to demonstrate, out of context and on simplified datasets, specific parts of that cleaning process. This README contains brief descriptions of each of the scripts.

<br>Note, December 13, 2019:
<br>Most of the files in this repository use functions from worrms and/or taxize. Some of the notes regarding those packages in the notebooks may be out of date, but nevertheless, reflect our knowledge of those package at the time of writing for the notebook. One of the more prevasive issues/notes is that the developmental version of 'taxize', which can be installed via "remotes::install_github("ropensci/taxize")" (which requires the package 'remotes' to be preinstalled), DOES have options for fuzzy matching, marine only or not, etc., while the one downloaded using "install_packages("taxize")" DOES NOT. Many of the files only note that "taxize" doesn't return non-marine results; this is because we were unaware of the developmental version of taxize at the time of writing. 
<br>
<br>Despite what the scripts in this folder may say, <b>please use the developmental version of taxize ("remotes::install_github("ropensci/taxize")"</b>, NOT the version installed via normal package installation. 

<h2>Contents</h2>
<b>Files that should be in this repository: </b>
<br>-BCODMO_demo_112019.Rmd
<br>-demo_modified_forLaurenM.Rmd
<br>-demo_modified_forLaurenM.nb.html
<br>-early_demo_BCODMO_2019_submission_worrms_taxize.Rmd
<br>-name_from_AphiaID_example.Rmd
<br>-name_from_AphiaID_example.nb.html
<br>-Snail_BCODMO_working_2019113.Rmd
<br>-Snail_plankton_BCODMO_working.Rmd
<br>-Snail_plankton_BCODMO_working.nb.html

<h2>Description of Each File</h2>
<b>File Name: BCODMO_demo_112019.Rmd</b>
<br><b>Purpose</b>: Share R functions used in cleaning data for BCO-DMO submission
<br><b>Description:</b> Demonstration of R functions used for cleaning data from hydrothermal vent macrofauna sample (Snail Vent, Mariana Back-arc) for submission to BCO-DMO and OBIS for end-of-semester lab meeting. Focused and formatted for usefulness to other students. Includes generation of a dataframe with common potential complications to cleaning (wrong AphiaID, misspelling, commentary in the name field, etc). Scripts involve retrieval of AphiaID, scientific name, taxonomic rank, kingdom, and phylum from the World Register of Marine Species (WoRMS), as well as creating occurrenceIDs unique within the dataset, and generating LSIDs using the AphiaID.
<br><b>Comments:</b> Uncertain version differences between this and early_demo_BCODMO_2019_submission_worrms_taxize.Rmd
<br><b>Status:</b> Not Updating(last update Nov. 20, 2019)

<br><b>File Name: demo_modified_forLaurenM.Rmd</b>
<br><b>Purpose:</b> Use list of names to get a dataframe (name, LSID, phylum, taxonomic rank) for submission to BCO-DMO
<br><b>Description:</b> Adapted from demonstrations of cleaning data for BCO-DMO (BCODMO_demo_112019.Rmd and early_demo_BCODMO_2019_submission_worrms_taxize.Rmd), specifically written for a specific dataset. Uses provided names to get WoRMS identifiers (AphiaID), which were in turn used to get LSIDs, scientific names, check assigned scientific name and taxonomic rank, check acceptance status of the name, provide the accepted name and associated AphiaID, check if accepted and assigned AphiaIDs match, and retrieve phylum.
<br><b>Comments:</b> Should be manually checked before submitting data, as entries in "scientificName" column may be inappropriately matched with the wrong taxon (eg, matching with the common name of plant instead of a marine species). The output dataset also needs to be manually checked/modified for entries for which no AphiaID/etc were found (eg. "unknown animal"). Some of the commentary outside of R chunks may be out of date.
<br><b>Status:</b> Not Updating (last update Dec. 9, 2019)

<br><b>File Name: demo_modified_forLaurenM.nb.html</b>
<br><b>Purpose:</b> Alternative viewing of R notebook demo_modified_forLaurenM.Rmd
<br><b>Description:</b> HTML output of the aforementioned notebook.
<br><b>Comments:</b> None.
<br><b>Status:</b> Not Updating (last update Dec. 4, 2019)

<br><b>File Name: early_demo_BCODMO_2019_submission_worrms_taxize.Rmd</b>
<br><b>Purpose:</b> Share R functions used in cleaning data for BCO-DMO submission.
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> Uncertain version differences are between this and BCODMO_demo_112019.Rmd
<br><b>Status:</b> Not Updating (last update Dec. 5, 2019; may just be from renaming)

<br><b>File Name: name_from_AphiaID_example.Rmd</b>
<br><b>Purpose:</b> Get scientific name using AphiaID
<br><b>Description:</b> A short script demonstrating a way to get the scientific name associated with an AphiaID, using either taxize or worrms. Creates an artificial dataframe with intentional errors (including missing AphiaIDs, incorrect AphiaIDs, and AphiaIDs as characters instead as numeric), with the columns AphiaID, scientificName, and counts. Uses for loops to check the list of AphiaIDs and get associated scientificName, via either id2name() (taxize) or wm_id2name (from worrms). Also checks retrieved scientific names against manually entered ones to make sure they match, and notes the result of that check in another column.
<br><b>Comments:</b> The functions used herein are also present in some of the other scripts, but are here separately to make them easier to find.
<br><b>Status:</b> Not Updating (last update Dec. 5, 2019)

<br><b>File Name: name_from_AphiaID_example.nb.html</b>
<br><b>Purpose:</b> Alternative viewing of R notebook name_from_AphiaID_eample.Rmd
<br><b>Description:</b> HTML output of the aforementioned notebook.
<br><b>Comments:</b> None.
<br><b>Status:</b> Not Updating (last update Dec. 5, 2019)

<br><b>File Name: Snail_BCODMO_working_20191113.Rmd</b>
<br><b>Purpose:</b> Clean Snail Vent macrofauna data for submission to BCODMO, OBIS
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> Last version of this notebook; previous versions on Google Drive with different dates at end
<br><b>Status:</b> Not Updating (last update Nov. 13, 2019)

<br><b>File Name: Snail_plankton_BCODMO_working.Rmd</b>
<br><b>Purpose:</b> Clean plankton data from multiple sites (including Snail Vent) for submission to BCODMO
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> Will not be complete by the end of volunteer appointment, but can be built upon.
<br><b>Status:</b> In Progress

<br><b>File Name: Snail_plankton_BCODMO_working.nb.html</b>
<br><b>Purpose:</b> Alternative viewing of R notebook Snail_plankton_BCODMO_working.Rmd
<br><b>Description:</b> HTML output of aforementioned notebook
<br><b>Comments:</b> None.
<br><b>Status:</b> In Progress
