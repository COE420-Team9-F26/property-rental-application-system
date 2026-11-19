# Architectural Design Goals

| Goal ID | Design Goal | Description | Related Requirement | Priority | Justification |
|---|---|---|---|---|---|
| DG-01 | Security | Users should only be able to see and change their own data. Passwords are hashed, accounts get locked after too many wrong logins, and admins get checked on every request. | NFR-07, NFR-11, NFR-15, NFR-16, FR-14 | High | Rental applications have personal info about tenants. In Lab 2 we listed this as a risk (R4). Almost every use case needs the user to log in first, so if login is weak the whole system is weak. |
| DG-02 | Maintainability | The system is split into parts like accounts, listings, viewings, applications and admin. If we change one part, the other parts should not need to change. | NFR-01, NFR-02 | High | NFR-01 says adding a new listing field should change at most 2 components. We also keep going back and updating our work every lab, so it has to be easy to change. |
| DG-03 | Performance | The main pages should load fast. Search results should show up in under 2 seconds and the landlord's viewing calendar should load in under 2 seconds. | NFR-06, NFR-14, NFR-10 | Medium | Search is the first thing a tenant does. If it is slow they will probably leave before booking or applying. We put it as medium because the number of users is not that big. |
