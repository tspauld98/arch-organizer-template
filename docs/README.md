# Overview

## Template Introduction

***This file is the main documentation file (`docs/README.md`) for the site. Regardless of your documentation structure, this file should always exist.***

This site contains the sample artifacts for the architecture organizer template project.  If you'd like to use this template for your own project, you can [fork it](https://github.com/tspauld98/arch-organizer-template/fork) or [create a new repository from it](https://github.com/new?template_name=arch-organizer-template).  You can also [view the source code](https://github.com/tspauld98/arch-organizer-template) for this site.  It is set up so that the site's content is in the `docs` folder.  Once you have set up this template in your own repository, make changes to any Markdown files in the `docs` folder to replace this documentation with your documentation for your project.  After making your changes, you can test it locally with the `docsify` command or host it on compatible services.  If you are using Github Pages, you can set the source for your site to be the `docs` folder in the `main` branch.

***Detailed instructions for using this template can be found [here](https://github.com/tspauld98/arch-organizer-template) in the `README.md` file.***

The **Template Introduction** section can be deleted when you customize this site for your own project.

## Purpose

The purpose of this site is to provide a template for creating an architecture organizer document that describes the design of a system or component.  The concept of an architecture organizer is a light-weight structure where design artifacts are organized by the stakeholders they are intended to address.  While this structure is opinionated, the notation for documenting the design is agnostic. The site is organized into the following sections:

- ***Logical View***: Describes the business problem and the solution in terms of the system's components and their interactions.
  - **Intended Audience**: Business stakeholders and technical leadership
  - **Abstraction Level**: Kite Level
  - **Included Artifacts**: Context Diagram, Key Use Cases, Capability Map, Target-State Solution, Representative Sequence Diagrams, and Journey Plan
- ***Deployment View***: Describes the physical infrastructure and the deployment of the system's components.
  - **Intended Audience**: Technical leadership such as architects, developers, operations staff, and technical parters such as security and compliance teams
  - **Abstraction Level**: Sea Level
  - **Included Artifacts**: Domain Object Model, Component Diagram, Deployment Diagram, and Service Level Agreements and Expectations
- ***Detailed View***: Describes the detailed internal design of the system's components.
  - **Intended Audience**: Developers, operations staff, and technical partners such as security and compliance teams
  - **Abstraction Level**: Fish Level
  - **Included Artifacts**: Interface Definitions, Class Diagrams, Sequence Diagrams, State Diagrams, Activity Diagrams, and Data Models
- ***Decision Log***: The repository for all technical decisions made in the course of developing the design and implementation of the target solution.
  - **Intended Audience**: All stakeholders
  - **Abstraction Level**: All levels
  - **Included Artifacts**: Architecture Decision Records

As the target project is developed, the artifacts in the organizer will be updated to reflect the current state of the system in the order they are listed.  The ***Logical View*** artifacts are required first.  As the design gets closer to finalized for the next release, artifacts from the ***Deployment View*** and ***Detailed View*** will be added to or updated in the organizer.  Individual artifacts always have **Purpose** and **Electivity** sections to help guide the author in customizing the artifact for their design.

The artifacts in the template illustrate a fictional design for an on-line banking system.

## Lifecycle

Current Status: **Under Development**

### Lifecycle Definitions

- **Experimental**: The target solution (system or component) is experimental so many parts of the design and any decisions are to be considered in a draft state.
- **Under Development**: The target solution (system or component) is under active development so some parts of the design and some decisions are still works in progress, however, the artifacts should be reviewed and evaluated with a `production-readiness` lense.
- **Released**: The target solution (system or component) is released and in production.
- **Contained**: The target solution (system or component) is no longer in active development and is in a maintenance phase. It is closed for adoption/integration into other systems or components. It will be maintained until all systems or components that depend on it have found new solutions or have been retired.
- **Retired**: The target solution (system or component) is no longer in production and is no longer maintained.  Any deployments have been shut down.

## Design Roles

| Role              | Occupants                                     |
| ----------------- | --------------------------------------------- |
| Primary Architect | [Tim Spaulding](https://github.com/tspauld98) |
| Approver          | [Tim Spaulding](https://github.com/tspauld98) |
| Contributors      | [Tim Spaulding](https://github.com/tspauld98) |
| Reviewers         | [Tim Spaulding](https://github.com/tspauld98) |

## Version Information

You can find the version information for this site [here](https://github.com/tspauld98/arch-organizer-template/releases/latest).  The version information is in [Semantic Versioning](https://semver.org/).
