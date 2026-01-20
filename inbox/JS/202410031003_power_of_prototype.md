### Properties:


##### id: 202410031003_power_of_prototype
##### hubs: [[js_prototype.md]], [[object.md]], [[this.md]], [[inheritance.md]]
##### source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain


### Content:

Reduce redundant, unnecessary code for create method [[202410030931_inheriting_method]]
```
const boxPrototype = {
  getValue() {
    return this.value;
  },
};

const boxes = [
  { value: 1, __proto__: boxPrototype },
  { value: 2, __proto__: boxPrototype },
  { value: 3, __proto__: boxPrototype },
];
```
==> lowering memory usage

Better way to do this:

```
// A constructor function
function Box(value) {
  this.value = value;
}

// Properties all boxes created from the Box() constructor
// will have
Box.prototype.getValue = function () {
  return this.value;
};

const boxes = [new Box(1), new Box(2), new Box(3)];
```
