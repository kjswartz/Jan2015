# Monday

## Weekly survey
* https://www.surveymonkey.com/s/RDF8QZN

## Thoughts on testing?

## Discuss Final Projects

### Groups
* First, only eligible to be on a group project to demo if you are 100% caught up on homework by Monday.
* Second, I highly recommend against it. It will be much harder to make a good impression. If you do groups, then you need to have three weeks worth of work that you can clearly point out your contributions. I will expect much more from your app. The app should be unbelievably polished. Test cases should be included.
* All in attendance last time were blown away that everyone built what they did in three weeks with no experience coming in. But it will be much harder to impress them when they know more than one worked on it.

### Ideas
* Thursday you will present your ideas to the class. The class and myself have to green light what you are doing. We will review the concept and the scope to ensure you pick something that is both possible in the time given and will reflect your skill level.
* Talk to me this week if you have no ideas.

### Not automatic that you will present
* Presenting is an earned privilege. You don't get to present automatically. Your app has to be of sufficient scope and quality, including it's presentation, in order to be approved to present. The staff here will watch your pitches in the final week and then let you know who will be able to present.

### Presentation Practice
* You will practice pitching several times in front of the class, and you should practice many, many times on your own.
* You will have five minutes to present both yourself and your app. Make sure you state who you are, what and you were doing prior. If you have a backstory on what led you to chose your app, be sure to share that too. Help them connect you to your idea. Personalize it!

## Eager Loading
* Show rake task example in Instagram app
* Note however, that in this example it loads ALL the post comments whereas without eager loading them we were only loading 10 comments. Have to weight this.
* http://guides.rubyonrails.org/active_record_querying.html#eager-loading-associations

### Assignment 57
* Read the following two articles by DHH on testing [Test Induced Design Damage](http://david.heinemeierhansson.com/2014/test-induced-design-damage.html) and [TDD is Dead, Long Live Testing](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)
* Review the [Rails guide on Eager Loading](http://guides.rubyonrails.org/active_record_querying.html#eager-loading-associations)
* Modify your Pinterest app to use eager loading in at least one place. Confirm in your logs that it has reduced the number of database queries.
* Try to find a place to use it that will not result in loading more data than necessary.

## Mailers
* Need to send a welcome email (or often other emails too)
* Use [letter opener gem](https://github.com/ryanb/letter_opener) so we can see emails in our browser.
* Add a welcome email to the sign in process and get working on Heroku
* http://guides.rubyonrails.org/action_mailer_basics.html
* Generate a mailer class, to group emails under, and generate a welcome email

```
rails generate mailer UserMailer welcome
```

* Modify the HTML and TEXT versions. Why do we use both?
* Send the email at the proper time (deliver_later)
* Need to set up an email service on Heroku
* [Sendgrid](https://addons.heroku.com/sendgrid)
* Add service. Run `heroku config` after to see SENGRID account info has been added
* [Installation of sendgrid](https://devcenter.heroku.com/articles/sendgrid#ruby-rails)

### Assignment 55
* Read the Rails guide on [Action Mailer](http://guides.rubyonrails.org/action_mailer_basics.html)
* Add a welcome mailer to the sign up process in your Pinterest app
* Get it working on your laptop first, using the [letter_opener gem](https://github.com/ryanb/letter_opener)
https://devcenter.heroku.com/articles/sendgrid#ruby-rails
* Next, deploy to Heroku and setup with sendgrid
* Ensure emails are being received by users when signing up on Heroku

# Tuesday

## /about
* Final project suggestion
* Create an /about page that has your name, links to your Twitter, GitHub, LinkedIn and blog
* Your avatar
* Lists the tech stack used
* Close your talk by going to the about page
* Possibly even create a tinyurl.com to share for audience to jot down to land on that /about page.

## RubyKoans reminder
* Ruby Koans are part of something I do with every class and always will. Other Rails instructors here at TIY do as well.

## Difference between using a foreign key and the association
* In my Instagram app
* Post model
* Show SQL diff between:

```ruby
p = Post.first
p.user_id
p.user
```

* keep in mind, to not load the entire user object if you don't need it
* also, you can't walk an association using the foreign key
* can't do this: `p.user_id.name`
* to get the name from the user object, you need the user from the db, ie. there must be an sql query, which means, you must use the association: `p.user.name`

## Let's plan an app: discussion forum & user stories
* What features will it have?
* What data is necessary? What models will we use? What attributes?
* What pages will we need?
* User stories: What should the user be able to do?
* The visitor should be able to see the home page
* The visitor should be able to click to login

## Is TDD Dead?
* [RailsConf 2014 - Keynote: Writing Software by David Heinemeier Hansson ](https://www.youtube.com/watch?v=9LfmrkyP81M)

# Wednesday

## Quiet in my room, please
* if you want to have a discussion take it outside the room
* that is one of the reasons I sit out in the main space so we aren't having discussions in there
* a developers number one friend is uninterrupted quiet time with no background noise or conversations

## Devise
* another Rails instructor said, "Now three of my groups have been using it for their final projects and wished they never heard the word Devise."
* never want to use gems like devise to replace knowledge
* example: I showed you how to create CRUD interfaces for admin'ing data BEFORE I showed you ActiveAdmin.

## Intro to Javascript
* We can't get into JS super deep like front end. My goal is to give you a general knowledge.
* You can take that knowledge farther if you choose.
* Help them get it setup with console.log and see that in their Chrome dev tool

### Assignment 58: Intro to JS and jQuery- in class
* Create an HTML page
* Create a Javascript file and include it in the HTML
* Read through this [JavaScript Basics](http://jqfundamentals.com/chapter/javascript-basics) and put all the examples in your JS and ensure they run, show the proper output in the console and that you understand the basics.
* Note: Use `console.log` where the demo shows just `log`.
* Note: The _this_ explanation is a tricky thing in JavaScript. Don't get bogged down by it. jQuery will help with that.
* Check the two HTML pages and two JS pages we created in class (and perhaps a css if you used one).

## Intro to JQuery
* continue with tutorial
* class now creates another HTML page and JS for jQuery demo

## Bootstrap Javascript
* http://getbootstrap.com/javascript/

## jQuery plugins
* http://plugins.jquery.com/
* http://dimsemenov.com/plugins/magnific-popup/
* http://blueimp.github.io/Bootstrap-Image-Gallery/
* http://plugins.jquery.com/chosen/

### Assignment 59: jQuery
* Add a [jQuery plugin](http://plugins.jquery.com/) to your Pinterest app
* Be sure to direct me to where on your app you've added it, both in your code and what page it's running on at Heroku so I can see it work.

# Thursday

## Learning isn't over
* final projects is still part of the learning process

## Show everyone CodeSchool
* Show the [Try SQL](http://campus.codeschool.com/courses/try-sql/)

## We are just doing a brief walk through of Javascript technologies
* enough that you gain some familiarity with it and so that you have a starting point for further learning if you desire to get more into it.
* we did JS and jQuery yesterday, today we'll look at a few more JS related technologies

## CoffeeScript
* What is it?
* http://coffeescript.org/#overview
* everyone open one of their apps, view the page source and then a JS file so we can put coffee in and see the results
* Show coffeescript compiled in browser
* Walk through Table of Contents
* http://js2.coffee/

## Working with JavaScript
* http://guides.rubyonrails.org/working_with_javascript_in_rails.html

### Ajax
* Show my fake name list and button to add to the list
* Currently returning HTML, can return JS

### UJS
* Show adding vowels class which allows us to click on the vowels
* Show the chosen jQuery plugin and how it works: http://harvesthq.github.io/chosen/

### Turbolinks
* Show what it does, how it works
* Could be the problem some of your are having with chosen not always working, unless you refresh
* I forget turbolinks is there because it's addition to rails is new

### Assignment 60: CoffeeScript
* Review the Rails guide on [Working with JavaScript in Rails](http://guides.rubyonrails.org/working_with_javascript_in_rails.html)
* Refer to the [CoffeeScript docs](http://coffeescript.org/)
* Write some CoffeeScript in your Pinterest app to listen for a click on the header/logo of your app (in the nav), and when clicked, popup a bootstrap modal with some about information for your app.
* Bonus: Use Ajax in one place in your Pinterest app (deleting an item, adding an item, etc)

## Students present their ideas
