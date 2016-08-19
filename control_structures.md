## Control Structures

**Control structures are bits of code that decide which part of a program to run next.** Examples include:
* If/else statements
* While and for loops


#### If/Else statements

Arguably the most important structure in programming is the if/else statement. You'll use them every day for incredibly complex decisions. Every one of those decisions comes down to:

**Is this true? If so, do this. If not, do this.**

Example in Ruby:
```
name = "Amber"
if name == "Amber"
  return "awesome!"
else
  return "that's ok too"
end
```
Example in Javascript:
```
name = "Amber";
if (name == "Amber") {
  return "awesome!";
} else {
  return "that's ok too";
};
```
Both of these functions will return "awesome!"

**The important thing to keep in mind is that anything following ```if``` in ```{}``` should evaluate to true or false.** If it evaluates to undefined, it will throw an error (Ruby) or simply show as false and move on (Javascript).

That looks like this:
```
var name;
if (name == "Amber") {
  return "awesome!";
} else {
  return "don't worry";
}
=> "don't worry"
```
We didn't define the variable name, so it is undefined. So we try ```undefined == "Amber"``` and of course it's not.

**A few more if/else statement examples:**
```
if (age > 20) {
  console.log("You are older than twenty");
} else {
  console.log("You are either exactly twenty or younger than twenty.")
}
```
```
if (number == 5 && other_number == 5) {
  return number * other_number;
} else if (number == 1 || other_number == 2) {
  return number / other_number;
}else {
  return number;
}
```
```
if (number % 15) {
  return "Fizz Buzz";
} else {
  return number;
}
```
This one's harder. Let's see if we can follow it:
```
var variable = 0;

function addOne(number) {
  number = number + 1;
  return number;
};

function subtractOne(number) {
  number = number - 1;
  return number;
}

if (0 == addOne(variable)) {
  console.log( "we used the addOne function");
} else if (1 == subtractOne(variable)) {
  console.log("we used the subtractOne function");
} else {
  console.log("we didn't use either function");
}
=> AMBER CHALLENGE!
```

#### While Loops

**While loops are related to if/then statements, but wait for a condition to be false.** Most commonly, we'll include a bit of code in the example that will affect the variable we're testing.

Let's look at an example:
```
age = 32;
while (age < 40) {
  console.log("you are younger than 40");
}
```
If we run this code as written, it will cause our program to *CRASH*! That's because, as written, the code will run *forever*. age will never be anything other than 32 so our conditional (the bit in parentheses) will always be true, forever and ever and ever and our computers can't handle it.

Here's how we use while loops effectively:
```
age = 32;
while (age < 40) {
  console.log("you are younger than 40");
  age = age + 1;
}
```
*Now* when we run our code, it will print 8 copies of "you are younger than 40" and then stop. Every time we run this bit of code, we *reassign* age to be one more than it was when it came in. At the end of our program, age = 40.

**There are other control structures in programming but these are the main two. If you understand them, the less commonly-used ones will be easier to use.**
