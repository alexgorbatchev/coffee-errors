# coffee-errors

Patches error stack to display correct line numbers.

## Usage

    require 'coffee-errors'

## Results

    Error: Hello error
      at Context.<anonymous> (/coffee-errors/test/coffee-errors.spec.coffee:9:17, <js>:14:15)
      at Test.Runnable.run (/coffee-errors/node_modules/mocha/lib/runnable.js:213:32)
      at Runner.runTest (/coffee-errors/node_modules/mocha/lib/runner.js:351:10)
      at /coffee-errors/node_modules/mocha/lib/runner.js:397:12
      at next (/coffee-errors/node_modules/mocha/lib/runner.js:277:14)
      at /coffee-errors/node_modules/mocha/lib/runner.js:286:7
      at next (/coffee-errors/node_modules/mocha/lib/runner.js:234:23)
      at Object._onImmediate (/coffee-errors/node_modules/mocha/lib/runner.js:254:5)
      at processImmediate [as _immediateCallback] (timers.js:317:15)