### The ABC of Programming

#### Using Scripts for the first time

>A: What is a script and how do I create one?

>- A script is a series of instructions that the computer can follow in order to achieve a goal.
>- Each time the script runs, it might only use a subset of all the instructions.
>- Computers approach tasks in a different way than humans, so your instructions must let the computer solve the task programmatically.
>- To approach writing a script, break down your goal into a series of tasks and then work out each step needed to complete that task (a flowchart can help.)

#### Expressions + Operators

There are two types of expressions. Those that just assign a value to a variable like `var color = 'beige';` (the color is now beige), and expressions that use **two or more** values to return a single value like `var area = 3 * 2;` (the value or area is now 6). The second example there is also known as an arithmetic operator in that it performs basic math. The first example is what's known as an assignment operator in that it just assigns a value to a variable. Another type of operator is what's known as a "String Operator", which just combines two strings like `greeting = 'Hi' + 'Molly';` (The value of greeting is now Hi Molly).

We also have comparison operators like `buy = 3 > 5;` (returns the value as false) and logical operators which combine expressions and return either true or false: `buy = (5 >3) && (2 < 4);` (which in this case would be true).

There is a single String Operator: the + symbol. It is use to join strings together that appear on either side of it, but not through addition, just combining (putting next to eachother). Think for a second:

`var cost1 = '7';
var cost 2 = '9';
var total = cost1 + cost 2;`

String becomes 79

#### Defining Functions