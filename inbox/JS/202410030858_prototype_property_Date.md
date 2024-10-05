### Properties:


##### id: 202410030858_prototype_property_Date
##### hubs: [[javascript.md]], [[constructor.md]], [[js_prototype.md]]
##### source:https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes


### Content:

```
const myDate = new Date();
let object = myDate;

do {
  object = Object.getPrototypeOf(object);
  console.log(object);
} while (object);

// Date.prototype
// Object { }
// null
```

this happen because when call a obj by constructor function [[202410030902_prototype_in_constructor.md]], it will assign the Date's property [[202410030850_property_prototype_of_a_function]] name prototype as the obj's prototype