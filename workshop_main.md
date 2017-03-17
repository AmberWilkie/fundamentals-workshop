# Fundamentals of Programming Workshop

## Variables

### Vad fan är "variable" för nåt?

**A variable is a thing, with a name, that holds information.**

Variables can hold information about:
* Strings (`"things in quotes are strings"`)
* Numbers
* Objects
  * Arrays
  * Hashes
  * Other stuff
* Other stuff
  * You can put almost anything into a variable.

You can think of variables as "nicknames" (smeknamn) for numbers, strings, functions, arrays, or just about anything else.

**When you create a variable, you "declare it".**

In Ruby, the first time you use (or assign a value to) a variable it is created in memory
```ruby
variable = 'something'
```

**When you "set" or "assign" a variable, you store some information in it. That information is called a "value".**

Ruby:
```ruby
variable = 10
```
#### Return
Methods often "return" or spit out information. When we say that a method "returns" `3`, that means that after all the code inside the method has finished running, the method gives `3` as output. We'll return to inputs later.

!['input-output image'](https://upload.wikimedia.org/wikipedia/commons/thumb/9/92/CPT_Hardware-InputOutput.svg/1212px-CPT_Hardware-InputOutput.svg.png)

#### Variable types

##### Strings
Any set of characters within `""` or `''` . Computers interpret strings from the start of a `'` or `"` until the "closing" `'` or `"`. That means a computer sees this:
```
"this      13497s234 function() //blahblah var setting = 12 'single quotes'    is all one string"
```
- You can put quotes inside each other, to be able to use a `'` inside a string. Like so: `"Here's a string with a 'bunch' of 'quoted text' inside"`
- There are ways to get a computer to interpret what's inside a string as an executable bit of code. This is called "string interpolation" - you'll learn about it later.

##### Integers
Whole numbers: `3`, `9`, `2349872357`

##### Floats
Non-integer numbers: `1.2`, `2349.23423`, `7/9`

Note, non-Americans, that we use a period (.) instead of a comma (,) for amounts less than 1.

##### Boolean
`True` or `false`. Nothing else is a boolean response - black or white, all or nothing, true or false. All of these examples return true:

```ruby
true == true
false == false
```

```ruby
craft = 3;
academy = 3;
craft == academy
```

**Dolla dolla bill y'all** 😎🎉💰💰💰💰💰💰🎉🎉💰💰💰🎉🎉🎉

## Operators
> Courtesy of [Craft Academy prep course](https://craftacademy.gitbooks.io/caa_precourse/content/)

### Mathematical Operators

An operator performs mathematical functions or compares between objects. You should be familiar with all of these:

```ruby
a = 3
b = 2
a + b => 5
a - b => 1
a * b => 6
a / b => 1.5
```

Let's pay special attention to these:
```ruby
a**b => 3^2 => 9
a%b
```

The `**` takes one number *to the power* of another. We haven't used this yet, but we might at some point.

The `%` is called a `modulus` and it calculates the *remainder* after dividing one number into another.
Say you have two kids and seven apples. You don't have a knife, so you'll have to divide the apples whole. Each kid gets three apples and there's one left over. That ONE is the remainder.
In our example above, `a%b = 1`.

### Comparison Operators

- `==` checks that two values are the same and returns true or false:
  ```ruby
  3 == 4
  # false
  ```

- `!=` checks that the two values are *not* equal.
  ```ruby
  3 != 4
  # true
  ```

- We have our greater-than or less-than operators:
  ```ruby
  3 > 4
  # false
  3 < 4
  # true
  ```

There are also operators that allow a value to be equal to *or* greater than another:
```ruby
3 >= 4
# false
3 <= 4
# true

# And, obviously:
3 == 3
# true
```

### Logical Operators

Logical operators also return `true` or `false`.

- `&&` checks that both sides of a statement are true. These examples return true:
  ```ruby
  true && true
  3 == 3 && 9 == 9
  ```
  And these return false:

  ```ruby
  true && false
  "craft" == "craft" && "craft" == "academy"
  ```

> Tip! If you're assessing a `&&` comparison and you find one side to be false, you don't even have to look at the other side. You know the comparison will return false.

- `||` only needs *one* side of the statement to be true in order to return true. These examples return true:

  ```ruby
  true || false
  3 == 3 || 3 == 9
  "craft" == "academy" || "craft" == "craft"
  ```
> Tip! If you're assessing a `||` comparison and you find one side to be true, you don't even have to look at the other side. You know the comparison will return true.

## Hashes and Arrays

### Arrays

**Arrays are groups of values, stored in `[]`.**  
You can store a nearly limitless number of items in an array. These values are accessed using a number called an `index`. It starts at `0`, so the first item is found at `[0]`, the second at `[1]` and so on:

```ruby
my_array = ["sunshine", "happiness", "balance"]
my_array[0]
=> "sunshine"
my_array[2]
=> "balance"
```

You can *also* use a variable to find a value in an array:

```ruby
number = 2
my_array[number]
=> "balance"
```

But you'll get `nil` if there's no value at that index:

```ruby
number = 12
my_array[number]
=> nil
```

### Hashes

**Hashes are a lot like arrays, but they have special properties.**

Here's an example of a hash:

```ruby
my_hash = {key: value, number: 8, name: "Amber"}
```

The bits behind the : are called the "key" and the bits after are called the "value". Different languages access the keys and values in hashes differently but the idea is the same.

Ruby:
```ruby
my_hash[:name]
=> "Amber"
my_hash[:number]
=> 8
```

> What about `my_hash[:key]`? That's going to throw an error. Can you tell me why?

### Complicating shit

So you've seen an array and you've seen a hash. Sometimes things can get really complicated. You can have arrays inside of hashes and hashes inside of arrays. And hashes inside of hashes inside of hashes. Ruby has no problem with this:

```ruby
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
We'll see complicated structures like this a lot in the camp, as JSON strings. The only takeaway at the moment: don't be afraid of them.

## A Bit of Theory

### How computers see our code

**First thing you need to know is that our computers will do exactly what we tell them to do, and nothing else.**
The best errors are the ones *we* make, because we can fix them. The worst errors are the ones that are related to the things we didn't build: problems with browsers, incompatibility, something called "deprecation" (which means we're using an old version of something), and problems with our testing or working environments.
Sometimes a problem is because of our code and sometimes it's because of some other thing we're using to run our code. Differentiating between the two is an amazing skill to build, but super hard.

**Computers read our code from top to bottom.**
Our computers can only see the code that's already run (that is earlier in the program).

```ruby
num1 = 3
num2 = 4
check = (num1 == num2)
num2 = 3
check
=> false
```

It's too late for `check` to ever read `num1 == num2` as true (even though it is now) because `check` has *already been set to "false"*. Even though `num2` changed, `check` was already set.

> This will become immediately apparent when we start debugging. You'll be able to watch your code move line by line and analyze it at each step.
