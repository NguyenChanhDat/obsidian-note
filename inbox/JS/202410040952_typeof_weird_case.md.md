### Properties:


##### id: 202410040952_typeof_weird_case
##### hubs: [[javascript.md]],  [[typeof.md]]
##### source:


### Content:

``` JavaScript
typeof NaN === "number"; // Despite being "Not-A-Number"
typeof Number("1") === "number"; // Number tries to parse things into numbers
typeof Number("shoe") === "number"; // including values that cannot be type coerced to a number
```
