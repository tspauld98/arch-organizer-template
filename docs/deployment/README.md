# Deployment View

## Purpose

The purpose of the deployment view is to describe the solution's deployment structure in a production environment.  The deployment view is intended to brief architects, developers, operations staff, and technical parters such as security and compliance teams.  The artifacts in the deployment view are at the `sea` level of abstraction.

## Electivity

This section is considered:  **Mandatory**

## Artifacts

| Artifact | Description |
| -------- | ----------- |
| [Deployment Diagram](/deployment/DeploymentDiagram.md) | A deployment diagram illustrates how a system or component is deployed in a production environment including any external service dependencies or connectivity required for the system or component's operation. |
| [Service Level Agreements and Expectations](/deployment/ServiceLevelAgreements.md) | The Service-Level Agreements and Expectations artifact outlines all the availability and performance metrics expected of the system or component as well as any links or references to monitor current values for comparison. |
| [Component Diagram](/deployment/ComponentDiagram.md) | A component diagram illustrates how the code and configuration artifacts are packaged into components. |
| [Domain Object Model](/deployment/DomainObjectModel.md) | A domain object model is a class diagram that only shows the classes which represent the real-world entities required to solve the business problem at hand.  Whenever possible, technical design patterns in class interactions and associations should be left out of this view. |
