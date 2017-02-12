---
layout: post
title: "Prying Eyes"
date: 2016-08-02 10:57:01 -0400
comments: true
categories:
---
I've spent some time learning how to code on various online learning sites that focus on small projects. When this progressed to creating larger programs that require variables to be manipulated several times things became hard to follow. My way to track it was to output the variables

A majority of my code ended up looking a like this....

{% highlight ruby %}
class RubyClassTest
  def method(foo, bar)
    puts "Let's see how this works"  
    puts other_method(foo)
    puts another_method(bar)
  end
end
{% endhighlight %}

Every other line I was outputting my variables then trying to decipher what each of them meant. This ends up being some kind of word-vomit printed on screen that I have to spend time trying to decipher.

Instead of having to fumble my way through this output I learned about Pry. Pry is a Read-eval-print-loop (REPL) environment that can be used for code testing and debugging apps in Ruby. Simply use `gem install pry` and you're ready to begin using it. In the command line it functions like IRB and can show you the output of your Ruby code.

{% highlight bash %}
[1] pry(main)> puts "Hello world"
Hello world
=> nil
[2] pry(main)>
{% endhighlight %}

You can use this to try out a new method or algorithm before you insert it into a larger program. Additionally you can use pry to debug in your program. Add `'require 'pry'` at the top of code and insert `binding.pry` into the program where you'd like it to stop running. You will end up with the following in your command line when you run the program:

{% highlight bash %}
    16: def values_for_insert
    17:   values = []
    18:   self.class.column_names.each do |col_name|
    19:     values << "'#{send(col_name)}'" unless send(col_name).nil?
    20:   end
 => 21:   binding.pry
    22:   values.join(", ")
    23: end
{% endhighlight %}

At this point you can look at the variables in your code, manipulate them, and understand what your program is doing. This is a great tool for not only debugging a program but also for understanding your code. I've found pry to be an invaluable tool for working with and learning Ruby.
