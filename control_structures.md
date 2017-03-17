## Control Structures

**Control structures are bits of code that decide which part of a program to run next.** Examples include:
* `if`/`else` statements
* `while` and `for` loops


#### If/Else statements

Arguably the most important structure in programming is the if/else statement. You'll use them every day for incredibly complex decisions. Every one of those decisions comes down to:

**Is this true? If so, do this. If not, do this.**

!['if-else diagram'](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/If-Then-Else-diagram.svg/2000px-If-Then-Else-diagram.svg.png)

Example in Ruby:

```ruby
if name == "Amber"
  "awesome!"
else
  "that's ok too"
end
```

**The important thing to keep in mind is that anything following `if` until the next line should evaluate to true or false.** If it evaluates to nil, it will throw an error.

A few more if/else statement examples:

```ruby
if 2 > 3
  'You will literally never see this message'
else
  'You will always see this one'
end

if 'hello' == 'hello'
  'hello is hello'
else
  'hello is never not hello'
end

if 'hello' != 'hello'
  'You will never see this either'
end
```
In the last example, we had no `else`. That's perfectly fine. Sometimes we don't need an `else` to our logic.

#### While Loops

**While loops are related to if/then statements, but wait for a condition to be false.** Most commonly, we'll include a bit of code in the example that will affect the condition we're testing.

Let's look at an example:

```ruby
age = 32;
while age < 40
  'you are younger than 40'
end
```

If we run this code as written, it will cause our program to *CRASH*! That's because, as written, the code will run *forever*. `age` will never be anything other than 32 so our conditional (the bit in parentheses) will always be true, forever and ever and ever and our computers can't handle it.

Here's how we use while loops effectively:

```ruby
age = 32;
while age < 40
  puts 'you are younger than 40'
  age = age + 1;
}
```

*Now* when we run our code, it will print 8 copies of "you are younger than 40" into the terminal and then stop. Every time we run this bit of code, we *reassign* age to be one more than it was when it came in. At the end of our program, `age == 40`.

**There are other control structures in programming but these are the main two. If you understand them, the less commonly-used ones will be easier to use.**
