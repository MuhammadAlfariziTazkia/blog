---
description: It's boring to do the same task over and over again, right?
---

# Loop

Imagine you have a task to print sequence of numbers from 1 to 3, based on previous sections, we will code like this:&#x20;

```
System.out.println("1");
System.out.println("2");
System.out.println("3");
```

The code above will give output that fit with the requirements, but how if the requirements is change become print sequence of numbers from 1 to 1000? or 1 to 1 millions? Do you want to copy paste `System.out.println` multiple times until your code file have 100++ line of codes? Wohoo it's sounds teribble.

Good news! in programming languages, we have looping concepts that able the program will execute a code line multiple times based on our commands, of course with a simple basic code syntax. So let's deep dive!

### For

This is basic format to create `for` looping

```
for (initial_declaration; continue_loop_condition; changes) {
    // statements
}
```

And this is simple example for the code format above -> requirements: print sequence of numbers from 1 to 1000

```
for (int i = 1; i <= 1000; i++) {
    System.out.println(i);
}
```

Simple explanation:

* What is the task that we need to do over and over again? -> print number -> so use `System.out.println(i)` to print the `i`, let treat `i` as dynamic variable whose value **changes from 1 to 1000**
* From previous point, please focus on bold text -> **value changes from 1 to 100,** so:
  * What is the initial declaration for `i`? -> of course `i = 1`
  * When will the value stop changing? -> when `i = 1000`, so the `continue_loop_condition` / loop still repeat while `i <= 1000`
  * What type of changes? from 1 to 100 is it increment or decrement? -> of course increment, so we can using `i++` (shorthand of `i = i + 1`

Done! so we don't need to write 1000 line of codes for this requirements

### While

This is basic syntax for while

```
while (continue_loop_condition) {
    // statement
    // changes
}
```

Let's using basic format of while to solve the same requirements (print 1 to 1000)

```
int i = 1;
while (i <= 1000) {
    System.out.println(i);
    i ++;
}
```

The main things is -> `while` loop will repeat the statements inside the block while `continue_loop_condition` is `true`, in this case `continue_loop_condition` is `i <= 1000`

### Do-While

We have another loop that similar with `while` loop, it is `do-while`.

This is simple basic code format for `do-while` loop:

```
do {
    // statements
    // changes
} while (continue_loop_condition);
```

And this is the code snippets to solve the same requirements:&#x20;

```
int i = 1;

do {
    System.out.println(i);
    i ++;
} while (i <= 100);
```

The main different of `do-while` and `while` is about order of `continue_loop_condition` checks.

In `while` loop, we notice that the program will check `continue_loop_condition` at the start process, so if before enter the `while` loop the `continue_loop_condition` is `false`, the block of `while` loop will be ignore and it won't run at all.

In `do-while` loop, the program will check the `continue_loop_condition` at the end, so whatever the condition, the program will execute the statements at least once.

### Break and Continue

#### Break

Is used for exit current looping process. For the example, let's see this requirements:

* Infinity while loop -> `continue_loop_condition` is `true`
* Statements is display `Loop for <i> times` where `i` is integers start from 0, that increase by 1 each iteration
* Loop will terminate if we have `i` is 122 in current iteration

So this is source code to solve that requirements:&#x20;

```
int i = 0

while (true) {
    System.out.println("Loop for " + i + " times");
    if (i == 122) {
        break;
    }
    i ++;
}
```

Please focus on `if` blocks that command the program to exit the loop if `i` is 122

#### Continue

Is used for skip the statement under `continue` line, and go to next iteration directly. For the examples, let's see this requirements:&#x20;

* Output odd numbers from 1 to 10

So to solve this simple requirement, we can command the program to ignore `System.out.println` and go to next iteration if found even number.

```
for (int i = 0; i <= 10; i ++) {

    if (i % 2 == 0) {
    // if i is even number, ignore System.out.println(i) and go to next iteration
        continue;
    }
    System.out.println(i);
}
System.out.println("You exited the for loop");
```

Result:&#x20;

```
1
3
5
7
9
You exited the for loop
```
