---
layout: post
title:  "Lets talk about some basic loops!"
date:   2017-07-17 14:25:36 +0000
---


What is a Loop? Well, a Loop is simply a way to repeat a line of code over and over adn over until a certain condition is met.  Loops have their advantages to programmers, but also have disadvantages. One of the biggest advantages include being able to repeat a line of code, or a block of code over and over again without having to rewrite the code. This allows the programmer to write clean concise code that doesn't take up too much room. A major diasdvantage, however, comes in the form of an infinite loop. That is a loop that doesn't end as it does not meet the conditions to return true and terminate.

The two main forms of loops that we have been taught are while and until. These pretty much can be used interchangeably. The while loop tells the code to run as long as the boolean expression(conditional) returns true. The until loop tells the code to run until a conditional has been met or returns false. Both of these loops are very useful when trying to build complex methods that require constant checking of a condition. Which one to use in a method really depends upon what you are trying to achieve in your code, but it doesn't matter which of the two you choose.

I recently used a loop to finish building my Tic Tic Toe game. Specifcally the Play method. This method combined all of the methods that we had built beforehand (A.K.A helper methods). I used the while method to basically say, while the game is not over return the turn method I had built. Once the game was over the while method no longer ran as it had met the condition and returned true, that the game was over. 

Below is a the while loop I built:

while !over?(board)
    turn(board)
  end
