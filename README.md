karma-chai
==========

[Chai](http://chaijs.com) for [Karma](http://karma-runner.github.io)


Requirements
------------

This module currently requires the `canary` version of Karma:

```sh
$ npm install 'karma@canary' --save-dev
```

Note that the Karma configuration file format has changed since `v0.8`. Use 
`karma init` to generate a fresh config.


Installation
------------

Install the module from Github:

```sh
$ npm install 'git+https://github.com/xdissent/karma-chai.git' --save-dev
```

Add `chai` to the `frameworks` key in your Karma configuration:

```coffee
module.exports = (karma) ->
  karma.configure

    # base path, that will be used to resolve files and exclude
    basePath: ''

    # frameworks to use
    frameworks: ['mocha', 'chai']

    # ...
```
