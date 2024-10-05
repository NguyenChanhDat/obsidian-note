### Properties:


##### id: 202410060018_try_catch_finally_return
##### hubs: [[javascript.md]],[[tryCatch.md]]
##### source: https://javascript.info/try-catch


### Content:


The `finally` clause works for _any_ exit from `try...catch`. That includes an explicit `return`.

In the example below, there’s a `return` in `try`. In this case, `finally` is executed just before the control returns to the outer code.

```javascript
function func() {

  try {
    return 1;

  } catch (err) {
    /* ... */
  } finally {
    console.log( 'finally' );
  }
}

console.log( func() ); // first works log from finally, and then this one
```