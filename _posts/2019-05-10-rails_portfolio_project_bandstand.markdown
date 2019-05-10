---
layout: post
title:      "Rails Portfolio Project | Bandstand"
date:       2019-05-10 14:15:59 +0000
permalink:  rails_portfolio_project_bandstand
---


For my Rails Portfolio Project, I created an application called Bandstand. The app is meant to be a meeting point for live music lovers everywhere. Users both big and small can add events to the calendar, whether it's a concert promoter alerting the public about a big upcoming show, or a local band trying to promote their upcoming jam session at a small neighborhood venue. Users can see what concerts are playing and where, as well as past shows they may have missed.

I used basic sign up and login forms for users, but also gave the users the option to login with their Google accounts. Login error messages are displayed, when necessary. Once a user is signed up or logged in, she is redirected to the index page displaying all the concerts that have been added to the application. These are displayed in inverse chronological order, with upcoming shows at the top. If a concert has already taken place, the message "Sorry, you missed this show!" appears alongside the other concert information. 

From here, the user can click on a concert title and see additional details, such as the name of the user who added the particular event. If the logged-in user is the same as the user who created the event, they have the additional options to edit their event information or delete the entry altogether. 

The index page is always accessible through a link at the top of each page, which was set up in the application layout. That's also where the user can opt to log out, as well as access her profile, which displays all the events created by the logged in user. Each user can also choose to add a new concert or add a new venue, should it not already exist in the venues list. 

In terms of improvements, I would add a social layer to the application, giving users the option to express interest in attending a particular event. The community-at-large would then be able to see how many people are interested in a particular concert and which specific users are planning on attending. I would also improve the look and feel of the whole application with CSS styling.




