### Properties:


##### id: 202410062250_memory_leaked_case
##### hubs: [[javascript.md]], [[garbage_collector.md]], [[object.md]]
##### source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Memory_management


### Content:

**NO MODERN JS ENGINES USES REFERENCE-COUNTING FOR GB_COLLECTOR ANYMORE

With circular reference, because of reference-counting algorithm, they won't be garbage collected => **memory leaked**

``` JavaScript
function f() {
  const x = {};
  const y = {};
  x.a = y; // x references y
  y.a = x; // y references x

  return "azerty";
}

f();
```
