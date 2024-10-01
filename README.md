# React + TypeScript + Vite

## Install Prettier

https://prettier.io/docs/en/install.html

First, install Prettier locally:
yarn add --dev --exact prettier

Then, create an empty config file to let editors and other tools know you are using Prettier:

node --eval "fs.writeFileSync('.prettierrc','{}\n')"

Next, create a .prettierignore file to let the Prettier CLI and editors know which files to not format. Here’s an example:

node --eval "fs.writeFileSync('.prettierignore','# Ignore artifacts:\nbuild\ncoverage\n')"

Now, format all files with Prettier:

yarn prettier . --write

npx prettier . --check

## ESLint (and other linters)

https://github.com/prettier/eslint-config-prettier#installation

## Git hooks

Install husky and lint-staged:

yarn add --dev husky lint-staged
npx husky init
node --eval "fs.writeFileSync('.husky/pre-commit','npx lint-staged\n')"

Add the following to your package.json:

Note: If you use ESLint, make sure lint-staged runs it before Prettier, not after.
