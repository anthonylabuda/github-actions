# github-actions

Collection of GitHub Actions for CI/CD

## Table of Contents

- [github-actions](#github-actions)
  - [Table of Contents](#table-of-contents)
  - [Directory Structure](#directory-structure)
  - [GitHub Action Components](#github-action-components)
    - [Workflows](#workflows)
  - [Packages](#packages)
    - [Dependencies](#dependencies)
    - [Development Dependencies](#development-dependencies)
  - [Scripts](#scripts)

## Directory Structure

For this project, the following directory structure is utilized:

```text
github-actions
├── .github/
│   └── workflows/
├── .husky/
│   └── commit-msg
├── node_modules/
├── .commitlintrc.json
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── LICENSE
├── package-lock.json
├── package.json
└── README.md
```

## GitHub Action Components

### Workflows

The following GitHub Action workflows are available to be called from other workflows:

| Type                   | Implementation | Description                                                         |
| ---------------------- | -------------- | ------------------------------------------------------------------- |
| Continuous Delivery    | Node.js        | Increments version, builds artifact, and uploads artifact to GitHub |
| Continuous Integration | Node.js        | Formatting, linting, and testing                                    |

## Packages

For this project, the following packages are utilized:

### Dependencies

| Package | Description | URL |
| ------- | ----------- | --- |
| n/a     | n/a         | n/a |

### Development Dependencies

| Package                           | Description                                    | URL                                                           |
| --------------------------------- | ---------------------------------------------- | ------------------------------------------------------------- |
| `@commitlint/cli`                 | CLI for linting commit messages                | https://www.npmjs.com/package/@commitlint/cli                 |
| `@commitlint/config-conventional` | Configuration for conventional commit messages | https://www.npmjs.com/package/@commitlint/config-conventional |
| `husky`                           | Git hook management                            | https://www.npmjs.com/package/husky                           |
| `rimraf`                          | Removing files and directories                 | https://www.npmjs.com/package/rimraf                          |
| `standard-version`                | Release flow management                        | https://www.npmjs.com/package/standard-version                |

## Scripts

For this project, the following scripts can be utilized:

| Script        | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| `prepare`     | Initializes Husky for git hooks                              |
| `refresh:npm` | Cleans and installs the project dependencies                 |
| `version`     | Increments version, generates CHANGELOG, and creates new tag |
