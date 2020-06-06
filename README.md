# npm-hello-world-consumer
Consuming the [@jlam55555-playground/npm-hello-world][1] GitHub NPM registry package

### Creating a Node.JS app

##### Creating package.json
Create a new directory for your project, and navigate into it. Make sure you have `npm` installed. run `npm init` to generate a `package.json` configuration file for your NPM module.
```shell script
$ mkdir npm-hello-world-consumer
$ cd npm-hello-world-consumer
$ npm init
```

### Installing a GitHub NPM registry package to your project
Create a file `.npmrc` in your project directory, and add the line:
```text
registry=https://npm.pkg.github.com/OWNER
```
where `OWNER` is the name of the GitHub user or organization that owns the rpository of the package. (In this case, `OWNER` is `jlam55555-playground`.) Now you can install NPM packages from that registry like normal:
```shell script
$ npm i @jlam55555-playground/npm-hello-world
```
and consume it as usual. The simple module in `@jlam55555-playground/npm-hello-world` exports a simple function, and we can import it in the usual Node fashion:
```javascript
const helloWorldModule = require('@jlam55555-playground/npm-hello-world');

helloWorldModule();
```

[1]: https://www.github.com/jlam55555-playground/npm-hello-world
