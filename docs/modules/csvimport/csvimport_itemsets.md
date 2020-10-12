Import Item Sets

## Initial Import Settings

Start an import by clicking on the CSV Importer tab on the left-hand navigation. This will open the initial Import Settings page. 

![A red arrow points to CSV Importer in the navigation](../../../modules/modulesfiles/csvimport_nav.png)

- For the Spreadsheet option, use the *Choose File* button to select the file from your computer. 
- From the *CSV Column delimiter* dropdown, choose from the following options (this should match the formatting of your file)
	- comma (default)
	- semi-colon
	- colon
	- tabulation
	- carriage return
	- space
	- pipe

- From the *CSV column enclosure* dropdown, choose the option which encloses long text in your file:
	- double quote (default)
	- quote
	- hash

- From the *Import Type* dropdown, select Item Sets. 

- Check the box to *Automap with simple labels.* This will automap not only specially formatted column headings but also column headings which match existing vocabulary property labels. Note that this option defaults to Dublin Core before proceeding through other installed vocabularies. 

- Comments are useful as they appear on the "Past Imports" page; make a note about what is being imported and any settings you may have on this page. 

![Import settings as described, no entries](../../../modules/modulesfiles/csvimport_settings.png)

Click the *next* button to continue with the import process.

## Map Data and Settings
When you click next, the page will load with the following tabs:

### Map to Omeka S data
This tab displays a table with the columns from your spreadsheet as rows. Each row displays:

- a Checkbox
- Column header from the spreadsheet
- A plus symbol button for adding or modifying a mapping
- A wrench symbol button for spreadsheet column options
- A trash can to delete mappings
- A column to show options selected

![Mappings for a spreadsheet with four columns, all of which have been automapped](../../../modules/modulesfiles/csvimport_ItemSet1.png)

#### Mapping options

To map a column header to a vocabulary property, click on the plus symbol button to the left of the column header. This will open a drawer on the right-hand side of the screen. 

![A red arrow points to the plus sign button to the left of the word "title"](../../../modules/modulesfiles/csvimport_itemsMapButton.png)

The drawer has multiple options for mapping:

**Properties** select a property to map the column data to, from any of the installed vocabularies. Use the Filter field to search the available properties for a specific property.

![Properties option open showing all of the installed vocabularies for the Omeka S installation: Dublin Core, Bibliographic Ontology, Friend of a Friend, Scripto and OWL-Time Ontology.](/../../modules/modulesfiles/csvimport_itemsMapProp.png)

**Item set-specific data** is a checkbox for "Open to additions." Check to allow other users to edit or add to the item set. Leave unchecked to have the item set be editable only by its creator, site admins, and global admins.

![Add mapping drawer showing the section "Item set-specific data". Below the section header is a single, unselected checkbox option labeled "Open to additions".](/../../modules/modulesfiles/csvimport_itemSetSD.png)

**Generic data** also has a dropdown where you can set one of four options:

- *Resource template (by label):* set the template for an item  set by name. The name of the template as entered in the spreadsheet and the name of the template in Omeka S must match exactly.
- *Resource class (by term):* set the resource class for an item set. The term for the class in the spreadsheet and in the Omeka S installation must match exactly.
- *Owner (by email address):* set an item set's owner by email address. This must be the email address associated with the user's account in the Omeka S installation.
- *Visibility public/private:* set the visibility of the item set. Use "private" or "public" in the spreadsheet. 

![Dropdown as described](../../../modules/modulesfiles/csvimport_itemsMapgeneric.png)

Be sure to click the "Apply Changes" at the bottom of the drawer or nothing you set here will be kept.

To remove a mapping, click the trash can icon in the row for that data mapping. It will remove *only* the mapping, not the column data. 

If you have data in a column in your CSV which you do not want to bring in to your Omeka S installation, simply do not map that column to a property or data type.

#### Column options
To access options for data in a column of your csv (represented by a row in the import table), click the wrench icon for that column heading. 

![A red arrow points to the wrench button to the left of the word "title"](../../../modules/modulesfiles/csvimport_itemsMapOptions.png)

Column options are in addition to mappings. If you add options without also mapping column data to resource, media, or other data, nothing will be imported. 

This will open a drawer on the right side of the browser window with the following options: 

- **Use multivalve separator:** check this box to use the multivalue separator for data in this column. You set the multivalue separator in the initial import page, but you can change it in the Basic Settings tab.  
- **Language:** is a field where you can set the language for this column using the [IETF Language tag](https://en.wikipedia.org/wiki/IETF_language_tag) for the language in which the text is written. This will override what you have entered in basic settings. 
- **Data type:** is a dropdown with at least three options, which correspond to the [values](../content/items/#values) one can use when adding properties to an item:
	- Import as text (default).
	- Import as URL reference. You can set the label for the URI by including the desired text after a space, for example:  `http://example.com This Is The Label`
	- Import as Omeka S resource ID. Note that you must have the correct ID for the resource. A resources' ID is the number sequence at the end of the url when on the view or edit page, so for `/admin/item/11576` the ID is 11576.
	- If you have certain modules installed, such as Numeric Data Types, there may be additional data type options supplied by those modules.
- **Import values as private**: check this box to set all property values *in this column* private.

![drawer with options as described above](../../../modules/modulesfiles/csvimport_ItemSetCol.png)

To remove a column option setting, click the wrench icon again and undo your changes manually.

#### Batch edit
When you select one or more rows in the table (columns from your csv file), you can use the "Batch edit options" button to apply the column options described above to multiple csv columns at once. 

![a screenshot of the Mapping tab, with the boxes for Columns Title and Creator checked. A red arrow points to the Batch edit options button. On the right side of the screen, a drawer offers options for changing the settings as described](../../../modules/modulesfiles/csvimport_batchEditItemSet.png)

Be sure to click the Apply Changes button at the bottom of the drawer in order to save your changes. 

### Item Set import Basic Settings
These settings apply to the entire csv which you are importing. Note that some of these settings can be overwritten by column options in the Map to Omeka S data tab. 

![options as described below](../../../modules/modulesfiles/csvimport_ItemSetBasic.png)

- **Resource Template:** select a resource template from the drop-down menu to apply to the imported item sets. You can use the search field at the top of the dropdown to narrow results or find a particular template.
- **Class:** select a class from the drop-down menu to apply to the imported item sets. You can use the search field at the top of the dropdown to narrow results or find a particular class.
- **Owner:** set the owner for the item sets by selecting a user from the drop-down menu. You can use the search field at the top of the dropdown to narrow results or find a particular user.
- **Visibility:** set the visibility of the imported item sets as public  or private. 
- **Open/Closed to additions:** set whether users other than the owner (and site & global admins) will be able to add or edit the item sets.
- **Multivalue Separator:** enter the multivalue separator character here, if you have used one. 
      - The columns of data in your CSV should be separated by commas, however within those columns you can add a special character to create multiple inputs, for example a semicolon.
- **Language:** set the language of the values in the spreadsheet using the appropriate [IETF Language tag](https://en.wikipedia.org/wiki/IETF_language_tag).

### Item Set import Advanced Settings

There are two options on this tab which are only for advanced use. 

![Advanced settings page showing only the Action dropdown and the field for number of rows to process. ](../../../modules/modulesfiles/csvimport_ItemSetAdv.png)

#### Action

This setting allows you to change the action of process from a straight import to one of the following options:

- **Create a new resource:** default option. Each row in the CSV will become a new resource.
- **Append data to the resource:** add new data to the resource.
- **Revise data of the resource:** replace existing data in the resource with data from the csv, except if empty.
- **Update data of the resource:** replace existing data in the resource with data from the csv, even when the cell is empty.
- **Replace all data of the resource:** remove all properties of the resource, and fill with new information from the sheet.
- **Delete the resource:** delete all matching resources

If you select one of these options from the dropdown, three additional settings will appear on the tab. These settings help the process determine which resources to take action on.

![Advanced options tab with options as described below](../../../modules/modulesfiles/csvimport_itemSetAdvAct.png)

- **Resource identifier column:** Select from a dropdown of the columns in your CSV. This is the data from your spreadsheet which maps to existing data in your Omeka S installation. 
- **Resource identifier property:** select from a dropdown of all properties in your Omeka S installation. This should be the property in which you already have data, that you used to create the column data above. 
	- Example: if the data in the Resource identifier column is "Title" with the first row of data having a title "A Study in Scarlet," and you set Resource identifier property to "Dublin Core: Title," then the actions will operate on a resource already in your Omeka S installation whose dc:title property is "A Study in Scarlet".
	- This will only work with exact matches.
	- If you have more than one resource with matching data, it will only take action on the oldest resource.
- **Action on unidentified resources:** This option determines what to do when no matching resource exists in the Omeka S installation, but the selected action only applies to an existing resource ("Append", "Revise", "Update", or "Replace"). This option is not used when the main action is "Create" or "Delete" Your options are two radio buttons:
	- Skip the row 
	- Create a new resource

#### Other advanced settings
In addition to the above, the Advanced Settings tab has an option to set the number of rows to process by batch. By default this is set to 20. However, if you are running into errors with an import you may want to set it to 5 or even 1 in order to troubleshoot and determine the source of the error. 

### Complete import
Once you have completed mappings, column options, and any settings, click the Import button in the upper right corner of the browser window. This should start the import and redirect you to the Past Imports tab. You should see a confirmation message saying "Importing in Job ID [number]"
