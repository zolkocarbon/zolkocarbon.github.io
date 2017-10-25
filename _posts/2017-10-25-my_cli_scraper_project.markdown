---
layout: post
title:      "My CLI Scraper Project"
date:       2017-10-25 13:58:08 -0400
permalink:  my_cli_scraper_project
---


For my first FlatIron project I chose to scrape my local theater for movies playing.

Originally I wanted to create a CLI that would accept a zip code to show the nearest theaters but I quickly realized that I don't know the coding logic required to do this. Therefore I changed the project to simply scrape the movies playing at all AMC theaters and have the option to get more information about a movie by scraping the detail page of that movie. 

The first challenge came when I saw the file structure in the examples. I didn't understand how they created those files, why I kept seeing the same files in all the examples and how to create my own. This was all confusing until I actually watched the lessons video and saw that the files are created automatically when you run "bundle gem -m." The -m is replaced by the file name of the gem you desire. 

After the file structure was there the next part was deciding how to start. At the time it seemed so confusing and the only way I got through it was by building it piece by piece. Plenty of scraping examples in the lessons so that was the first piece. However, at first I made all the methods instance methods. But why do we need an instance of a scraper. We don't need the behavior of an instance so why not just use the scraper as a class method. A few "self" statements along with a change in how we call the scraper class and it was done.

When it came to the movie class a instance for each movie did make sense. Each movie will have its own unique properties such as title and plot so creating instances of each movie is appropriate. What I like about the program structure is that each instance of a movie is only created with a title. Only when a user request more information about a particular movie is the instance populated with more data by scraping the appropriate page. This saves time and keeps data size to a minimum. 


The first time I saw the CLI populate with movie titles scraped from a live website I got very excited. How cool? The code I wrote pulled selected information from an external source!

Chris Ziolkowski
