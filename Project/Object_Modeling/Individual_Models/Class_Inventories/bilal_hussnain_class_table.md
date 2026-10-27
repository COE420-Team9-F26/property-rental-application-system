# Individual Class Inventory — Syed Bilal Hussnain (b00104970)

Component: tenant-side functionality (UC-06 to UC-10): search listings, view listing details, book a viewing, submit a rental application, view application status. Derived from FR-06 to FR-10, scenarios S-01/S-03/S-04, DFD processes P3/P4/P5 and data stores D2/D3/D4.

Diagram: `../Class_Diagrams/bilal_hussnain_class_diagram.png`.

| Class ID | Class Name | Purpose/Responsibility | Related Use Case(s) | Contributor |
|---|---|---|---|---|
| C01 | User *(abstract)* | Common identity and contact data for every platform user; generalization of Tenant and Landlord. | UC-06 to UC-10 (indirectly) | Syed Bilal Hussnain |
| C02 | Tenant | Searches listings, views details, books viewings and submits/tracks rental applications. | UC-06, UC-07, UC-08, UC-09, UC-10 | Syed Bilal Hussnain |
| C03 | Landlord | Owns listings and the viewing slots tenants book. Included only as far as this component needs it. | UC-07, UC-08 | Syed Bilal Hussnain |
| C04 | PropertyListing | Rental property with location, price, type, amenities, availability and status (D2). | UC-06, UC-07, UC-08, UC-09 | Syed Bilal Hussnain |
| C05 | ListingPhoto | One photo of a listing; enforces the 5 MB per-photo limit (NFR-05). | UC-07 | Syed Bilal Hussnain |
| C06 | SearchCriteria | Tenant's search filters: location, price range, property type, sort order (FR-06). | UC-06 | Syed Bilal Hussnain |
| C07 | ListingCatalog | Searches active listings, sorts by price, finds a listing by ID (P3). | UC-06, UC-07 | Syed Bilal Hussnain |
| C08 | ViewingSlot | Time slot offered by the landlord for a listing; bookable by only one tenant (FR-13, D3). | UC-08 | Syed Bilal Hussnain |
| C09 | ViewingAppointment | A tenant's confirmed booking of a viewing slot (FR-08, D3). | UC-08 | Syed Bilal Hussnain |
| C10 | RentalApplication | Tenant's application with personal details, move-in date and status (FR-09, FR-10, D4). | UC-09, UC-10 | Syed Bilal Hussnain |

*AI-drafted with Claude, reviewed by Syed Bilal Hussnain.*
