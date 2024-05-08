# WithDraw Request Use Case
## Actor:
•	Employee
## Goal: 
The employee wants to withdraw an outstanding request for vacation time.
## Preconditions: 
An employee has made a vacation time request, and that request has yet to be approved or denied by an authorized manager. See also main flow preconditions.
## Entity Diagram:
![image](https://github.com/Gioushy/VTS/assets/105521854/4d797e58-f82a-4e89-9f74-acab949401ca) 

## Flow Chart:
![image](https://github.com/Gioushy/VTS/assets/105521854/c4343e4e-7334-4970-a8ff-bad0ae83fcfd)

## State Machine Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/e21b6f4e-e648-41e3-9c99-0ca3aef9ed28)

## Sequence Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/21406104-56ad-405b-8024-a6534c8e224c)

## Pseudocode:

```
public void withdrawRequest(Request request) {
	updateRequestStatus(request);
	@asnyc 
	//send email to manager
	// send email to HR.
}
```
```
public void updateRequestStatus(Request request) {
	// will be used by manager and hr clerk in the case of approval and rejection of the request.
	//Connect to DB.
	//Update the status of the given request
}
```
