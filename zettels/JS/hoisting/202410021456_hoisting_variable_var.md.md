#hoisting
### Properties:


##### id: 202410021456_hoisting_variable_var
##### hubs:[[javascript.md]], [[hoist.md]]
##### source:
https://www.digitalocean.com/community/tutorials/understanding-hoisting-in-javascript
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules#import_declarations_are_hoisted


### Content:

```
function hoist() {
  a = 20;
  var b = 100;
}

hoist();

console.log(a);
```
this will return 20 because a wasn't declared
```
console.log(b); 
```
return error: b is not defined

```
console.log(hoist); // Output: undefined

var hoist = 'The variable has been hoisted.';
```
this happens cuz [[javascript.md]] hoisted [[hoist.md]]  the variable declaration, this also apply to function scope
