---
title: uom
summary: Typed quantities and units of measurement for Java, with a native API and a JSR-385 implementation on one exact engine.
status: released
version: 0.1.0
weight: 10
links:
  - {name: Source, url: "https://github.com/TinyGearsOrg/uom"}
  - {name: Maven Central, url: "https://central.sonatype.com/artifact/org.tinygears/uom"}
  - {name: Documentation, url: "https://github.com/TinyGearsOrg/uom/blob/main/docs/NATIVE.md"}
---
uom is a Java 17+ library for typed quantities and units of measurement. It has
two APIs on one engine: `uom`, its own API with typed products, and `uom-jsr`, a
JSR-385 (unit-api 2.2) implementation that passes the TCK.

Units convert exactly (rationals, powers of pi and roots), and values are
`double` or exact `BigDecimal`.

```java
Length marathon = Length.of(42.195, SI.KILOMETRE);
Speed pace = marathon.divide(Time.of(3, SI.HOUR));
System.out.println(pace.to(USCustomary.MILE_PER_HOUR)); // prints: 8.739585818818103 mph
```

```xml
<dependency>
  <groupId>org.tinygears</groupId>
  <artifactId>uom</artifactId>
  <version>0.1.0</version>
</dependency>
```
