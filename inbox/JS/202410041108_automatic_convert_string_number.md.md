### Properties:


##### id: 202410041108_automatic_convert_string_number
##### hubs: [[javascript.md]], [[typeof.md]]
##### source: https://www.w3schools.com/js/js_type_conversion.asp


### Content:

with '+' , it will automatically make it a string concatenate
```JavaScript
console.log("5"+9) // => 59
console.log(9+"5") // => 95
```

with other operator (-, /, * ), JS will tryna convert it to number
```JavaScript
console.log("5"*9) // => 45
console.log(9*"5") // => 45
```
