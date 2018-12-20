---
layout: post
title:      "Linda's Rick And Morty CLI - Project #1 "
date:       2018-12-20 13:18:10 -0500
permalink:  lindas_rick_and_morty_cli_-_project_1
---


For my first project, I decided to scrape the Rick And Morty API website to create a character finder as well as a random character generator. 

Setting up the project was the first obstacle I came across. I was very unfamiliar with how to set up a terminal or run a test since I was so used to using the Learn IDE. However, the video walkthroughs provided were very helpful for setting it up. The rest was more of a trial and error on tying to figure out how to get the tests to run.

The first obstacle I experienced was a code block when I was trying to scrape the website. I was walking in circles trying to figure out how to access the data. I was able to scrape it but since it was not in ruby format it was difficult trying to figure out how to grab all the relevant information. Then I met with Dakota who helped me turn the code into readable Ruby using JSON to parse the data into a variable. The website data was parsed and turned into a hash which was a lot easier to iterate through to create all the character objects. With his help I was also able to create all the objects in my scraper.rb and scrape through all 25 pages and have all 493 characters saved as objects in my characters.rb `@@all `array. 

```
def get_characters_from_page(url= "https://rickandmortyapi.com/api/character")
    data = open(url).read
    response = JSON.parse(data)
    response["results"].each do |character_hash|
      RickAndMortyCli::Character.new(character_hash)
    end
    next_url = response["info"]["next"]
    if next_url != ""
      get_characters_from_page(next_url)
    end
  end
```


This is when I was able to create my random character finder which generates a random number. I set a variable x equal to the length of the @@all array. I also created a number variable which stores a random number between 1 and x. Then I was able to grab the character information and interpolate it into a string so that it is easier to read in string form. 


```
def self.find_random
      x = @@all.length
      number = rand(1...x)
      @@all[number]
      puts "Name: #{@@all[number].name}"
      puts "Species: #{@@all[number].species}"
      puts "Status: #{@@all[number].status}"
  end
```

My find by name method asks users to type in a character's name to find out more about them. This is a method that goes through the array of characters and finds the name that the user typed in and prints out all the relevant information.  Note: I had to add the ID's in the character finder since there are multiple universes and multiple Rick and Morty's so the names come up more than once. You can tell the diffference by their status of dead or alive but mainly by their character ID's. 

```
def self.find_by_name(name)
    @@all.find do |character|
      if name == character.name
        puts "Name: #{character.name}"
        puts "Species: #{character.species}"
        puts "Status: #{character.status}"
        puts "Id: #{character.id}"
      end
    end
  end
```

It was really satisfying to see my code working in the end but there was a lot of times when I felt like I wasn't confident my code was going to work. I had to use binding.pry a lot. I also felt like a lot of the times I was over complicating what had to be done in my head which meant I needed to walk away and listen to my advice in the [previous blog post](https://lindachang186.github.io/top_3_ways_to_deal_with_coders_block). 

But now you can check out my project on github. It interacts with the user and asks them if they want to find a character or if they want to generate a random character! That's my project in a nutshell...and as Rick would say Wubba-lubba-dub-dub!

