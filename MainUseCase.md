# Manage Time Use Case
## Actor:
•	Employee
## Goal: 
The employee wishes to submit a new request for vacation time.
## Preconditions: 
The employee is authenticated by the portal framework and identified as an employee of the company with privileges to manage his or her own vacation time.

## Entity Diagram:
![image](https://github.com/Gioushy/VTS/assets/105521854/a32753c2-72e4-49c8-8e4b-76232de84c25)
 
## Flow Chart:
![image](https://github.com/Gioushy/VTS/assets/105521854/453b3159-feb4-4016-9ad8-d1ae62820c05)

## State Machine Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/a564228f-de6d-4314-94b0-801a2e8a82d6)

## Sequence Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/8995718c-e847-47d2-b9f5-2ef21b9fa563)
![image](https://github.com/Gioushy/VTS/assets/105521854/f17c37b8-04fc-4b10-95dd-eaf24c423fb7)
![image](https://github.com/Gioushy/VTS/assets/105521854/b09ad7b3-2580-4abf-a049-992f1860553d)

## Pseudocode:
```
public void requestInfo(Employee employee) {
	// Call external API with employee id to get his information.
}
```
```
public Request createRequest(Employee employee, Date fromDate, Date toDate,…..) {
	// create new request with the given parameters.
	return the new request
}
```
```
public boolean validUIRequest(Request request) {
	//Check the request information 
	// Check if there is description
	// Check dates
}
```
```
public boolean validRequest(Request request) {
	boolean valid  = validUIRequest(request);
	if (valid) {
		// request employee info.
		// check the request against business validation according to employee info.
	} else {
		Throw error;
		Return false;
	}
}
```
```
public void saveRequest(Request request) {
	boolean valid  = validRequest(request);
	if (valid) {
		// save request in db;
		//@async 
notify manager with email.
	}
	else { 
		// throw error.
	}
}
```
```
public void updateRequestStatus(Request request) {
	// will be used by manager and hr clerk in the case of approval and rejection of the request.
	//Connect to DB.
	//Update the status of the given request
}
```
```
public void updateEmployeeBalance(Employee employee) {
	//Connect to DB
	//Update user balance in case of confirmation or cancellation.
}
```
