---
layout: post
title:      "Sinatra Meeting Tracker App"
date:       2021-02-08 20:23:26 +0000
permalink:  sinatra_meeting_tracker_app
---


Going into the Sinatra project, I knew that I wanted to create a management system for meetings. I thought it would be good to have a meeting tracker where I can take notes and track client progress.  I utilized the corneal gem to set everything up and worked my way through the application after deciding that all I needed was two models: users and meetings. 

After creating my tables and running my migrations, I began going through the project requirements. Going back and forth between my controller and views, I was able to create the necessary functionality for my users. I found the labs in prior lessons as a useful reference to guide me along the way. My meetings_controller handles everything regarding the tracking meetings. It features all of the CRUD functionalities and follows the RESTful conventions. Preventing users from viewing pages without being logged in required some research. I knew I had to create a helper method, but I did not want to if statements in each of my routes to handle this. This is where the before filter came in handy.  

By adding this filter, I was able to require authentication for all meetings routes. 
```
class MeetingsController < ApplicationController
    
    before '/meetings/*' do
        authentication_required
    end

    get '/meetings' do
        authentication_required
        @meetings = Meeting.all
        erb :'meetings/index'
    end
```

After finishing up my CRUD routes, I played around with different view options and decided to add numbering to my index page in meetings where all meetings are displayed. To do that I created a new syle sheet and linked it to my view page. 

```
.counter {
    list-style-type: none;
    counter-reset: css-counter 0; 
  }
  
  .counter h4 {
    counter-increment: css-counter 1; 
  }
  
  .counter h4:before {
    content: counter(css-counter) ". "; 
  }
```
 
 I thought that the styling was necessary to make the view page more organized. 

Overall, the project was a great review of the Sinatra module. It helped me better understand some concepts that did not stick as well. I definitely look forward to building more complete apps and webpages as I learn about Rails in upcoming lessons. 

