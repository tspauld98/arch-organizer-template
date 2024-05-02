# Domain Object Model

## Purpose

The purpose of domain object model is to describe the classes and relationships in the system that model real-world entities and their relationships.  The class diagrams are intended to describe in detail the bounded context of the target-state solution to provide additional clarity on the system's primary structures and their interactions for developers.  The artifacts in the domain object model are at the `sea` level of abstraction.

## Electivity

This section is considered:  **Optional**

## Domain Object Model for Online Banking

The class diagram below shows the structure of the domain objects for the online banking system.

<div style="width:100%; text-align: center; border-style: solid;">
<br/>

```mermaid
classDiagram
    class Bank {
        -name: string
        -location: string
        +Bank(name: string, location: string)
        +getName(): string
        +getLocation(): string
        +setName(name: string): void
        +setLocation(location: string): void
    }

    class Customer {
        -customerId: int
        -name: string
        -email: string
        -address: string
        +Customer(customerId: int, name: string, email: string, address: string)
        +getCustomerId(): int
        +getName(): string
        +getEmail(): string
        +getAddress(): string
        +setEmail(email: string): void
        +setAddress(address: string): void
    }

    class Account {
        -accountId: int
        -balance: float
        -type: string
        -customer: Customer
        +Account(accountId: int, balance: float, type: string, customer: Customer)
        +getAccountId(): int
        +getBalance(): float
        +getType(): string
        +getCustomer(): Customer
        +setBalance(balance: float): void
        +setType(type: string): void
    }

    class Transaction {
        -transactionId: int
        -amount: float
        -type: string
        -timestamp: Date
        -sourceAccount: Account
        -destinationAccount: Account
        +Transaction(transactionId: int, amount: float, type: string, timestamp: Date, sourceAccount: Account, destinationAccount: Account)
        +getTransactionId(): int
        +getAmount(): float
        +getType(): string
        +getTimestamp(): Date
        +getSourceAccount(): Account
        +getDestinationAccount(): Account
    }

    Bank -- Customer : has
    Customer "1" -- "*" Account : owns
    Account "1" -- "*" Transaction : has
```

<br/>
</div>
