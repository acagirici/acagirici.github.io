---
layout: post
title:      "CLI Data Gem Project - Process "
date:       2020-08-21 00:18:42 +0000
permalink:  cli_data_gem_project_-_process
---


That was fun! 

Getting stuck, watching live builds, and doing extensive...extensive google searches pretty much sum up my process. The CLI Data Gem project provided a much needed review and helped me get a better grasp on prior topics in the curriculum. 

I started by contemplating which websites I can scrape and what my application would look like. Ultimately, I decided that it would be fun to scrape a school job website hoping that I could show off to my educator friends that are familar with the site. After watching the CLI Cem Walkthrough, I set up my gem, required all my lib files, and got acquainted with my bin files. I was ready to start coding. 

The most frustrating part was scraping. My initial plan was to do a one level scrape, as all the information I wanted to pull out was in a single link. However, I just could not figure out how to iterate over each of the five categories I wanted pull out and associate my objects with one another. After watching Jennifer's Dealio live build, I got the idea of pulling out the title and link for each job listing then running my link as an argument to do a second level scrape. Within the first level of my scrape, I created a new instance for each job listing with a title and link with the .map method and initialized them in my Job class. In the second level scrape, I pulled out all useful information I thought my users would need before they decided to apply. I used an add_detail method from my Job class to create association between my objects. 

I organized my CLI class similar to the structures presented in the live builds. With call, menu, get_jobs, list_jobs, get_user jobs, show_details, and second menu methods, I was able provide users with a simple and easy to follw interface. Overall, I thought that this project gave me an in depth understanding of object relationships. Just by looking through my classes, I notice the responsibilities that each of my methods and classes have and how the form relationships with each object.  
