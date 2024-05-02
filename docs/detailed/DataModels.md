# Data Models

## Purpose

The purpose of the data models is to describe the data structures and relationships that are used by the system.  The data models are intended to specify the structure of the data stores for developers and database administrators.  The artifacts in the data models are at the `fish` level of abstraction.

## Electivity

This section is considered:  **Mandatory, if Detailed View is included**

## Online Banking Data Model

The data model below shows the structure of the database for the online banking system.

### Online Banking Entity Relationship Diagram

<div style="width:100%; text-align: center; border-style: solid;">
<br/>

```mermaid
    erDiagram
        CUSTOMERS {
            int id PK
            string name
            string email
            date dob
            string address
        }
        ACCOUNTS {
            int id PK
            string account_number
            decimal balance
            string type
            int customer_id FK
        }
        TRANSACTIONS {
            int id PK
            decimal amount
            string type
            timestamp date
            int account_id FK
        }
        CUSTOMERS ||--o{ ACCOUNTS : "has"
        ACCOUNTS ||--o{ TRANSACTIONS : "has"
```

<br/>
</div>
