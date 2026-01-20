### Properties:


##### id: 202410061117_why_use_arrowFunc_in_callbackFunc
##### hubs: [[javascript.md]], [[arrow_function.md]], [[this.md]]
##### source: ChatGPT


### Content:

- because of this behavior in arrow function [[202410061108_this_in_arrow_function]], they inherits ``this`` from surrounding scope
- cleaner, shorter codes
- no need for ``bind()`` like in regular function:
```JavaScript
function MyObject() 
{ 
this.value = 10;
setTimeout(function() {
console.log(this.value); // undefined without .bind(), but with .bind() it works
}.bind(this), 1000); // Here, we bind the `this` of MyObject to the callback function
}
 const obj = new MyObject(); // After 1 second, this will print: 10
```
- arrow function don't have their own argument => easy to defer ``this`` and arguments to a callback
```javascript
function defer(f, ms) {
  return function() {
    setTimeout(() => f.apply(this, arguments), ms);
  };
}

function sayHi(who) {
  alert('Hello, ' + who);
}

let sayHiDeferred = defer(sayHi, 2000);
sayHiDeferred("John"); // Hello, John after 2 seconds
```
