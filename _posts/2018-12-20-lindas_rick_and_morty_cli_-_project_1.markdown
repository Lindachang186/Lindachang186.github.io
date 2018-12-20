---
layout: post
title:      "Linda's Rick And Morty CLI - Project #1 "
date:       2018-12-20 18:18:09 +0000
permalink:  lindas_rick_and_morty_cli_-_project_1
---


For my first  project, I decided to scrape the Rick And Morty API website and create a character finder and random character generator. 

Setting up the project was the first obstacle I came across. Only because I was unfamiliar with how to set up a terminal or run a test since I started I was very used to just using the Learn IDE. However the video walkthroughs were very helpful for setting it up. The rest was more of a trial and error on tying to figure out how to get the tests to run and such.

I also experienced a code block when I was trying to scrape the website. I was walking in circles trying to figure out how to access the data. I was able to scrape it but since it was not in ruby form it was difficult trying to figure out how to grab all the relevant information. Then I met with Dakota who helped me figure out how to turn the code into readable Ruby. 

With his help I was able to create all the objects in my scraper.rb and scrape through all the pages and have all 493 characters saved as objects in my characters.rb. Then I created a random character finder which generated a random number between the size of the array holding all the character objects and 1. This would then print out random characters using the index (which is the random number generated). I also created a find character method which helps users type in a character name to find out more about them. This is a method that goes through the array of characters and finds the name and prints out all the relevant information. 

It was really satisfying to see my code working in the end but there was a lot of times when I felt like I wasn't confident my code was going to work. I had to use binding.pry a lot. I also felt like a lot of the times I was over complicating what had to be done in my head which meant I needed to walk away and listen to my advice in the previous blog post. 

But now you can check out my project on github. It interacts with the user and asks them if they want to find a character or if they want to generate a random character. 
