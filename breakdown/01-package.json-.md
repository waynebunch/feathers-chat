#_package.json#

I started off with package.json because I believe it would be the first file touched after the
cloning of https://github.com/waynebunch/feathers-chat.git.  When `npm install` is ran, npm looks
through `package.json` to get all the app information needed to install and run my app.  This would
be the case for any program available through npm.  It takes that information and reaches out to 
npmjs.com and installs the dependencies.  Damn straight.

```
All npm packages contain a file, usually in the project root, called package.json - this file holds 
various metadata relevant to the project. This file is used to give information to npm that allows
it to identify the project as well as handle the project's dependencies.

https://docs.nodejitsu.com/articles/getting-started/npm/what-is-the-file-package-json

```
```
{
  "name": "feathers-chat",

```
Name is important and required.  Should be lowercase.   This will indentify your project and how 
else are they going to find your app on npmjs.com, should you choose to publish it?  

```
  "description": "First Feathers App",
  "version": "0.0.0",
```
Standard versioning here.  MAJOR.MINOR.PATCH (0.0.0) whereas major is any API incompatibility 
issues, minor being added functionality with backward compatibility, patch being bug fixes.

```
  "homepage": "",
  "main": "src/",
```
 `main` tells npm where to find the main app.  In this app, if the developer does a 
 `require(app)` it will return your main modules exports. More on this in breakdown of
 /feathers-chat/src/app.js.  ###ADD REF
```
  "keywords": [
    "feathers"
  ],
  "license": "MIT",
```
 Choose your license.  Best way to read about this if it's new is:
 choosealicense.com.  This tells other dev's how they can use your code.   Just choose MIT...

```
  "repository": {
    "type": "git",
    "url" : "https://github.com/waynebunch/feathers-chat.git"
  },
  "author": {},
  "contributors": [],
  "bugs": {},
  "engines": {
    "node": ">= 0.12.0"
```
 `node` tells user what node version they must have installed to run the app.  Very important
as features have changed drastically over time.

```
  },
  "scripts": {
```

Scripts are seperate options that can be run with npm.  This object key is the npm command and 
the value is the script path.  This comes in very handy when the dev has other cli options.
`npm run {command}`
`npm run start`
`npm run jslint` etc..
```
    "test": "npm run jshint && npm run mocha",
    "jshint": "jshint src/. test/. --config",
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
```
`body-parser` brings us to an important part of Express and Node.  

```
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
