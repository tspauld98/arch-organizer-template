# Representative Sequence Diagrams

## Purpose

The representative sequence diagrams are a set of diagrams that shows the interactions between the system components of the target-state solution.  These diagrams are used to demonstrate how the key use cases exercise the functionality of the target-state solution. The representative sequence diagrams are intended to illustrate the behavior of the target-state solutions for business stakeholders and technical leadership.  The artifacts in the representative sequence diagrams are at the `kite` level of abstraction.

## Electivity

This artifact is considered:  **Optional**

## Representative Sequence Diagrams for Online Banking System

Usually, there is at least one representative sequence diagram for each key use case.  The diagram below shows the interactions between the system components for the `Transfer Funds` use case.

### UC-03: Transfer Funds Sequence Diagram

<div style="width:100%; text-align: center; border-style: solid;">
<br/>

```mermaid
sequenceDiagram
    box White Transfer Funds
        actor ac1 as Authenticated Customer
        participant comp1 as Banking React App
        participant comp2 as Banking Web Service
        participant comp3 as Banking Service
        participant db1 as Transactions Database
        participant bus1 as Transactions Service Bus
    end
    
    activate ac1
    ac1->>comp1: Select 'Transfer Funds'
    activate comp1
    comp1->>comp2: Request to transfer funds
    activate comp2
    comp2-->>comp3: Retrieve user's accounts
    activate comp3
    comp3-->>db1: Retrieve user's accounts
    db1-->>comp3: User's accounts retrieved
    comp3-->>comp2: User's accounts retrieved
    deactivate comp3
    comp2-->>comp1: User's accounts retrieved
    deactivate comp2
    comp1-->>ac1: Display user's accounts
    deactivate comp1
    
    ac1->>comp1: Select 'From Account' and 'To Account'
    activate comp1
    comp1->>comp2: Send transfer details
    comp2-->>comp1: Validate transfer details
    comp1-->>ac1: Display transfer details
    deactivate comp1
    
    ac1->>comp1: Enter transfer amount and confirm
    activate comp1
    comp1->>comp2: Request to process transfer
    activate comp2
    comp2-->>comp3: Update account balances
    activate comp3
    comp3-->>db1: Update account balances
    comp3-->>bus1: Publish transfer event
    comp3-->>comp2: Account balances updated
    deactivate comp3
    comp2-->>comp1: Transfer successful
    deactivate comp2
    comp1-->>ac1: Transfer successful
    deactivate comp1
    
    deactivate ac1
```

<br/>
</div>
