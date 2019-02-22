---
title: first() function
description: The first() function selects the first non-null record from an input table.
aliases:
  - /v2.0/reference/flux/functions/transformations/selectors/first
menu:
  v2_0_ref:
    name: first
    parent: built-in-selectors
weight: 501
---

The `first()` function selects the first non-null record from an input table.

_**Function type:** Selector_  
_**Output data type:** Object_

```js
first()
```

## Examples
```js
from(bucket:"telegraf/autogen")
  |> range(start:-1h)
  |> filter(fn: (r) =>
    r._measurement == "cpu" and
    r._field == "usage_system"
  )
  |> first()
```

<hr style="margin-top:4rem"/>

##### Related InfluxQL functions and statements:
[FIRST()](https://docs.influxdata.com/influxdb/latest/query_language/functions/#first)