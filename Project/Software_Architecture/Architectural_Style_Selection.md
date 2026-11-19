# Architectural Style Selection

## 1. Selected Style

We chose a layered architecture (three-tier). The system has three layers:

- Presentation layer: the web pages for tenants, landlords and admins.
- Business logic layer: the rules of the system. We split this layer into modules based on our Lab 4 DFD processes: accounts and login (P1), listings and search (P2, P3), viewings (P4), rental applications (P5) and admin (P6).
- Data layer: the database that stores D1 to D5 (accounts, listings, viewings, applications and admin data).

## 2. Main Characteristics

- Each layer only talks to the layer right below it. The pages never go to the database directly.
- Each layer gives services to the layer above it through interfaces and hides how it does them.
- Every request goes through the business layer, so checks like login happen in one place.

## 3. Why It Fits Our Project

Our system is a normal web app with a frontend, a backend and a database, which is what we said in our Lab 2 feasibility study. Our Lab 6 sequence diagrams and Lab 7 activity diagrams already follow this flow: the user uses the page, the page calls the logic, and the logic saves or reads the data. We also have three types of users who see different pages but use the same data and rules, so they can all share the same business layer.

## 4. How It Supports Our Design Goals

| Goal ID | Design Goal | How the Style Supports It |
|---|---|---|
| DG-01 | Security | All requests go through the business layer, so login (UC-14), the account lock (NFR-11) and the admin check (NFR-16) cannot be skipped. Only the data layer can touch the stored data, and passwords are hashed before they are saved (NFR-07). |
| DG-02 | Maintainability | Each layer and module has its own job. Adding a new listing field (NFR-01) only changes the listings module and the listing page, which is 2 components. |
| DG-03 | Performance | Search filtering is done in the listings module close to the data, and only the results are sent to the page (NFR-06). Since the layers are separate, the database or the server can be upgraded on its own if there are more users (NFR-10). |

## 5. Advantages and Limitations

**Advantages**

- Each layer is easier to understand, design and test on its own.
- It is easy to split the work between the 4 of us since each person already worked on one area.
- Changing one layer, like redesigning a page, does not affect the others.
- It is a common style, so there are a lot of examples and frameworks for it.

**Limitations**

- Every request has to go through all the layers, even simple ones like opening a listing, which adds a small delay.
- A new feature that needs new data still touches more than one layer.
- If the database or the server goes down, the whole system goes down.
- All modules share one database, so one slow query can slow down everything else.
