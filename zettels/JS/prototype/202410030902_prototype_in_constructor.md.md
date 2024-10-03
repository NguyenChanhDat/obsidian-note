### Properties:


##### id: 202410030902_prototype_in_constructor
##### hubs: [[javascript.md]], [[constructor]], [[js_prototype.md]]
##### source: https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object_prototypes


### Content:

When calling  a function as a constructor, the prototype property [[202410030850_property_prototype_of_a_function]] is set as the prototype of a newly constructed obj

By default, prototype prop has it own prop constructor which reference to constructor function itself.
`Box.prototype.constructor === Box`
