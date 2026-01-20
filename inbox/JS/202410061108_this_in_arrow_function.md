### Properties:


##### id: 202410061108_this_in_arrow_function
##### hubs: [[javascript.md]], [[this.md]],[[arrow_function.md]]
##### source: https://javascript.info/arrow-functions


### Content:

arrow functions do not have `this`. If `this` is accessed, it is taken from the outside. 


```javascript
let group = {
  title: "Our Group",
  students: ["John", "Pete", "Alice"],

  showList() {
    this.students.forEach(
      student => alert(this.title + ': ' + student)
    );
  }
};

group.showList(); // Our group ....
```


regular func => error:

```javascript
let group = {
  title: "Our Group",
  students: ["John", "Pete", "Alice"],

  showList() {
    this.students.forEach(function(student) {
      // Error: Cannot read property 'title' of undefined
      alert(this.title + ': ' + student);
    });
  }
};

group.showList();
```