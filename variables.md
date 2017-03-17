## Variables, Continued

### Local Variables

Local variables are only available within their own block (typically a function). They are destroyed when the computer is done running the code.
```ruby
def variable_method
  variable = "woohoo!"
  puts variable
end
```
When the computer hits that `end`, `variable` is destroyed and it cannot be read anywhere. It can only be read directly *while the function is running* (through a debugging program).

### Instance Variables
Instance variables are available to an entire *instance*, across different functions. In our `Person` example, if every person has an `address` (declared perhaps with `attr_accessor :address`) and set when we create a `Person` instance, the `address` variable will be available for any activity (`method`) a person does.

In Ruby, instance variables are declared, set and called with the `@` symbol:
```ruby
@address = "Banggatan, Gothenburg, Sweden"
```
These are variables we can access from our testing environment.

### Global Variables
Global variables are available *anywhere* within our application. They always start with a $ and are declared like this:
```ruby
$LOAD_PATH = 'myapp/lib/'
```
We don't use global variables very frequently because they can be dangerous - typically we don't need information to persist across our entire function. But they are helpful for a couple of isolated things.
