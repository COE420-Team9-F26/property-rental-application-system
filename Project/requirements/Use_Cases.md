# Use Cases

## Zohair Syed Contributions

- **UC-01** — Create Property Listing (Actor: Landlord): Landlord enters location, price, type, amenities, and photos to publish a new listing.
- **UC-02** — Edit Property Listing (Actor: Landlord): Landlord updates details of an existing listing (price, availability, description).
- **UC-03** — Withdraw Rental Application (Actor: Tenant): Tenant retracts a submitted application before the landlord accepts or rejects it.
- **UC-04** — View Submitted Applications (Actor: Landlord): Landlord reviews all applications received for their listings.
- **UC-05** — Review Rental Application (Actor: Landlord): Landlord accepts or rejects a specific application, updating its status.





add urs here






## Use Case Relationships

| Relationship ID | Base Use Case | Related Use Case | Relationship | Justification |
|---|---|---|---|---|
| R-01 | UC-09 Submit Rental Application | UC-14 Log Into System | `<<include>>` | A tenant must always be authenticated before submitting an application; login is a mandatory step, not optional. |
| R-02 | UC-08 Book Viewing Appointment | UC-14 Log Into System | `<<include>>` | Booking a viewing always requires the tenant to be logged in first. |
| R-03 | UC-01 Create Property Listing | UC-14 Log Into System | `<<include>>` | A landlord must always be authenticated to publish a listing. |
| R-04 | UC-17 Suspend/Reactivate User Account | UC-16 View Registered User Accounts | `<<include>>` | The admin must always locate the account in the user list before taking action on it. |
| R-05 | UC-09 Submit Rental Application | UC-03 Withdraw Rental Application | `<<extend>>` | Withdrawal only happens conditionally, for some submitted applications, not every one. |
| R-06 | UC-08 Book Viewing Appointment | UC-15 Cancel/Reschedule Viewing | `<<extend>>` | Cancelling or rescheduling is an optional follow-up that only applies to some bookings. |
| R-07 | UC-18 View Flagged Listings Log | UC-19 Remove Policy-Violating Listing | `<<extend>>` | Removal only happens conditionally, if the admin's review confirms an actual violation. |