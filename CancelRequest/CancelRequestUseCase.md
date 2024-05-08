# Cancel Request Use Case
## Actor:
•	Employee
## Goal: 
The employee wants to cancel an approved vacation time request.
## Preconditions: 
The employee has a vacation time request that has been approved and is scheduled for some time in the future or the recent past (previous 5 business days). See also main flow preconditions.
## Entity Diagram:
![image](https://github.com/Gioushy/VTS/assets/105521854/aad7aaa6-b986-47a4-b731-b6908b966cda)

## Flow Chart:
![image](https://github.com/Gioushy/VTS/assets/105521854/f1d5cc8b-49cd-42a0-9926-185ebbff56a5)

## State Machine Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/8423844b-0b1c-47b4-ab23-0defdd3497a5)

## Sequence Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/e8ddfea6-74df-4aa1-af1e-6bdd1fb95d72)

## Pseudocode:
```
public void updateRequestStatus(Request request) {
	// will be used by manager and hr clerk in the case of approval and rejection of the request.
	//Connect to DB.
	//Update the status of the given request
}
```
```
public void updateEmployeeBalance(int id) {
	//Connect to DB
	//Update user balance in case of confirmation or cancellation.
}
```
```
public void cancelRequest(Request request) {
	if(request.cancel_comment) {
		updateRequestStatus(request);
		updateEmployeeBalance(request.employee_id);
		@async
		Send email to manager
		Send email to HR.
	}
}
```
