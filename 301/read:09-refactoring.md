# Read:09 - Refactoring

## Article: Concepts of Functional Programming in JavaScript
[Medium.com](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

System Complexity: "Complexity is anything that makes software hard to understand or to modify." - John Outerhout

What is Functional Programming?

"Functional programming is a programming paradigm - a style of building the structure and elements of computer programs - that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data" - [Wikipedia](https://en.wikipedia.org/wiki/Functional_programming)

The first concept to learn when trying to understand functional programming is pure functions. Pure functions are any functions that returns the same result if given the same arguments AND does not cause any observable side effects.

Reading Files: if our functions reads external files, it's not a pure function as the contents of the external file can change. The same goes for any function that relies on a random number generator.

Pure functions are stable, consistent, and predictable.

Immutability - When data is immutable, its state cannot change after it's created. If you want to change an immutable object, you can't. Instead, you create a new object with the new value.

## Article: Refactoring JavaScript for Performance and Readability
[Dev](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec
)

The middle ground between speed and comprehension is where good code lives. 