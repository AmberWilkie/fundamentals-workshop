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

**When you "set" a variable, you store some information in it. That information is called a "value".**

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
