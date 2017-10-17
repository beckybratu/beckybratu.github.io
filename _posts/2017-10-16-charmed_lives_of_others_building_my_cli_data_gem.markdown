---
layout: post
title:      "Charmed Lives of Others: Building My CLI Data Gem"
date:       2017-10-17 02:14:46 +0000
permalink:  charmed_lives_of_others_building_my_cli_data_gem
---


If only I could get myself to start. In the beginning, sitting down with a notebook and a pen, every idea that crossed my mind seemed stupid. Too easy. Too difficult. Too predictable. Others have already thought of this. Nothing was good enough for this project. Mind you, all this pressure was internal, but I still couldn't get myself to start working on it. Simultaneously, I felt guilty about procrastinating. I finally had to admit to myself I found the project daunting, had to suck it up and get to work. 

Before deciding on an idea, I watched and re-watched Avi's Daily Deal video walkthrough, which shows you how to use Bundler to quickly and orderly build your gem's structure. For all of you out there about to embark on this project, this step is essential. 

Then, as I tried to narrow down my list of possible projects, I turned to my job for some inspiration. 

In my day-to-day, I am a journalist. As reporters, there are certain evergreen stories we get to tell year after year, whether it's the list of the 10 most popular baby names in the United States, what the most wanted Christmas toy is this year, or who the richest people in the world are. Publications such as Forbes and [Bloomberg](https://www.bloomberg.com/billionaires/) have built a whole apparatus around the big reveal of the year's richest billionnaires -- and it was the news coverage around this list that sparked my gem idea. 

It turns out that thanks to the fluctuating nature of financial markets, this list is a living and breathing thing that makes news more than just once a year. Those billionaires switch rankings sometimes several times a day, although dethroning the man at the top of the list is still a rare occurrence. This year, second-ranked Amazon CEO Jeff Bezos, who was having what I presume was a very financially successful day, took the number one spot from Microsoft founder Bill Gates and held on to it for a day or so. Gates reclaimed the title pretty quickly, but with a paltry $2 billion difference between the two men's net worths, it's likely we'll see some changes again pretty soon. Enter my CLI gem, "bratu_world_richest."

At its core, the gem scrapes Bloomberg's billionaire list, printing out the top three richest people in the world along with their net worth. The user can then pick one of the three billionaires from the list to learn a little bit more about him, such as his country of origin and the industry they operate in. The finished product now [lives on GitHub](https://github.com/beckybratu/bratu-world-richest) -- check it out.

When first running the program, the user is shown the up-to-the-minute list of the world's richest. The user is then invited to choose one of the three people on the list to find out a bit more about them. There are also options to go back to the main list or exit the CLI altogether. 

On the inside, the gem consists of three main files, *cli.rb, richest.rb* and *scraper.rb*. 

The CLI consists of a general call method that compiles the main three methods that do all the heavy lifting: the Richest class method ".now," list_richest and the menu. The ".now" method takes the information collected by the scrapers and records it into an array. List_richest then looks at the @@all array (saved in an ".all" method in my Richest class) and iterates over it. The output is an ordered list containing the billionaires' names and net worths. The menu method starts by offering the user the option to select one person on the list to get to know better. I wrote this as a case method, a statement for each option the user has. The CLI concludes with a brief goodbye method that puts out a string. 

As the scraper methods were crowding my *richest.rb* file, I decided in the refactoring phase to move them to a separate file. There is a scrape method for each rich guy, as each represents a row in the table on Bloomberg's list. The scraped information includes name, networth, industry and country of origin. 

Finally, these scrapers feed their information into the Richest class' ".now" method. This also relies on the ".all" method, whose array contains all of the scraped instances. 

I have enjoyed going back to my gem and seeing how the rankings have changed over a period of time. It feels good to build something from scratch. 
