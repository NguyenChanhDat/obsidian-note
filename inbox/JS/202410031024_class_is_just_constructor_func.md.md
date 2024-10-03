### Properties:


##### id: 202410031024_class_is_just_constructor_func

##### hubs: [[javascript.md]], [[constructor]], [[class.md]], [[inheritance.md]]
##### source:https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain


### Content:
Classes are syntax sugar over constructor functions
this:
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

equal to 

```
class Box {
  constructor(value) {
    this.value = value;
  }

  // Methods are created on Box.prototype
  getValue() {
    return this.value;
  }
}
```
