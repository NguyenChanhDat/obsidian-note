### Properties:


##### id: 202410021455_hoisting_global
##### hubs:[[javascript.md]], [[hoist.md]]
##### source:https://www.digitalocean.com/community/tutorials/understanding-hoisting-in-javascript


### Content:
an assignment to a non-existing variable creates a new global variable

``` JavaScript
function hoist() {
  a = 20;
  var b = 100;
}

hoist();

console.log(a); 
/* 
Accessible as a global variable outside hoist() function
Output: 20
*/

console.log(b); 
/*
Since it was declared, it is confined to the hoist() function scope.
We can't print it out outside the confines of the hoist() function.
Output: ReferenceError: b is not defined
*/
```