# Monday

## Fear cards and class survey
* Apologies that I failed to review you fear cards early last week. I always have in the past, but last week just flat out beat me.
* Then, when I did review them there was very clearly confusion over the ranking system we are using. That's my fault. I need to do a better job making it clearer. Some of you changed your fear numbers so drastically you must have thought the ranking was going in the opposite direction.
* I think it's much more telling for me to use the "fear" terminology than comfort levels. The challenge is that while you may feel very comfortable, you can still be very afraid you aren't going to be where you need to be. And in fact, your results indicated exactly that.
* I'll be following up with you each individually this week to discuss your progress, and how you feel you are doing in your journey to become a developer.
* One thing you shouldn't be using these surveys for is a cry for help. Don't put numbers down and then hope someone comes and talks with you. While I fully to intend to do so this week, that philosophy will not serve you well at a job. On the job, you must take initiative to talk to your manager or whoever you report to if you are feeling uncomfortable. You cannot sit back and hope someone realizes you are struggling.
* Waiting around for someone to give you unsolicited feedback may result in a surprise termination. I've seen it happen many ties.
* This week, to be more clear in the survey, I've created an online one: https://www.surveymonkey.com/s/RDF8QZN

## Don't wait for someone to notice you need help
* This is a sure fire way to get let go from a tech job.
* Justin himself had to let a jr dev go for this reason and one of our founders shared a story of a graduate who recently lost his job for the same reason.
* Most all tech jobs want developers who can manage themselves; who can solve their own problems and who will proactively seek help from online, peers, mentors and Sr. Devs.

## Question: Which is the most important characteristic for a software developer to have?
- [ ] Pleasant disposition
- [ ] High IQ
- [ ] Passion for software development
- [ ] Desire to earn big bucks
- [ ] Knowing how to find solutions to problems
- [ ] Ability to memorize APIs
- [ ] Understanding of software development principles

## The passion
* Just as Bob Damato at Valpak said, passion is most important.
* "Passion for software development" will lead to all the others
* How do you know if you have the passion? What does it look like?
* If you have the passion, you'll stick with a problem until you get it, thereby, over time, learning how to solve problems on your own.
* You can't stop writing code. You do it so often, you memorize APIs and become familiar with software development principles.
* When you need to take a break from coding, it won't be very long before you just have to get back to it again.
* You have to constantly be reminded to come ask for help because your default mode is to want to solve it yourself without asking for help.
* That's great, but, particularly when you are a junior developer, and in a 12 week course, you can't try and solve a problem by yourself for three days when it's due the next day.

## The important of struggle
* It's important to understand, completing the assignments is not the number one goal here.
* http://scontent.cdninstagram.com/hphotos-xaf1/t51.2885-15/e15/11055472_346952545508202_216365713_n.jpg
* So what is the number one goal? Learning how to code, how to get unstuck, how to learn new things and when to ask for help.
* As well, it's learning how to work with your sr devs/manager, and your peers.
* Which means, if you get stuck on an assignment your first thought should not be that you want help so you can get it done quick and get the assignment checked off. That would be the goal if you think checking off assignments equals making you a good developer, which it doesn't.
* It's the process of figuring out problems that will make you a good developer.
* If I, or a peer, or anyone else, hands you the answer, or plops you down right in front of the answer, it will defeat the entire point of the assignment.
* Analogy: a baby is learning to walk. She naturally has the desire to do so because the baby wants to get to point B from point A. The baby takes his first step and falls down. If the parent sees this, and every time the baby starts to walk, the parents picks her up and carries her to point B, she will never, ever learn to walk. The baby must go through the process of trying and stumbling a thousand times. Only then will the baby both conquer walking, but also build some inner confidence to take on the next learning challenge.
* The parent is there to encourage the child, protect the child, at first perhaps even move the child's legs at first until the child's nature kicks in. Eventually, the child must fail on his own to ever make progress.
* This is why I want you to struggle. I want you to go through 100 possible solutions before you get it. That is how you will become a software developer, not through any other means.
* If you hate the process of trying 100 things and having them all fail, I promise you, you will hate being a full time software developer.

## QA for weekend homework
* Where did you get stuck?
* Anyone get stuck on something and can show how they got past it?

## SCSS
* http://railscasts.com/episodes/268-sass-basics
* Note, when you are using something like bootstrap, you want your custom css to be listed below bootstrap
* also, if you are using bootstrap you can stop including scaffold
* as mentioned before, probably don't want to require tree when we have active admin in place

## Assignment 52
- [ ] Read the [Asset Pipeline Rails guide](http://guides.rubyonrails.org/asset_pipeline.html)
- [ ] Read through the [SASS Basics guide](http://sass-lang.com/guide)
- [ ] Use SASS in one of your past apps, and ensure you do the following:
- [ ] Change your application.css to be a SASS file and to use `import` statement instead of the require tree.
- [ ] Ensure your custom css is listed in your layout file below bootstrap, so they override any bootstrap files
- [ ] Create and use at least one partial. Suggestion: place a few color variables in a `colors` partial
- [ ] Ensure the scaffold.css from the Rails scaffold generator is no longer in use
- [ ] Use the `darken` function to have one color be auto darkened off of another.
- [ ] Set your site's background color via a variable
- [ ] Use a few "nested" styles
- [ ] Setup [bourbon](http://bourbon.io/) in your app
- [ ] Look through bourbon's mixins and use at least one in your app. Find them in the [documentation](http://bourbon.io/docs/)
- [ ] Link to the repository for the app where you made these changes
- [ ] Also link to the Heroku app where the changes are visible. Be sure to let me know which page to look at on the app if not the home page.

# Tuesday

## I'll be out Thu afternoon. Gavin to be here and teach about testing.

## Challenge of instilling tech culture to you as well as coding
* It's quite a bit different, and I've been doing it so long it's some times hard to remember the differences between most industries and tech.
* Startups and tech like to shatter the mold.

## quiet_assets gem
* https://github.com/evrone/quiet_assets

## Review current user of guest record
* `current_user` method in application controller
* Review `before_action` functionality
* Add logger to `before_action`

## Cookies
* Cookies are stored inside the browser. Been around since 1994. Caused a huge stir when people found out they were in use. Some went so far as to delete them regularly or even turn them off, which caused a lot of problems for us developers.
* They are secure because they cannot be read by any site other than the one that sets them.
* Remember that when an HTTP request ends, there is no "state" stored in between. Every HTTP request is like starting from scratch. Except, that we can store values in cookies.
* Without this addition, someone would have to login on every request because we couldn't remember them without it.
* Like the `params` Hash, Rails provides a `cookies` hash, which is a Hash it creates upon reach request and fills with the cookies in the user's browser. We can use it to store key/value pairs of information across requests.
* Show how to set, read and delete cookies. Same as any Hash.
* `cookies[:user_id] = User.first`
* `User.find_by(user_id: cookies[:user_id])`
* `cookies.delete(:user_id)`
* See [guide](http://api.rubyonrails.org/classes/ActionDispatch/Cookies.html) for further info and how to "sign" a cookie.
* See how value can be removed when browser closes, versus kept for a period of time.
* There is a "permanent" method, but that is simply a short hand for setting the expiration date for 20 years from now.
* You can store JSON in them
* Cookies can only be read by the domain they are stored from for security purposes.

## Convert app to sign in and sign out using cookies
* Ensure there is a logger in current_user before action to show current user id
* Generate a session controller with signin and signout methods
* Create a sign in and sign out link and action. One creates the cookie, one deletes it.
* Change the current_user to no longer hard code the user, but load it from the cookie stored user id
* Use the `delete` method to destroy the user id cookie

## Session
* We used to only have cookies to keep track of data between user requests (for example, who it is that is logged in).
* Rails has added the concept of a "session". With this, we can store small amounts of data in the session between requests.
* Four ways to store a session. All four use a cookie to remember the current user's session id. (Then the session id is looked up in the storage mechanism depending on which is in use).
* Read through the [session guide](http://guides.rubyonrails.org/action_controller_overview.html#session)

## Convert `current_user` method to now use session to store the user_id
* Convert sign in and sign out to now modify the session.

## Authentication

## Pass in email to sign in for that user or another

## Passwords

* http://api.rubyonrails.org/classes/ActiveModel/SecurePassword/ClassMethods.html

```ruby
  gem 'bcrypt'

  validates :password, length: { minimum: 6 }

  has_secure_password

  rails g migration add_password_digest_to_users password_digest:string

  <h3>Sign Up</h3>
  <%= form_tag signup_path, class: 'form' do %>
    <%= text_field_tag "name", nil, placeholder: 'Name' %>
    <%= text_field_tag "email", nil, placeholder: 'Email' %>
    <%= text_field_tag "password", nil, placeholder: 'Password' %>
    <%= text_field_tag "password_confirmation", nil, placeholder: 'Password Confirmation' %>
    <%= submit_tag "Sign up", class: 'btn btn-sm' %>
  <% end %>


  def signup

    user = User.new(name: params[:name], email: params[:email], password: params[:password], password_confirmation: params[:password_confirmation])
    if user.save
      session[:user_id] = user.id
      flash[:notice] = 'You have successfully signed up.'
    else
      flash[:error] = "We were unable to sign you up. #{user.errors.full_messages.join('. ')}"
    end
    redirect_to root_path

  end

```


### Assignment 53
* Review [using cookies in Rails](http://api.rubyonrails.org/classes/ActionDispatch/Cookies.html)
* Review [Rails sessions](http://guides.rubyonrails.org/action_controller_overview.html#session)
* Review [has_secure_password](http://api.rubyonrails.org/classes/ActiveModel/SecurePassword/ClassMethods.html)
* Add real user authentication to your Pinterest app
* User sign up, sign in, sign out
* Adjust current_user method in application controller to use the signed in user from the session

# Wednesday

## Ruby Koans
* http://rubykoans.com/
* Start in class

### Assignment 54: RubyKoans, through 100
* Download the koans.
* Version control them with git.
* Push them to a new GitHub repo.
* Once they are all completed, provide a link in this issue to the repo.

# Thursday

## Testing, Gavin

### Assignment 56
* Review the [Rails testing guide](http://guides.rubyonrails.org/testing.html)
* Using your Pinterest app and conventional built in testing (not, you can load the testing db using any preferred means).
* Write some unit tests to check that all the models will not save unless they have valid data (testing the validations).
* Write a functional test to ensure the home page comes up with the proper data on it.
* Write a functional test to ensure clicking on a pin link display the correct view.
* Write a functional test to ensure the search works correctly.
* Write an integration test to ensure there is a nav providing links to the home page, the user's pins, and the user's boards
* Write an integration test to ensure only admins can get to the admin section.
* Write an integration test to ensure users can only see their own pins and only when they are logged in.
