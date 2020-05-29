### Operators and Loops

#### Comparison Operators: Evaluating Conditions

You can evaluate a situation by comparing one value in the script to what you expect it might be. The results will be a Boolean: true or false.

Examples:

#### == (is equal to)

This operator compares two values (numbers, strings, or Booleans) to see if they are the same.

`'Hello' == 'Goodbye'` returns false because the are *not* the same string.
`'Hello' == 'Hello'` returns true because they *are* the same string.

It is usually preferable to use the strict method:

#### === (strict equal to)

This operator compares two values to check that both the data type and value are the same.

`'3' === 3` returns false
because they are *not* the same data type or value.
`'3' === '3'` returns true

#### != (is not equal to)

This operator compares two values (numbers, strings, or Booleans) to see if they are *not* the same.

`'Hello' != 'Goodbye'` returns true
`'Hello' != 'Hello'` returns false

#### !== (strict not equal to)

This operator compares two values to check that both the data type and value are not the same.

`'3' !== 3` returns true
`'3' !== '3'` returns false

Programmers refer to the testing or checking of a condition as evaluating the condition. Conditions can be much more complex than those shown here, but they usually result in a value of true or false.

#### > (greater than)
#### < (less than)
#### >= (greater than or equal to)
#### >= (less than or equal to)

### Logical Operators

Comparison operators usually return single values of true or false. Logical operators allow you to compare the results of more than one comparison operator.

In the example below, do espression 1 and espression 2 both evaluate to true? false

##### Expression 3

`((5 < 2) && (2 >= 3))`

- Is five less than two? false
- Is two greater than or equal to three? false

In this one line of code are three expressions, each of which will resolve to the value true or false.

The expressions on the left and the right both use comparison operators, and both return false.

The third expression uses a logical operator (rather than a comparison operator). The logical AND operator checks to see whether both expressions on either side of it return true (in this case they do not, so it evaluates to false).

#### Types of Logical Operators

#### && (logical and)

This operator tests more than one condition.

`((2 < 5) && (3 >= 2))` returns true

#### || (logical or)

This operator tests at least one condition.

`((2 < 5) || (2 < 1))` returns true

If either expression evaluates as true, then the expression returns true, even if one of them is false.

true || true returns true
true || false returns true
false || true returns true
false || false returns false

#### ! (logical not)

This operator takes a single Boolean value and inverts it.

`!(2 < 1)` returns true

This reverses the state of expression

#### Short-Circuit Evaluation

Logical expressions are evaluated left to right. If the first condition can provide enough information to get the answer, then there is no need to evaluate the second condition.

false && anything
^ it has found a false

There is no point continuing to determine the other result. The cannot both be true.

true || anything 
^ it has found a true

There is no point continuing because at least one of the values is true.


### Loops

Loops check a condition. If it returns true, a code block will run. Then the condition will be checked again and if it still returns true, the code block will run again. It repeats until the condition returns false. There are three common types of loops.

#### For

If you need to run code a specific number of times, use a **for** loop. (It is the most common loop.) In a **for** loop, the condition is usually a counter which is used to tell how many times the loop should run.

#### While

If you do not know how many times the code should run, you can use a **while** loop. Here the condition can be something other than a counter, and the code will continue to loop for as long as the condition is true.

#### Do while

The **do...while** loop is very similar to the **while** loop, but has one key difference: it will always run the statements inside the curly braces at least once, even if the condition evaluates to false.

`for (var i = 0; i < 10; i++> {
    document.write(i);
})`

This is a **for** loop. The condition is a counter that counts to ten. The result would write "0123456789" to the page. If the variable i is less than ten, the code inside the curly braces is executed. Then the counter is implemented. The condition is checked again, if i is less than ten it runs again. The next three pages show how this loop works in greated detail.

A **for** loop uses a counter as a condition. This instructs the code to run a specified number of times. Here you can see the condition is made up of three statements:

#### Initialization

Create a variable and set it to 0. This variable is commonly called i, and it acts as the counter.

`var i = 0;`

#### Condition

The loop should continue to run until the counter reaches a specified number.

`i < 10;`

#### Update

Every time the loop has run the statements in the curly braces, it adds one to the counter.

`i++`