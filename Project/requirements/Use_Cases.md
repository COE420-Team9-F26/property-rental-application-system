# Use Cases

## Zohair Syed Contributions

- **UC-01** — Create Property Listing (Actor: Landlord): Landlord enters location, price, type, amenities, and photos to publish a new listing.
- **UC-02** — Edit Property Listing (Actor: Landlord): Landlord updates details of an existing listing (price, availability, description).
- **UC-03** — Withdraw Rental Application (Actor: Tenant): Tenant retracts a submitted application before the landlord accepts or rejects it.
- **UC-04** — View Submitted Applications (Actor: Landlord): Landlord reviews all applications received for their listings.
- **UC-05** — Review Rental Application (Actor: Landlord): Landlord accepts or rejects a specific application, updating its status.


## Syed Bilal Hussnain Contributions


- **UC-06** — Search Property Listings (Actor: Tenant): Tenant filters listings by location, price range, and property type.
- **UC-07** — View Listing Details (Actor: Tenant): Tenant opens a listing to see photos, price, location, amenities, and availability.
- **UC-08** — Book Viewing Appointment (Actor: Tenant): Tenant selects an available time slot to schedule a property viewing.
- **UC-09** — Submit Rental Application (Actor: Tenant): Tenant submits personal details and desired move-in date for a listing.
- **UC-10** — View My Application Status (Actor: Tenant): Tenant checks the current status (submitted/accepted/rejected) of their own applications.


## Eyad ElBaha Contributions

- **UC-11** — Define Viewing Availability (Actor: Landlord): Landlord sets available time slots for property viewings.
- **UC-12** — View Viewing Calendar (Actor: Landlord): Landlord views all upcoming scheduled viewings across their listings.
- **UC-13** — Register Account (Actor: Tenant/Landlord): New user creates an account with email and password before using the platform.
- **UC-14** — Log Into System (Actor: Tenant/Landlord): Registered user authenticates with email and password to access their account.
- **UC-15** — Cancel/Reschedule Viewing (Actor: Landlord): Landlord cancels or reschedules a confirmed viewing appointment, notifying the tenant.

## Marwan Rashid Alkashf Contributions

- **UC-16** — View Registered User Accounts (Actor: Admin): Admin views a list of all tenant and landlord accounts.
- **UC-17** — Suspend/Reactivate User Account (Actor: Admin): Admin suspends or reinstates a user account (e.g., for policy violations).
- **UC-18** — View Flagged Listings Log (Actor: Admin): Admin reviews listings flagged as duplicate or inappropriate.
- **UC-19** — Remove Policy-Violating Listing (Actor: Admin): Admin removes a listing that violates platform policy.
- **UC-20** — View System Activity Statistics (Actor: Admin): Admin views platform-wide stats (active listings, weekly applications, etc.).






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

## Team Consolidated Use Cases

No duplicates or conflicts were found across individual contributions (confirmed during Exercise 6 consistency check); all 20 UCs are carried forward unchanged, and the diagram in `Use_Case_Diagram/` and the relationship table above reflect this full set.

| UC ID | Use Case Name | Primary Actor | Short Description | Contributor |
|---|---|---|---|---|

| UC-01 | Create Property Listing | Landlord | Landlord enters location, price, type, amenities, and photos to publish a new listing. | Zohair Syed |
| UC-02 | Edit Property Listing | Landlord | Landlord updates details of an existing listing (price, availability, description). | Zohair Syed |
| UC-03 | Withdraw Rental Application | Tenant | Tenant retracts a submitted application before the landlord accepts or rejects it. | Zohair Syed |
| UC-04 | View Submitted Applications | Landlord | Landlord reviews all applications received for their listings. | Zohair Syed |
| UC-05 | Review Rental Application | Landlord | Landlord accepts or rejects a specific application, updating its status. | Zohair Syed |
| UC-06 | Search Property Listings | Tenant | Tenant filters listings by location, price range, and property type. | Syed Bilal Hussnain |
| UC-07 | View Listing Details | Tenant | Tenant opens a listing to see photos, price, location, amenities, and availability. | Syed Bilal Hussnain |
| UC-08 | Book Viewing Appointment | Tenant | Tenant selects an available time slot to schedule a property viewing. | Syed Bilal Hussnain |
| UC-09 | Submit Rental Application | Tenant | Tenant submits personal details and desired move-in date for a listing. | Syed Bilal Hussnain |
| UC-10 | View My Application Status | Tenant | Tenant checks the current status (submitted/accepted/rejected) of their own applications. | Syed Bilal Hussnain |
| UC-11 | Define Viewing Availability | Landlord | Landlord sets available time slots for property viewings. | Eyad ElBaha |
| UC-12 | View Viewing Calendar | Landlord | Landlord views all upcoming scheduled viewings across their listings. | Eyad ElBaha |
| UC-13 | Register Account | Tenant/Landlord | New user creates an account with email and password before using the platform. | Eyad ElBaha |
| UC-14 | Log Into System | Tenant/Landlord | Registered user authenticates with email and password to access their account. | Eyad ElBaha |
| UC-15 | Cancel/Reschedule Viewing | Landlord | Landlord cancels or reschedules a confirmed viewing appointment, notifying the tenant. | Eyad ElBaha |
| UC-16 | View Registered User Accounts | Admin | Admin views a list of all tenant and landlord accounts. | Marwan Rashid Alkashf |
| UC-17 | Suspend/Reactivate User Account | Admin | Admin suspends or reinstates a user account (e.g., for policy violations). | Marwan Rashid Alkashf |
| UC-18 | View Flagged Listings Log | Admin | Admin reviews listings flagged as duplicate or inappropriate. | Marwan Rashid Alkashf |
| UC-19 | Remove Policy-Violating Listing | Admin | Admin removes a listing that violates platform policy. | Marwan Rashid Alkashf |
| UC-20 | View System Activity Statistics | Admin | Admin views platform-wide stats (active listings, weekly applications, etc.). | Marwan Rashid Alkashf |