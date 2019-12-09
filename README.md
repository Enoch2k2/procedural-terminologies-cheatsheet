# Terminologies Cheatsheet for Procedural Ruby

## Variable
Variables are used in order to name a value of some sort to reference later.
```
name = "Bob"

puts "Hello #{name}"
```

Here we store the value "Bob" in the variable `name` in order to be referenced in our puts line.

## Interpolation
Interpolation is where we take a ruby expression and get the value of that expression to inject in a ruby string.

```
name = "Bob"

puts "Hello #{name}"
```

Here when we interpolate the `name` variable, we are using ruby to run `name` which gives us back `"Bob"` and injects "Bob" into the puts statement.

## Integer
Integers are numbers in code. We use integers to do math.

```
1 + 1 # gives us 2
```

## Boolean
Booleans are `true` or `false` values. True and false are used in code in order to determine flow.

```
if true
  puts "This statement is true"
else
  puts "This won't even read because it stopped at the if"
end
```

So here we use a boolean to tell the code what to print out.

*Pro Tip* Booeans are not the same as truthy and falsey, which work a lot like true and false, however can have values such as integers, strings, etc. Only nil or false is falsy in Ruby, everything else is truthy. Booleans are just more to the point of yes or no.

## Method
Where variables are used to store values, methods are used to run a block of logic and print or send back (return) some sort of information to be used in the code.

```
# defining a method
def greeting
  puts "Hello World!"
end

# callings or using our method
greeting
```

## Arguments
When a method needs a value from an external source. The only way we can pass it information is via an argument. For example:
```
def say_hello_to(name)
  puts "Hi #{name}!"
end

say_hello_to("Bob") # prints Hi Bob!
say_hello_to("Sarah") # prints Hi Sarah!
```

In this example we create a method that takes in 1 argument of name. We don't know who's name that might be, however we will assume it will be a name that is a string. Then we'll take that name and inject it into our puts statement. Therefor when we call it
with `say_hello_to("Bob")`. We print out `"Hi Bob!"`, we can use that same method over and over again as long as we pass in names. Arguments allows us the ability for our logic to change based on what we pass in.

## Default Arguments
Default arguments give us the option to pass in an argument, or let it fall back to a default value. For example:

```
def say_hello_to(name="Ruby Programmer")
  puts "Hello #{name}!"
end

say_hello_to # prints out Hello Ruby Programmer!

say_hello_to("Bob") # prints out Hello Bob!
```

By not passing in an argument in the first call, it defaults to the string we set that argument to. However when we pass in an argument to the method, it will override the default value and the value we passed in becomes the value of the argument.
