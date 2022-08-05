# Operators

## Learning Goals

- Define what an operator is
- Review the different types of operators

## Introduction

**Operators** are special instructions that allow us to inspect, manipulate and
assign values. As such they can operate on either variables or directly on
values.

These are the types of operators we will cover in this lesson:

- Assignment operators
- Arithmetic (i.e. math) operators
- Relational operators

## Assignment Operators

The **assignment operator** allows us to assign values to variables. As we now
know, variables are used to store values so that they can be used repeatedly
in a program. The way a value gets stored in a variable is with the assignment
operator (`=`). The left operand of the assignment operator is the variable
while the right operand is the value we want to assign to the variable. Note
that the value must be the same data type as the variable.

```java
String example = "this is a sample string"; 
```

In the above example, we are combining the variable definition `String example`
and the assignment `example = "this is a sample string"`. This does not have to
be the case. For example, we could declare the variable earlier in the program
and then initialize it later.

```java
String example; 

// some other code here

example = "another sample value for my string";  
```

## Arithmetic Operators

**Arithmetic operators** help us perform simple mathematical operations. These
operators are very similar to the arithmetic operators we may have learned in
elementary school. Consider the following table of arithmetic operators known
in Java:

| Operator | Description    |
|----------|----------------|
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |
| `%`      | Modulus        |
| `++`     | Increment      |
| `--`     | Decrement      |

These operators can be applied to numerical data types, like `int` and
`double`. They can also be used on `char` data types, but we will learn more
about that later on. Let's look at the addition operator to learn more on
how operators can be used within Java! But to help us, consider the following
variables when reading about each operator:

```java
int firstNumber = 20;
int secondNumber = 10;
```

- The plus symbol (`+`) is a binary operator that adds the values on
  either side of the operator. Let's look at the "expression"
  `firstNumber + secondNumber`.
  - `firstNumber + secondNumber` is an expression. An **expression** is a
    combination of operators and variables that evaluate to a single value.
  - When the computer evaluates the expression, we tend to say it "returns"
    that value.
  - Once the value is returned, it can then be used in other expressions.
  - Expressions cannot be left on its own line within the source code. If they
    are, then it will result in a compilation error. Expressions aren't a full
    instruction to the computer until its value is assigned to a variable or
    used in another expression.
  - Combining the expression with the assignment operator will provide a full
    statement: `int result = firstNumber + secondNumber;`. This is an
    instruction that the computer can understand and compile.
    - The `firstNumber` variable has the value `20`.
    - The `secondNumber` variable has the value `10`.
    - The code will take `20` and add it to `10` to return the value of `30`.
    - The variable `result` of type `int` is then declared.
    - Finally, the `result` variable is assigned to the value of `30`.
  - Note how the operators all have spaces between them and the variable
    operands. This is common stylistic syntax within Java to have spaces
    between binary operators.

Here is the full list of Java arithmetic operators, including the `+` operator
again, so we have an easy place to look them all up:

- `+` is a binary operator that adds values on either side of the operator:
  `firstNumber + secondNumber`returns `30`.
- `-` is a binary operator that subtracts the right-hand operand from the
  left-hand operand: `firstNumber - secondNumber` returns `10`.
- `*` is a binary operator that multiplies the values on either side of the
  operator: `firstNumber * secondNumber` returns `200`.
- `/` is a binary operator that divides the right-hand operand by the left-hand
  operand: `firstNumber / secondNumber` return `2`.
- `%` is the modulus operator (or mod for short). It is a binary operator that
   returns the remainder value of dividing two numbers:
  - `firstNumber % secondNumber` returns `0` because 20 divided by 10 is an
    even 2 with a remainder of 0.
- `++` is the increment operator. The increment operator is a unary operator
  and increases the value of the single operand by 1:
  - `firstNumber++` returns `21`.
  - Notice that the increment operator is placed directly after the variable
    name with no space between the variable name and the operand.
- `--` is the decrement operator. The decrement operator is a unary operator and
   decreases the value of the single operand by 1:
  - `secondNumber--` returns `9`
  - Notice that the decrement operator is placed directly after the variable
    name with no spaces between the variable name and the operand.

Note that both the increment and decrement operators operate on the operand
and assign it the new value. For example:

```java
firstNumber++; 
```

Has the exact same result as:

```java
firstNumber = firstNumber + 1; 
```

Another thing we should note about the increment and decrement operators is that
the operator could be placed directly before or after the variable. In the
examples above, we placed the operators after the variable. But we could have
also done this:

```java
++firstNumber;
--secondNumber;
```

When we place the operator before the variable, it will still have the same
result as before: `++firstNumber` will return `21` and `--secondNumber` will
return `9`. But order still matters! Let's take a look at an example of when
the placement of the increment or decrement operator would make a difference:

```java
int result = ++firstNumber;
System.out.println(result);

// Reset firstNumber to 20
firstNumber = 20;
result = firstNumber++;
System.out.println(result);
```

Now let's look at the output of the code above:

```
21
20
```

So why are the outputs different? When the first line is run with the `++`
preceding the variable, Java will first perform the operation of
`firstNumber = firstNumber + 1;` before assigning the value of `firstNumber`
to `result`. The next time when the increment operator is used is in the
format of `firstNumber++`. When the `++` follows the variable, Java will
access the value of `firstNumber` before completing the increment.

## Relational Operators

Let's say we would like to compare two values to each other. Are there any
operators that exist for that? The answer is yes!

**Relational operators** are operators that are available in java that allow
us to perform comparisons against two values. Like the arithmetic operators,
these operators will apply to numerical data types and the `char` data type.
Consider the following table of relational operators known in Java:

| Operator | Description           |
|----------|-----------------------|
| `==`     | Equal                 |
| `!=`     | Not Equal             |
| `>`      | Greater Than          |
| `<`      | Less Than             |
| `>=`     | Greater Than or Equal |
| `<=`     | Less Than or Equal    |

We can now use this table of relational operators to help us with comparisons!
Note that all of these operators are binary operators - this means they require
two values on either side of the operator. For example: 
`firstNumber > secondNumber`. Relational operators will also always return a
**boolean** value. This means that it will either return a true or false
value. So `firstNumber > secondNumber` would return a value of true.

## Combining Operators

Multiple operators can be combined in a single statement:

```java
int result = firstNumber * 10 + secondNumber * 2; 
```

In this example, `result` will have a value of `(20 * 10) + (10 * 2)`, which is
`220`.

Note the parentheses with the expressions `20 * 10` and `10 * 2`. These were
grouped together with parentheses to show that the multiplication will evaluate
first when the computer executes this statement. This is because Java
follows the order of operations precedence. If no parentheses are specified,
the order of precedence will be the default:

1. Postfix: `++` and `--`
2. Multiplicative: `*`, `/` and `%`
3. Additive: `+` and `-`
4. Assignment: `=`

It is recommended to always be explicit about the precedence desired. It makes
the code more readable and more maintainable:

```java
int result = (firstNumber * 10) + (secondNumber * 2); 
```
