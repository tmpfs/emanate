Table of Contents
=================

* [Emanate](#emanate)
  * [Install](#install)
  * [EventEmitter](#eventemitter)
    * [Methods](#methods)
      * [emitter.addListener(event, listener)](#emitteraddlistenerevent-listener)
      * [emitter.removeListener(event, listener)](#emitterremovelistenerevent-listener)
      * [emitter.once(event, listener)](#emitteronceevent-listener)
      * [emitter.removeAllListeners([event])](#emitterremovealllistenersevent)
      * [emitter.listeners(event)](#emitterlistenersevent)
      * [emitter.emit(event, [arg1], [arg2], [...])](#emitteremitevent-arg1-arg2-)
  * [Developer](#developer)
    * [Test](#test)
    * [Start](#start)
    * [Cover](#cover)
    * [Lint](#lint)
    * [Clean](#clean)
    * [Spec](#spec)
    * [Instrument](#instrument)
    * [Readme](#readme)
  * [License](#license)

Emanate
=======

> `Stability: stable`.

Event emitter for the browser.

## Install

```
npm i emanate --save
```

## EventEmitter

The event emitter class is the base class that provides event dispatching. It is designed to mimic the [node event emitter](http://nodejs.org/api/events.html#events_class_events_eventemitter).

### Methods

#### emitter.addListener(event, listener)

Adds a listener to the end of the listeners array for the specified event.

Returns emitter, so calls can be chained.

Aliased via the `on` method.

#### emitter.removeListener(event, listener)

Remove a listener from the listener array for the specified event. Caution: changes array indices in the listener array behind the listener.

Returns emitter, so calls can be chained.

Aliased via the `off` method.

#### emitter.once(event, listener)

Adds a one time listener for the event. This listener is invoked only the next time the event is fired, after which it is removed.

Returns emitter, so calls can be chained.

#### emitter.removeAllListeners([event])

Removes all listeners, or those of the specified event.

Returns emitter, so calls can be chained.

#### emitter.listeners(event)

Returns an array of listeners for the specified event.

#### emitter.emit(event, [arg1], [arg2], [...])

Execute each of the listeners in order with the supplied arguments.

Returns true if event had listeners, false otherwise.

## Developer

Developer workflow is via [gulp](http://gulpjs.com) but should be executed as `npm` scripts to enable shell execution where necessary.

### Test

Run the headless test suite using [phantomjs](http://phantomjs.org):

```
npm test
```

To run the tests in a browser context open [test/index.html](https://github.com/socialally/emanate/blob/master/test/index.html) or use the server `npm start`.

### Start

Serve the test files from a web server with:

```
npm start
```

### Cover

Run the test suite and generate code coverage:

```
npm run cover
```

### Lint

Run the source tree through [eslint](http://eslint.org):

```
npm run lint
```

### Clean

Remove generated files:

```
npm run clean
```

### Spec

Compile the test specifications:

```
npm run spec
```

### Instrument

Generate instrumented code from `lib` in `instrument`:

```
npm run instrument
```

### Readme

Generate the project readme file (requires [mdp](https://github.com/freeformsystems/mdp)):

```
npm run readme
```

## License

Everything is [MIT](http://en.wikipedia.org/wiki/MIT_License). Read the [license](https://github.com/socialally/emanate/blob/master/LICENSE) if you feel inclined.

Generated by [mdp(1)](https://github.com/freeformsystems/mdp).

[node]: http://nodejs.org
[npm]: http://www.npmjs.org
[gulp]: http://gulpjs.com
[phantomjs]: http://phantomjs.org
[browserify]: http://browserify.org
[eslint]: http://eslint.org
[sa-test]: https://github.com/socialally/sa-test
[mdp]: https://github.com/freeformsystems/mdp
