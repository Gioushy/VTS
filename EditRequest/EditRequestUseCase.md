# Edit Pending Request Use Case
## Actor:
•	Employee
## Goal: 
The employee wants to edit the description or title of a pending request.
## Preconditions: 
An employee has made a vacation time request, and that request has yet to be approved or denied by an authorized manager. See also main flow preconditions.
## Entity Diagram:
![image](https://github.com/Gioushy/VTS/assets/105521854/177e12c1-a607-4764-941d-c80bb56b67d4)

## Flow Chart:
![image](https://github.com/Gioushy/VTS/assets/105521854/09a4e999-13cd-42dc-8722-2ef01245a609)

## State Machine Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/a5a32144-8870-4cac-b468-26f332e5f767)

## Sequence Diagram
![image](https://github.com/Gioushy/VTS/assets/105521854/23518b94-f727-4e2a-a224-1c6b0d133258)

## Pseudocode:
```
public void updateRequestInformation(Request request) {
	// use the same function  of updating status but instead change the request information not status
}
```
```
Public void editRequestInformation(Request request) {
	If(withdraw) {
		withdrawRequest(request);
	}
	else {
		//change title, description
		updateRequestInformation(Request request);
	}
}
```
