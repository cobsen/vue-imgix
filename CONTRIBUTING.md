# Contributing

Contributions are a vital part of this library and imgix's commitment to open-source. We welcome all contributions which align with this project's goals. All we ask is that you please take a moment to review this document in order to make the contribution process easy and effective for everyone involved.

Following these guidelines helps to communicate that you respect the time of
the developers managing and developing this open source project. In return,
they should reciprocate that respect in addressing your issue or assessing
patches and features.

<!-- NB: Run `npx markdown-toc CONTRIBUTING.md` to generate TOC :) -->

<!-- prettier-ignore-start -->

- [Contributing](#contributing)
  * [Project Goals](#project-goals)
  * [Using the issue tracker](#using-the-issue-tracker)
  * [Development](#development)
  * [Code Conventions](#code-conventions)
    + [Project setup](#project-setup)
    + [Compiles and hot-reloads for development](#compiles-and-hot-reloads-for-development)
    + [Compiles and minifies for production](#compiles-and-minifies-for-production)
    + [Run your unit tests](#run-your-unit-tests)
    + [Run your end-to-end tests](#run-your-end-to-end-tests)
    + [Lints and fixes files](#lints-and-fixes-files)
    + [Customize configuration](#customize-configuration)


<!-- prettier-ignore-end -->

## Project Goals

- Provide a simple, easy-to-understand API that users can use to get started in **the shortest time possible**. This API should cover a large amount (~80%) of use cases of a normal img element without making the API surface too large or complicated.
- Provide a separate, powerful, low-level API that gets out of the way to allow developers to use the imgix API in Vue how they like.
- The code should be well-tested and of high quality.
- The public API should be handled with care because a) once an API is submitted, we are committed to supporting it for a reasonable amount of time, and b) any changes to the API creates exponentially more work for the users of our libraries.

## Using the issue tracker

The issue tracker is the preferred channel for [bug reports](#bugs),
[features requests](#features), questions, and [submitting pull
requests](#pull-requests), but please respect the following restrictions:

- Please **do not** derail or troll issues. Keep the discussion on topic and
  respect the opinions of others.

## Development

The development of this library follows [this very useful guide about Outside-In Frontend Development in Vue](https://outsidein.dev/exercise-intro.html). I highly recommend at least becoming familiar with some of the core concepts of Outside-In TDD.

## Publishing

Semantic-release will auto-publish anything that is merged into the `next` branch to npm under the `next` dist-tag. Users can install this version by running `npm install vue-imgix@next`. To facilitate this, every commit must follow the [conventional commit specification](https://www.conventionalcommits.org/en/v1.0.0-beta.2/).

The current process to publish the master dist-tag from the master branch:

1. Merge the latest changes from `next`
1. Run `yarn` to install the latest deps
1. Bump the package version in package.json and vue-imgix.ts by a patch version. This is important because if we release with the same version as what's on the next branch, it won't work.
1. `npm publish`

## Code Conventions

1.  Make all changes to files under `./src`, **not** `./dist` or `./es`.
2.  Use [Prettier](https://prettier.io/) for code formatting. Code will automatically be formatted upon submitting a PR.

## Project setup

```
yarn install
```

## Compiles and hot-reloads for development

```
yarn serve
```

## Compiles and minifies for production

```
yarn build
```

## Run your unit tests

```
yarn test:unit
```

## Run your end-to-end tests

```
yarn test:e2e
```

## Lints and fixes files

```
yarn lint
```

## Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
