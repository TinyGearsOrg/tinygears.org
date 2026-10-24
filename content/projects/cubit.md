---
title: cubit
summary: "A dimensional-analysis calculator on uom: units, typed products and exact conversions, as a command line tool and a web app."
status: in development
accent: "#2dd4bf"
featured: true
weight: 20
links:
  - {name: Source, url: "https://github.com/TinyGearsOrg/cubit"}
  - {name: Run with jbang, url: "https://www.jbang.dev"}
tagline: A dimensional-analysis calculator
subtitle: Units, typed products and exact conversions, as a command line tool and a web app.
features:
  - title: Exact conversions
    text: "Built on [uom](/projects/uom/). `:exact on` makes decimals exact, so `0.1 m + 0.2 m` is `0.3 m`."
  - title: Typed products
    text: "A product is typed where uom declares a relation (`Force · Length` is an `Energy`). `-v` shows the type and the dimension."
  - title: Dimension errors
    text: "A sum of different dimensions is an error that names both: `cannot add Length [L] and Time [T]`."
---
```
$ cubit '3 kN * 2 m to J'
6000.0 J
$ cubit -v '10 mi / 2 h to km/h'
8.04672 km/h
  Speed  [L·T^-1]
$ cubit '3 m + 2 s'
error: cannot add Length [L] and Time [T]
```

cubit needs Java 25 or later. With [jbang](https://www.jbang.dev) no build is
needed, and the same jar serves the web app:

```
jbang cubit@TinyGearsOrg/cubit '20 °C to °F'
jbang cubit@TinyGearsOrg/cubit --serve    # http://localhost:8080
```

A cubit is an old unit of length, the span of a forearm. See the
[README](https://github.com/TinyGearsOrg/cubit#readme) for the expression
language, variables and your own units.
