# ui-event [![Build Status](https://travis-ci.org/angular-ui/ui-event.svg?branch=master)](https://travis-ci.org/angular-ui/ui-event) [![npm version](https://badge.fury.io/js/angular-ui-event.svg)](http://badge.fury.io/js/angular-ui-event) [![Bower version](https://badge.fury.io/bo/angular-ui-event.svg)](http://badge.fury.io/bo/angular-ui-event) [![Join the chat at https://gitter.im/angular-ui/ui-event](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/angular-ui/ui-event?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Bind a callback to any event not natively supported by Angular. For Blurs, Focus, Double-Clicks or any other event you may choose that isn't built-in.

## Requirements

- AngularJS

## Usage


You can get it from [Bower](http://bower.io/)

```sh
bower install angular-ui-event
```

Load the script files in your application:

```html
<script type="text/javascript" src="bower_components/angular/angular.js"></script>
<script type="text/javascript" src="bower_components/angular-ui-event/dist/event.js"></script>
```

Add the specific module to your dependencies:

```javascript
angular.module('myApp', ['ui.event', ...])
```

## Development

We use Karma and jshint to ensure the quality of the code.  The easiest way to run these checks is to use grunt:

```sh
npm install -g gulp-cli
npm install && bower install
gulp
```

The karma task will try to open Firefox and Chrome as browser in which to run the tests.  Make sure this is available or change the configuration in `karma.conf.js`


### Gulp watch

`gulp watch` will automatically test your code and build a release whenever source files change.

### How to release

Use gulp to bump version, build and create a tag. Then push to GitHub:

````sh
gulp release [--patch|--minor|--major]
git push --tags origin master # push everything to GitHub
````

Travis will take care of testing and publishing to npm's registry (bower will pick up the change automatically). Finally [create a release on GitHub](https://github.com/angular-ui/ui-event/releases/new) from the tag created by Travis.
