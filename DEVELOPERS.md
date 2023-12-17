# Developing Fast Resume

1. [Getting started](#getting-started)
   - [Install dependencies](#install-dependencies)
2. [Local development](#local-development)
   - [Fork the repo](#fork-the-repo)
   - [Clone the repo](#clone-the-repo)
   - [Running turborepo](#running-turborepo)
     - [Shared components](#shared-components)
     - [Installing packages](#installing-packages)


## Getting started

Thank you for your interest in [Fast Resume](https://fastresu.me) and your willingness to contribute!

To ensure a positive and inclusive environment, please read our [code of conduct](https://github.com/FastResu.me/.github/blob/main/CODE_OF_CONDUCT.md). We encourage you to explore the existing [issues](https://github.com/FastResume/FastResu.me/issues) to see how you can make a meaningful impact. This document will help you setup your development environment.

### Install dependencies

You will need to install and configure the following dependencies on your machine to build [Fast Resume](https://fastresu.me):

- [Git](http://git-scm.com/)
- [Node.js v20.x (LTS)](http://nodejs.org)
- [npm](https://www.npmjs.com/) version 9.x.x
- [Docker](https://docs.docker.com/get-docker/) (to run studio locally)

## Local development

This repo uses [Turborepo](https://turborepo.org/docs).

All of our apps are in this [Turborepo](https://turborepo.org/docs), which make it easy to share packages and config between projects.

### Fork the repo

To contribute code to [Fast Resume](https://fastresu.me), you must fork the [Fast Resume repo](https://github.com/FastResume/FastResu.me).

### Clone the repo

1. Clone your GitHub forked repo:

   ```sh
   git clone https://github.com/<github_username>/FastResu.me.git
   ```

2. Go to the Fast Resume directory:
   ```sh
   cd FastResu.me
   ```

### Install dependencies

1. Install the dependencies in the root of the repo.

   ```sh
   yarn install # install dependencies
   ```

2. After that you can run the apps simultaneously with the following.
   ```sh
   yarn  dev # start all the applications
   ```



#### Running sites individually

You can run any of the sites individually by using the scope name. For example:

```sh
npm run dev:web
```

#### Shared components

The monorepo has a set of shared components under `/packages`:

- `/packages/ui`: Common React components, shared between all sites.


#### Installing packages

Installing a package with Yarn workspaces requires you to add the `-w` flag to tell Yarn which workspace you want to install into. Do not install dependencies in their local folder, install them from the route using the `-w` flag.

The format is: `yarn add <package name> -w=<workspace to install in>`.

For example:

- `yarn add  react -w web`: installs into `./apps/web`
- `yarn add  react -w docs`: installs into `./apps/docs`

You do not need to install `devDependencies` in each workspace. These can all be installed in the root package.

---

