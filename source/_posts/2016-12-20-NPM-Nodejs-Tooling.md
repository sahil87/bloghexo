---
title: NPM Nodejs Tooling
author: Sahil Ahuja
categories: blog
date: 2016-12-20 01:48:40
tags: node, tools, es6
---
An opinionated list of great tools for NodeJS Tooling:

* Compilers
  * [Babel](https://babeljs.io/)
  * [Webpack](https://webpack.github.io/), [Webpack2](https://webpack.js.org/) - Webpack is also does all of the below
  
* Module bundlers
  * [Browserify](http://browserify.org/), works well with [npm](https://www.npmjs.com/) packages
  * [RequireJS](http://requirejs.org/), works well with [bower](https://bower.io/) packages
  * [jspm](http://jspm.io/)
  
* Task Runners
  * [Gulp 4.0](https://github.com/gulpjs/gulp/tree/4.0)

* Process Monitors
  * [Nodemon](https://github.com/remy/nodemon/)
  * [Supervisor](https://github.com/Supervisor/supervisor)
  * [PM2](https://github.com/Unitech/pm2)
  * [Forever](https://github.com/foreverjs/forever)

* Watch mode live reload tools
  * [Browsersync](https://github.com/Browsersync/browser-sync)
  * [livereload](http://livereload.com/)
  * [watchify](https://github.com/substack/watchify) watch mode for browserify builds

Refernces
--
* http://jamesknelson.com/which-build-system-should-i-use-for-my-javascript-app/
* https://www.leanpanda.com/blog/2015/06/28/amd-requirejs-commonjs-browserify/
