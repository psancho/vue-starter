# vue-starter

vueJs starter kit, is my new webapp starter: initialy I was on the React road, but VueJs took its place...


[![Dependency Status](https://david-dm.org/psancho/vue-starter/status.svg)](https://david-dm.org/psancho/vue-starter#info=dependencies) [![devDependency Status](https://david-dm.org/psancho/vue-starter/dev-status.svg)](https://david-dm.org/psancho/vue-starter#info=devDependencies)

Here is a more complete [description](./description.md).

## Main features

* Babel
* VueJS
* Webpack
* ESLint
* config file injection
* very light custom logger

## Quick start

```bash
# Clone this repo
git clone https://github.com/psancho/vue-starter.git vue-starter

# change directory to your app
cd vue-starter

# install the dependencies with npm
npm i

# start the server
npm start
```

Go to http://localhost:8080 in your browser.

Note you can change the port (see [devServe.port](https://webpack.js.org/configuration/dev-server/#devserverport) doc) in 3 ways:

* in the `scripts` section of the `package.json`

  ```json
  "start": "cross-env NODE_ENV=development webpack-dev-server --hot --port 9000"
  ```

* in `webpack.config.js`

  ```javascript
  module.exports = {
      //...
      devServer: {
          port: 9000
      }
  };
  
  ```
* directly in the CLI:

  ```bash
  npm start --port=9000
  ```

## Building the app

Just launch the following:

```bash
npm run build
```

By default, it uses the `config/production.js` file.
To use an alternate configuration, launch the following:

```bash
npm run build myServerConfig
```

## License

[MIT](./LICENCE)

## Logger

see comments in [src/services/consoleLogger.service.js](./src/services/consoleLogger.service.js)
