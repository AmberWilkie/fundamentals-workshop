# Fundamentals of Programming Workshop

#### Hosted by Amber


```
describe "it teaches fundamentals of coding" do
    workshop(programming_fundamentals)
    expect(August_Cohort).toProduce(20%_more_awesome_code)
  end
```

## Variables

### Vad fan är "variable" för nåt?

**A variable is a thing, with a name, that holds information.**

Variables can hold information about:
* Strings ("things in quotes are strings")
* Numbers
* Objects
  * Arrays
  * Hashes
  * Other stuff
* Other stuff
  * You can put almost anything into a variable.

You can think of variables as "nicknames" (smeknamn) for numbers, strings, functions, arrays, or just about anything else.

**When you create a variable, you "declare it".**

Javascript:
```
var variable;
```

In Ruby, we declare our variables but at the same time give them certain properties. The idea is the same:
```
attr_accessor :variable
```

**When you "set" or "assign" a variable, you store some information in it. That information is called a "value".**

Javascript:
```
variable = 10;
```

Ruby:
```
@variable = 10
```

**We can declare variables and set them at the same time:**
```
var variable = 10;
```

**We store information in variables in the same way, regardless of what the information is. Examples from Javascript:**
```
var variable1 = "Amber";
var variable2 = [];
var variable3 = function () { do_something };
```

In our last example, if we "call" variable3, it will perform the function that it is "set" to.
>If you "call" a variable, you are just using it:
>```
console.log(variable1);
=> "Amber"
  ```

#### Variable types

##### Strings
Anything within ```" "```.

##### Integers
Whole numbers: 3, 9, 2349872357

##### Floats
Non-integer numbers: 1.2, 2349.23423, 7/9  
Note, non-Americans, that we use a period (.) instead of a comma (,) for amounts less than 1.

##### Boolean
True or false. Nothing else is a boolean response - black or white, all or nothing, true or false. All of these examples return true:
```
return true;
```
```
true == true
```
```
false == false
```
```
var craft = 3;
var academy = 3;
craft == academy
```
And in Javascript this is also true:
```
var craft = 3;
var academy = "3";
craft == academy
```
But not in Ruby:
```
craft = 3;
academy = "3";
craft == academy
=> false
```
Every language has its own rules and it's a matter of learning them. It kinda sucks, but being able to work in different languages is a SKILL that will get you more MONEY.

#### Dolla dolla bill y'all

## Operators
#### Courtesy of Craft Academy prep course

### Mathematical Operators

An operator performs mathematical functions or compares between objects. You should be familiar with all of these:
```
a = 3
b = 2
a + b = 5
a - b = 1
a * b = 6
a / b = 1.5
```

Let's pay special attention to these:
```
a**b = 3^2 = 9
a%b = whaaaaa? (it's 1 in our example here)
```
The ```**``` takes one number *to the power* of another. We haven't used this yet, but we might at some point.

The ```%``` is called a "modulus" and it calculates the *remainder* after dividing one number into another.  
Say you have two kids and seven apples. You don't have a knife, so you'll have to divide the apples whole. Each kid gets three apples and there's one left over. That ONE is the remainder.

### Comparison Operators

We'll use ```a = 3, b = 4, c = "3"``` for our examples.

== checks that two values are the same and returns true or false:
```
a == b
=> false
```
=== checks that two values are the same AND checks that they are the same *type*. Not every language cares about that.
```
a == c
=> true (in Javascript, not in Ruby)
a === c
=> false
```

!= checks that the two values are *not* equal.
```
a != b
=> true
```

We can talk about the rest together:
```
a > b
=> false
a < b
=> true
```
There are also operators that allow a value to be equal to *or* greater than another:
```
a = 3
b = 3
a >= b
=> true
a <= b
=> true
```

### Logical Operators

Logical operators also return true or false.

&& checks that both sides of a statement are true. These examples return true:
```
true && true
```
```
3 == 3 && 9 == 9
```
And these return false:
```
false && false
```
```
a = "craft"
b = "academy"
a == b && "craft" == "academy"
```

> Tip! If you're assessing a && comparison and you find one side to be false, you don't even have to look at the other side. You know the comparison will return false.

|| only needs *one* side of the statement to be true in order to return true. These examples are true:
```
true || false
```
```
3 == 3 || 3 == 9
```
```
a = "craft"
b = "academy"
a == b || a == "academy"
```
> Tip! If you're assessing a || comparison and you find one side to be true, you don't even have to look at the other side. You know the comparison will return true.

## Hashes and Arrays

### Arrays

**Arrays are groups of values, stored in ```[]```**
You can store a nearly limitless number of items in an array. These values are accessed using a number called an "index". It starts at 0, so the first item is found at [0], the second at [1] and so on:
```
myArray = ["sunshine", "happiness", "balance"]
myArray[0]
=> "sunshine"
myArray[2]
=> "balance"
```
Let's get complicated for a second. You can *also* use a variable to find a value in an array:
```
number = 2
myArray[number]
=> "balance"
```
But you'll get nothing if there's no value at that index:
```
number = 12
myArray[number]
=> undefined
```
>Tip! You'll do shit like that *constantly* in programming.

### Hashes

**Hashes are a lot like arrays, but they have special properties.**

Here's an example of a hash:
```
myHash = {key: value, number: 8, name: "Amber"}
```
The bits behind the : are called the "key" and the bits after are called the "value". Different languages access the keys and values in hashes differently but the idea is the same.

Ruby:
```
myHash[:name]
=> "Amber"
```
```
myHash.number
=> 8
```
> What about ```myHash[:key]```? That's going to return undefined. Can you tell me why?

### Complicating shit

So you've seen an array and you've seen a hash. The tricky part is when things get really complicated. You can have arrays inside of hashes and hashes inside of arrays. And hashes inside of hashes inside of hashes. Javascript has no problem with this:
```
a = {key: "value"};
b = {a, number: 3};
c = {b, a, sign: "pisces"};
d = [c, "hotdogs"]
d
=> [{b: {a: {key: "value"},
    number: 3},
    a: {key: "value"},
    sign: "pisces"},
    "hotdogs"]
```

## A Bit of Theory

### How computers see our code

**First thing you need to know is that our computers will only do what we tell them to do, and nothing else.**  
The best errors are the ones *we* make, because we can fix them. The worst errors are the ones that are related to the things we didn't build: problems with browsers, incompatibility, something called "deprecation" (which means we're using an old version of something), and problems with our testing or working environments.

**Computers read our code from top to bottom.**
Our computers can only see the code that's already run (that is earlier in the program).
```
a = 3
c = (a == b)
b = 3
c
=> false
```
It's too late for c to ever read ```a == b``` as true (even though it is now) because c has *already been set to "false"*.

> A major (perceived) exception to this is when we call functions from within other functions. We'll get to that. Suffice to say that this is *not* an exception at all, it just looks like it.
