# grunt-express-runner

> Simple express server runner

This task mimics running express by from the command line `node server.js` or `DEBUG=app* server.js`. It supports [debug](https://github.com/visionmedia/debug) environment variables to output debug statements. 

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-express-runner --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-express-runner');
```

## The "express_runner" task

### Overview

In your project's Gruntfile, add a section named `expressrunner` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  expressrunner: {
    options: {
      script: 'src/server.js',
      debug: 'app*'
    }
  },
});
```

### Options

#### options.script (Required)
Type: `String`

The path to the express server start-up file.

#### options.debug
Type: `String`

Environment variable value for use with the [debug](https://github.com/visionmedia/debug) module.

### Usage Examples

```js
grunt.initConfig({
  expressrunner: {
    options: {
      server: 'src/server.js',
      debug: 'server*'
    }
  },
});
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
0.1.0 Initial release
