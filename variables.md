### Variables, Continued

**Some languages care about variables *types*.** Javascript, for instance, has a method called ```typeof()``` that checks the type of information stored in the variable:
```
var number = 3;
typeof(number);
=> "number"
```

But the variable (nickname) can be overwritten and hold *any* information.
```
var number = "three";
typeof(number);
=> "string"
```

Not all languages define variables by what is stored inside them. In Ruby you don't ask ```typeof``` but instead ask about the information contained inside:
```
@number = 3
number.respond_to?(:to_s)
=> true (and if we ran .to_s on 3, we would get "3")
```

**Some languages also define variables by how long they live.**

**Instance variables** are available to an entire *instance*, across different functions.

**Local variables** are only available within their own block (typically a function). They are destroyed when the computer is done running the code.
