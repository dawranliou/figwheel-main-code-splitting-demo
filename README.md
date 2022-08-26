# ClojureScript Code Splitting Demo with figwheel-main

This is a working demonstration of [the Code Splitting documentation on the
figwheel.org site](https://figwheel.org/docs/code_splitting.html).

## Dev compilation with interactive REPL

```shell
clojure -m figwheel.main -b dev -r
```

We will see the page with our button on it and get a working REPL. We
are now in a normal Figwheel hot reloaded workflow.

## Release compilation

The release compile is the same as other [advanced builds][advanced]:

```shell
clojure -m figwheel.main -O advanced -bo dev
```

The advanced compile still outputs a `cljs_base.js` file and a
compressed output file for each module so your HTML host page will
still work just fine.

To serve the compiled JS files, use the `-s` option:

``` shell
clojure -m figwheel.main -O advanced -bo dev -s
```

Or alternatively you can watch and compile the advanced build so that you can
have it recompiled after you change it.

``` shell
clojure -m figwheel.main -O advanced -b dev -s
```
