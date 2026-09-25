### What would hurt users

### Bug1: task keeps changing whenever you change project and comes back
### Severity: High
### steps
open taskflow application
select a project 
switch to another project 
comapre the task displayed with what was reflecting earlier
### Expected 
only task relatedd to the project should show
### Actual
Task is different evreytime we go back to the old project. it gets mixed up and could confuse the user.
### who is hurt
End user, admin


### Bug2: Unable to complete or undo a ticket. the button is not functioning 
### Severity: High
### steps
open taskflow application
select a project 
Click the button to complete  the task
### Expected 
Task should be completed
### Actual
complete button not reacting but on the network tab we can see the staus code is succesful
### who is hurt
End user, admin
 
### Bug3: Unable to change task status 
### Severity: Normal
### steps
open taskflow application
select a project 
Change the status of task fro todo to process for example
### Expected 
Task status should be able to get switched
### Actual
button not reacting 
### who is hurt
End user, admin

### Bug4- Task Status name not matching with the network tab api response 
### Severity: Normal
### steps
open taskflow application
select a project with a Done status
Reopen it
check the network tab response
### Expected 
it should match done status call 
### Actual
rather TODO status is shown
### who is hurt
End user, admin

### Evidence
In the screenshot folder

### Bug 5-Invalid Url exposed backend stack trace unstead of a user friendly message 

severity Major
### steps
open link "https://cautious-garbanzo-v6jxpprjjxp6f6gr7-8080.app.github.dev/"

Observe the response
### Expected 
Application should return a clean 404 page error with a friendly message  

### Actual
a full error is shown with details of stack trace

### who is hurt
End user who is confuse, 
admin with security issue

Risk Based test plan

### what i will cover as critical flow
verify that each task belongs to the appropriate project 
create complete and update task status
Reassignment work properly
verify Api response matches the actual state shown

### Highest risk as we ship
data integrity  
api inconsistency
Error handling stack trace

### vwhat to could be skipped overnight 
perfect pixel UI
full testing on rarely used features

### Release recommendation
before release i will verify that critical task or project or high business impact areas are bug free or flow properly and confirm the application state, api reponse and user variable results