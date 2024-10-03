### Properties:


##### id: 202410021511_hoisting_function
##### hubs: [[hoist.md]]
##### source: https://www.digitalocean.com/community/tutorials/understanding-hoisting-in-javascript


### Content:

function declaration allow hoist [[hoist.md]]:
```
hoisted(); // Output: "This function has been hoisted."

function hoisted() {
  console.log('This function has been hoisted.');
};
```
function expressions allow hoist also, but in this case it hoist the declaration of expression but the assignment of function haven't done yet:
```
expression(); //Output: "TypeError: expression is not a function

var expression = function() {
  console.log('Will this work?');
};
```
