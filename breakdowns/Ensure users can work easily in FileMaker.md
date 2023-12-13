#infinityIntegration 
## Ensure users can work easily in FileMaker
### Ability to push next action records to Infinity
- [ ] as a user i can associate an opportunity to an event record. 
	- [ ] should only show active opportunities.
- [x] As a user, i can update my custom value lists from Infinity within FileMaker
	- [ ] move all of these to a single table
	- [ ] add an attribute id field
	- [ ] use a global field to filter the related value list.
	- [ ] save the current value of the attribute ids using CFs.
	- [x] test this with the 'location' values.
- [x] As a user I can create a folder in FileMaker to hold tasks for a specific user in Infinity
	- [ ] I can push this folder record to infinity
	- [ ] i can specify which FileMaker user owns which folder.
	- [ ] If i attempt to push items to the api and my user does not have a folder, return an error.
- [ ] As a user i can 'push' next action records to infinity using a button on the related next action record.
	- [ ] button should run custom script that will determine the users folder and set it in the record before attempting to push it. 
- [ ] As a user when i 'push' an Next Action record of type 'appointment', a task will be created inside of Infinity
	- [ ] if there is an opportunity associated to the next action, the next action should be created as a sub task of the opportunity.
	- [ ] the task is created inside of MY user folder on Infinity
	- [ ] i can select the location for the event
	- [ ] i can indicate whether a meeting is virtual
- [ ] As a user when i 'push' a next action record 


### Breakdown
- [x] create drop down list of active opportunities

#### Thoughts
- the issue is that Opportunities and NextActions, need to be created as Items, and sometimes comments in Infinity.
	- Opportunity > Item
	- NextAction > Item
	- NextAction > Comment
