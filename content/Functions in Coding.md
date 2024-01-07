---
{"dg-publish":true,"permalink":"/functions-in-coding/","title":"Functions in Coding"}
---

# Functions in [[Coding\|Coding]]
## Functions should be small, do one thing

All things in the function should **be at the same abstraction level**. You can describe a function with only one level of abstraction by using "TO" paragraphs. This allows readability like a story, *"To do a, you must do b"*

>TO RenderPageWithSetupsAndTeardowns, we check to see whether the page is a test page and if so, we include the setups and teardowns. In either case we render the page in HTML. [^2]

"if you can extract another function from it with a name that is not merely a restatement of its implementation" [^2]

---

Nested structures like if, else, while, for, try, etc should ideally call another function in their code block. This makes the code easier to read and understand. [^1]
>[!example]-
>```js
>//Write a function that takes in an object, and a method name, using a 2D array "inputObjArray", run each item with the specified method
>function 2DLoop(inputObjArray, inputMethod) {
>	for(let i=0; i<inputObjArray.length; i++) {
>		for(let i=0; i<inputObjArray.length; i++) {
>			inputObjectArray[i][j].inputMethod();
>		}
>	}
>}
>
>//Calling Example
>2DLoop(cellsArray, draw);
>```


# References
[^1]: # [How to Design Good Functions and Classes | Writing Clean Code](https://workat.tech/machine-coding/tutorial/design-good-functions-classes-clean-code-86h68awn9c7q)
 [^2]: FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY, CLEAN CODE: A HANDBOOK OF AGILE SOFTWARE CRAFTSMANSHIP Robert C. Martin