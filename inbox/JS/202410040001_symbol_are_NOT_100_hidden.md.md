### Properties:


##### id: 202410040001_symbol_are_NOT_100_hidden
##### hubs: [[javascript.md]], [[symbol_datatype.md]]
##### source:https://javascript.info/symbol


### Content:


Technically, symbols are not 100% hidden. There is a built-in method [Object.getOwnPropertySymbols(obj)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertySymbols) that allows us to get all symbols. Also there is a method named [Reflect.ownKeys(obj)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Reflect/ownKeys) that returns _all_ keys of an object including symbolic ones. But most libraries, built-in functions and syntax constructs don’t use these methods.