npm-typeahead
=============

[![Build Status](https://travis-ci.org/bcoe/npm-typeahead.png)](https://travis-ci.org/bcoe/npm-typeahead)

A lightweight web-app that implements typeahead search functionality for [npm packages](http://www.npmjs.org).

Try it out here: http://npm-typeahead.herokuapp.com

The Motivation
-------

*npm-typeahead* was put together as part of an article for [CODE Magazine](http://www.codemag.com/magazine). It's an attempt to demonstrate Node.js best practices, and covers:

* using [node-restify](https://github.com/mcavage/node-restify), to get a bare-bones server up and running.
* using [browserify](https://github.com/substack/node-browserify), to install client-side dependencies using npm (such as [typeahead.js](https://github.com/twitter/typeahead.js))
* using [mocha](https://github.com/visionmedia/mocha), to wrie unit tests.

Usage
-----
* **npm test:** run the mocha unit tests.
* **npm start:** run the web-server.
* **npm run-script build:** build the client-side dependencies.

Integration With Browserify
---------------------

_npm-typeahead_ exposes client-side bindings, so that it can be used in other sites, e.g., npm-www.

* use `npm install npm-typeahead --save` to add the npm-typeahead dependency.
* add the following snippet of code to your project,

```javascript
require('npm-typeahead')({
  npmUrl: 'https://www.nmjs.org',// URL to re-direct the user to.
  searchUrl: '', // URL for search npm-typeahead REST server.
  $: $ // jQuery dependency.
});
```
