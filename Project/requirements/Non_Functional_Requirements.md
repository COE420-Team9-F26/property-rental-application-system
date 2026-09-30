# Non-Functional Requirements

## Zohair Syed Contributions

- **NFR-01** (Maintainability): The system's codebase shall be modular such that adding a new listing field (e.g., pet policy) requires changes to no more than 2 components.
- **NFR-02** (Robustness): The system shall validate all listing form inputs and reject submissions with missing required fields, returning a clear error message.
- **NFR-03** (Portability): The web application shall render correctly on the latest two versions of Chrome, Firefox, and Safari.
- **NFR-04** (Usability): A landlord shall be able to create a new listing in under 10 minutes on first use, verified via usability testing.
- **NFR-05** (Size): Uploaded property photos shall be limited to 5MB each, with a maximum of 10 photos per listing.

## Syed Bilal Hussnain Contributions

- **NFR-06** (Performance): Property search results shall return within 2 seconds for a catalog of up to 10,000 listings.
- **NFR-07** (Security): Tenant and landlord passwords shall be stored using a one-way hashing algorithm (e.g., bcrypt) and never in plaintext.
- **NFR-08** (Usability): A first-time tenant shall be able to search for and submit an application to a property within 5 minutes without assistance, verified via usability testing with 5 test users.
- **NFR-09** (Reliability): The system shall maintain at least 99% uptime during business hours (9 AM-9 PM), measured over a rolling 30-day period.
- **NFR-10** (Scalability): The system shall support at least 500 concurrent users browsing listings without average page load time exceeding 3 seconds.


## Eyad ElBaha Contributions

- **NFR-11** (Security): The system shall lock a user account for 15 minutes after 5 consecutive failed login attempts.
- **NFR-12** (Reliability): Scheduled viewing appointment data shall be persisted to the database within 1 second of confirmation, surviving a server restart.
- **NFR-13** (Usability): Login and registration forms shall provide inline validation feedback (e.g., invalid email format) within 1 second of user input.
- **NFR-14** (Performance): The landlord's viewing calendar shall load within 2 seconds for up to 50 scheduled appointments.
- **NFR-15** (Security): Passwords shall be required to be at least 8 characters, including one number and one special character.

## Marwan Rashid Alkashf Contributions

- **NFR-16** (Security): Admin dashboard access shall require a separate admin-role authentication check on every request, not just at login.
- **NFR-17** (Reliability): Admin actions (suspend account, remove listing) shall be logged with a timestamp and admin ID, retained for at least 1 year.
- **NFR-18** (Performance): The admin activity statistics dashboard shall refresh with data no older than 5 minutes.
- **NFR-19** (Usability): An administrator shall be able to locate and suspend a flagged account within 3 clicks from the admin dashboard.
- **NFR-20** (Scalability): The admin user list view shall support pagination for up to 10,000 user accounts without performance degradation.

## Team Consolidated Non-Functional Requirements

No duplicates or conflicts were found across individual contributions (confirmed during Exercise 6 consistency check); all 20 NFRs are carried forward unchanged.

| NFR ID | Category | Non-Functional Requirement | Contributor |
|---|---|---|---|

| NFR-01 | Maintainability | The system's codebase shall be modular such that adding a new listing field (e.g., pet policy) requires changes to no more than 2 components. | Zohair Syed |
| NFR-02 | Robustness | The system shall validate all listing form inputs and reject submissions with missing required fields, returning a clear error message. | Zohair Syed |
| NFR-03 | Portability | The web application shall render correctly on the latest two versions of Chrome, Firefox, and Safari. | Zohair Syed |
| NFR-04 | Usability | A landlord shall be able to create a new listing in under 10 minutes on first use, verified via usability testing. | Zohair Syed |
| NFR-05 | Size | Uploaded property photos shall be limited to 5MB each, with a maximum of 10 photos per listing. | Zohair Syed |
| NFR-06 | Performance | Property search results shall return within 2 seconds for a catalog of up to 10,000 listings. | Syed Bilal Hussnain |
| NFR-07 | Security | Tenant and landlord passwords shall be stored using a one-way hashing algorithm (e.g., bcrypt) and never in plaintext. | Syed Bilal Hussnain |
| NFR-08 | Usability | A first-time tenant shall be able to search for and submit an application to a property within 5 minutes without assistance, verified via usability testing with 5 test users. | Syed Bilal Hussnain |
| NFR-09 | Reliability | The system shall maintain at least 99% uptime during business hours (9 AM-9 PM), measured over a rolling 30-day period. | Syed Bilal Hussnain |
| NFR-10 | Scalability | The system shall support at least 500 concurrent users browsing listings without average page load time exceeding 3 seconds. | Syed Bilal Hussnain |
| NFR-11 | Security | The system shall lock a user account for 15 minutes after 5 consecutive failed login attempts. | Eyad ElBaha |
| NFR-12 | Reliability | Scheduled viewing appointment data shall be persisted to the database within 1 second of confirmation, surviving a server restart. | Eyad ElBaha |
| NFR-13 | Usability | Login and registration forms shall provide inline validation feedback (e.g., invalid email format) within 1 second of user input. | Eyad ElBaha |
| NFR-14 | Performance | The landlord's viewing calendar shall load within 2 seconds for up to 50 scheduled appointments. | Eyad ElBaha |
| NFR-15 | Security | Passwords shall be required to be at least 8 characters, including one number and one special character. | Eyad ElBaha |
| NFR-16 | Security | Admin dashboard access shall require a separate admin-role authentication check on every request, not just at login. | Marwan Rashid Alkashf |
| NFR-17 | Reliability | Admin actions (suspend account, remove listing) shall be logged with a timestamp and admin ID, retained for at least 1 year. | Marwan Rashid Alkashf |
| NFR-18 | Performance | The admin activity statistics dashboard shall refresh with data no older than 5 minutes. | Marwan Rashid Alkashf |
| NFR-19 | Usability | An administrator shall be able to locate and suspend a flagged account within 3 clicks from the admin dashboard. | Marwan Rashid Alkashf |
| NFR-20 | Scalability | The admin user list view shall support pagination for up to 10,000 user accounts without performance degradation. | Marwan Rashid Alkashf |