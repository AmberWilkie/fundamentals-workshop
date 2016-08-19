## Functions / methods

>The words "function" and "method" are used interchangeably, depending on what you're reading. You should think of them as the same thing.

**A function is a bit of code that *does* something.**

This is a function in Ruby:
```
def do_something
  return "something"
end
```

And here's one in Javascript:
```
function do_something() {
  return "something"
};
```

#### Passing information into our methods

Our functions can also *accept* information and use it. Here we are going to pass in the value stored in the variable "number".
```
number = 5
def show_number(whatup)
  return whatup*2
end
show_number(number)
=> 10
```
> Remember that Ruby doesn't need us to type "return", it will automatically return from the last line of code in our function. However I've kept it here because there's nothing wrong with doing it and it makes everything more explicit.

#### Following inputs all the way down
Let's head back to the example above. What is the relationship between ```whatup``` and ```number```? In this example, I've replaced the variables (nicknames) with the values they are holding.
```
number = 5
show_number(5)
// and when it goes into our function
  return 5*2
end
=> 10
```

**It's critically important to be able to follow your values all the way down into the functions you are calling.** Many times we are putting variables into functions into variables on and on. If we can keep track of what information those variables hold the whole way through, we will be able to write our code. Otherwise, we will be completely lost.
