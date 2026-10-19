---
title: cubit
summary: "A dimensional-analysis calculator on uom: units, typed products and exact conversions, as a command line tool and a web app."
status: in development
weight: 20
links:
  - {name: Source, url: "https://github.com/TinyGearsOrg/cubit"}
  - {name: Run with jbang, url: "https://www.jbang.dev"}
---
cubit is a calculator for quantities with units, built on
[uom](/projects/uom/). It converts exactly, types the product of two quantities
(`Force · Length` is an `Energy`), and reports a sum of different dimensions as
an error that names both. It runs as a command line tool and as a small web app,
from one jar. A cubit is an old unit of length, the span of a forearm.

```
$ cubit '3 kN * 2 m to J'
6000.0 J
$ cubit -v '10 mi / 2 h to km/h'
8.04672 km/h
  Speed  [L·T^-1]
$ cubit '3 m + 2 s'
error: cannot add Length [L] and Time [T]
```

It needs Java 25 or later. With [jbang](https://www.jbang.dev) no build is
needed:

```
jbang cubit@TinyGearsOrg/cubit '20 °C to °F'
jbang cubit@TinyGearsOrg/cubit --serve    # the web app on http://localhost:8080
```

See the [README](https://github.com/TinyGearsOrg/cubit#readme) for the
expression language, exact decimals, variables and your own units.
