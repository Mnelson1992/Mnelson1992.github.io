---
layout: post
title:      "Let's look at the basics of Nested Resources"
date:       2018-01-26 02:05:03 +0000
permalink:  lets_look_at_the_basics_of_nested_resources
---


Imagine having just finished building an application you have spent hours on. Eveything looks great, the code is clean and refacotred, the views are beautfully designed with CSS and HTML, and all the models are correctly associated to one another. However, one issue remains. When you go to the routes for your application, you see that it looks insane! However, using nested resources we can refactor our routes to look more appealing and easier for our users to navigate through our application. 
 
So let's start off with what is a nested route. Nested Routes give us the ability to navigate to the following routes                     '/magazines/:magazine_id/ads' & '/magazines/:magazine_id/ads/:id' . We get magazine_id from the nested resource set up that you see below. A nested resource builds off of the association "has_many" & "belongs_to". In order to fully understand how nested resources work, we are going to use the following models: magazines and adds. Our associations would look as follows:

									 `class Magazine < Activerecord::Base 
                          has_many :ad 
                   end' 
									 
									 
									 `class Add < Activerecord::Base 
                           belongs_to :magazine 
                   end `
									 
									 
									 
Our routes will look as follows:

resources :magazine do 
         resources :ads  
end 

Our index controller action for ads would look like the following:

                `class AdsController < ApplicationController 
								      def index
											      if params[:magazine_id]
														     @magazines = Magazine.find_by(params[:magazine_id]
																 @ads = @magazines.ads
														else
														     @ads = Ad.all
														end
											end `
											
So how does the above actually work? Well we first check to see whether or not there is an id for magazines within the ads table. If there is then we retrieve that magazine by finding the magazine_id. Then we collect all the ads that are associated with that magazine and set it to the instance variable @ads that can be used to display in our view (index.html.erb). If there isn't a magazine_id, then it will simply display all of the ads that are in our database.
								
