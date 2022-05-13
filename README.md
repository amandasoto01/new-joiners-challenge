### New Joiners Challenge

#### Service 1 - Processor File:
- This service should get a new joiner Endava profile file in pdf or docx format, extract basic information and publish this information into a message broker.

#### Service 2 - Joiner Service:
-  This service should get a message from the queue created with the first service and insert it into a database.

- Endpoints for the service:

	•	POST /joiner (return 200 or error as needed) . Create joiner from data provided in the body of the request
  
	•	PUT /joiner/{joiner _id} (Return updated details of the given joiner). Update provided fields in the body for the given joiner
  
	•	GET /joiner/{joiner_id} (Return all joiner information in json)
  
  •	DELETE /joiner/{joiner_id} (return a message with the confirmation of deletion)
  
 Repository Link: https://github.com/amandasoto01/joiners-service

#### Service 3 - Task Service:
- This service should get requests and manage a simple CRUD for the tasks that could be assigned to a new joiner, a task could have 1 or more subtask (1 level only) and the status of those inherence subtask will be used to calculate the status of the principal task

- Endpoints:
	•	GET /task (Return a list of all tasks ids)
		Response example: 123456789,987654321,123,642375]
    
	•	GET / task /{ task _id} (Return the details of the given task)
		Response example:  { 
		"task _id": 34382,	
		"field_2": "string-type-field", 
		"field_3: [“XXX”,”YYY”,”ZZZZ”],
		}

	•	 POST /task (return 200 or error as needed)
       create task from data provided in the body

	•	PUT / task /{ task _id} (Return updated details of the given task)
Update provided fields in the body for the given task

	•	DELETE / task /{ task _id} (return 200 or error as needed)
delete provided task

  •	Get / task / tasks (return 200 or error as needed)
Return a list of all tasks by joiner 

#### Service 4 - Task Report:
- This service should create a report using csv format..

- Generate the following report in csv file:

  •	Top ‘N” joiners by “X” stack (order by amount of task completed).

  •	Tasks completed and pending by joiner.

  •	Task completed an uncompleted by “X” joiner.

  •	Days left to complete the tasks by joiner (only for joiners with pending tasks, assume 8 hours 1 day).

### Architecture:
![alt text](https://github.com/amandasoto01/new-joiners-challenge/blob/master/New%20Joiners%20Challenge%20Diagram.png)

### Planning:

Task  | Deadline 
------------- | -------------
Define Architecture | May 13
Joiner Service | May 18
Consumer Processor File  | May 25
Task Service  | June 1
Processor File Service  | June 8
Task Reports | June 15
Api Gateway  | June 22
AWS Services  | June 29
Prepare presentation | July 4

Planner: https://tasks.office.com/endava.onmicrosoft.com/en-US/Home/Planner/#/plantaskboard?groupId=72941b40-bbc0-486b-9b98-2bfdd66e8fa1&planId=mFP0Dk7Sq0KK4ZXTPD5dNZYAAwky

