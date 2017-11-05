---
layout: post
title:      "Learning the basics of Sinatra"
date:       2017-11-05 21:32:57 +0000
permalink:  learning_the_basics_of_sinatra
---


Last week I finished off rack and began Sinatra. It is amazing to see what the code that I write actually renders on a web page. I believe that I am finally becoming comfortable with my skills as a programmer, which has given me a boost of motivation to learn as much as I can about various aspects of coding. So far Sinatra has been very interesting and easy to follow. I want to take it somewhat slowly so that I have a genuine understanding of what I have learnt, so that I will be more than prepared for my Sinatra final projects. 

In this blog post I will be going over the two important aspects of Sinatra (the files types and Sinatra Routes). There are 2 files that are crucial to have in order for a Sinatra Web Application to run successfully. The 2 files are a App.rb file and a Config.ru file. The App.rb file is the heart and soul of a Sinatra app. It is the Controller of the Siantra web application and is where we define our routes to various parts of our application. A basic App.rb file looks like this:
                
								require_relative 'config/environment'
								class App < Sinatra::Base 
								     get '/' do 
										 "Hello World" 
										 end  
								end 
								
In this file we require our config/environment file which sets up our environment. Then we define a class called App, which inherits from Siantra::Base. After setting up our class we can define routes to various locations of our web application. 

The next important file is the config.ru file. An example of this file is as follows:
                require 'sinatra'
                require_relative './app.rb'
                run App
								
								
In this file we are requiring the Siantra gem. This will give us access to the Sinatra library. We are calling require_relative on our app.rb file so that we can have access to its defiend routes. and the we are calling 'run App' which will start the application for us. It is very important that the class defined in the app.rb and the 'run App' line in the config.ru file match. Otherwise, the program won't work correctly. 

Routes are an important part of your web application as they tell the program where the client has requested. Routes connect HTTP requests to a specific method in your application code built to handle responding to such a request. Think of it as your Controller Application. Routes will live in your app.rb file. Routes basically send a request to get a certain URL. Once the methods in your application are mathced to that URL, the code will be executed.

A simple Route is a follows: 

           get '/' do 
					   "Hello World!" 
					 end 
