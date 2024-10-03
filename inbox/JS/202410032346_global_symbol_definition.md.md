### Properties:


##### id: 202410032346_global_symbol_definition
##### hubs: [[javascript.md]], [[symbol_datatype.md]]
##### source:https://javascript.info/symbol


### Content:

Mean the symbol that in entire application, whenever create new symbol with that key, it return the same symbol

```javascript
// read from the global registry
let id = Symbol.for("id"); // if the symbol did not exist, it is created

// read it again (maybe from another part of the code)
let idAgain = Symbol.for("id");

// the same symbol
alert( id === idAgain ); // true
```
