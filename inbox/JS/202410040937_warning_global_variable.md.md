### Properties:


##### id: 202410040937_warning_global_variable
##### hubs: [[javascript.md]], [[scope.md]]
##### source:


### Content:

Do NOT create global variables unless you intend to.

Your global variables (or functions) can overwrite window variables (or functions).  

Any function, including the window object, can overwrite your global variables and functions.

```JavaScript
let varA = 3;

function changeVarA() {

varA = 10;

}

  

console.log(varA); //3

changeVarA();

console.log(varA); //10
```
