# WoRMS_matching

<b>Files that should be in this repository: </b>
-BCODMO_demo_112019.Rmd
-demo_modified_forLaurenM.Rmd
-demo_modified_forLaurenM.nb.html
-early_demo_BCODMO_2019_submission_worrms_taxize.Rmd
-name_from_AphiaID_example.Rmd
-name_from_AphiaID_example.nb.html
-Snail_BCODMO_working_2019113.Rmd
-Snail_plankton_BCODMO_working.Rmd
-Snail_plankton_BCODMO_working.nb.html

##Description of Each File
<b>File Name:</b> BCODMO_demo_112019.Rmd
<br><b>Purpose</b>: Share R functions used in cleaning data for BCO-DMO submission
<br><b>Description:</b> Demonstration of R functions used for cleaning data from hydrothermal vent macrofauna sample (Snail Vent, Mariana Back-arc) for submission to BCO-DMO and OBIS for end-of-semester lab meeting. Focused and formatted for usefulness to other students. Includes generation of a dataframe with common potential complications to cleaning (wrong AphiaID, misspelling, commentary in the name field, etc). Scripts involve retrieval of AphiaID, scientific name, taxonomic rank, kingdom, and phylum from the World Register of Marine Species (WoRMS), as well as creating occurrenceIDs unique within the dataset, and generating LSIDs using the AphiaID.
<br><b>Comments:</b> Uncertain version differences between this and early_demo_BCODMO_2019_submission_worrms_taxize.Rmd
<br><b>Status:<b> Not Updating (last update Nov. 20, 2019)

<br><b>File Name:</b> demo_modified_forLaurenM.Rmd
<br><b>Purpose:</b> Use list of names to get a dataframe (name, LSID, phylum, taxonomic rank) for submission to BCO-DMO
<br><b>Description:</b> Adapted from demonstrations of cleaning data for BCO-DMO (BCODMO_demo_112019.Rmd and early_demo_BCODMO_2019_submission_worrms_taxize.Rmd), specifically written for a specific dataset. Uses provided names to get WoRMS identifiers (AphiaID), which were in turn used to get LSIDs, scientific names, check assigned scientific name and taxonomic rank, check acceptance status of the name, provide the accepted name and associated AphiaID, check if accepted and assigned AphiaIDs match, and retrieve phylum.
<br><b>Comments:</b> Should be manually checked before submitting data, as entries in "scientificName" column may be inappropriately matched with the wrong taxon (eg, matching with the common name of plant instead of a marine species). The output dataset also needs to be manually checked/modified for entries for which no AphiaID/etc were found (eg. "unknown animal"). Some of the commentary outside of R chunks may be out of date.
<br><b>Status:</b> Not Updating (last update Dec. 9, 2019)

<br><b>File Name:</b> demo_modified_forLaurenM.nb.html
<br><b>Purpose:</b> Alternative viewing of R notebook demo_modified_forLaurenM.Rmd
<br><b>Description:</b> HTML output of the aforementioned notebook.
<br><b>Comments:</b> None.
<br><b>Status:</b> Not Updating (last update Dec. 4, 2019)

<br><b>File Name:</b> early_demo_BCODMO_2019_submission_worrms_taxize.Rmd
<br><b>Purpose:</b> Share R functions used in cleaning data for BCO-DMO submission.
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> Uncertain version differences are between this and BCODMO_demo_112019.Rmd
<br><b>Status:</b> Not Updating (last update Dec. 5, 2019; may just be from renaming)

<br><b>File Name:</b> name_from_AphiaID_example.Rmd
<br><b>Purpose:</b> [Forthcoming]
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> [Forthcoming]
<br><b>Status:</b> Not Updating (last update Dec. 5, 2019)

<br><b>File Name:</b> name_from_AphiaID_example.nb.html
<br><b>Purpose:</b> Alternative viewing of R notebook name_from_AphiaID_eample.Rmd
<br><b>Description:</b> HTML output of the aforementioned notebook.
<br><b>Comments:</b> [Forthcoming]
<br><b>Status:</b> Not Updating (last update Dec. 5, 2019)

<br><b>File Name:</b> Snail_BCODMO_working_20191113.Rmd
<br><b>Purpose:</b> Clean Snail Vent macrofauna data for submission to BCODMO, OBIS
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> Last version of this notebook; previous versions on Google Drive with different dates at end
<br><b>Status:</b> Not Updating (last update Nov. 13, 2019)

<br><b>File Name:</b> Snail_plankton_BCODMO_working.Rmd
<br><b>Purpose:</b> Clean plankton data from multiple sites (including Snail Vent) for submission to BCODMO
<br><b>Description:</b> [Forthcoming]
<br><b>Comments:</b> [Forthcoming]
<br><b>Status:</b> In Progress

<br><b>File Name:</b> Snail_plankton_BCODMO_working.nb.html
<br><b>Purpose:</b> Alternative viewing of R notebook Snail_plankton_BCODMO_working.Rmd
<br><b>Description:</b> HTML output of aforementioned notebook
<br><b>Comments:</b> [Forthcoming]
<br><b>Status:</b> In Progress
