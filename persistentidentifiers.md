# Persistent Identifiers 

The Persistent Identifiers module allows users to create or import persistent identifiers (PIDs) & assign them to Omeka S items. These PIDs can be either assigned at item creation or assigned or removed later via the item edit or batch edit screens. PIDs may also be "extracted" from existing metadata fields. Once assigned, accessing an item's PID in browser should resolve to a stable, non-site-specific landing page containing the items metadata, media & any sites the item is assigned to.

As there are more than a few existing services for PID "minting" (generation) and management, the module is designed to be flexible enough to allow for multiple PID services to be used (though only one PID service may be used at a time to mint and assign PIDs to items). Most PID services will mint and manage only a certain type of PID. The current PID services for testing and initial release are:

+ EZID (used to mint and manage ARKs)
+ DataCite (used to mint and manage DOIs)

## General Settings

After installation, _Persistent Identifiers_ should appear in the left nav bar under Modules. The _Settings_ subpage features general settings:

+ **PID Service:** Select which of the available PID services to use for minting/extraction.
+ **Assign PID to New Items:** Check this box to automatically either newly mint or extract an existing PID (see "Fields with Existing PIDs" below) and assign to every new item in Omeka S, whether created from within the Omeka S interface or imported from another Omeka/Dspace/etc. instance using another module.
+ **Fields with Existing PIDs:** A list of metadata fields, separated by commas, that may contain PID values within a newly created or imported item. If found, the existing PID will be assigned to the item instead of a new PID being minted.

## EZID Configuration

When completing the configuration process for EZID, you will need to provide the:
+ **NAAN & Shoulder Namespace:** the Name Assigning Authority Number (NAAN) and ARK shoulder value uniquely assigned to an organization, which will appear in every ARK generated. 
+ **EZID Username:** the EZID user with permission to create and update identifiers for the above namespace. 
+ **EZID Password:** password for the above EZID user. Note that this password does not "save", so if changes are made to the NAAN or Username, you must also re-enter the password before pressing "submit".

## DataCite Configuration

When completing the configuration process for DataCite, you will need to provide the:
+ **Repository DOI Prefix:** the prefix assigned to an institution's DOI minting and management repository, which will appear in every DOI generated. 
+ **DataCite Repository ID:** the unique identifier assigned to an institution's DOI repository. 
+ **DataCite Password:** password associated with the above DataCite Repository ID. Note that this password does not "save", so if changes are made to any field on the DataCite Configuration screen, you must also re-enter the password before pressing "submit".

### DataCite Required Metadata
DataCite requires five descriptive metadata values in order to generate a DOI: Title, Creators, Publisher, Publication Year, and Resource Type. All of these fields must be mapped to an existing metadata field, selected from the list of available metadata vocabularies in your Omeka S instance.

## Minting and Removing PIDs

To mind a PID from the item edit page, click on an item and select "Edit Item." Navigate to the Advanced tab, and click "Mint PID." 

After a few moments, the ARK or DOI should appear. The "Mint PID" button should now show "Remove PID." You can now remove the PID using this button. If you select "Remove PID," a dialogue will pop up warning you that this will remove the PID and break any incoming links. Click "Confirm Remove PID" to delete the PID.

Click "Save" before navigating away from the page when both minting and removing PIDs.

## Assigning PIDs to All New Items

Check Assign PIDs to new items on the PID module Settings page. Create a new item within Omeka S interface and ensure that a PID value appears in the item's right nav metadata, as well as when you click "Edit Item"->Advanced Tab. Next, uncheck Assign PIDS to new items and create a new item, ensuring that no PID appears.

## Extracting PIDs from Existing Fields

On the PID module Settings page, enter several fields that may contain PID values, such as dcterms.identifier,dcterms.relation, etc. go to an item edit page and put a "dummy" PID value such as ark:/99999/fk4kw6wp07 or 10.82157/7mzm-ee29 in to each of the entered fields, then test minting a PID from the Advanced tab for each metadata field, to make sure that the dummy value you entered in the metadata field gets saved as the items PID value.

## Batch editing PIDs

From the admin interface Items page, select the checkbox beside several items without PIDs, choose "Edit Selected" and press "Go". Near the bottom of the Batch edit items screen, you should see a Persistent Identifiers row. Test the Mint PIDs, Remove PIDs and [no action] buttons in turn, ensuring that PIDs are minted or removed for the selected items. Also ensure that one or two of the items have PID values in an "Existing Field" value from above, and that these PIDs are properly extracted while other PIDs are newly minted.

## Importing PIDs from Other Sources

Import a small collection from another Omeka S Instance or DSpace/Fedora repository, CSV import etc. using another module. When Assign PIDs to all new items is checked, ensure that all imported items have a PID assigned. Also see if you can put PID values in the relevant Existing Field within the source repository, BEFORE import, and ensure that those PIDs are assigned to the newly imported items after import.
