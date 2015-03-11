# Half Way Challenge

1. What is a class?

    A class something used in object oriented programming in order to layout a blueprint for the 'class' objects created. You can have multiple instances of a class (class objects), which all inherit the methods and attributes defined within your class. A class always starts with a capital letter.

2. What is an attribute?

    An attribute is a characteristic of an object. Meaning, if you have a class called Person, then attributes for that class may include name, age, and gender. So each instance, or object of that class you create could then have a name, age and gender assigned to it.

3. What is an object?

    An object is an instance of a class. But more importantly, everything in Ruby is an object, and as such you can call class methods upon them. 'This is a string object' because it is a string of text. You can call String methods on that text, such as 'this is a string object'.length. 13 is part of the FIXNUM class and can have FIXNUM methods called on it. Using the previous example of creating a Person class with age, name, and gender class. Any methods defined in your Person class can then be called on any objects created.  

4. What type of object is a PORO?

    Plain Old Ruby Object

5. What is a Rails model?

    A rails model is essentially a representation of a class, that is used by the application in order to manipulate and retrieve data from the database. The model is the go between for the controller and the database.

6. What is your absolute favorite meal?

    I really like sushi, specifically salmon based rolls, but I do not discriminate.  

7. What is the difference between a locally scoped variable and an instance variable?

    An locally scoped variable is a variable that is only available in that local area of code. If you are operating in IRB and you type in x = 10, you are defining a locally scoped variable. It only exists where it is being defined. x will only equally 10 until you exit, or jump to another block of code. Instance variables, or 'object' variables, are associated to a current object. They are prefixed with an @ symbol, and are accessible via any method inside that object.

8. Why do we use version control like git?

    Because chances are once we 'fix', or change something, we will break are app in another spot. A lot of times we won't know it is broken or where the break is until users report it. We can then roll back to a functioning version, until further testing fixes the problem for good. Also, this allows us to have multiple people working on the same project at once. Again, if someone submits a change and the app breaks, you can rollback to a functioning version versus trying to ctrl-z through all the changes.

9. What is the difference between git and GitHub?

    Git is the tool for version control, where as GitHub is the service for hosting your versions.

10. What is your ideal vacation?

    Anything involving golfing and the beach.

11. What does the pattern of Separation of Concerns mean and why do we use it?

    The pattern of Separation of Concerns means keeping code separated amongst different sections. We use separation of concerns to keep our code segments looking clean. You do not want to mix code dealing with business logic and views together. This will help simplify any maintenance and development that needs to take place with your code.

12. What does the pattern MVC mean?

    Model View Controller. It is a software architectural pattern that splits applications into three interconnected parts.

13. What is the difference between a Rails model and a database table? What is their relationship?

    The model is an object, backed by a database (or some type of persistent        storage). The model defines associations and validations for information going into the table.

14. How do we modify the database for our Rails app?

    generate a migration
    http://edgeguides.rubyonrails.org/active_record_migrations.html

15. What do you do to relax?

    I go golfing to relax.

16. What is a gem and how do we use them in our Rails apps?

    A gem is a helper package that allows added functionality to our applications, such as the ability to utilize Amazon Web Services (AWS), or pagination. We install gems by including them in our Gemfile and running bundle install.

17. In what part of a Rails application do we tell it how to handle an HTTP request to a specific path, like: `http://localhost:3000/movies`?

    We would do that within our routes file.

18. In what part of a Rails application do we hold data provided by the user, in order to use it, save it to the database, or retrieve it from the database?

    We hold data in the model section before retrieving, or saving it to the database.

19. In what part of a Rails application do we render data, in HTML, to present to the user?

    Within the views.

20. What TV show do you never want to miss?

    That's a tough one, there are so many and since beginning this course I've been missing all of them. Order on which ones I catch up on Hulu when I get some free time: Arrow, Gotham, Nashville. Popcorn time: Always Sunny in Philadelphia, Walking Dead, Better Call Saul (only the first episode, but want to catch more). HBO: Game of Thrones, Silicon Valley, Veep. Netflix: House of Cards.

21. What part of a Rails application processes actions, uses models, and directs flow to the proper view?

    Within the controller.

22. If your app gave you the following error message, on this line of code, what would it indicate?


        undefined method `downcase' for nil:NilClass


        <%= user.name.downcase %>

        This would indicate that the name attribute for user is not set. The name is nil.

23. What gem did we use to paginate our Collections?

    Kaminari
    https://github.com/amatsuda/kaminari

24. What gem did we use to provide upload functionality?

    gem 'carrierwave'
    place require 'carrierwave/orm/activerecord' in config/application.rb after Bundler.require(*Rails.groups).

    May also want to include gem "mini_magick" and enable it within your image uploader.

    https://github.com/amatsuda/carrierwave

25. What is your favorite musical artist or group?

    Van Morrison

26. What technology do we use to style HTML in the browser?

    CSS with massive help from Bootstrap.

27. What type of view templates have we been using in our class to create dynamic HTML?

    ERB (Embedded Ruby)


28. What type of helpers do we use to check data against certain rules and requirements before it is saved to our database?

    Active Record Validations
    http://edgeguides.rubyonrails.org/active_record_validations.html

29. What are model associations?

    Links between tables in the SQL database that allow us to associate and link data.
    http://edgeguides.rubyonrails.org/association_basics.html

30. Based on the name, if The Iron Yard wasn't a code school, what else might it be?

    A gym

31. What code would you use to find the a User record in the database with an id of 17?

    User.find(17)

32. If you want to use an image inside your app, in what directory do you put it?

    app/assets/images

33. What helper do you use to create a form to edit or create a specific resource?

    form_for
    http://edgeguides.rubyonrails.org/form_helpers.html#binding-a-form-to-an-object

34. What does this mean? `||=`

    That deals with memoization, which is an optimization technique used to limit the amount of network calls you have to make. You can use it as

        @current_user ||= User.find_by(email: "guest@guest.com")

    This breaks down to @current_user = @current_user || (or) User.find_by(email: "guest@guest.com")

    The network will only be contacted the first time to set @current_user, and then future calls will only occur on the instance variable. This way the network is not being pinged repeatedly.


35. What is your nickname? If you don't have one, what do you wish it was?

    I have several: K Swizzie, swizzle sticks, Swartzie Poo, clutch, cotton

36. What is a scope? Please provide one example.

    Used for repetitive database queries and called on like a method. They are defined within the class in the model section.

    class User < ActiveRecord::Base
        scope :admin, -> {where(admin: true)}
        scope :non_admin, -> {where(admin: false)}
        scope :has_bio, -> {where("bio is not NULL")}
    end

    Then in rails console you can call Board.id and the call to the database will look like this:

    Board Load (7.8ms)  SELECT "boards".* FROM "boards"  ORDER BY id asc

    http://guides.rubyonrails.org/active_record_querying.html#scopes

37. What is _rake_? Give some examples of how and when we use it?

    Rake is a Ruby utility that is used for administrative tasks. We use it to setup and migrate our database. i.e. rake db:create and rake db:migrate. You can also create your own custom rake commands, and use rake -T to get a list of rake tasks.

    http://edgeguides.rubyonrails.org/command_line.html#rake

38. How do you deploy your app to Heroku?

    Setup a Procfile within your app's root directory.

        web: bundle exec thin start -p $PORT

    Include the following within your Gemfile

      gem 'thin'

      group :production do
        gem 'rails_12factor'
      end

    Within your console do the following:
      heroku login
      cd into the app
      heroku create
      setup heroku config if you have any environments to configure, such as AWS variables.
      Make sure you have everything pushed to GitHub.
      git push heroku master
      heroku run rake db:migrate
      https://devcenter.heroku.com/articles/getting-started-with-ruby#introduction

39. What gem can we use to provide a fast, yet custom and robust, administrative section for our apps?

    gem 'activeadmin', github: 'activeadmin'

40. What is does _anopisthographic_ mean?

    To only have writing on one side only.

41. If a User has many ParkingTickets, and the `user` variable points to a User object, what code would you use to get all the ParkingTickets?

    user.parking_tickets

42. If an Address model has a postal code attribute, what code would you use to get all Addresses from the database with a postal code of _33771_?

    Address.where(postal_code: 33771)

43. How do you create a new Book object in the database, if a Book class has the following required attributes: title, author, publish_year, pages?

    Book.create(title: 'Awesome Book', author: 'Kyle', publish_year: '2015', pages: '4,534')

    Use create to create the object in the database. using .new would require you to call .save before it would be committed to the database.

44. If we get this message in our log after attempting to save an object, what does it mean?


        Unpermitted parameters: first_name

        Scary internet!!!! Go to your controller and add it to the list of allowed params.  


45. What one question do you wish I would have asked?
    I got nothing for this.
