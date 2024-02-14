# 2. First Principles

Date: 2024-02-12

## Roles

| Role            | Occupants                                     |
| --------------- | --------------------------------------------- |
| Driver          | [Tim Spaulding](https://github.com/tspauld98) |
| Approver        | [Tim Spaulding](https://github.com/tspauld98) |
| Contributors    | [Tim Spaulding](https://github.com/tspauld98) |
| Target Audience | Users of this template                        |

## Scope

The scope of the decision: **Architecture Organizer Template Project**.

## Type

The type of the decision: **Principles Declaration**.

## Status

Approved

## Context

With any project, it is important to establish a set of first principles that will guide the decision-making process.  These principles will help to ensure that the project is aligned with the goals and objectives of the organization and that the project is being executed in a manner that is consistent with the organization's values and culture.  First principles also help other contributors to understand the context and constraints of the project and to make decisions that are consistent with the project's goals and objectives.

The principles are listed in order of precedence, with the most important principles listed first.  Ordering them in this way helps resolve conflicts between principles when they arise.

The principles in this decision guide how this template was constructed and how it will be maintained in the future.

## Decision

The following principles will guide the development and maintenance of this template:

1. **Light-Weight and Simple**: The template focuses on requiring the minimum amount of design direction required to communicate the architecture to a specific target audience.  It is not to be considered comprehensive and it should not be mistaken for a full software design methodology.
2. **Targeted Audience**: The artifacts in the template are targeted for specific stakeholders and their placement in the organizer reflects the artifacts' intended audience.
3. **Methodology Agnostic**: The template is not tied to any specific software development methodology.  It is intended to be used with any methodology that the team is using.  There is not prescriptive guidance on notation or process.
4. **Maximum Flexibility**: The template is designed to be flexible.  It can be used as the documentation for a single repository implementing a single project or it can be used in a standalone repository to document a complex system of systems.  In addition, the artifacts are authored in Markdown so they can be read as plain text or rendered as HTML using a static site generator.  With a static site generator, the artifacts can be hosted by any service that can host static HTML (i.e. GitHub Pages, Azure Blob Storage, or AWS S3).

## Consequences

Any new features or versions of this template will adhere to these principles.  Any contribution to this template will be evaluated and reviewed for conformance to these principles and anything that does not conform will be rejected.  Any changes to the principles will require a new decision to be made.
