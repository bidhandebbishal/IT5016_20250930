Requisition System (Part B Task 1 & 2)

Project Overview
This project is a Python-based Requisition Management System that demonstrates the use of Object-Oriented Programming (OOP). It enables staff members to submit requisitions for items. Requests with a total amount below $500 are automatically approved, while those above the threshold remain pending and require manager approval. The system also records overall statistics, such as how many requests have been submitted, approved, left pending, or rejected.
Features
- Each requisition is assigned a sequential counter-based ID (starts at 10001 and increments automatically)
Capture staff details such as date, ID, and name
Enter multiple items with their prices and compute the total
Automatically approve requests under $500
Manager can approve or reject pending requisitions
Show full details of each requisition
Generate statistics including total submitted, approved, pending, and rejected requisitions
Software Design Principles

1. KISS (Keep It Simple, Stupid)
The design of the code is kept simple for readability and ease of use. For instance, the auto-approval is handled with one clear condition:
if self.total < 500:
    self.status = 'Approved'
This makes the rule very easy to follow.

3. DRY (Don’t Repeat Yourself)
Repetition of logic is avoided by using class-level counters and methods that handle recurring tasks. For example, variables like total_submitted and total_approved are updated directly in the class. The reporting function show_statistics() also prevents duplication by centralising all output of statistics.

5. Single Responsibility Principle (SRP)
Every method in the system has a single, well-defined responsibility:

get_staff_info() → gathers staff details
get_items() → handles item input and totals
check_approval() → checks if requisition meets approval rules
manager_decision() → applies manager’s final choice
show_details() → displays requisition information

show_statistics() → outputs statistics summary
This separation makes the program easier to update and test.

4. Separation of Concerns
The system is divided into separate concerns. Input collection is done in get_staff_info() and get_items(), business logic is performed in check_approval() and manager_decision(), and reporting is handled in show_details() and show_statistics(). This ensures that modifying one area does not affect the others.

6. YAGNI (You Aren’t Gonna Need It)
The implementation includes only the functionality required at this stage. For example, it does not maintain a full list of item names because the task only required calculation of the total price. This prevents overengineering.

7. Clean Code
The program makes use of descriptive variable and method names such as staff_id, approval_ref, and show_statistics(). This improves clarity and helps others quickly understand the purpose of each element in the code.
Software Development Life Cycle (SDLC)
Planning – Defined the goal of building a requisition management system.
Requirements – Gathered the need for staff information, requisition details, approval rules, and statistics.
Design – Organised the solution into OOP methods, applying KISS, DRY, and SRP principles.
Implementation – Developed the code in Python.
Testing – Verified with different input scenarios (requests under $500, over $500, and manager approvals).
Maintenance – Ensured that changing approval rules or outputs requires minimal code updates.
Conclusion
This project demonstrates how applying software design principles results in a clean and maintainable program. By following KISS, DRY, SRP, Separation of Concerns, YAGNI, and Clean Code, the system is easy to understand, extend, and manage. It highlights how structured design and OOP concepts can be applied effectively in Python projects.
<img width="432" height="635" alt="image" src="https://github.com/user-attachments/assets/edbe83f1-2a93-42cd-90fc-308de4b62b9e" />
