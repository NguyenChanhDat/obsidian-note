### Properties:


##### id: 202410051723_object_is_compare_to_equal
##### hubs: [[javascript.md]], [[comparison.md]]
##### source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/is


### Content:

``Object.is()`` doesn't support coercion to both side 
The only difference between ``===``  and ``Object.is()`` is in their treatment of signed zeros and ``NaN`` [[202410051644_NaN_in_strict_equality.md]] values

```JavaScript
console.log(Object.is('1', 1));
// Expected output: false

console.log(Object.is(NaN, NaN));
// Expected output: true

console.log(Object.is(-0, 0));
// Expected output: false

const obj = {};
console.log(Object.is(obj, {}));
// Expected output: false
```
