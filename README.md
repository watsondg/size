size.js
===

Small util to centralize and debounce window 'resize' events.

## Install

```
npm install watsondg/size -S
```

## Usage

```
var size = require('size');

size.addListener(function() {
    console.log('resized', size.width, size.height);
});
```

## Instance Methods

### addListener(handler[, context])

Bind a function to the resize event
* `handler` - the function to call after a resize event
* `context` - (OPTIONAL) - the context to bind the event callback to


### removeListener(handler[, context])

Unbind a function to the resize event
* `handler` - the function to call after a resize event
* `context` - (OPTIONAL) - the context to bind the event callback to

### bind(options)

Enable the singleton by listen to the window `onresize` event.
* `options` - a hash containing configurable options:
- `debounceTime`: debounce delay for the window `onresize` event. Defaults is 150.

### unbind()

Unbind the window `onresize` event.

## Instance Properties

### width
### height
### isLandscape
### hasBar (experimental)
true on mobile if the browser bar is shown on iOS.

## License
MIT.
