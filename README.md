# coffee-errors

Patches error stack to display correct line numbers. [CoffeeScript](http://coffeescript.org) has built in support for this, but it only works when the script is executed through the `coffee` command. If you are running mocha, node-dev, jasmine or any other method, the functionality isn't on.

This is a pretty much straight copy of the original source, except it doesn't compile the source maps until necessary therefore speeding up the initial bootup process.

The package reuses expects you to have `coffee-script` already installed in your project.

[![Dependency status](https://david-dm.org/alexgorbatchev/coffee-errors.png)](https://david-dm.org/alexgorbatchev/coffee-errors)
[![devDependency Status](https://david-dm.org/alexgorbatchev/coffee-errors/dev-status.png)](https://david-dm.org/alexgorbatchev/coffee-errors#info=devDependencies)
[![Build Status](https://secure.travis-ci.org/alexgorbatchev/coffee-errors.png?branch=master)](https://travis-ci.org/alexgorbatchev/coffee-errors)

[![NPM](https://nodei.co/npm/coffee-errors.png?downloads=true)](https://npmjs.org/package/coffee-errors)

## Support

Please help me spend more time developing and maintaining awesome modules like this by donating!

The absolute best thing to do is to sign up with [Gittip](http://gittip.com) if you haven't already and donate just $1 a week. That is roughly a cup of coffee per month. Also, please do donate to many other amazing open source projects!

[![Gittip](http://img.shields.io/gittip/alexgorbatchev.png)](https://www.gittip.com/alexgorbatchev/)
[![PayPayl donate button](http://img.shields.io/paypal/donate.png?color=yellow)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=PSDPM9268P8RW "Donate once-off to this project using Paypal")

## Installation

    npm install coffee-errors

## Using

To get this to work, you just need to require the module once per run-time, like so.

    require 'coffee-errors'

## Results

Whenever an error is thrown, all stack lines in `.coffee` files will be fixed to show correct line number. YES!

    Error: Hello error
      at Context.<anonymous> (/coffee-errors/test/coffee-errors.spec.coffee:9:17)
      at Test.Runnable.run (/coffee-errors/node_modules/mocha/lib/runnable.js:213:32)
      at Runner.runTest (/coffee-errors/node_modules/mocha/lib/runner.js:351:10)
      at /coffee-errors/node_modules/mocha/lib/runner.js:397:12
      at next (/coffee-errors/node_modules/mocha/lib/runner.js:277:14)
      at /coffee-errors/node_modules/mocha/lib/runner.js:286:7
      at next (/coffee-errors/node_modules/mocha/lib/runner.js:234:23)
      at Object._onImmediate (/coffee-errors/node_modules/mocha/lib/runner.js:254:5)
      at processImmediate [as _immediateCallback] (timers.js:317:15)

## Other modules

* [jade-compiler](https://github.com/alexgorbatchev/jade-compiler)
* [stylus-compiler](https://github.com/alexgorbatchev/stylus-compiler)
* [coffee-compiler](https://github.com/alexgorbatchev/coffee-compiler)
* [coffee-errors](https://github.com/alexgorbatchev/coffee-errors)
* [bubble-boy](https://github.com/alexgorbatchev/bubble-boy)
* [syntaxhighlighter](https://github.com/alexgorbatchev/syntaxhighlighter)

## License

The MIT License (MIT)

Copyright (c) 2013-2014 Alex Gorbatchev

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
