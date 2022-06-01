# Operators

## Learning Goals

- Use different operators

## Introduction

Operators are special instructions that allow you to inspect, manipulate and assign values. As such they can operate on either variables (that store values) or directly on values.

These are the types of operators we will cover in this unit:

    Assignment operators allow you to assign values to variables
    Arithmetic (i.e. math) operators allow you to combine values
    Comparison operators allow you to test the values of two variables, which we will cover in another unit


## Assignment Operators

As you now know, variables are used to store values, so they can be used over and over again in your program. The way that a 
value gets stored in a variable is with the `=` operator: 

```java 
String example = "this is a sample string"; 
```

In the above example, we are combining the variable definition `String example` and the variable value assignment 
`example = "this is a sample string"`. This does not have to be the case: 

```java 
String example; 

// some other code here

example = "another sample value for my string";  
```

Later in this unit, we will look at assignment operators that combined assigning a value to a variable and apply  some calculation 
to it 

## Arithmetic Operators

We can assign a set value to a variable, meaning that the value of the variable is hard coded in our source code: 

```java 
int age = 20;  
```

Or we can apply some calculation to the way we come up with the value for a variable: 

```java
int birthYear = 2002; 
int currentYear = 2022; 
int age = currentYear - birthYear; 
```

The arithmetic operators in Java are mostly like the arithmetic operators in day-to-day life. Consider the following variables: 

```java
int firstNumber = 20; 
int secondNumber = 10; 
```

Let's look at our first operator and use it to learn two more concepts:  

* `+` adds values on either side of the operator: the "expression" `firstNumber + secondNumber` will "return" `30`

Let's break down what this means before we go over more operators: 

* `firstNumber + secondNumber` is an "expression", which means it's an instruction that can be combined with other instructions, but 
has meaning on its own. 
* An "expression" evaluates to "something", which means it can be interpreted by the computer and replaced by the value the
computer calculated when it interpreted the expression. 
* When the computer calculates a value for an expression, we say that it "returns" that value
* When that value is returned, it can then be used in whatever other expressions are part of statement the expression is in

For example, `firstNumber + secondNumber` is an expression that returns a value. If you try to leave this expression on 
its own line in your source file: 

```java
firstNumber + secondNumber; 
```

You will get a compilation error that indicates that your expression is not a "statement", i.e. it's not a full instruction
to the computer. That's because even though the expression could evaluate to a value, that value is never assigned to 
anything or used in any other expression, therefore it would have no meaning to your program. 

We can now combine the `+` arithmetic operator and the `=` assignment operator: 

```java
int result = firstNumber + secondNumber; 
```

That's now a full statement that: 

* References the value stored in the `firstNumber` variable: `20`
* References the value stored in the `secondNumber` variable: `10`
* Takes `20` and adds it to `10`, and returns `30`
* Defines a variable `result` of type `int`, which means we expect it to store whole numbers 
* Takes the value `30` and assigns it to the variable `result` 

Here is the full list of Java arithmetic operators, including the `+` operator again, so you have an easy place to look them 
all up: 

* `+` adds values on either side of the operator: `firstNumber + secondNumber` returns `30`
* `-` subtracts the right-hand operand from the left-hand operand: `firstNumber - secondNumber` returns `10`
* `*` multiplies the values on either side of the operator: `firstNumber * secondNumber` returns `200`
* `/` divides the right-hand operand by the left-hand operand: `firstNumber / secondNumber` return `2`
* `%` is the modulus operator and it returns the remainder value of dividing two numbers: 
`firstNumber % secondNumber` returns `0` because 20 divided by 10 is even 2, with no remainder. 
* `++` is the increment operator and increases the value of the single operand by 1: `firstNumber++` returns `21` 
* `--` is the decrement operator and decreases the value of the single operand by 1: `secondNumber--` returns `9`

Note that both the increment and decrement operators operate on the operand and assign it the new value. For example, writing: 

```java
firstNumber++; 
```

Has the exact same result as writing: 

```java
firstNumber = firstNumber + 1; 
```

## Combining Operators 

Multiple operators can be combined in a single statement: 

```java
int result = firstNumber * 10 + secondNumber * 2; 
```

In this example, `result` will have a value of `(20 * 10) + (10 * 2)`, which is `220` 

Note that when I tried to calculate the result for myself, I grouped the expressions in my statement in a particular way. 
That's because the operators we have seen so far have a specific precedence, which is their default grouping if none is specified: 

1. Postfix: `++` and `--`
2. Multiplicative: `*`, `/` and `%`
3. Additive: `+` and `-`
4. Assignment: `=`

I would recommend that you always be explicit about the precedence you desire - it makes your code more readable and more 
maintainable: 

```java
int result = (firstNumber * 10) + (secondNumber * 2); 
```
