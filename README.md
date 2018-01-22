# CW-ESLINT-CONFIG

`(ESLINT && PRETTIER) === "CODE QUALITY"`

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
   `npm install --save-dev babel-eslint prettier-eslint`

2. On Linux/OSX run

```sh
(
  export PKG=eslint-config-airbnb-base;
  npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"
)
```

3. Create `.eslintrc.json` file inside the project directory and paste the content accordingly below inside the file

For project using `es5` and below use content of `.eslintrc.json` from [api-eslint-es5/.eslintrc.json](api-eslint-es5/.eslintrc.json)

For `es6` enviroment and above use content of `.eslintrc.json` from [api-eslint/.eslintrc.json](api-eslint/.eslintrc.json)
