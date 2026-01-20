### Properties:


##### id: 202410052208_try_catch_synchronously
##### hubs: [[javascript.md]], [[tryCatch.md]], [[asynchronous.md]]
##### source: https://javascript.info/try-catch


### Content:

If an exception happens in “scheduled” code, like in `setTimeout`, then `try...catch` won’t catch it, 

```javascript
try {
  setTimeout(function() {
    noSuchVariable; // script will die here
  }, 1000);
} catch (err) {
  alert( "won't work" );
}
```

That’s because the function itself is executed later, when the engine has already left the `try...catch` construct.

To catch an exception inside a scheduled function, `try...catch` must be inside that function:

```javascript
setTimeout(function() {
  try {
    noSuchVariable; // try...catch handles the error!
  } catch {
    alert( "error is caught here!" );
  }
}, 1000);
```
