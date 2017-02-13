<!-- toc -->

# C++ Language Constructs

## Loop Constructs


### for-loop

The syntax of a for loop in C++ is:

```c++
for ( <initialization>; <condition>; <increment> ) {
   // statemetns
}
```

* The **initialization step** is executed first, and only once. This step allows you to declare and initialize any loop control variables. You are not required to put a statement here, as long as a semicolon appears.

Next, **the condition is evaluated**. If it is true, the body of the loop is executed. If it is false, the body of the loop does not execute and flow of control jumps to the next statement just after the for loop.

After the body of the for loop executes, the flow of control jumps back up to the **increment statement**. This statement allows you to update any loop control variables. This statement can be left blank, as long as a semicolon appears after the condition.

The condition is now evaluated again. If it is true, the loop executes and the process repeats itself (body of loop, then increment step, and then again condition). After the condition becomes false, the for loop terminates.

An example of a simple for-loop that iterates between 0 and 9.

```c++
for (int i = 0; i < 10; i++) {
  // Do something
}
```

Note that `i` actually has block scope here and will not be available outside of the for-loop. If you want to keep the last iteration value after the for-loop you need to define the iterator before the for-loop.

```c++
int i = 0;

for (; i < 10; i++) {
  // Do something
}
```

An endless loop would look like this.

```c++
for (;;;) {
  // Do something forever
}
```