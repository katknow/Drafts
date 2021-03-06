# Data Repository Connector

The Data Repository Connector module allows users to import records and/or data files from several different data repository platforms: Dataverse, Zenodo and CKAN.

To install Data Repository Connector, follow the instructions for [Installing Modules](https://omeka.org/s/docs/user-manual/modules/#installing-modules) on the Modules documentation.

You can view past imports by going to the Data Repository Connector tab on the left-hand navigation of the admin dashboard and clicking the Past Imports sub-tab.

## Import Data

To use the Data Repository Connector, navigate to the tab labelled Data Repository Connector on the left-hand navigation of the admin dashboard. Then, you will have the option to select Dataverse, Zenodo, or CKAN.

<img width="266" alt="datarepoconnect_tabs" src="https://user-images.githubusercontent.com/84726696/174340090-3fad9bdd-1f3c-43f3-8934-3903e52981a4.png">

### Shared Options

Regardless of the service you have selected, you will be provided with the following options:
+ **Limit**: The maximum number of results to retrieve at once. If you notice errors or missing data, try lowering this number. Increasing it might make imports faster. (This field is required)
+ **Import Files into Omeka S**: If checked, all data files associated with a record will be imported into Omeka S.
+ **Comment**: A note about the purpose or source of this import.
+ **Item Sets**: The items sets to import items into.
+ **Sites**: The sites to import items into.

<img width="1169" alt="datarepoconnect_dataverse" src="https://user-images.githubusercontent.com/84726696/174340123-b8cc62e7-dffd-49a4-b59f-258c48097fe5.png">

Once you have filled out these fields as well as those specific to the option you have selected, be sure to click "Submit".

### Dataverse Options

If you select Dataverse, you should see a screen with the following options:
+ **Main Dataverse URL**: The URL of the main Dataverse site. (This field is required)
+ **Dataverse Identifier**: The identifier of the Dataverse to import from. If blank, all datasets under **Main Dataverse URL** will be imported.
+ **Metadata Format**: The metadata format to export from Dataverse. The options for Dataverse are dcterms, oai_dc, and schema.org. The format must exist as a vocabulary in your Omeka instance before import. (This field is required)

### Zenodo Options

If you select Zenodo, you should see a screen with the following options:
+ **Zenodo Community ID**: The short string identifying which Zenodo community to import from. Found in the URL after https://zenodo.org/communities/ and before any search parameters. (This field is required)
+ **Metadata Format**: The metadata format to export from Zenodo. The option for Zenodo is oai_dc. The format must exist as a vocabulary in your Omeka instance before import.

### CKAN

If you select CKAN, you should see a screen with the following options:
+ **Main CKAN URL**: The URL of the main Dataverse site. (This field is required)
+ **CKAN Organization**: The identifier of the CKAN organization to import from. If blank, all datasets under **Main CKAN URL** will be imported.

### Checking Import Status

After you have hit submit, you can track the status of the import by navigating to the Data Repository Connector > Past Imports tab or the Jobs tab of the left-hand navigation on the admin dashboard.

+ Are your jobs starting and not completing? You might need to set the path for PHP so that your system can perform the background process to make the items.

## Review Imports

Go to the Data Repository Connector tab on the left-hand navigation of the admin dashboard, click on Data Repository Connector and then click on Past Imports, which should appear below the Data Repository Connector tab.

This page displays a table of Past Imports, with a checkbox option to Undo, the Job ID for the import, any Comments made during import, the number of Items imported, the Date of the import, the import Status, and the Owner, or user who initiated the import.

<img width="1160" alt="datarepoconnect_pastimports" src="https://user-images.githubusercontent.com/84726696/174340236-dd5493a7-45f1-4b77-b690-662bf7702e9d.png">

## Update Imported Resources

To update resources created using the Data Repository Connector, simply re-run an import from the same source. The resources will be updated, not reimported. This allows you to use the Connector to sync data between your Data Repository and Omeka S installations.

## Undo an Import

To undo a completed import and remove all associated items, go to the Data Repository Connector tab on the left-hand navigation of the admin dashboard, click on Data Repository Connector and then click on Past Imports, which should appear below the Data Repository Connector tab.

Check the box for each import you wish to undo and click submit.
