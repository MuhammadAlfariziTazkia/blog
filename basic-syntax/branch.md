---
description: Making decisions in your code
---

# Branch

Branching is a fundamental concept in programming that able program make a decision / action based on specified condition. In Java Programming Language, we can using `if-else` and `switch-case` branching.

### If-Else

#### If Statement

`if` statement will able the program to evaluate specified condition, if that condition is `true`, the program will execute the statement inside the `if` code block. But if the condition is `false` the code block inside `if` will be ignored.

{% code title="Basic Syntax Format" %}
```
if (specifiedCondition) {
    // statement that will execute if specified condition == true
}
```
{% endcode %}

{% code title="Example - Code Snippets" %}
```
String name = "John Doe";

if (name == "John Doe") {
    System.out.println("Hello John Doe!");
}
```
{% endcode %}

{% code title="Example - Console Output" %}
```
Hello John Doe!
```
{% endcode %}

#### Else if statement

Like `if` statement, `else if` have specified condition too. When specified condition in `if` is `false`, then next step is check the condition in `else if` statements. **Please take a note that `else if` statement can more than 1.**

{% code title="Example - Code Snippets" %}
```
String name = "Andy";

if (name == "John Doe") {
    System.out.println("Hello John Doe!");
} else if (name == "Andy") {
    System.out.println("Hello Andy!"); // this statement will be executed
} else if (name == "Jane Doe") {
    System.out.println("Oh, hello ms Jane!");
}
```
{% endcode %}

{% code title="Example - Console Output" %}
```
Hello Andy!
```
{% endcode %}

#### Else statement

`else` statement will be executed when all of the specified condition in `if` and `else if` is `false`.

{% code title="Example - Code Snippets" %}
```
String name = "Bejo";

if (name == "John Doe") {
    System.out.println("Hello John Doe!");
} else if (name == "Andy") {
    System.out.println("Hello Andy!"); 
} else if (name == "Jane Doe") {
    System.out.println("Oh, hello ms Jane!");
} else {
    System.out.println("Oh sorry, I don't know your name, please mention it!"); // this statement will be executed
}
```
{% endcode %}

{% code title="Example - Console Output" %}
```
Oh sorry, I don't know your name, please mention it!
```
{% endcode %}

### Switch Case

Let's see this code snippets to understand about basic format of `switch case` branching.

{% code title="Basic Syntax Format" %}
```
switch (swithVariable) {
    case "SWITCH_VALUE_A" : 
        // this statement will be executed if swithVariable is "SWITCH_VALUE_A"
        break;
    case "SWITCH_VALUE_B" :
        // this statement will be executed if swithVariable is "SWITCH_VALUE_B"
        break;
    case "SWITCH_VALUE_C" :
        // this statement will be executed if swithVariable is "SWITCH_VALUE_C"
        break;
    default:
        // this statement will be executed if there is no case value that fit with switchVariable
}
```
{% endcode %}

* Every case, program will compare the value in `switchVariable` with the case value, in code snippets above, case values are `SWITCH_VALUE_A`, `SWITCH_VALUE_B`, and `SWITCH_VALUE_C`
* If there is no case value that fit with `switchVariable`, the program will executed the statement inside `default` block
* `break` keywords is used to ignore another case value, if the program found the first case value that fit with `switcVariable`

For the example, let's see this code snippets

{% code title="Example - Code Snippets" %}
```
int dayInt = 2;
String dayString;

switch (dayInt) {
    case 1:
        dayString = "Monday";
        break;
    case 2:
        // will be executed because dayInt is 2
        dayString = "Tuesday";
        System.out.println("Woohoo this is Tuesday");
        break;
    case 3:
        dayString = "Wednesday";
        break;
    case 4:
        dayString = "Thursday";
        break;
    case 5: 
        dayString = "Friday";
        break;
    case 6:
        dayString = "Saturday";
        break;
    case 7: 
        dayString = "Sunday";
        System.out.println("It's time for chill in the weekend");
        break;
    default:
        System.out.println("Hmm it seems you are not talking about day");
}

System.out.println("So, day string is : " + dayString);
```
{% endcode %}

{% code title="Example - Console Output" %}
```
Woohoo this is Tuesday
So, day string is : Tuesday
```
{% endcode %}
