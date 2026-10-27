# Class Model Consistency Check



## 1. Use cases to classes

| Use case | Requirement | Classes used |
|----------|-------------|--------------|
| UC-01 Create Property Listing | FR-01 | Landlord, PropertyListing, ListingPhoto |
| UC-02 Edit Property Listing | FR-02 | Landlord, PropertyListing, ListingPhoto |
| UC-03 Withdraw Rental Application | FR-03 | Tenant, RentalApplication |
| UC-04 View Submitted Applications | FR-04 | Landlord, PropertyListing, RentalApplication |
| UC-05 Review Rental Application | FR-05 | Landlord, RentalApplication, PropertyListing |
| UC-06 Search Listings | FR-06 | Tenant, PropertyListing, SearchCriteria |
| UC-07 View Listing Details | FR-07 | Tenant, PropertyListing, ListingPhoto |
| UC-08 Book Viewing Appointment | FR-08, FR-13 | Tenant, PropertyListing, ViewingSlot, ViewingAppointment, Notification |
| UC-09 Submit Rental Application | FR-09, FR-10 | Tenant, PropertyListing, RentalApplication |
| UC-10 View My Application Status | none | Tenant, RentalApplication |
| UC-11 Define Viewing Slots | FR-11 | Landlord, PropertyListing, ViewingSlot |
| UC-12 View Viewing Calendar | FR-12 | Landlord, ViewingAppointment |
| UC-13 Register Account | none | User, Tenant, Landlord |
| UC-14 Log Into System | FR-14 | User (and its subclasses) |
| UC-15 Cancel or Reschedule Viewing | FR-15 | Landlord, ViewingAppointment, ViewingSlot, Notification |
| UC-16 View Registered User Accounts | FR-16 | Admin, User |
| UC-17 Suspend or Reactivate Account | FR-17 | Admin, User, AdminActionLog |
| UC-18 View Flagged Listings Log | FR-18 | Admin, PropertyListing, ListingFlag, AdminActionLog |
| UC-19 Remove Policy-Violating Listing | FR-19 | Admin, PropertyListing, AdminActionLog |
| UC-20 View System Activity Statistics | FR-20 | Admin, ActivityStatistics, PropertyListing, RentalApplication |

Result: all 20 use cases have at least one class, and every class is used by at least one use case.

## 2. DFD data stores to classes

| Data store | Classes |
|------------|---------|
| D1 User Accounts | User, Tenant, Landlord, Admin |
| D2 Property Listings | PropertyListing, ListingPhoto |
| D3 Viewing Slots and Appointments | ViewingSlot, ViewingAppointment |
| D4 Rental Applications | RentalApplication |
| D5 Admin Action and Flag Log | ListingFlag, AdminActionLog |



## 3. Multiplicities

| Relationship | Multiplicity | Requirement |
|--------------|--------------|-------------|
| Landlord owns PropertyListing | 1 to * | FR-01, FR-02, FR-04 |
| PropertyListing has ListingPhoto | 1 to 1..10 | FR-01, NFR-05 |
| PropertyListing receives RentalApplication | 1 to * | FR-04 |
| Tenant submits RentalApplication | 1 to * | FR-09 |
| PropertyListing offers ViewingSlot | 1 to * | FR-11 |
| ViewingSlot is reserved by ViewingAppointment | 1 to 0..1 | FR-13 |
| Tenant books ViewingAppointment | 1 to * | FR-08 |
| ViewingAppointment triggers Notification | 1 to 1..* | S-03, FR-15 |
| Admin raises ListingFlag | 1 to * | FR-18 |
| Admin performs AdminActionLog | 1 to * | NFR-17 |

FR-10 (one active application per tenant per listing) cannot be shown with a multiplicity, so it is a note on the diagram and is checked in RentalApplication.

