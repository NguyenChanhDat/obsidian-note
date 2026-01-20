### Properties:


##### id: 202410061636_immediately_invoked_function_use_case
##### hubs: [[javascript.md]], [[function.md]], [[scope.md]]
##### source:  https://developer.mozilla.org/en-US/docs/Glossary/IIFE


### Content:

- Limit the number of global variables, because inside function => local scope [[202410040932_local_scope.md]]
``` JavaScript
(() => {
  // some initiation code
  let firstVariable;
  let secondVariable;
})();

// firstVariable and secondVariable will be discarded after the function is executed.
```

