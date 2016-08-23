### Variables, Continued

**Some languages care about variables *types*.** Javascript, for instance, has a method called `typeof()` that checks the type of information stored in the variable:

```javascript
var number = 3;
typeof(number);
=> "number"
```

But the variable (nickname) can be overwritten and hold *any* information.

```javascript
var number = "three";
typeof(number);
=> "string"
```

Not all languages define variables by what is stored inside them. In Ruby you don't ask `typeof` but instead ask about the information contained inside:

```ruby
number = 3
number.respond_to?(:to_s)
=> true (and if we ran .to_s on 3, we would get "3")

number.class
=> Fixnum
```

**Some languages also define variables by how they are used.**

**Local variables** are only available within their own block (typically a function). They are destroyed when the computer is done running the code.
```ruby
def variable_method
  variable = "woohoo!"
  puts variable
end
```
When the computer hits that `end`, `variable` is destroyed and it cannot be read anywhere. It can only be read directly *while the function is running* (through a debugging program).

**Instance variables** are available to an entire *instance*, across different functions. In our `Person` example, if every person has an `address` (declared perhaps with `attr_accessor :address`) and set when we create a `Person` instance, the `address` variable will be available for any activity (`method`) a person does.

In Ruby, instance variables are declared, set and called with the `@` symbol:
```ruby
@address = "Banggatan, Gothenburg, Sweden"
```
These are variables we can access from our testing environment.

**Global variables** are available *anywhere* within our application. They always start with a $ and are declared like this:
```ruby
$LOAD_PATH = 'myapp/lib/'
```
We don't use global variables very frequently because they can be dangerous - typically we don't need information to persist across our entire function. But they are helpful for a couple of isolated things.
