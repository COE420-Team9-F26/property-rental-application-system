# Work Breakdown Structure (WBS)

Durations are expected times (E) in working days.

| ID | Task Name | Description | Predecessor(s) | Duration (Days) |
|---|---|---|---|---|
| T1 | Requirements refinement and rule definition | Settle the open rules (application states, booking and cancellation rules) and finalize the requirements. | None | 3 |
| T2 | Architecture and technology stack selection | Choose the frontend, backend and database tools, and split the system into modules. | T1 | 3 |
| T3 | Database design | Design the tables for users, listings, viewings, applications and the admin log. | T2 | 4 |
| T4 | User interface design | Sketch the screens for tenants, landlords and admins. | T1 | 5 |
| T5 | Authentication and account management | Build registration, login, user roles, password rules and account lockout (UC-13, UC-14). | T3 | 6 |
| T6 | Listing management module | Build listing creation and editing with photo upload and input checks (UC-01, UC-02). | T4, T5 | 6 |
| T7 | Search and listing details module | Build listing search, filters, sorting and the listing details page (UC-06, UC-07). | T6 | 5 |
| T8 | Viewing scheduling module | Build viewing slots, booking, the landlord calendar and cancel or reschedule (UC-08, UC-11, UC-12, UC-15). | T6 | 7 |
| T9 | Rental application module | Build application submit, withdraw, status check and landlord accept or reject (UC-03, UC-04, UC-05, UC-09, UC-10). | T6 | 6 |
| T10 | Admin module | Build the user list, suspend and reactivate, flagged listings, listing removal and statistics (UC-16 to UC-20). | T6 | 6 |
| T11 | System integration | Connect all modules and run the main scenarios (S-01 to S-05) end to end. | T7, T8, T9, T10 | 4 |
| T12 | Test plan and test case preparation | Write test cases from the requirements and scenarios, and prepare test data. | T2 | 4 |
| T13 | System testing and defect fixing | Run the tests, check performance and usability targets, and fix bugs. | T11, T12 | 7 |
| T14 | Technical documentation and user guides | Write the system documentation and the user guides for each user type. | T11 | 4 |
| T15 | Deployment preparation | Set up hosting and the live database, and run a final check. | T13 | 3 |
| T16 | Final report and presentation | Write the final report and prepare the presentation. | T14, T15 | 3 |
