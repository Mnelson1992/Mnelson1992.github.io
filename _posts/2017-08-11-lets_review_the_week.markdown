---
layout: post
title:  "Let's review the week"
date:   2017-08-11 13:38:05 +0000
---


This week went by way too fast. I didn't get as much done as I wanted to, but I did gain a better understanding of iterators. So I'm counting that as a win. Last ngiht I finallly finished the arrays section of procedural ruby. I am feeling pretty proud of myself as this was one of my goals for the week. Only a few more section to go then I will be onto OO!

Last nights lesson included the .sort method. This methd takes an array and sorts it based on the conditions you set for it. You use comaprables just as you would for comparing an array, however, this time you have to give 2 elements for it to compare. The layout for a .sort method is as follows:

```
def example(array)

        array.sort do |a,b|
				if a == b
				    0
				if a > b 
				   1
				if a < b 
				   -1
				end
end 
```

* if the 2 values are equal, it will return 0 and leave the 2 elements in place
* if a is greater than b it will return a -1 and switch the 2 elements
* if a is less than b it will return 1 and leave the elements in place

A way to abstract you code is to use the <=> spaceship

```
def example(array)
   array.sort do |a,b|
	   a <=> b
	end 
end 
```

This basically says everything the code above says., but it makes it easier to follow, and keeps you code concise and easy to read. 

Lessons Completed: 5
Total Lessons Completed: 194
Karma Points: 56
