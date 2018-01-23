# CW-ESLINT-CONFIG

`(ESLINT && PRETTIER) === "Automatically Curing the formatting fatigue with the style guidelines"`

## API Development:

For API Development following enviroment is enabled in the config file

```JavaScript
{
"node": true,
"mocha": true,
"mongo": true
}
```

For other supported environment check `ESlint` [Specifying Environments](https://eslint.org/docs/user-guide/configuring#specifying-environments)

Configuration step for each individual projects.

1. Install the following plugin as dev-dependency
   `npm install --save-dev babel-eslint eslint-config-prettier prettier`

2. On Linux/OSX run

```sh
(
  export PKG=eslint-config-airbnb-base;
  npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"
)
```

3. Create `.eslintrc.json` file inside the project directory and paste the content accordingly below inside the file

For project using `es5` and below use content of `.eslintrc.json` from [api-eslint-es5/](api-eslint-es5/.eslintrc.json)

For `es6` enviroment and above use content of `.eslintrc.json` from [api-eslint/](api-eslint/.eslintrc.json)

4. Create `.prettierrc` file inside project directory and update the content with the content from file [.prettierrc](.prettierrc)

5. Add the below script inside the `package.json` file.

```json
"scripts": {
  "lint": "eslint '**/*.{js,}'",
  "format": "prettier --write '**/*.{js,}'"
},
```

After saving the changes run the script to format the code and see error and warning, for fix.

> `npm run format && npm run lint`

> Note: Editor like `vscode` and `atom` etc can be configured to lint and format the code automatically on save
