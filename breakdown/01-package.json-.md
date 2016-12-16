Starting off with package.json as it's the first file that actually looked
at upon running `npm install`.

```
All npm packages contain a file, usually in the project root, called package.json - this file holds various metadata relevant to the project. This file is used to give information to npm that allows it to identify the project as well as handle the project's dependencies.

https://docs.nodejitsu.com/articles/getting-started/npm/what-is-the-file-package-json

```
In English, this gives npm all the information it needs to install your package, down to all the dependencies.
When you run `npm install`, it checks this to see what engines, scripts, and node_modules are needed to run
your app.

{
  "name": "feathers-chat",
  "description": "First Feathers App",
  "version": "0.0.0",
  "homepage": "",
  "main": "src/",
  "keywords": [
    "feathers"
  ],
  "license": "MIT",
  "repository": {},
  "author": {},
  "contributors": [],
  "bugs": {},
  "engines": {
    "node": ">= 0.12.0"
  },
  "scripts": {
    "test": "npm run jshint && npm run mocha",
    "jshint": "jshint src/. test/. --config",
    "start": "node src/",
    "mocha": "mocha test/ --recursive"
  },
  "dependencies": {
    "body-parser": "^1.15.2",
    "compression": "^1.6.2",
    "cors": "^2.8.1",
    "feathers": "^2.0.3",
    "feathers-authentication": "^0.7.12",
    "feathers-configuration": "^0.3.3",
    "feathers-errors": "^2.5.0",
    "feathers-hooks": "^1.7.0",
    "feathers-nedb": "^2.6.0",
    "feathers-rest": "^1.5.2",
    "feathers-socketio": "^1.4.2",
    "nedb": "^1.8.0",
    "passport": "^0.3.2",
    "serve-favicon": "^2.3.2",
    "winston": "^2.3.0"
  },
  "devDependencies": {
    "jshint": "^2.9.4",
    "mocha": "^3.2.0",
    "request": "^2.79.0"
  }
}
