### Properties:


##### id: 202410051738_why_primitive_string_can_use_stringObj_method
##### hubs: [[javascript.md]], [[string.md]]
##### source: https://chatgpt.com/share/67011765-c188-8007-8a9f-f262c9dabdb4


### Content:

Even though primitive strings are not objects, JavaScript automatically **temporarily wraps** the primitive string in a `String` object when you call a method or access a property on it. After the operation is completed, the wrapper is discarded. This is called **autoboxing**.
