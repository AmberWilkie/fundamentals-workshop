## Objects and Attributes

### Everything* is an object
\*almost everything

What we've been doing is called "object oriented programming" because we are working with languages that use objects. Consider this example:

```ruby
my_array = []
```

We've created a variable, which is an object, called "myArray" and we've set it equal to an empty array. By doing so, we've given myArray a whole set of properties that are built into Ruby. Every array in Ruby has certain properties and now ours does too. For instance:

```ruby
my_array.length
=> 0
```

Here we're calling a *method* that is defined as part of the `Array` class in Ruby. We didn't write it and we can't get rid of it (that's not entirely true but just go with it). `Array#length` tells you how many items are in your array.
>There are a bunch of things like this in programming - you'll just have to google for what's available. (Or ask your teachers)

**Back to Objects**

What's an object?
* Variables
* Arrays
* Hashes
* Instances of Classes

Consider:

```ruby
amber = new Person()
amber.name = "Amber"
amber.age = 32
amber.location = "Gothenburg"
```

`amber` is an object. And that object is an *instance* of `Person`. The object `amber` has properties / attributes of `name`, `age` and `location`. The values of those attributes are `Amber`, `32` and `Gothenburg`.

When we create an object, we are making a new, blank version of everything in Person(). We can define that object based on the rules we establish in Person() (the methods and variables we have written into it). And that object can do everything a Person() can do.
