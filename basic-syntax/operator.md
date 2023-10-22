---
description: Basic operation in Java Programming Languages
---

# Operator

### Arithmatic Operator

This operation is used for math calculation on numeric data (can be `byte`, `short`, `int`, `long`, `float`, and `double`)

These are mark operations for math calculation

* `+` -> used for addition operation
* `-` -> used for subtraction operation &#x20;
* `*` -> used for multiplication operation
* `/` -> used for division operation
* `%` -> used for return remainder of division operation
* `++` -> increment, will add a value by 1, shorthand for this operation -> `x = x + 1`
* `--` -> decrement, will substract a value by 1, shorthand for this operation -> `x = x - 1`

{% code title="Code Snippets" %}
```
int a = 10;
int b = 20;

System.out.println(a + b);
System.out.println(a - b);
System.out.println(a * b);
System.out.println(a / b);
System.out.println(a % b); 
```
{% endcode %}

{% code title="Console" %}
```
30
-10
200
0.5
10
```
{% endcode %}

### Comparison Operator

Used for compare between two values, and will return `boolean` based on comparison statement. These are comparison operators that provided in Java :&#x20;

* `==` -> return `true` if value on the left is equals with value on the right
* `!=` -> return `true` if value on the left is not equals with value on the right
* `>` -> return `true` if value on the left is greater than value on the right
* `<` -> return `true` if value on the left is smaller than value on the right
* `>=` -> return `true` if value on the left is greater **or** equals with value on the right&#x20;
* `<=` -> return `true` if value on the left is smaller **or** equals with value on the right

{% code title="Code Snippets" %}
```
int a = 10;
int b = 20;

System.out.println(a == b);
System.out.println(a != b);
System.out.println(a > b);
System.out.println(a < b);
System.out.println(a >= b); 
System.out.println(a <= b); 
```
{% endcode %}

{% code title="" %}
```
false
true
false
true
false
true
```
{% endcode %}

### Logical Operator

Used for manipulate `boolean` value. Logical operator in Java are :&#x20;

* `&&` -> **AND** operator -> will return `true` only if both of statements (left and right statement) are `true`
* `||` -> **OR** operator -> will return `true` if at least one of statements is `true`
* `!` -> **NOT** operator -> will return `true` become `false`, or vice versa

{% code title="Code Snippets" %}
```
System.out.println(true && false) // will output false, because right statement is false
System.out.println(true || false) // will return true, because at least left statement is true
System.out.println(!true) // will return false
System.out.println(!false) // will return true
System.out.println(true && true) // will return true because both of them are true

System.out.println( 10 > 5 || 5 > 20 ) // will return true because at least left statement (10 > 5) is true
System.out.println( 10 > 5 && 5 > 20 ) // will return false because at least right statement (5 > 20) is false
```
{% endcode %}

