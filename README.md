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

    # frameworks to use
    frameworks: ['mocha', 'chai']

    # ...
```


Usage
-----

Each of the different Chai assertion suites is available in the tests:

```coffee
describe 'karma tests with chai', ->

  it 'should expose the Chai assert method', ->
    assert.ok('everything', 'everything is ok');

  it 'should expose the Chai expect method', ->
    expect('foo').to.not.equal 'bar'

  it 'should expose the Chai should property', ->
    1.should.not.equal 2
    should.exist 123
```