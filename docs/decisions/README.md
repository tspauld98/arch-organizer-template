# Decision Log

This repository is the source of truth for technical decisions related to the architecture described by this organizer.  The decisions are authored as [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) files using [adr-tools](https://github.com/npryce/adr-tools).

## Default Approver

The approver for this repository is [Tim Spaulding](https://github.com/tspauld98) unless he delegates the responsibility.

## Current Decisions

The following decisions have been approved and are in effect:

| Serial Number | Driver        | Title                                                                             |
| ------------- | ------------- | --------------------------------------------------------------------------------- |
| 0001          | Tim Spaulding | [Record Architecture Decisions](/decisions/0001-record-architecture-decisions.md) |
| 0002          | Tim Spaulding | [First Principles](/decisions/0002-first-principles.md)                           |
| 0003          | Tim Spaulding | [Technology Stack](/decisions/0003-technology-stack.md)                           |
| 0004          | Tim Spaulding | [Initial Release](/decisions/0004-initial-release.md)                             |

## Superseded and Rescinded Decisions

The following decisions have been superseded or rescinded and are no longer in effect:

| Serial Number | Status        | Title                                                                             |
| ------------- | ------------- | --------------------------------------------------------------------------------- |
| None          | N/A           | N/A                                                                               |

## Getting Started

### Pre-requisites

To author decisions, you will need to install [adr-tools](https://github.com/npryce/adr-tools) on your local machine.  This toolset will help you create new ADR documents ensuring they are in the correct location and using the correct template.

In addition to `adr-tools`, since these decisions are tracked in a Git repository, you will need to have `git` installed on your local machine and the local repository on your machine should be synced with an `origin` repository on Github.

### Requesting a Decision

To request a decision, [create an issue](https://github.com/tspauld98/arch-organizer-template/issues/new) for this repository on Github with the following information:

* Title: A short title for the decision
* Description: A detailed description of the requested decision with the following information:
  * Context: The issue motivating the decision, and any context that influences or constrains the decision.
  * Scope: The scope of the requested decision (i.e. specific component, service-wide or organization-wide).
  * Type: The type of the requested decision (i.e. Technology Selection or Process Change).
* Labels: Add the `Requested` label to the issue to distinguish it from a normal change request.

### Authoring a Decision

### Contributing to a Decision

### Reviewing a Decision

## Authoring Good Decisions

TBD

## Decision Lifecycle

TBD

### Status

* Requested
* In Progress
* Comments Requested
* Approval Requested
* Approved
* Superseded
* Rescinded
