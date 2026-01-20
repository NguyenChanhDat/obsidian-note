### Properties:


##### id: 202410051656_string_match_method
##### hubs: [[javascript.md]], [[symbol_datatype.md]]
##### source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/match


### Content:

```JavaScript
const anyString ="the dog barked at the bat";
const regex=/a/g;
const found = anyString.match(regex);
console.log(found) //=> ["a", "a", "a"]
```

if regex isn't a regular expression,  convert it back to regex by using ``new RegExp()`` then return array of matching content 

###### Description:
It simply calls the ``Symbol.match()`` [[202410051652_well_known_symbol.md]]  method of the ``RegExp`` 