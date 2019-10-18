# TypeScript React App with AirBnB Linter rules
I found a lot if out of date info while trying to configure our TypeScript React app to use ESLint with AirBnB rules and Prettier. I'm creating this repo for future reference.

## Sample Create React App using Typescript
* `npx create-react-app <my-app-name> --typescript`

## Add ESLint for TypeScript and configure
see: https://github.com/typescript-eslint/typescript-eslint/issues/147
* `yarn add -D eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-react @typescript-eslint/parser @typescript-eslint/eslint-plugin`
* `eslint --init`
* use defaults, except I saved my .eslintrc as JSON

## Add Prettier, Prettier Config, Prettier Plugin
* `yarn add prettier --dev --exact`
* `yarn add --dev eslint-config-prettier`
* `yarn add --dev eslint-plugin-prettier`
* make updates to .eslintrc
see: https://prettier.io/docs/en/integrating-with-linters.html#eslint

## Tweak ESLint / Prettier Rules
* update .eslintrc
* add .prettierrc
Note: .prettierrc is a JSON file, but you cannot add .json extension or Prettier will ignore it (https://github.com/prettier/prettier-vscode/issues/734)

### I made 3 changes to the default rules:
* add .ts, .tsx files to contain JSX
* prefer single quotes
* optimize prettier for 100 char width

## TODO
Use npm instead of yard for app configuraion



-----

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
