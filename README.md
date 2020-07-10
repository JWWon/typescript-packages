# Typescript Packagess

## How to use

> Reference: https://musma.github.io/2019/08/23/nodejs-offline-deployment.html

Before you download packages on offline,

You need to use latest `yarn` package manager.

Because, `npm` does not support offline package download.

To use `yarn`, you can use auto installer or `node ./yarn-1.22.4.js <command>`.

1. Move `npm_packages/` to your project

2. Create `.yarnrc` on your root directory

3. Copy & Paste to `.yarnrc`

   ```bash
   yarn-offline-mirror "./npm_packages"
   yarn-offline-mirror-pruning true
   ```

4. To download package, type `yarn install --offline`

### How to deploy

1. If you need to "build" project, install packages once more by typing `yarn install --offline --production`

   > By use `--production` flag, it automatically download packages only notify on `package.json` and uninstall all unused packages.

2. Move `dist/`, `package.json`, `npm_packages/`, and other setting files to your deploy environment

3. Type `yarn install --offline --production`

## Package List

### UI Library

1. [Blueprint](https://blueprintjs.com/docs/)
2. [Material-UI](https://material-ui.com/getting-started/installation/)
3. [AntDesign](https://ant.design/docs/react/introduce)

### Network Client

1. [axios](https://github.com/axios/axios)
2. [socket.io](https://socket.io/docs/)

### React

1. [react](https://ko.reactjs.org/docs/getting-started.html)
2. [redux](https://redux.js.org/introduction/getting-started)
3. [redux-saga](https://redux-saga.js.org/)
4. [redux-thunk](https://github.com/reduxjs/redux-thunk)

### React Helper

1. [immer](https://immerjs.github.io/immer/docs/introduction)
2. [react-dnd](https://react-dnd.github.io/react-dnd/about)
3. [react-hook-form](https://react-hook-form.com/get-started)
4. [react-lazylog](https://github.com/mozilla-frontend-infra/react-lazylog)
5. [react-mosaic](https://github.com/nomcopter/react-mosaic)
6. [styled-components](https://styled-components.com/)
7. [typesafe-actions](https://github.com/piotrwitek/typesafe-actions)

### React Test

1. [storybook](https://storybook.js.org/docs/guides/guide-react/)
2. [jest](https://jestjs.io/docs/en/getting-started)

### Compiler

1. [Babel](https://babeljs.io/docs/en/index.html)

### Typescript

1. [ts-jest](https://kulshekhar.github.io/ts-jest/user/install)
2. [tslint](https://palantir.github.io/tslint/)
3. [Typescript](https://www.typescriptlang.org/docs/home.html)
