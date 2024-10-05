### Properties:


##### id: 202410052341_try_catch_practical_tip
##### hubs: [[javascript.md]], [[tryCatch.md]]
##### source:  https://javascript.info/try-catch


### Content:

Catch should only process technique that it knows and "rethrow" all others

```javascript
let json = '{ "age": 30 }'; // incomplete data
try {

  let user = JSON.parse(json);

  if (!user.name) {
    throw new SyntaxError("Incomplete data: no name");
  }

  blabla(); // unexpected error

  alert( user.name );

} catch (err) {

  if (err instanceof SyntaxError) {
    alert( "JSON Error: " + err.message );
  } else {
    throw err; // rethrow (*)
  }

}
```
In example above, catch only handle ``SyntaxError``


