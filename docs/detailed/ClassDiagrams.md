# Class Diagrams

## Purpose

The purpose of class diagrams is to describe the structure of the system by illustrating the classes and their relationships.  The class diagrams are intended to describe in detail the structure of the target-state solution to provide additional clarity on the system's components and their interactions for developers.  The artifacts in the class diagrams are at the `fish` level of abstraction.

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

## More Information on Class Diagrams

While class diagrams can be critical to understand how a system works, they are often not necessary for every system.  The decision to include class diagrams should be based on the complexity of the system and the need to understand the structure of the system by developers.  If the system is simple and the structure is obvious, then class diagrams may not be necessary.  For more information on class diagrams, see the [UML Class Diagrams](https://www.uml-diagrams.org/class-diagrams-overview.html) page.  Both Mermaid and Lucidchart support class diagrams.
