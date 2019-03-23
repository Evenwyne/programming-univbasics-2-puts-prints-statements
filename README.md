# Print and Puts

## Learning Goals

- Define and distinguish `puts` from `print`
- Recognize the difference between `p` and other print methods

## Introduction

There are a few ways to output text in Ruby. In previous lessons, we've used the
keyword `puts` in order to display text in the console, but we can also use
`print`. How are these different? And when should you use one or the other?

We'll cover how the `puts` and `print` commands display Ruby code in the console,
and its limitations.

## Define and Distinguish `puts` From `print`

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

The methods `puts` and `print` tell the program to display specific information.
Without `puts` or `print`, Ruby will evaluate the code, but does not display
anything in the console.

You can also see `nil` after the text is printed in the command line. This is
the _return value_. The return value is the object returned by a Ruby method,
but when we use `puts` and `print`, we are returned `nil`, or "nothing".

**Note**: The `print` and `puts` methods have other options available for
formatting text output. Both `printf` and `puts` are capable of doing things
like have a leading zero even if the number is under 10, (for example: 01, 02,
03, etc.), or correctly formatting floats in monetary calculations (for example:
displaying "$13.50" instead of "$13.5"). These are somewhat more advanced
concepts that require mastering [formatting options], but they will most likely
come in handy as you work more with numbers in Ruby.

## Recognize the Difference Between `p` and Other Print Methods

We've mentioned that both `puts` and `print` do not return values -- instead
they return `nil`. There's actually a method that both _outputs_ the data and
gives a _return value_; this method is `p`. 

```ruby
p "Hello World"
 => "Hello World"
 ```

It actually does more than just that -- It's designed for debugging. `p` is a
method that shows a more "raw" version of an object. For example:

```ruby
puts "Hello World\n"
Hello World
 => nil

print "Hello World\n"
Hello World
 => nil

p "Hello World\n"
 => "Hello World\n"
 ```

Newline (`\n`) and other encoded characters are normally invisible, but if you
want to look for these characters, or you want to make sure some value is
correct, then you could use `p`. Also, you'll notice in the output that the `"`
are not removed when displaying the text in the command line.

## Conclusion

We’ve talked about the differences between `puts`, `print` & `p` in Ruby.
Understanding how methods print and format values can offer feedback to users
while programs are being run. This can be a line asking for user input, letting
the user know that a process is running and how much time has elapsed,or
printing to the command line while debugging, or troubleshooting, code.

## Resources

["Understanding The Differences Between Puts, Print & P"](https://www.rubyguides.com/2018/10/puts-vs-print/)