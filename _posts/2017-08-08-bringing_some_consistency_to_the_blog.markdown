---
layout: post
title:  "Bringing some Consistency to the blog"
date:   2017-08-08 12:59:14 +0000
---


The past few weeks have been crazy busy with work and learning code everynight. Thankfully work has started to slow down for the year, so now I can invest more time developing my coding skills. With that being said I am going to start trying to put up a blog post everyday. This post will outline what I did for the day, how many lessons I got done, my goals for the week, and examples of the labs and codes that I ahve worked on. I'm also going to leave a report of how many Karma points I gain every day. I believe that one of the best ways to learn something is to teach others. With Flatiron, everytime you answer another student's questions you get a Karma point.

Last night I spent about 4 hours working on the ruby iterator labs. So far procedural ruby has been pretty easy for me to grasp. However, iterators aren't following suit, so i'm spending a little more time ont hem to try and grasp a better understanding of how they work. With every lab I gain a better sense of how the enumerables affect arrays.

The 2 major learning labs that I worked on last night were the Deli Counter and the Reverse Word labs. 

Deli Counter

```
# Write your code here.
def line(katz_deli)
  if katz_deli.length == 0
    puts "The line is currently empty."
  else
    deli_line = "The line is currently:"
    katz_deli.each_with_index do |element, index|
      deli_line += " #{index+1}. #{element}"
    end
    puts deli_line
  end
end

def take_a_number(katz_deli, name)
  katz_deli.push(name)
  puts "Welcome, #{name}. You are number #{katz_deli.size} in line."
end

def now_serving(katz_deli)
  if katz_deli.size == 0
    puts "There is nobody waiting to be served!"
  else
    puts "Currently serving #{katz_deli.shift}."
  end
end
```

What I found most interesting about this lab was the fact that you had to apply all knowledge of arrays in order to complete it. For instance I had to use the .length enumerable and set it equal to 0 to show that if there was no one in the line (the array was empty) it would output the string of the line being empty.


My goals for the week:
     1.) Finish the arrays section of procedural ruby
     2.) Finish procedural ruby
     3.) Try and get at least 40% done with OO by the end of the week
     4.) Get a blog post out every night this week. 

**Lessons and labs yesterday: 5
  Total lessons and labs done: 182
  Karma Points : 50**


