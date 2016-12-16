Starting off with package.json as it's the first file that actually looked
at upon running `npm install`.

```
All npm packages contain a file, usually in the project root, called package.json - this file holds 
various metadata relevant to the project. This file is used to give information to npm that allows
it to identify the project as well as handle the project's dependencies.

https://docs.nodejitsu.com/articles/getting-started/npm/what-is-the-file-package-json

```
This gives npm all the information it needs to install your package, down to all the 
dependencies.  When you run `npm install`, it checks this to see what engines, scripts, and 
node_modules are needed to run your app.  Easy peesy.

```
{
  "name": "feathers-chat",
```
Name is important.  

```
  "description": "First Feathers App",
  "version": "0.0.0",
  "homepage": "",
  "main": "src/",
```
 `main` tells npm where to find the main app.  In this app, if the developer does a 
 `require(app)` it will return your main modules exports. More on this in breakdown of
 src/app.js
```
  "keywords": [
    "feathers"
  ],
  "license": "MIT",
```
 Choose your license.  Best way to read about this if it's new is:
 choosealicense.com.  Just choose MIT...
```
  "repository": {},
  "author": {},
  "contributors": [],
  "bugs": {},
  "engines": {
    "node": ">= 0.12.0"
```
 This tells user what node they must have installed.  Very important as features have changed
 drastically over time.
```
  },
  "scripts": {
    "test": "npm run jshint && npm run mocha",
```
 `npm test` will run the above.  If you're unfamiliar with testing, get familiar.
 https://mochajs.org/
 jshint.com
 This will be vital for any situation in a real developing situation, or just for fun projects.
```
    "jshint": "jshint src/. test/. --config",
```
 Tells npm where to find config for jshint
```
    "start": "node src/",
```
 When `npm start` is ran, npm looks here to know where to find your main app to run.  In this
 example, `npm start` looks in `src` and runs `index.js` %%% need to find out why it uses 
 index.js and not app.js
```
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
```
 ##Very Important.  This is all the dependencies (deps from now on) that are a must to run this.
 Need to pay very close attention to this if you're going to be doing your own or modifying an app.
 Example:  
    "body-parser": "^1.15.2",
    "body-parser": "~1.15.2",
 Two very big points here:
	1. The ^ will match all 1.15.X versions of `body-parser`.    
	2. The ~ is more relaxed.  It will match all minor versions 1.X.X of `body-parser`.   
 This could be a big difference in functionality and could crash your app.  
```
  },
  "devDependencies": {
    "jshint": "^2.9.4",
    "mocha": "^3.2.0",
    "request": "^2.79.0"
```
 This is a list of modules that were used when the dev was creating app.  Would be needed to 
 correctly modify this app the way it is.  Same as deps above
```
  }
}
```
