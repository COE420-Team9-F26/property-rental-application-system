# Component Descriptions


The 4 components make up the application layer of the closed 3-layer architecture. The Web Browser (presentation layer) and the Relational Database (data layer) are external systems and are not counted as components.

## Components

| ID | Component | Responsibilities | Supported functionality | Provides | Requires |
|----|-----------|------------------|-------------------------|----------|----------|
| CO1 | AccountManagement | Registration, login and account lockout, account status, user roles, and the actor operations that run each use case. It is the entry point of the application layer. | UC-13, UC-14, UC-16, UC-17 and the entry point of all other use cases | IUserService | IRentalService, IViewingService, IAdminLogService, IDataAccess |
| CO2 | RentalManagement | Creating and editing listings and photos, search, and the rules of rental applications (submit, withdraw, accept, reject). | UC-01 to UC-07, UC-09, UC-10, and the listing parts of UC-08, UC-11, UC-18, UC-19 | IRentalService | IViewingService, IDataAccess |
| CO3 | ViewingManagement | Viewing slots, booking without double booking, cancelling and rescheduling appointments, and notifications. | UC-08, UC-11, UC-12, UC-15 | IViewingService | IDataAccess |
| CO4 | Administration | Flagged listings log, admin action log and activity statistics. | UC-17 (log part), UC-18, UC-19 (log part), UC-20 | IAdminLogService | IRentalService, IDataAccess |

The Web Browser requires IUserService, and the Relational Database provides IDataAccess.
