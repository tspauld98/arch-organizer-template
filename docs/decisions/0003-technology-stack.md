# 3. Technology Stack

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

The type of the decision: **Technology/Approach Selection**.

## Status

Approved

## Context

Based on the [First Principles](/decisions/0002-first-principles.md) for this project, the implementation of this template needed to be light-weight and flexible. Markdown provides the most flexible and light-weight approach to authoring the artifacts in the organizer since Markdown-based artifacts can be co-located with code.  There are a number of Markdown rendering frameworks.  As part of the development of this template, the following frameworks were evaluated:

1. [MkDocs](https://www.mkdocs.org/)
2. [Jekyll](https://jekyllrb.com/)
3. [Docsify](https://docsify.js.org/)

The above frameworks provide the most compatibility with hosting on Github Pages.  While the template is designed to be hosted anywhere, Github Pages is the preferred hosting mechanism for this template.  The following frameworks were investigated but were not formally evaluated:

1. [Hugo](https://gohugo.io/)
2. [VuePress](https://vuepress.vuejs.org/)
3. [Docusaurus](https://docusaurus.io/)
4. [Gatsby](https://www.gatsbyjs.com/)
5. [Sphinx](https://www.sphinx-doc.org/en/master/)
6. [GitBook](https://www.gitbook.com/)

While `MkDocs` has many great features and a large community, it must run a build process to generate the static HTML.  Ideally, the template should be immediately renderable without a build process. `Jekyll`, similar to `MkDocs`, requires a build process to generate the static HTML, but at least, Github Pages support this process "out of the box".  The build process is still more complex to maintain and would create friction for anyone adopting this template.  In addition, the build process would make it more complex to host the documentation on infrastructure other than Github Pages.

`Docsify`, on the other hand, does not require a build process and can render the Markdown artifacts immediately.  It works by having a root `index.html` that loads the framework using `<script/>` tags. This makes `Docsify` easy to use locally, easy to deploy anywhere, and the best choice for this template.

## Decision

* This template will use [Docsify](https://docsify.js.org/) as the framework for rendering Markdown as static HTML.
* The following `Docsify` plugins are pre-installed and configured in the template:
  * [Docsify Accordion](https://github.com/isaozler/docsify-accordion)
  * [Docsify Copy Code](https://github.com/jperasmus/docsify-copy-code)
  * [Docsify Mermaid](https://github.com/Leward/mermaid-docsify)
  * [Docsify Mermaid Zoom](https://github.com/corentinleberre/docsify-mermaid-zoom)
  * [Docsify Pagination](https://github.com/imyelo/docsify-pagination)
  * [Docsify PlantUML](https://github.com/imyelo/docsify-plantuml)
  * [Docsify Sidebar Collapse](https://github.com/iPeng6/docsify-sidebar-collapse)
  * [Docsify Sidebar Footer](https://footer.docsify.markbattistella.com/#/)
  * [Docsify Tabs](https://jhildenbiddle.github.io/docsify-tabs/#/)
  * [Docsify Themeable](https://jhildenbiddle.github.io/docsify-themeable/#/)
* All of the template's dependencies, include the above plugins and their dependencies, are pinned to specific versions and distributed locally as part of the template in the `docs/_vendors` directory.

## Consequences

While using `Docsify` with a pinned set of versioned dependencies makes this template extremely flexible and portable, it does make the upgrade process manual. The template will need to be updated to include the latest versions of the dependencies and the template will need to be re-distributed.  This is a trade-off that is acceptable given that `Github` and `git` provide great tools for merging upstream changes to local versions.  The template will be updated to include the latest versions of the dependencies on a regular basis with instructions on adopting the new versions.  The template will also be updated to include the latest versions of the dependencies when a new version of the template is released.
