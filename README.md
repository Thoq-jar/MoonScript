# MoonScript

### Example code:
> **Pt.1: Button push counter**
```moonscript
// Check that the DOM is fully loaded
doc.addEventListener("DOMContentLoaded", fun() {
    // Ensure Moonscript is running
    printlog("Moonscript running!")

    // Example syntax:
    printlog("This is a log");
    printinfo("This is info");
    warn("This is a warning");
    error("This is an error");

    // Init vars
    var clickCount = 0;
    var clickCountParagraph = doc.element("click-count");
    
    // Get element
    doc.element("btn-1").addEventListener("click", fun() {
        // Increment counter
        clickCount++;

        // Tell the user how many times the button has been pushed with the GUI
        clickCountParagraph.textContent = "Button clicked " + clickCount + " times!";

        // Tell the user how many times the button has been pushed with the console
        printlog("Button clicked: " + clickCount + " times!");
    });
});
```

---------------------------------------

>**Pt. 2: Code comparrison**

 Original JavaScript Code:
```js
console.log("Hello, world!");
document.getElementById("myButton").addEventListener("click", function() {
    console.log("Button clicked!");
});
```

Moonscript Code:
```js
printlog("Hello, world!");
eventListener(myButton, "click", fun() => {
    printlog("Button clicked!");
});
```
---------------------------------------

> **Pt.3: The Syntax**
```
printlog: console.log
printinfo: console.info
warn: console.warn
error: console.error
element: getElementById
eventListener: addEventListener
fun: function
doc: document
```

---------------------------------------


>**Pt.4: Explanation**

`printlog`, `printinfo`, `warn`, and `error` are the *syntax* for logging messages to the console.
`element` is a the way of selecting an HTML element by its ID.
`fun` is a concise way to declare a function.
`doc` is the syntax to quickly reference to the document object, which represents the entire HTML document.

---------------------------------------


>**Pt.5: Why use Moonscript:**

- Readability: Simplified syntax makes code easier to read and understand.
- Efficiency: Reduces the amount of typing required, especially in large codebases.
- Consistency: Ensures a consistent coding style across projects.
- Interop: Any JS code will compile to a Moonscript Binary.

---------------------------------------
