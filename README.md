# Print, Puts, and Return Values

## Learning Goals

- Define and distinguish `puts` from `print`

## Introduction

There are a few ways to output text in Ruby. In previous lessons, we've used the
keyword `puts` in order to display text in the console, but we can also use
`prints`. How are these different? And when should you use one or the other?

We'll cover how the `puts` and `print`commands display Ruby code to the console,
and its limitations.

## Define and distinguish `puts` from `print`

The `puts` (short for "out**put s**tring") and `print` commands are both used to
display in the console the results of evaluating Ruby code. The primary
difference between them is that `puts` adds a new line after executing, and
`print` does not.

```ruby
3.times { print "Hello!" }
# > Hello!Hello!Hello!

3.times { puts "Hello!" }
# > Hello!
# > Hello!
# > Hello!
```

The methods `puts` and `print` are a great way to explicitly tell the program to
display specific information. Without these printing methods, Ruby will read the
line, but not print anything out. 

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
