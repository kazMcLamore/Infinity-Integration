## New Architecture
- there is now an additional file (integrator bridge)
- you will auto-login to this file
- this file holds all data for infinity/integrating with infinity
- File should be visible on list of hosted files

## How to create an opportunity
- open Integrator Bridge file
- go to layout "Opportunity - Detail"
- create a new record
- name your opportunity 
	- this will show in Infinity
- click the magnifying glass to search for a party
	- in the popover search window, enter your search criteria
	- this should be doing an "or" search where any record that matches any criteria should be returned
	- searches for names and organization names are fuzzy searches that will return other things that are spelled similarly
	- searches for names and organization names should also include exact matches.
	- select a party by clicking on their line
		- you should see their details show up in the opportunity.
- select a status, salesperson, and folder.
- push the upload button to push to infinity
	- if this is not viewable, click the background after selecting a status, salesperson, and folder.
- you should now see the opportunity show up in Infinity
- NOTE: opportunities are **ALWAYS** created from FileMaker. If you create a task in infinity, it will not be considered an opportunity.

## How to find a person for an opportunity
- enter your search terms
- this should do an or search where any matches are included
- to filter the list of records DOWN enter your search term in the 'filter' field below and then press enter or press the button next to the field. 
- this should return any records that contain the exact text string in any of the fields.
## Update an opportunity from Infinity
- modify a field value on Infinity website
	- only some fields are mirred in FM:
		- opportunity status
		- due date
		- contact fields are updated, but not visible as they're not written back to people table.

## How to create a new folder
- create folder in infinity
- go to board map layout
- find board record
- pull folders

## How to associate a salesperson to an infinity id
- add anyone needed to the attribute in Infinity
	- modify the salesperson label attribute
	- add any salespeople we need
- pull all Salesperson label options in FileMaker
	- go to the layout
	- set the global field on the layout the exact name of the attribute you want to pull values for e.g. "Salesperson"
	- pull all records.
- pull all users in FileMaker
	- go to the layout
	- pull all records
- select a label value for each user that we want to use.
- also enter their FM user name.

## How to create a task for an opportunity through Infinity
- create a task on infinity that is a sub-item to your opportunity record.
- use the salesperson field to select which FM user this should go to.
	- [[#How to associate a salesperson to an infinity id | How to set up a new salesperson]] 
- this record should show up in FM as a next action record and associated to the correct person by their people id.

## Create a task through infinity
- create the task
- assign sales person ([ensure they're set up correctly](#how-to-associate-a-salesperson-to-an-infinity-id))
- record should show in nextactions table with correct fm username


## How to associate an opportunity to a CaterEvent
- 
- from the Event Summary layout
- set today's date in the global field
- this will automatically filter out an opportunity records that have expired.
- on the far right, select the opportunity id ![[CleanShot 2023-12-13 at 14.05.01@2x.png|image]] 
## Why associate an opportunity to a CaterEvent?
- the opportunity record allows comments/activity for this opportunity to show up under the same infinity task. 