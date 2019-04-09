# Print and Puts

## Learning Goals

- Use `puts` statement to send content to the screen
- Force text to the next line with the newline character `\n`
- Use `print` statement to send content to the screen
- Use `p` statement to send content to the screen and return a value
- Recognize the difference between `p` and other output methods

## Introduction

As we said in the introduction, in the previous section of Programming as
Conversation, you learned a lot of _expressions_. We're going to teach you your
first _statements_ right now. These are the statements that print your
`String`s to the screen:

* `puts`
* `print`
* `p`

There are others, but `puts` and `p` are going to be your best buddies through
your career learning to code in Ruby. We'll cover these old reliable friends
right now.

## Use `puts` statement to send content to the screen

The command to "out**put s**tring" to the screen is `puts`. This command prints
the `String` you supply it as well as a newline character. That's the invisible
character that tells the cursor to go to the next line. In IRB you can try

```ruby
puts "hi"
hi
 => nil
```

versus:

```ruby
2.3.3 :002 > print "hi"
hi => nil
2.3.3 :003 >
```

Did you see how `puts` "pushed" the `=> nil` to the next line? That's the
"newline" character that `puts` appends to the end.

## Force Text to the Next Line With the Newline Character `\n`

Ruby saw an invisible `\n` character (which represents the `\n`ewline) at the
end of the `String` given to `puts`.

When the newline character is inside a `String` it causes the next letter to
start on the next line. Try out `puts "EdvardnMunch"` in IRB to see `\n` do its
thing.

## Use `print` Statement to Send Content to the Screen

The `print` statements prints out the given `String` with no newline (`\n`)
character at the end. You use it like `puts` though.

```ruby
print "Razmatazz" #=> "Razmatazz"
```

## Use `p` statement to send content to the screen and return a value

The methods `puts` and `print` tell the program to display specific information.
Without `puts` or `print`, Ruby will evaluate the code, but does not display
anything in the console.

You can also see `nil` after the text is printed in the command line. This is
the _return value_. The return value is the value returned by a Ruby expression,
but when we use `puts` and `print`, we are returned `nil`, or "nothing".

If you want to print a value **and** return it, you should use `p`:


```ruby
p "Hello World"
 => "Hello World"
 ```

> **CONFIRM UNDERSTANDING**: Compare the return result of `p` versus `puts` to
> make sure you see the difference between returning `nil` and `"Hello World"`.

It actually does more than just that -- it's designed for debugging. `p` is a
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

Newline (`\n`) and other "system" characters are normally invisible, but if you
want to look for these characters, or you want to make sure some value is
correct, then you could use `p`. Also, you'll notice in the output that the `"`
are not removed when displaying the text in the command line.

## Conclusion

We've talked about the differences between `puts`, `print` & `p` in Ruby.
Understanding how methods print and format values can offer feedback to users
while programs are being run. This can be a line asking for user input, letting
the user know that a process is running and how much time has elapsed,or
printing to the command line while debugging, or troubleshooting, code.

## Resources

["Understanding The Differences Between Puts, Print & P"](https://www.rubyguides.com/2018/10/puts-vs-print/)
