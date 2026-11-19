# Architectural Style Selection


## 1. Selected Architectural Style

Closed 3-layer architecture, with the application layer divided into four partitions.

| Layer | Content |
|-------|---------|
| Presentation layer | The web browser (external system). |
| Application layer | The four components: AccountManagement, RentalManagement, ViewingManagement and Administration. |
| Data layer | The relational database (external system). |

## 2. Main Characteristics

- A layer only uses the layer directly below it (closed architecture). The browser calls only AccountManagement, and only the four components call the database.
- Partitions of the same layer may call each other in one direction only, with no cycles.
- Every call goes through a provided interface.

## 3. Why It Is Appropriate

- The project is a web application with a browser, a backend and a database.
- The Lab 5 classes group into four business areas, which become the four partitions.
- The Lab 6 sequence diagrams only call downward, so they fit the layers without change.

## 4. How It Supports the Design Goals

| Goal | How the style supports it |
|------|---------------------------|
| AG-01 Maintainability and Modularity | Closed layers and narrow interfaces give low coupling, so a change stays inside one partition. |
| AG-02 Security | Every request passes through AccountManagement, so login, the account lock and the admin check sit in one place. The browser cannot read the data directly. |


## 5. Advantages and Limitations

| Advantages | Limitations |
|------------|-------------|
| Easy to explain: each layer has one job. | Every request crosses the layers, which adds a small delay. |
| The partitions can be built in parallel by the team. | NFR-01 is at risk: a new listing field changes the browser form, PropertyListing and the database table. Objects must be mapped to tables generically to stay within 2 components. |
| The browser and the database can change independently. | The database is a single point of failure. |
