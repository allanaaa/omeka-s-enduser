---
title: Data Cleaning
---

An Omeka S module for low-level auditing and cleaning of resource metadata. It is designed to be used to prepare resource metadata for use in visualizations.

Changes made in Data Cleaning cannot be easily undone. Due to the powerful nature of the module, it can only be used by Global Administrator users. 

Before running any audit, make sure you have a recent backup of your data. 


## Sample Workflow
This is a sample workflow for a user who wants to audit the titles of items in a specific item set:

- In the left-hand navigation, go to the Data Cleaning module
- Click on "Prepare new audit" button (top right)
- Select criteria (expand arrows for info):
	- Resource type: "Item"
	- Resource query: item_set_id[]=1234
	- Audit column: "value"
	- Property: "Dublin Core: Title"
	- Data type: "Text"
- Ignore the "Advanced" section
- Click "Submit" (top right)
- Audit the "From: value" column for potential corrections or removals
- Make corrections by entering the correct text into the "To: value" column
- Make removals by checking the "Remove" checkbox
- Click "Submit" (top right)
- Click to confirm the submission
- Refresh the "Past audits" page until the job is marked as "Completed"
- Check the items to see if the values were corrected and removed.