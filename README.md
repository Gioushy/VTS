# VTS Project

## Vision
The vision for the VTS is to provide individual employees with the capability to manage their own vacation time, sick leave, and personal time off, without having to be an expert in company policy or the local facility’s leave policies.
The most important goal of this system is to give individual employees the capability and responsibility to manage this particular aspect of their employment agreements with the company. The underlying motivations for this desire include the need to streamline the functions of the human resources (HR) department, to minimize noncore, business-related activities of management, and to give a sense of empowerment to the employees. The main goal of this application is to improve the internal business processes of this organization.

## Functional Requirements
•	Implements a flexible rules-based system for validating and verifying leave time requests. <br/>
•	Enables manager approval (optional). <br/>
•	Uses e-mail notification to request manager approval and notify employees of request status changes. <br/>
•	Is implemented as an extension to the existing intranet portal system, and uses the portal’s single-sign-on mechanisms for all authentication. <br/>
•	Keeps activity logs for all transactions. <br/>
•	Enables the HR and system administration personnel to override all actions restricted by rules, with logging of those overrides. <br/>
•	Allows managers to directly award personal leave time (with system-set limits). <br/>
•	Provides a Web service interface for other internal systems to query any given employee’s vacation request summary. <br/>
•	Interfaces with the HR department legacy systems to retrieve required employee information and changes. <br/>

## Non-Functional Requirements
•	Uses existing hardware and middleware. <br/>
•	 The system must be easy to use. [usability] <br/>

## Domain Knowledge
•	All employees work eight-hour days. <br/>
•	Each employee’s vacation time requests are subject to the restrictions of each employee’s primary work location in addition to overall company policies and restrictions. <br/>
•	Vacation time request validation rules are defined and owned by the HR department. <br/>

## Constraints
•	Integrations <br/>
•	Legacy Hardware <br/>
•	Single-sign-on <br/>
•	User experience <br/>

## Definition Problem
For many businesses today, the independence of workers has been ever increasing. It is not uncommon for workers to divide their time across multiple projects and to report to multiple project managers. As a result, managers have fewer informal interactions with their workers and find it increasingly difficult to be aware of and manage their workers’ vacation time.<br/>
In the past, all vacation time had to be approved by an immediate manager and then checked by a clerk in the HR department before it was authorized. Sometimes this manual process could take days.

## Actors
•	Employee: The main user of this system. An employee uses this system to manage his or her vacation time [Use cases: Manage Time]. <br/>
•	Manager: An employee who has all the abilities and goals of a regular employee, but with the added responsibility of approving vacation requests for immediate subordinates. A manager may award subordinates comp time, subject to certain limits set in the system [Use cases: Approve Request, Award Time]. <br/>
•	Clerk: A member of the HR department who has sufficient rights to view employees’ personal data and is responsible for ensuring that employees’ information in all HR systems is up to date and correct. An HR clerk can add or remove nearly any record in the system. In the real world, HR clerks may or may not be employees; however, if they are employees, they use two separate login IDs to manage these two different roles [Use cases: Edit Employee Record, Manage Locations, Manage Leave Categories, Override Leave Records]. <br/>
•	System Admin: A role responsible for the smooth running of the system’s technical resources (e.g., Web server, database) and for collecting and archiving all log files [Use cases: Backup System Logs]. <br/>
![image](https://github.com/Gioushy/VTS/assets/105521854/3445e3a7-d970-446c-8420-e5b5448716d7)

## Use Cases:
•	Manage time [Create Request] <br/>
•	Withdraw Request <br/>
•	Cancel Request <br/>
•	Edit Pending Request <br/>




