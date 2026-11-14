## Data Independence

- **Definition** : Data independence in a Database Management System (DBMS) is the ability to modify a schema definition at one level without affecting a schema definition at the next higher level. 
- It separates the data from the applications that use it, ensuring that changes to how data is stored or organized do not require rewriting application code.

- Data independence depends on the [[#3 schema architecture]]
- ***schema* :** A database schema is a logical structure that defines how data is organized within a database.
## 3 schema architecture

![[Pasted image 20261114104030.png]]

1. **View Level (External Schema):** Describes the part of the database that a specific user or application is permitted to see.
2. **Logical Level (Conceptual Schema):** Describes what data is stored in the database and the relationships among those data (e.g., tables, columns, data types, constraints).
3. **Physical Level (Internal Schema):** Describes how data is physically stored on hardware (e.g., file structures, indexing, compression).
### Types of Data Independence

#### Logical Data Independence
- **Definition:** The capacity to change the conceptual schema without having to change external schemas or application programs.
- **Examples of changes:**
    - Adding a new column or table to the database.
    - Removing an attribute that existing applications do not use.
    - Splitting one table into two (normalization) or combining two tables into one (denormalization).
- **Difficulty:** Harder to achieve than physical data independence because applications are heavily dependent on the logical structure of the data they access.

#### **Physical Data Independence**
- **Definition:** The capacity to change the internal schema without having to change the conceptual (logical) schema or external application programs.
- **Examples of changes:**
    - Switching from hard disk drives (HDD) to solid-state drives (SSD).
    - Creating or deleting indexes to improve query performance.
    - Changing file organization methods (e.g., from sequential to hash files) or compression algorithms.
- **Difficulty:** Relatively easy to achieve, as most modern DBMS handle physical storage details automatically.