# Target-State Solution

## Purpose

The target-state solution is a diagram that illustrates and describes the desired state of the solution required to solve the business problem as described by stakeholders.  It is a high-level diagram that shows the primary system components of the solution and the environment in which it runs including any technical dependencies required at run-time.  The target-state solution is intended to brief business stakeholders and technical leadership on what components need to be built to deliver the solution.  The artifacts in the target-state solution are at the `kite` level of abstraction.

## Electivity

This artifact is considered:  **Mandatory**

## Target-State Solution Diagram

```mermaid
flowchart TD

subgraph "User Interface"
    UI[User Interface] --> LB[Load Balancer]
end

subgraph "Load Balancer"
    LB --> WF[Web Frontend]
end

subgraph "Web Frontend"
    WF --> |HTTPS| API[API Gateway]
end

subgraph "API Gateway"
    API --> AS[Authentication Service]
    API --> BS[Banking Service]
    API --> MS[Notification Service]
end

subgraph "Authentication Service"
    AS --> DB[Database]
end

subgraph "Banking Service"
    BS --> DB
    BS --> ESB[External Service Bus]
end

subgraph "Notification Service"
    MS --> Email
    MS --> SMS
end

subgraph "External Service Bus"
    ESB --> EB[External Banking System]
end

subgraph "Database"
    DB[User Data]
    DB[Transactions]
end
```
