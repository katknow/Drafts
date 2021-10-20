# Extract Metadata

Once installed and active, the Extract Metadata module allows site administrators to extract embedded metadata from file. 

## Configuring the module

When configuring the module, you can:
+ View and enable/disable extractors;
+ View and enable/disable mappers;
+ Configure the metadata crosswalk for the JSON Pointer mapper (if enabled).
    
You can choose from four different extractors, including ExifTool, Tika, Exif, and getID3. 

For mappers you can either select to enable no mappers or JSON Pointer. If you decided to use the JSON pointer mapper, you will need to define the metadata crosswalk. You will be asked to select the Resource, Extractor, and Property from a dropdown menu as well as provide a Pointer formatted using a JSON pointer as defined by the [IETF standard](https://datatracker.ietf.org/doc/html/rfc6901). If you would like to replace the metadata values through this pointer, make sure to select the checkbox to the right of these fields.

When you are finished configuring the module, click the Submit button in the upper right corner of the screen.

![extractmetadata_configsubmit](https://user-images.githubusercontent.com/84726696/138010740-3a7c3697-25bb-4d66-8576-bfff71fdb60d.png)


## Adding media

When adding media, the module will automatically:
+ Extract metadata from the file using enabled extractors;
+ Save the metadata alongside the media;
+ Map metadata to resource values.

Once you've added media to an item, you can add the extracted metadata to the item's metadata under the Values tab. You will be able to add a new field for the extracted metadata from the drawer on the right side of the screen labeled "Click on a property to add it to the edit panel." Click the arrow next to "Extract Metadata" to view the 23 options and select the one that is most appropriate for the media you have added.

![extractmetadata_addproperty](https://user-images.githubusercontent.com/84726696/138015034-f386fd9a-67a7-45a2-acf3-c81f73fbb6f7.png)

After adding the new field, you will be able to select one of the buttons to input Text, select an Omeka resource, or input a URI to add the media's extracted metadata to the item.

![extractmetadata_itemedit](https://user-images.githubusercontent.com/84726696/138017344-9bcfc460-aefe-44c7-9668-5d6706fce2b3.png)

Be sure to save your changes. To delete the field, select the trash can button to the right of the field.

You can view the extracted metadata under the Extract Metadata tab on the item edit page.

![extractmetadata_tab](https://user-images.githubusercontent.com/84726696/138012187-20094e98-9913-4777-95f6-09571f27264c.png)

Alternatively, you can click the link in your newly added field to view the media page with extracted metadata.

![extractmetadata_medialink](https://user-images.githubusercontent.com/84726696/138019680-ffe4e6c2-7f3e-4f7e-8c46-05882611c1c6.png)


## Editing media and items

When editing a media/item or batch editing media/item, the user can choose to perform a number of actions:
+ Refresh metadata: (re)extract metadata from files;
+ Refresh and map metadata: (re)extract metadata from files and map metadata to resource values;
+ Map metadata: Map extracted metadata to resource values;
+ Delete metadata: Delete extracted metadata.

You can access these options on the Extract Metadata tab on the item edit screen.

Then, you can select one of the four options from the dropdown menu.

![extractmetadata_tabdropdown](https://user-images.githubusercontent.com/84726696/138012355-dda4f40e-cae8-406b-a5b3-32b98bf695a0.png)

Be sure to click the "Save" button in the top right corner of the screen.

When viewing and editing a media, the user can see the extracted metadata in the "Extract metadata" section.

## Extractors:

Extractors extract metadata from files. Note that extractors must be enabled on
the module configuration page. This module comes with four extractors, but more
can be added depending on your need.

### ExifTool

Used to extract many types of metadata from many types of files. Requires the
[ExifTool](https://exiftool.org/) command-line application.

### Exif

Used to extract EXIF metadata that is commonly found in JPEG and TIFF files. Requires
PHP's [exif](https://www.php.net/manual/en/book.exif.php) extension.

### getID3

Used to extract many types of metadata from many types of files. Uses the
[getID3](https://github.com/JamesHeinrich/getID3) PHP library, which comes with
this module.

### Tika

Used to extract many types of metadata from many types of files. Requires the
[Apache Tika](https://tika.apache.org/) content analysis toolkit. Java must be installed
and the path to the `tika-app-*.jar` file must be configured in `config/module.config.php`
under `[extract_metadata_extractor_config][tika][jar_path]`.

## Mappers

Mappers map extracted metadata to resource values. Note that a mapper must be enabled
on the module configuration page. This module comes with one mapper, but more can
be added depending on your need.

### JSON Pointer

Used to map metadata to resource values using [JSON pointers](https://datatracker.ietf.org/doc/html/rfc6901).
You must define your own metadata crosswalk in the module configuration page under
"JSON Pointer crosswalk".

One common example is to map a JPEG file's creation date to Dublin Core's "Date
Created" property:

- Resource: [Media or Item]
- Extractor: "Exif"
- Pointer: `/EXIF/DateTimeOriginal`
- Property: "Dublin Core : Date Created"
- Replace values: [checked or unchecked]

Note that the pointer points to the DateTimeOriginal value in the Exif metadata
output, which you can view in a JPEG media's "Extract metadata" section. Once you've
saved this map, perform the "Map metadata" action as described above and, if your
JPEG file includes DateTimeOriginal, the media/item should now have a "Date Created"
value.

