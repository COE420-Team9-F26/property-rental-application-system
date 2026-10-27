# Integration Notes 

Team: Syed Zohair Hussnain (00098429), Syed Bilal Hussnain (b00104970), Eyad Tarek ElBaha (b00096104), Marwan Rashid Alkashf (b00100951)



## Main decisions

- We only kept entity classes. Eyad's two service classes and Bilal's ListingCatalog were moved into the entity classes, like the examples in the lecture slides.
- All statuses are now enumerations (AccountStatus, ListingStatus, ApplicationStatus, SlotStatus, AppointmentStatus, FlagReviewStatus). Before, some of us used Strings.
- We dropped the role attribute because Tenant, Landlord and Admin already show the role.
- Common data (fullName, email, phoneNumber, status, login and lockout data) is now in User.
- We removed attributes that no requirement needs (title, companyName, adminId).
- Marwan's "manages", "moderates" and "views" associations were replaced by dependencies and one association called "raises". We also removed "Landlord defines ViewingSlot" because a slot belongs to a listing and the listing belongs to the landlord.
- We added Admin.flagListing so the flag log from FR-18 can actually be filled.

## Duplicates and conflicts

| Item | Found in | Problem | What we decided |
|------|----------|---------|-----------------|
| User | All four | Four versions with different names, visibility and status fields. Bilal added phone. | One abstract User with fullName. status : AccountStatus replaces isSuspended and accountStatus. Role dropped. phone becomes phoneNumber. "removed" status dropped. |
| Tenant, Landlord | Zohair, Eyad, Bilal | Different operations. Extra phoneNumber and companyName. | Operations merged. phoneNumber moved to User. companyName dropped. |
| Admin | Marwan, Eyad | Two names. Extra adminId. No way to create a flag. | Named Admin. adminId dropped. hasAdminAccess kept. flagListing added. |
| PropertyListing | All four | Different attribute and operation names. Bilal added title and bedrooms. | Used availabilityDate, listingId and status : ListingStatus. Kept bedrooms, dropped title. Kept updateStatus for REMOVED. |
| ListingPhoto | Zohair, Bilal | Different file and size attributes. Bilal added displayOrder. | Used fileUrl and fileSizeBytes. Kept displayOrder. |
| RentalApplication | Zohair, Bilal | personalDetails against occupation and numberOfOccupants. Two association names. | occupation and numberOfOccupants replace personalDetails. Association named "receives". |
| ViewingSlot | Eyad, Bilal | Date fields differed. Bilal had a booked flag. | startTime and endTime as DateTime, with SlotStatus. Booked flag dropped. |
| ViewingAppointment | Eyad, Bilal | Enumeration against String status. | Used Eyad's version. Kept slot 1 to 0..1 appointment (FR-13). |
| AuthenticationService | Eyad only | Control class with no data. | Moved into User. |
| ViewingScheduler | Eyad only | Repeats operations from other classes. | Moved into Landlord, Tenant and the viewing classes. |
| ListingCatalog | Bilal only | Repeats search operations already in Tenant and PropertyListing. | Removed. SearchCriteria keeps the sort order. |
| ListingFlag | Marwan only | reviewStatus was a String. Association named "has". | reviewStatus becomes FlagReviewStatus. Association renamed "is flagged by". |
| AdminActionLog | Marwan only | Linked to UC-20. Stored adminID. | Linked to UC-17 to UC-19. adminID dropped. |
| ActivityStatistics | Marwan only | Table description did not match the class. | Kept as drawn (FR-20, NFR-18). Description shortened. |
| Admin associations | Marwan, Eyad | "manages", "moderates" and "views" imply one admin per item. | Replaced by dependencies and "raises". |
| Landlord defines ViewingSlot | Eyad | A slot already belongs to a listing. | Association removed. |
| Status fields | All four | Strings in three models, enumerations in one. | Enumerations for all (E01 to E06). |

## AI use declaration

Claude was used for formatting the tables.