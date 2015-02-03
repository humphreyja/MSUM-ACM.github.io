# msumacm.org

Our main website at [msumacm.org](http://msumacm.org)

* Shout out to Jason Mayes for the javascript Twitter Post Fetcher 


This project currently contains -  
- Main Blog
- Workshops & Events
- Pages
    - Officer List
    - Mailing List Instructions

Building the website
- compile using jekyll build
	- it may be jekyll2.0
	- use jekyll build --watch to watch for changes and automatically build
	- use jekyll serve to start a webserver to see your changes
- The css is generated using sass.  Use jekyll's built in sass generator to compile the css when it compiles the website.


How to add content to the website.
- Twitter is automatically pulled in
- Posts
	- Create a post file with name like year-mo-da-name-of-post.markdown
	- Add '---' at the top of the file. 
	- Depending on the type of content added the following will be added to the file
	- Events
		- Required yaml tags
			- layout: post
			- title:  "<title of post>"
			- date:   year-mo-da hr:mi:se  
			- event-date: year-mo-da hr:mi:se #This is important as the website displays different content based on the date
			- author: "<name of presenter>"
			- location: BR 165/166  #most likely
			- duration-in-minutes: 60 #most likely
			- presentation-data: #can be left blank or will be a link in http://... format
			- categories: events
	- Reminders
		- Required yaml tags
			- layout: post
			- title:  "<title of reminder>"
			- date:   year-mo-da hr:mi:se
			- categories: info
			- location: BR 165/166
	- Articles
		- Required yaml tags
			- layout: post
			- title:  "<name of article>"
			- date:   year-mo-da hr:mi:se
			- author: "<author of article>"
			- minutes-to-read: <aprox time to read in mins>
			- categories: article
	- Close the yaml tags section with '---'
	- Below that in plain text, write the content of the post.
	- Use appropriote html tags for links and images/videos etc.
- Content is displayed based on the date.
	- Articles have no date restriction.
	- Reminders will show up for a month before the event and will disappear afterwards.  
	- The current event will show up a week before the event and will move to the past events section after the presentation date.  
	- Future events will show up in upcoming events until the week it will be presented.
- There are 2 rss feeds for the website.  The main page one is to subscribe to articles. There is a second one on the events page for sending out the current events.