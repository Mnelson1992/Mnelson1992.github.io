---
layout: post
title:  "The OO journey so far"
date:   2017-09-11 23:08:35 +0000
---


I have spent the past 3 weeks working on the Object Oriented Ruby section. After working on the first few lessons and labs of the OO section, I found that I enjoy it more and understand it better than the procedural section. So I have been spending more time on it to ensure that I understand and memorize all the concepts and fundamentals of it. I found that thinking of OO as unique objects that arise from instantiation significtantly helps when trying to understand the concepts. 

OO begins with a class. Once you have a class you can use an instantiation method to set up evey new instance with a unique set of attributes. For example, you can do the following:

```
class Person
    attr_accessor :name, :age
		
		def initialize (name, age)
		    @name = name
				@age = age
		end
```

This allows you to call the Person.new moethod in an instance and it will let you provide the new instance with a name and age

Beyonce = Person.new("Beyonce", "31")

OO also has 2 different method types, Instance methods and Class methods. Instance methods only apply to the instance that gets instantiated, and class methods apply to the entire class. Instance methods are defined by (class run), class methods are defined by (class self.run)

Variables are also a little different in OO than they are in prodecural ruby. Instance variable are defined by (@age), class methods are defined by (@@age).

OO allows us to create methods that are easily refactorable by using modules, inheritance, and object relationships. 

These past few weeks have been a little crazy. Trying to balance coding and work has gotten a little difficult, but I make my best effort to get at least 4 hours a night. 

Lessons completed : 225
Karma Points : 122
