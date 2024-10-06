### Properties:


##### id: 202410061053_this_no_bounding
##### hubs: [[javascript.md]], [[this.md]]
##### source:


### Content:

In JavaScript, keyword `this` behaves unlike most other programming languages. It can be used in any function, even if it’s not a method of an object.

There’s no syntax error in the following example:

```javascript
function sayHi() {
  alert( this.name );
}
```

```javascript
let user = { name: "John" };
let admin = { name: "Admin" };

function sayHi() {
  alert( this.name );
}

// use the same function in two objects
user.f = sayHi;
admin.f = sayHi;

// these calls have different this
// "this" inside the function is the object "before the dot"
user.f(); // John  (this == user)
admin.f(); // Admin  (this == admin)

admin['f'](); // Admin (dot or square brackets access the method – doesn't matter)
```