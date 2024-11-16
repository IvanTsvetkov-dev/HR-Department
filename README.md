# HR-Department

## Simple database design practice

*Task: Build an ERD in accordance with the requirements. Use Oracle Date Modeler*

_Requirements:_
Subject area: Human Resources Department.

There is a human resources department of a large company. It is necessary to store information about all employees of the company. The following information about the employee is important: first name, last name, position, date of employment and salary. Each position has an interval of acceptable salary values (minimum and maximum). Some employees work not only on a fixed salary, but also have a certain percentage of the commission, for them it is necessary to keep this value.

Each employee has a unique employee number.

The company has several divisions. Each employee is assigned to a certain department (for example, production, sales, accounting, etc.). Each department is located in a separate building with an address in a certain country. At the same time, several departments may be located in some buildings. Each division has a unique number.

Some of the employees are also managers. It is necessary to store information about the manager of each employee, as well as about all employees who are subordinate to each manager.

## My Solution: 
I encountered a problem - redundancy of the country and address attributes in the Department entity, for example, one building may contain several Departments, such as SELL-Department, IT-Department, etc. It would be good to separate the country and city into a separate entity, so that there is no redundancy of data in the country and address attributes and there is compliance with the normal form. However, I did not do this: it is not said what company we are talking about: For example, if the company is not large and does not have many departments and employees, there is simply no need to decompose the database scheme and such a result will satisfy all the requirements. If we are talking about a large company that operates in several countries and cities, then it is necessary to select additional entities, for example - countries, cities, buildings (where the departments are located)

Bachman-Notation:

![Bachman-Notation-PR-Department](https://github.com/user-attachments/assets/061305b5-0eb6-41b4-b1b4-3e0c4ad1466e)



Barker-Notation:

![Barker-Notation-PR-Department](https://github.com/user-attachments/assets/2c0e8bde-a997-4312-b97c-fafa39fdb31e)



Relation-Model

![Relation-Model-PR-Department](https://github.com/user-attachments/assets/70f863ed-48d1-4097-9911-bc329661b3c4)

