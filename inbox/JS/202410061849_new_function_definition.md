### Properties:


##### id: 202410061849_new_function_definition
##### hubs: [[javascript.md]], [[function.md]]
##### source:  https://javascript.info/new-function


### Content:

```javascript
let func = new Function(str);
func();
```
it can turn string into a function:

```javascript
let sum = new Function('a', 'b', 'return a + b');

console.log( sum(1, 2) ); // 3
```
