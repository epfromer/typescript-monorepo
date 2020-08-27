# Lerna monorepo + yarn workspaces + typescript project references + tsc --build

## Features

- lerna monorepo
- yarn workspaces
- typescript project references for incremental build setup according to https://www.typescriptlang.org/docs/handbook/project-references.html

## Organization

There are two packages:

- common, which exports a sayHello() function returning a single string
- use-common, which references common to log sayHello() to the console

## Building

- `yarn build` uses tsc to build packages in proper order using references
- `yarn start` runs use-common to print sayHello() to console, incrementally compiling common if necessary

## Setting up this repo

```bash
yarn install
yarn build
yarn start
```
