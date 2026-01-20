### Properties:


##### id: 202410040926_variable_block_scope
##### hubs: [[javascript.md]], [[scope.md]]
##### source:https://www.w3schools.com/js/js_scope.asp


### Content:

only let, const provided block scope
it wont happen with VAR

```JavaScript
{
	var x=10;
	let y=10;
}
console.log(x) // => 10
console.log(y) // => Error
```