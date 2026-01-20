### Properties:


##### id: 202410061021_default_param_scope
##### hubs: [[javascript.md]], [[scope.md]], [[function.md]]
##### source:  https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Default_parameters


### Content:


The default parameter initializers live in their own scope, which is a parent of the scope created for the function body.

This means that earlier parameters can be referred to in the initializers of later parameters. However, functions and variables declared in the function body cannot be referred to from default value parameter initializers; attempting to do so throws a run-time [`ReferenceError`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError). This also includes [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)-declared variables in the function body.

For example, the following function will throw a `ReferenceError` when invoked, because the default parameter value does not have access to the child scope of the function body:

``` JavaScript
function f(a = go()) {
  function go() {
    return ":P";
  }
}

f(); // ReferenceError: go is not defined
```

This function will print the value of the _parameter_ `a`, because the variable `var a` is hoisted [[202410021456_hoisting_variable_var.md]] only to the top of the scope created for the function body, not the parent scope created for the parameter list, so its value is not visible to `b`.

```JavaScript
function f(a, b = () => console.log(a)) {
  var a = 1;
  b();
}

f(); // undefined
f(5); // 5
```