# Detailed View

## Purpose

The purpose of the detailed view is to describe the solution's inner design and structure with specifics regarding interfaces and contracts.  The detailed view is intended to brief developers, operations staff, and technical partners such as security and compliance teams.  The artifacts in the deployment view are at the `fish` level of abstraction.  Since it's not always necessary to document every detail of a solution, the artifacts in this view are considered optional.  It's important to create/maintain the artifacts in this section when the solution requires a large team of developers to build/maintain it or when the consumers of the solution are developers.  In more simple cases, well-commented and documented code may be sufficient for communicating the detailed view of the solution.

## Electivity

This section is considered:  **Optional**

## Artifacts

| Artifact | Description |
| -------- | ----------- |
| [Interface Definitions](/detailed/InterfaceDefinitions.md) | This artifact, when present, contains the definitions of any public interfaces for the solution including both user experience definitions (storyboards) and API specifications. |
| [Class Diagrams](/detailed/ClassDiagrams.md) | The Class Diagrams artifact contains any class diagrams required to clarify the design or provide engineers with design direction and is only included as needed. |
| [Sequence Diagrams](/detailed/ComponentDiagram.md) | The Sequence Diagrams artifact contains any sequence diagrams for use cases that are complex enough to require illustration for the engineers working on the solution. |
| [State Diagrams](/detailed/StateDiagrams.md) | This artifact organizes and maintains any state diagrams required to clarify state changes occurring during the execution of complex use cases. |
| [Activity Diagrams](/detailed/ActivityDiagrams.md) | This artifact contains activity diagrams for use cases as an alternative to using sequence diagrams.  Since there is significant overlap in purpose between sequence diagrams and activity diagrams, this section usually only contains either the Sequence Diagrams artifact or the Activity Diagrams artifact. Only very rarely does this section contain both artifacts. |
| [Data Models](/detailed/DataModels.md) | The Data Models artifact is used to organize and maintain any data models that describe the persistence structure of the solution if needed.  The models in this artifact could be any combination of the following model types: SQL-based entity-relationship models, document models, name/value pair models, and/or blob models. |
