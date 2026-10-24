---
title: uom
summary: Typed quantities and units of measurement for Java, with a native API and a JSR-385 implementation on one exact engine.
status: released
version: 0.1.0
accent: "#f0a030"
featured: true
weight: 10
links:
  - {name: Source, url: "https://github.com/TinyGearsOrg/uom"}
  - {name: Maven Central, url: "https://central.sonatype.com/artifact/org.tinygears/uom"}
  - {name: Documentation, url: "https://github.com/TinyGearsOrg/uom/blob/main/docs/NATIVE.md"}
tagline: Typed quantities and units of measurement for Java
subtitle: A native API with typed products and a JSR-385 implementation, on one exact engine.
features:
  - title: Exact conversions
    text: "Units convert exactly (rationals, powers of pi and roots). Values are `double` or exact `BigDecimal`."
  - title: Typed products
    text: "`Length / Time` is a `Speed` and `Force · Length` an `Energy`, wherever a relation between the types is declared."
  - title: JSR-385
    text: "`uom-jsr` implements unit-api 2.2 on the same engine and passes the TCK, 113 of 113 tests."
---
```java
Length marathon = Length.of(42.195, SI.KILOMETRE);
Speed pace = marathon.divide(Time.of(3, SI.HOUR));
System.out.println(pace.to(USCustomary.MILE_PER_HOUR)); // prints: 8.739585818818103 mph
```

uom needs Java 17 or later and is on Maven Central. Its only third-party runtime
dependency is the JSR-385 `unit-api`, and only for `uom-jsr`.

```xml
<dependency>
  <groupId>org.tinygears</groupId>
  <artifactId>uom</artifactId>
  <version>0.1.0</version>
</dependency>
```
