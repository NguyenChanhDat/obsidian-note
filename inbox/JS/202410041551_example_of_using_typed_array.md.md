### Properties:


##### id: 202410041551_how_to_use_typed_array
##### hubs:[[javascript.md]], [[typed_array.md]], [[memory_buffer.md]]
##### source: https://chatgpt.com/c/66ffa064-5050-8007-88c8-2d5cac34011f


### Content:

suppose we have a buffer [[202410041553_memory_buffer.md]], represent a file of color in binary form. So we call typed Array [[202410041407_typed_array_definition.md]] as a view [[202410041555_buffer_view_use.md]], every modify in that typed array(view) can modify the buffer

```JavaScript
// Step 1: Create an ArrayBuffer (this represents the raw binary data)
let buffer = new ArrayBuffer(6);
// Step 2: Create a Typed Array view (Uint8Array) to access the buffer
let pixels = new Uint8Array(buffer);
// Step 3: Set RGB values (this modifies the buffer too)
pixels[0] = 255; // Red 
pixels[1] = 0; // Green 
pixels[2] = 0; // Blue 
pixels[3] = 0; // Red 
pixels[4] = 255; // Green 
pixels[5] = 0; // Blue
// Step 4: Check the contents of the ArrayBuffer by creating another view 
let anotherView = new Uint8Array(buffer); // Creating another Uint8Array view of the same buffer 
console.log(anotherView); // Output will be the same: Uint8Array(6) [255, 0, 0, 0, 255, 0] 
// The buffer is indeed affected by changes made to the pixels array!
```

