# Guidelines for Contribution

###### Last updated September 21, 2019

:::

##### All May Contribute

We would love for you to contribute to Cashmere and be part of the community making this project better! To get started, follow the [Getting Started guide](http://cashmere.healthcatalyst.net/guides/getting-started).

:::

:::

##### Setup Environment

1.  Install the latest version of `node` with at _least_ version 8.9.
2.  Fork the `@healthcatalyst/cashmere` repo.
3.  Clone your fork. Recommendation: name your git remotes `upstream` for `@healthcatalyst/cashmere`
4.  From the root of the project, run `npm install`
5.  Running `npm run build` will build the entire project.
6.  `npm start` will serve the default project which is `user-guide` (the documentation site)

:::

:::

##### Contributing to Cashmere

### While Developing

1.  You may need to run `npm run build` before you start, especially if it's your first time running Cashmere.
2.  Run `npm start`. This will fire up the user guide website, and rebuild/reload when changes are made to the user guide site or the Cashmere library.

### Pull Requests

Before you submit your pull request (PR), consider the following guidelines:

-   Search [GitHub](https://github.com/HealthCatalyst/Fabric.Cashmere/pulls) for an open or closed PR that relates to your submission. You don't want to duplicate effort.
-   Development happens on the `dev` branch and `master` is used to create a new release.
-   From the dev branch create a new branch. Here is a good [guide](https://gist.github.com/Chaser324/ce0505fbed06b947d962) if you're just getting started.
-   Verify all changes look and function properly in different browsers and at different resolutions.
-   Run the following commands:
    -   `npm run lint` should result in `All files pass linting`
    -   If there are problems with prettier linting rules, running `npm run prettier` can be helpful. This will automatically make needed formatting changes based on our prettier rules. For Windows users, runs best in bash.
    -   `npm run test:unit` should result in `All tests passing`
    -   `npm run build` should pass and build the library successfully.
-   New components and directives must be accompanied by:
    -   A component demonstrating the functionality; this component should be added to the demo app's routes.
    -   Unit tests demonstrating that it functions as intended.
-   A new component should adhere to the [Health Catalyst style](http://cashmere.healthcatalyst.net).
-   When creating a PR you must set the base branch to dev(master is for release only)

:::

:::

##### Commit Message Guidelines

We have very precise rules over how our git commit messages can be formatted. This leads to **more
readable messages** that are easy to follow when looking through the **project history**. But also,
we use the git commit messages to **generate the Cashmere change log** and **determine the next semver
version** of the package.

(To help with creating commit messages you should use `commitizen` by running `npm run cm` when you want to commit)

### Commit Message Format

Each commit message consists of a **header**, a **body** and a **footer**. The header has a special
format that includes a **type**, a **scope** and a **subject**:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

The **header** is mandatory and the **scope** of the header is optional.

Any line of the commit message cannot be longer than 100 characters! This makes the message easier
to read on GitHub as well as in various git tools.

### Revert

If the commit reverts a previous commit, it should begin with `revert:`, followed by the header of
the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the hash is
the SHA of the commit being reverted.

### Type

Must be one of the following:

-   **feat**: A new feature.
-   **fix**: A bug fix.
-   **docs**: Documentation only changes.
-   **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
-   **refactor**: A code change that neither fixes a bug nor adds a feature.
-   **perf**: A code change that improves performance.
-   **test**: Adding missing tests or correcting existing tests.
-   **build**: Changes that affect the build system, CI configuration or external dependencies
    (example scopes: gulp, broccoli, npm).
-   **chore**: Other changes that don't modify `src` or `test` files.

### Scope

The scope could be anything specifying the place of the commit change. For example
`button`, `dialog`, etc.

### Subject

The subject contains succinct description of the change:

-   use the imperative, present tense: "change" not "changed" nor "changes".
-   don't capitalize first letter.
-   no dot (.) at the end.

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the motivation for the change and contrast this with previous behavior.

### Footer

The footer should contain any information about **Breaking Changes** and is also the place to
reference GitHub issues that this commit **Closes**.

**Breaking Changes** should start with the word `BREAKING CHANGE:` with a space or two newlines.
The rest of the commit message is then used for this.

A detailed explanation can be found in this [document](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines).

:::
