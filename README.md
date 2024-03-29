# construx-browserify

Lead Maintainer: [Matt Edelman](https://github.com/grawk)

[![Build Status](https://travis-ci.org/krakenjs/construx-browserify.svg?branch=master)](https://travis-ci.org/krakenjs/construx-browserify)
[![NPM version](https://badge.fury.io/js/construx-browserify.png)](http://badge.fury.io/js/construx-browserify)

[construx](https://github.com/krakenjs/construx) plugin for JIT-compiling browserify resources during development of [express](http://expressjs.com/) applications.

## REMOVE THIS SECTION

This repository is meant as a template for `construx` plugins. If you wish to use it:
* create a repository named `construx-<wrapped compiler>`
* use the github import feature to pull in this repository
* If you aren't a PayPal employee, remove the PayPal license text in the source code
* author your plugin functionality into `index.js`

If you want the krakenjs team to promote your plugin:
* edit this `README` to reflect your plugin's requirements, configuration, and purpose
* write unit tests which sufficiently exercise the most likely encountered use cases
* publish your plugin to npm
* Inform us by filing an issue [here](https://github.com/krakenjs/construx/issues), to add your plugin to the list of `construx` plugins
* The team will process your request as quickly as possible

## Requirements

This plugin requires your project to have `<whatever module>@<whatever semver>`.

## Usage

### Install

```shell
$ npm install --save-dev construx-browserify
```

### Configure

Where you configure your construx plugins:

```json
{
    "browserify": {
        "module": "construx-browserify",
        "files": "**/*.js",
        "bundles": {
            "/bundle.js": {
                "src": "path:./public/main.js",
                "options": {
                    "transform": ["reactify", "require-globify"]
                }
            }
        }
    }
}
```

_Note: See [construx README](https://github.com/krakenjs/construx/blob/master/README.md) for general usage of construx_

