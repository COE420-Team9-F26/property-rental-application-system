# Non-Functional Requirements

## Zohair Syed Contributions

- **NFR-01** (Maintainability): The system's codebase shall be modular such that adding a new listing field (e.g., pet policy) requires changes to no more than 2 components.
- **NFR-02** (Robustness): The system shall validate all listing form inputs and reject submissions with missing required fields, returning a clear error message.
- **NFR-03** (Portability): The web application shall render correctly on the latest two versions of Chrome, Firefox, and Safari.
- **NFR-04** (Usability): A landlord shall be able to create a new listing in under 10 minutes on first use, verified via usability testing.
- **NFR-05** (Size): Uploaded property photos shall be limited to 5MB each, with a maximum of 10 photos per listing.

## Marwan Rashid Alkashf Contributions

- **NFR-16** (Security): Admin dashboard access shall require a separate admin-role authentication check on every request, not just at login.
- **NFR-17** (Reliability): Admin actions (suspend account, remove listing) shall be logged with a timestamp and admin ID, retained for at least 1 year.
- **NFR-18** (Performance): The admin activity statistics dashboard shall refresh with data no older than 5 minutes.
- **NFR-19** (Usability): An administrator shall be able to locate and suspend a flagged account within 3 clicks from the admin dashboard.
- **NFR-20** (Scalability): The admin user list view shall support pagination for up to 10,000 user accounts without performance degradation.