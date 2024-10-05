### Properties:


##### id: 202410041138_obj_in_dataStructure_garbage_collector
##### hubs: [[javascript.md]], [[garbage_collector.md]], [[object.md]]
##### source: https://javascript.info/weakmap-weakset


### Content:

The obj be a prop inside an a data structure(arr, set, map ... ) wont be garbage collected even if there aren't other references to it (unreachable) [[202410041328_unreachable_definition.md]]

```javascript
let john = { name: "John" };

let array = [ john ];

john = null; // overwrite the referenc
```
