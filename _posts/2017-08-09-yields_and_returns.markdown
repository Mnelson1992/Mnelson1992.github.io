---
layout: post
title:  "Yields and Returns"
date:   2017-08-09 13:09:00 +0000
---


Yesterday was a pretty succesful day for me. I didn't get as many labs and lessons done as I would have liked, but I spent time reading about yields and iterations. This turned out to be fruitful as I now have a stronger grasp on how both work. The few labs that I did work on were about the each and collect iterations in the form of yields, and how to control return values from yields. 

Yields are pretty much calling a seperate block in a method and iterating each element of an array into that method. The output will be the result of each element in the array after they have gone through the yield block. Very similar to a basic iteration. However, If you want return a new array with the results of the iteration, you need to explicitly tell the code to do so. THis is because the return value of a while loop is nil. All you need to do is remove the puts, add a new array that will display your return values and use the shovel or .push iterators to place the return values into the new array.

Here is my code that sets up a collection iteration for an array and will return the iteration into a new array:

```
def my_collect(array)
  i = 0
  collection=[]
  while i < array.length
    collection << yield(array[i])
    i += 1
  end
  collection
end
```

As you can see, I have defined the my-collect method to accept an argument of an array. Then I set up a while loop that will go back and iterate over all the elements in that array. You may also notice that I set up a new array called collection. This is the array that will display the returns value from the iteration. I also used the shovel to place each element that has gone through the loop/iteration into my collection array. One of the very last things to remember is to call the new array at the end. The result of this will be a return value for my collection array. 

My goals for the week: 1.) Finish the arrays section of procedural ruby 2.) Finish procedural ruby 3.) Try and get at least 40% done with OO by the end of the week 4.) Get a blog post out every night this week.

Lessons and labs yesterday: 3 Total lessons and labs done: 185 Karma Points : 50
