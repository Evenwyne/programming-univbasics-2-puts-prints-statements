# Print and Puts

## Learning Goals

- Define and distinguish `puts` from `print`
- Recognize the `print f` method
- Recognize the difference between `p` and other print methods

## Introduction

There are a few ways to output text in Ruby. In previous lessons, we've used the
keyword `puts` in order to display text in the console, but we can also use
`print`. How are these different? And when should you use one or the other?

We'll cover how the `puts` and `print` commands display Ruby code in the console,
and its limitations.

## Define and distinguish `puts` from `print`

The `puts` (short for "out**put s**tring") and `print` commands are both used to
display the results of evaluating Ruby code in the console. The primary
difference between them is that `puts` adds a new line (represented by the `\n`
character encoding) after executing, and `print` does not.

```ruby
def print_hello
  print "Hello!"
  print "Hello!"
  print "Hello!"
end

print_hello
# > Hello!Hello!Hello! => nil

def puts_hello
  puts "Hello!"
  puts "Hello!"
  puts "Hello!"
end

puts_hello
# > Hello!
# > Hello!
# > Hello!
#  => nil
```

The methods `puts` and `print` explicitly tell Ruby to display text output.
Without `puts` or `print`, Ruby will evaluate the code, but does not display
anything in the console.

## Recognize the `printf` Method

The `printf` method is similar to `print`, however it has a number of
[formatting options]. This is a more advanced concept derived from other
programming languages such as C. However, in the future, as you work with more
numbers that may have decimal values (floats), such as monetary calculations,
`puts` may not work as expected:

```ruby
def discount_calculator(price)
  discount = 0.10
  sale_price = price - (discount * price)
  puts "The sale price is $#{sale_price}."
end

discount_calculator(15)
# > The sale price is $13.5.
```

This may not look too bad, but the issue here is we don't see two digits after
the decimal point; we would rather display "$13.50", which is standard
formatting for money. Ruby provides you a solution for this sort of problem:

To get complete control over your output, you need to master the `printf`
method. With `puts`, we used a format called "interpolation" to combine the
variables with the string we wanted to output. In `printf`, we separate the
string from the variables by:
- First, giving the format string that displays text
- And next, "placeholder" information that will fill in the variable values into
  the placeholders

Think of it like the ["Mad Libs"] game, where you fill in the blanks. The format
string is followed by the items that fill in the blanks.

The placeholders always begin with a `%`. The letter following the placeholder
(often called a conversion character) tells it what kind of data you are filling
in. The most popular conversion characters are `%s` for a `string`, `%d` for an
`integer`, and `%f`for a float.

So, instead of a `puts`, you would use `printf` like this.

```ruby
def discount_calculator(price)
  discount = 0.10
  sale_price = price - (discount * price)
  printf("The sale price is $%f.\n", sale_price)
end

discount_calculator(15)
# > The sale price is $13.500000.
```

Like `print`, the `printf` method does not automatically add a newline after
your data is printed; if you want a newline, you must put in a `\n` to your
string.

But, wait! That output still doesn't look right. This is where it becomes a
little more advanced.

## Recognize the Difference Between `p` and Other Print Methods



## Conclusion

Knowing how methods print and return values is crucial as you'll be using them
constantly in programs both big and small. Knowing the difference between puts
and return will help you avoid a common pitfalls.

Return values are how different parts of your program communicate with one
another. You don't have to worry too much about this for now, but as you start
to build more complicated programs, you'll find that the return value of one
method might be operated on by a subsequent method. Don't forget to watch out
for those `nil`s!

## Resources

["Understanding The Differences Between Puts, Print & P"](https://www.rubyguides.com/2018/10/puts-vs-print/)
[formatting options]:(https://alvinalexander.com/programming/printf-format-cheat-sheet)
["Mad Libs"]:http://www.madlibs.com/