### Properties:


##### id: 202410061733_lexical_definition
##### hubs: [[javascript.md]], [[scope.md]], [[lexical_env]]
##### source:  https://javascript.info/closure


### Content:

In JavaScript, every running function, code block `{...}`, and the script as a whole have an internal (hidden) **associated object** known as the _Lexical Environment_.  [[202410062305_lexical_env_definition]]

The Lexical Environment object consists of two parts:

1. _Environment Record_ – an object that stores all local variables as its properties (and some other information like the value of `this`).
2. A reference to the _outer lexical environment_, the one associated with the outer code.