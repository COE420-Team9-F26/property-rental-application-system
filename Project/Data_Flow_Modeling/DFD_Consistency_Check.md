# DFD Consistency and Balancing Check

## Consistency Checks

| Check | Result |
|---|---|
| External entities (Tenant, Landlord, Admin) match the Use Case actors | Pass |
| Context Diagram and Level-0 DFD use the same external entities | Pass |
| Level-0 has at least 5 processes (6: P1 to P6) | Pass |
| Level-0 has at least 2 data stores (5: D1 to D5) | Pass |
| Core Processes Matrix has the same processes as Level-0 | Pass |
| Processes match the Use Cases and Functional Requirements | Pass |

## Balancing Check

The Context Diagram has 33 external data flows (17 in, 16 out). All 33 appear in the Level-0 DFD, entering or leaving the processes below.

| Process | Flows in | Flows out |
|---|---|---|
| P1 Manage Accounts and Authentication | 3 | 3 |
| P2 Manage Property Listings | 1 | 1 |
| P3 Search and View Listings | 1 | 1 |
| P4 Manage Viewing Appointments | 4 | 4 |
| P5 Process Rental Applications | 4 | 3 |
| P6 Administer Platform | 4 | 4 |
| Total | 17 | 16 |