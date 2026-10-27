# Class Inventory (Individual): Eyad Tarek ElBaha

Component: Accounts/Login and Viewing Scheduling

| **ID** | **Class Name** | **Purpose / Responsibility** | **Use Case(s)** | **Contributor** |
|---|---|---|---|---|
| Class ID | Class Name | Purpose/Responsibility | Related Use Case(s) | Contributor |
| C01 | User (abstract) | Base class for anyone with an account. Holds the email, hashed password, role, account status, and the failed login count/lock time. This is basically an account record in D1. | UC-13, UC-14, UC-17 | Eyad ElBaha |
| C02 | Tenant | A user who books viewings. Gets a confirmation when they book and a notice if the landlord cancels or reschedules. | UC-08, UC-13, UC-14, UC-15 | Eyad ElBaha |
| C03 | Landlord | A user who sets the viewing times for their listings and can see all their upcoming viewings in a calendar. | UC-11, UC-12, UC-13, UC-14, UC-15 | Eyad ElBaha |
| C04 | Admin | A user who logs in as admin (P1 in our DFD). Admins can't sign up themselves (A-7) and their role gets checked on every admin request (NFR-16). What admins actually do is in Marwan's part. | UC-14, UC-16 to UC-20 | Eyad ElBaha |
| C05 | AuthenticationService | Takes care of sign up and login. Checks the password rules (NFR-15), hashes passwords (NFR-07), locks the account for 15 min after 5 wrong tries (NFR-11) and stops suspended users from logging in (FR-17). | UC-13, UC-14 | Eyad ElBaha |
| C06 | ViewingSlot | A time the landlord makes available for viewing a listing (date, start/end time, status). Only one tenant can book a slot (FR-13). Saved in D3. | UC-08, UC-11, UC-15 | Eyad ElBaha |
| C07 | ViewingAppointment | Created when a tenant books a slot. Connects the tenant to the slot and has a status (confirmed, cancelled, rescheduled). Saved in D3 within 1 second (NFR-12). | UC-08, UC-12, UC-15 | Eyad ElBaha |
| C08 | ViewingScheduler | Handles the scheduling logic: adding slots (FR-11), booking without double booking (FR-13), cancelling/rescheduling (FR-15) and getting the landlord's calendar (FR-12). | UC-08, UC-11, UC-12, UC-15 | Eyad ElBaha |
| C09 | Notification | Message that shows up on a user's dashboard, like the booking confirmation both sides get (S-03) or the notice the tenant gets when a viewing changes (FR-15). | UC-08, UC-15 | Eyad ElBaha |
