# breakpoints.js


## What it does

Breakpoints.js allows you to trigger JS callbacks when the document is ready, or when the window is resized.


## How to use it

#### Resize Breakpoints 

```
$.breakpoints.min(<width>, <callback>);
$.breakpoints.max(<width>, <callback>);
```

#### Initial Callbacks
```
$.breakpoints.initial.min(<width>, <callback>);
$.breakpoints.initial.max(<width>, <callback>);
```

___
**width** | *integer* : The width of the window that will trigger the callback(s)
___
**callback** | *function or array* : The callback(s) to be triggered
___



## Examples

```
// resize BP
$.breakpoints.min(768, [
    app.fn.kill_slider,
    app.fn.init_sticky
  ]);

$.breakpoints.max(768, [
    app.fn.kill_sticky,
    app.fn.init_slider,
  ]);

// initial BP
$.breakpoints.initial.min(768, app.fn.init_sticky);
$.breakpoints.initial.max(768, app.fn.init_slider);

```




#### Requirements

- jQuery
- [O2 Raf](https://github.com/o2web/raf) (requestAnimationFrame handler)

