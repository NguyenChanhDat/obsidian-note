### Properties:


##### id: 202410031100
##### hubs: [[javascript.md]], [[object.md]], [[security.md]]
##### source:  https://github.com/eslint-community/eslint-plugin-security/blob/main/docs/the-dangers-of-square-bracket-notation.md


### Content:
Using square bracket with object gonna grants access ot all property available on the object. This is bad for application since user can input, change sensitive property
Ex:
 `userInput = ['constructor', '{}'];
`exampleClass[userInput[0]] = userInput[1];`

