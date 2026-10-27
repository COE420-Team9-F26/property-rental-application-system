# Class Inventory – Class Responsibilities

**Student:** Marwan Rashid  
**AUS ID:** b00100951  
**Course:** COE420L, Lab 5

| Class ID | Class Name | Purpose/Responsibility | Related Use Case(s) | Contributor |
|---|---|---|---|---|
| C01 | UserAccount | Stores user profile information and account status, including whether an account is active, suspended, or removed. | UC-16, UC-17 | Marwan Rashid |
| C02 | Administrator | Represents an administrator who reviews flagged listings, removes listings, and manages user account status. | UC-16, UC-17, UC-18, UC-19 | Marwan Rashid |
| C03 | PropertyListing | Represents a property listing and its information, including its current status, for review, flagging, or removal. | UC-18, UC-19 | Marwan Rashid |
| C04 | ListingFlag | Records a report against a property listing, including the reason, date, and review status. | UC-18 | Marwan Rashid |
| C05 | AdminActionLog | Records administrator actions, including action type, affected item or account, and date/time, for accountability and traceability. | UC-20 | Marwan Rashid |
| C06 | ActivityStatistics | Provides summary statistics on users, property listings, and flagged listings for administrative monitoring. | UC-20 | Marwan Rashid |

## UML Class Diagram

![UML Class Diagram](UML_Diagram.png)
