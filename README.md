# Architecture Organizer Template

This project is a template for creating and documenting the architecture of a system built with software.  This template is based on the [Basic Docsify Github Template](https://github.com/tspauld98/basic-docsify-gh-template) and is designed to be used as a starting point for creating an architecture for a software project, an online service, or an entire platform.  Just like the Basic Docsify Github Template, this template is designed to be used as a standalone documentation repository or as a documentation site that is part of a larger project and is intended to be hosted on Github Pages.  You can find out more about the Basic Docsify Github Template by visiting the [Basic Docsify Github Template](https://github.com/tspauld98/basic-docsify-gh-template) repository.

## Getting Started

There are two methods for utilizing this repository as a template for your own documentation site. The first method is to use the Github template feature. This will create a new repository in your account that is a copy of this repository. This method is very convenient and well-suited for a standalone documentation repository. Most architectures span multiple components from multiple repositories, so this method should be used for any project bigger than a single component.

The second method is to add this repository as a remote to your existing repository. This will allow you to pull in changes from this repository to a branch in your repository. This method allows you to keep your documentation in the same repository as your code. This method is well-suited for a documentation site that is part of a larger project. Use this method if your architecture is small enough to fit in a single repository.

### Template Adoption Method

Use this method if you are creating a new standalone documentation repository.

1. Click the "Use this template" button at the top of the repository page.
2. Enter a name for your new repository.
3. Click the "Create repository from template" button.

Once created, you can clone your new repository and start editing the markdown files in the `docs` folder. You can also customize the site by editing the `index.html` file.

### Merge Adoption Method

Use this method if you want to add a documentation site to an existing repository.

1. Add this repository as a remote to your existing repository using the following command:

```bash
git remote add upstream-template git@github.com:tspauld98/basic-docsify-gh-template.git
```

2. Fetch the contents of the remote repository using the following command:

```bash
git fetch upstream-template
```

3. Create a branch to hold the contents of the remote repository using the following command:

```bash
git checkout -b upstream-template-main --track upstream-template/main
```

4. Switch back to the `main` branch using the following command:

```bash
git checkout main
```

5. Merge the contents of the `docs` directory from the remote repository into your existing repository's `main` branch using the following command:

```bash
git checkout upstream-template-main -- docs
```

6. Commit the changes to your repository using the following command:

```bash
git commit -am "Add docs folder from upstream-template"
```

**Note:** You may need to resolve conflicts before you can commit the changes to the `main` branch.

Once you have the contents from the template repository in your existing repository, you can start editing the markdown files in the `docs` folder. You can also customize the site by editing the `index.html` file to make the site your own.

## Developing Your Documentation

TODO: Modify the following section to match your project.

### Prerequisites

Make sure the following software is installed on your system:

- [Node.js](https://nodejs.org/en/)
- [npm](https://www.npmjs.com/)
- [Docsify CLI](https://docsify.js.org/#/quickstart?id=quick-start)

### Development Process

This process assumes you have the prerequisites installed on your system and that you have used one of the methods above to create your documentation repository.  It also assumes that you have cloned the repository to your local system.

1. Make changes to the markdown files in the `docs` folder.  Mermaid and PlantUML are integrated with Docsify, so you can use them to create diagrams and illustrations in your documentation to support the text content.
2. If you add or remove markdown files, you will need to update the `_sidebar.md` file to add or remove links to the files.
3. Commit the changes to the local repository.
4. Run the following command to serve the documentation site locally:

```bash
docsify serve docs
```

5. Open a browser and navigate to `http://localhost:3000` to view the documentation site.
6. Repeat steps 1-4 until you are satisfied with the changes to the documentation site.
7. Push the changes to the remote repository on Github.

When you push the changes to the remote repository, Github will automatically deploy the documentation site to Github Pages if you have configured Github Pages for your repository. You can view the deployed site by navigating to `https://<your-github-username>.github.io/<your-repository-name>` once the Github deployment process has completed.

## Deploying Your Documentation Site on Github Pages

Once you have a version of the `docs` folder in your repository on Github, you can configure the repository to deploy the documentation site on Github Pages.  To do this, follow these steps:

1. Navigate to the repository on Github.
2. Click the "Settings" tab on the repository page.
3. Click on the "Pages" menu item in the left navigation bar.
4. Select the `main` branch from the first dropdown list.
5. Select the `/docs` folder from the second dropdown list.
6. Click the "Save" button.

At this point, it will take a few minutes for Github to deploy the documentation site.  Once the deployment process has completed, you can view the deployed site by navigating to `https://<your-github-username>.github.io/<your-repository-name>`.

## Dependencies and Plugins

The following dependencies and plugins are currently configured and included in this repository:

### Dependencies

- [node](https://nodejs.org/en/)
- [npm](https://www.npmjs.com/)
- [docsify-cli v4.4.4](https://cli.docsifyjs.org/#/)
- [docsify v4.13.1](https://docsify.js.org/#/)

### Plugins

- [docsify-accordion v0.0.3](https://www.npmjs.com/package/docsify-accordion)
- [docsify-copy-code v3.0.0](https://www.npmjs.com/package/docsify-copy-code)
- [docsify-mermaid v2.0.1](https://www.npmjs.com/package/docsify-mermaid)
  - [mermaid v10.6.1](https://mermaid.js.org/intro/)
- [docsify-mermaid-zoom v3.0.0](https://www.npmjs.com/package/docsify-mermaid-zoom)
  - [d3 v7.8.5](https://d3js.org/)
- [docsify-pagination v2.10.1](https://www.npmjs.com/package/docsify-pagination)
- [docsify-plantuml v1.3.2](https://www.npmjs.com/package/docsify-plantuml)
- [docsify-sidebarfooter v5.0.6](https://www.npmjs.com/package/@markbattistella/docsify-sidebarfooter)
- [docsify-tabs v1.6.0](https://www.npmjs.com/package/docsify-tabs)
- [docsify-themeable v0.9.0](https://www.npmjs.com/package/docsify-themeable)
- [gitalk v1.8.0](https://www.npmjs.com/package/gitalk)

## Future Enhancements

- [x] ~~Add a LICENSE file~~
- [x] ~~Add a robot.txt file~~
- [ ] Add a CONTRIBUTING file
- [ ] Add a CODE_OF_CONDUCT file
- [ ] Add a SECURITY file
- [ ] Add a CHANGELOG file
- [ ] Set up a .github folder
