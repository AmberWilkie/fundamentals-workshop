## Functions / methods

>The words "function" and "method" are used interchangeably, depending on what you're reading. You should think of them as the same thing.

**A function is a bit of code that *does* something.**

This is a function in Ruby:

```ruby
def do_something
  return "something"
end
```

### Passing information into our methods

Our functions can also *accept* information and use it. Here we are going to pass in the value stored in the variable "number".

```ruby
def show_number(num)
  num * 2
end

number = 5
show_number(number)
=> 10
```

> Remember that Ruby doesn't need us to type "return", it will automatically return from the last line of code in our function.

#### Inputs
In our method above, `num` is our input. The method `show_number` takes one _argument_ or piece of information. That means it will not run unless given a piece of information. If we try to give it two pieces of information, it will also complain.
This method takes two pieces of information:
```ruby
def two_infos(info1, info2)
    // code
end
```
This method will be called like this: `two_infos(3, 'house')` where `x` and `y`, in our example, can be literally any type of information. The number 3 will be stored inside of `info1` and used in the method, whereas `'house'` will be stored in `info2`. This concept can be tricky at first - make sure you understand arguments!

## Classes

Classes are collections of functions and variables that can be encapsulated in one object.

An example (in Ruby):

```ruby
class Person
  attr_accessor :name

  def go_to_bootcamp
    "Bootcamp is great!"
  end
end
```

We've created a class `Person` that has one attribute, `name`, and who can do one thing: `go_to_bootcamp`. So now we can create an *instance* of Person. We can create an infinite number of instances of Person and they can interact.

Ruby:
```ruby
amber = Person.new
amber.name = "Amber"

amber.go_to_bootcamp
=> "Bootcamp is great!"

amber.name
=> "Amber"
```
