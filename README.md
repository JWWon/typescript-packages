# Typescript Packagess

## How to contribute

1. Create branch after your issue number `<issue_number>-<branch_name>`

2. Install all dependencies you need

3. Update `Package List` on README.md

4. Create merge request to `master` branch

5. Project manager will review your updates and merge it

## How to use

> Reference: <https://classic.yarnpkg.com/blog/2016/11/24/offline-mirror/>, <https://musma.github.io/2019/08/23/nodejs-offline-deployment.html>

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

2. Move `build/`, `package.json`, `yarn.lock`, `npm_packages/`, and other setting files to your deploy environment

3. Type `yarn install --offline`
