# CS 197 FZZQ Assessment

Submitted by Stephen Sabas Singer on September 4, 2026

## Entities and Attributes

- Faculty Member
	- <u>Employee ID</u>
	- Name
		- First Name
		- Middle Name
		- Last Name
	- Office Address
		- Room Number
		- Building
		- Campus
	- {Specialization}
- Research Project
	- <u>Project Code</u>
	- Title
	- Start Date
	- End Date
	- Budget
- Funding Agency
	- <u>Agency Code</u>
	- Name
	- Contact Information
		- Email Address
		- {Contact Numbers}
- Graduate Student
	- <u>Student ID</u>
	- Name
		- First Name
		- Last Name
	- Email Address
	- Degree Program

## Relationships

- Leads (1:N)
	- Faculty Members: Partial One-to-Many (0..N)
	- Research Project: Total One-to-One (1..1)
- Funded By (M:N)
	- Funding Agency: Total One-to-Many (1..N)
	- Research Projects: Total One-to-Many (1..N)
	- Attribute: Amount Funded
- Participates In (M:N)
	- Graduate Student: Partial One-to-Many (0..N)
	- Research Project: Partial One-to-Many (0..N)
	- Attributes: Participation Type, Duration, Role Description

## Entity Relationship Diagram


![[ER Diagram.png]]


## Relational Logical Schema

- faculty_member(<u>employee_id</u>, first_name, middle_name, last_name, room_number, building, campus)
- faculty_specialization(<u><b>employee_id</b></u>, <u>specialization</u>)
- research_project(<u>project_code</u>, title, start_date, end_date, budget, **employee_id**)
- funding_agency(<u>agency_code</u>, name, email_address)
- agency_contact_number(<u><b>agency_code</b></u>, <u>contact_number</u>)
- project_funding(<u><b>project_code</b></u>, <u><b>agency_code</b></u>, amount_funded)
- graduate_student(<u>student_id</u>, first_name, last_name, email_address, degree_program)
- student_participation(<u><b>student_id</b></u>, <u><b>project_code</b></u>, participation_type, duration_in_months, role_description)