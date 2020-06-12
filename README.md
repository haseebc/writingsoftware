# Table of contents
1. [Frontend](#frontend)
    1. [Header](#subparagraph1)
    2. [Banner](#subparagraph2)
    3. [Container](#subparagraph3)
    4. [Button](#subparagraph4)
    5. [Card Product](#subparagraph5)
    5. [Card](#subparagraph6)
    6. [Card Category](#subparagraph7)
    7. [Footer](#subparagraph8)
    8. [Navbar](#subparagraph9)
    9. [Tabs](#subparagraph10)
    10. [Search Form](#subparagraph11)
    11. [Alert](#subparagraph12) 
    12. [Avatar](#subparagraph13) 
    12. [What is href="#"](#subparagraphhref)
    13. [Reading Margins](#subparagraphmargin)

    
2. [Ruby](#ruby)

3. [Rails MVP](#paragraph2)
	1. [Debubugging](#subparagraphpry)
	2. [Rails Generate](#railsgenerate)
	2. [Rails Overview:The Basics](#railsbasics)
	
4. [Object Oriented Programming](#oop)
	1. [Class and Instances](#class)
	2. [Instantiation](#instance)
	3. [OOP in a Nutshell](#OOBsummary)

## Frontend <a name="frontend"></a>
HTML
CSS
JS
### Header <a name="subparagraph1"></a>

```html
  <head>
     <!-- Responsiveness,one lined below detect width of the device  -->
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta charset="utf-8">
    <title>Haseeb Chaudhary Profile Page</title>
    <!-- Fontawesome Stylesheet -->
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.3/css/all.css">

    <meta charset="utf-8">
    <!-- Google result text-->
    <title>Haseeb Chaudhary Profile Page</title>
    <!-- Google result description-->
    <meta name="description" content="Haseeb Chaudhary profile page describing who is is and what he does.">
    <!-- Facebook metadata-->  
    <meta property="og:title" content="Haseeb chaudhary Profile Page">
    <meta property="og:image" content="<meta property="og:image" content="http://euro-travel-example.com/thumbnail.jpg">
    <meta property="og:description" content="Haseeb Chaudhary profile page describing who is is and what he does.">
    <meta property="og:site_name" content="Le Wagon"/> 
    <!-- Twitter metadata-->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:site" content="@haseebchaudhary">
    <meta name="twitter:title" content="Haseeb Chaudhary profile page describing who is is and what he does">
    <meta name="twitter:description" content="Haseeb Chaudhary is a fullstack developer and application security expert.">
    <meta name="twitter:creator" content="@haseebchaudhary">
    <meta name="twitter:image:src" content="http://twitter-card.jpg">

  </head>
```
### Banner <a name="subparagraph2"></a>
I wanted to put an image in my banner so I did this:
```html
 <div class="banner" style="background-image: url('images/coding.jpg');"> 
        <div class="container">
            <h1>Zodium gives web skills to creative people.</h1>
            <p>Change your life and learn to code.</p>
            <a href="#" class="btn-primary">Book now!
            </a>
        </div>

    </div>
```
I then styled it as follows
```css
.banner {
    /* says top bottom 200px, left right 0px */
    padding: 200px 0;
    background-size: cover;
    background-position: center;
  }
/* says top bottom 200px, left right  */
.banner h1 {
    color: white;
    font-size: 35px;
  }

.banner p {
    color: white;
    font-size: 20px;
  }
```

####LeWagon Banner
```html
<div class="banner" style="background-image: linear-gradient(rgba(0,0,0,0.4),rgba(0,0,0,0.4)), url(https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/background.png);">
  <div class="container">
    <h1>Le Wagon brings <strong>tech skills</strong> to <strong>creative people</strong>!</h1>
    <p>Change your life and learn to code at one of our campuses around the world.</p>
    <a class="btn btn-flat" href="#">Apply now</a>
  </div>
</div>
```
```css
.banner {
  background-size: cover;
  background-position: center;
  padding: 150px 0;
}

.banner h1 {
  margin: 0;
  color: white;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
  font-size: 32px;
  font-weight: bold;
}

.banner p {
  font-size: 20px;
  color: white;
  opacity: .7;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
}
```

### Container <a name="subparagraph3"></a>
Maybe have a generic container that stretches across the screen
```css
.container {
    width: 900px;
    margin: auto;
}
```
### Button <a name="subparagraph4"></a>
	
`padding: 16px 36px;` This means 16px space aove and 36px to the side.
`display: inline-block;` this is to get space between end of the last line of text and the start of the button. Just looks good.

```css
.btn-primary {
  background-color: #6B72E1;
  color: white;
  padding: 15px 20px;
  border-radius: 4px;
}
```
####LeWagon button
```html
<a class="btn btn-ghost" href="#">Write a story</a>
<a class="btn btn-flat" href="#">Book now</a>
<a class="btn btn-gradient" href="#">Start now</a>
```
```erb
<%= link_to "Write a story", "#", class: "btn btn-ghost" %>
<%= link_to "Book now", "#", class: "btn btn-flat" %>
<%= link_to "Start now", "#", class: "btn btn-gradient" %>
```
```css
.btn-ghost {
  color: #4A4A4A;
  border: 1px solid #4A4A4A;
  padding: 8px 24px;
  border-radius: 50px;
  font-weight: lighter;
  opacity: 0.6;
  transition: opacity 0.3s ease;
}

.btn-ghost:hover {
  opacity: 1;
}

.btn-flat {
  color: white;
  padding: 8px 24px;
  border-radius: 4px;
  background: #1EDD88;
  transition: background 0.3s ease;
}

.btn-flat:hover {
  background: #1BCB7F;
  color: white;
}

.btn-gradient {
  color: white;
  padding: 8px 24px;
  border-radius: 4px;
  font-weight: bold;
  background: linear-gradient(#167FFB, #0F60C4);
  transition: background 0.3s ease;
  border: 1px solid #0F60C4;
}

.btn-gradient:hover {
  background: linear-gradient(#147EFF, #0F67DA);
  color: white;
}
```
### Card Product<a name="subparagraph5"></a>
####Le Wagon Card product
```html
<div class="card-product">
  <img src="https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/skateboard.jpg" />
  <div class="card-product-infos">
    <h2>Product name</h2>
    <p>Product description with <strong>relevant info</strong> only.</p>
  </div>
</div>
```
```css
.card-product {
  overflow: hidden;
  height: 120px;
  background: white;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
  display: flex;
  align-items: center;
}

.card-product img {
  height: 100%;
  width: 120px;
  object-fit: cover;
}

.card-product h2 {
  font-size: 16px;
  font-weight: bold;
  margin: 0;
}

.card-product p {
  font-size: 12px;
  line-height: 1.4;
  opacity: .7;
  margin-bottom: 0;
  margin-top: 8px;
}

.card-product .card-product-infos {
  padding: 16px;
}
```
### Card  <a name="subparagraph6"></a>
First make the images smaller in the cards `width: 150px;` Mase sure use .card img so only this card image is changed.
```css
.card img {
  width: 150px;
}
```
Then use inspect to style as below.
```css
.card {
  width: 200px;
  border-radius: 3px;
  box-shadow: 0 0 5px rgb(230,230,230);
  text-align: center;
  padding: 10px; /* padding to give some internal  */
  border: 1px solid rgb(230,230,230); /* no horizontal or vertical shift, 5px level of blur and color same color as border  */
}
```
Change the text to make it a bit lighter:
```css
.card p {
  opacity: 0.5;
}
```
### Card Category <a name="subparagraph7"></a>
This is a separate div for a selection of cards.
Align elements next to each other using flexbox.
```css
.cards {
  display: flex;
  justify-content: space-between;
  margin-bottom: 30px ;
}
```
####LeWagon Card category
```html
<div class="card-category" style="background-image: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url(https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/breakfast.jpg)">
  Breakfast
</div>
```
```css
.card-category {
  background-size: cover;
  background-position: center;
  height: 180px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 24px;
  font-weight: bold;
  text-shadow: 1px 1px 3px rgba(0,0,0,0.2);
  border-radius: 5px;
  box-shadow: 0 0 15px rgba(0,0,0,0.2);
}
```

### Footer <a name="subparagraph8"></a>
Got o fontawesome and get the code for each font you want to use, for instance for twitter copy `<i class="fas fa-heart"></i>`.
First sort out its background-color, padding and text-align.
```css
.footer {
    background-color: #2c2b2b;
    text-align: center;
    padding: 60px;
}  
```
### Navbar <a name="subparagraph9"></a>
Firtly centre the navbar logo, then style it.
```html
<div class="navbar_dribble">
    <img src="https://raw.githubusercontent.com/lewagon/fullstack-images/master/uikit/logo.png" />
</div>
```

```css
.navbar_dribble {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90px;
  background: white;
  box-shadow: 5px 0 10px rgba(0,0,0,0.15);
} 
.navbar_dribble img {
  width: 50px;
}
```
### Tabs <a name="subparagraph10"></a>
Tabs are really easy and vvery useful.
```html
<div class="tabs">
  <a href="#" class="tab active">Traveling</a>
  <a href="#" class="tab">Hosting</a>
</div>
```
Here's some styling of tabls that could be useful.
```css
.tabs {
    list-style: none;
    margin-bottom: 16px;
    display: flex;
  }
  .tab {
    font-size: 18px;
    font-weight: bold;
    padding: 10px;
    opacity: 0.3;
    border-bottom: 5px solid transparent;
    text-decoration: none;
    color: black;
  }
  .tab:hover {
    opacity: 1;
  }
  .tab.active {
    opacity: 1;
    border-bottom: 3px solid #555555;
  }
```
### Search Form <a name="subparagraph11"></a>
```html
<form novalidate="novalidate" class="simple_form search" action="/" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
  <div class="search-form-control form-group">
    <input class="form-control string required" type="text" name="search[query]" id="search_query" />
    <button name="button" type="submit" class="btn btn-flat">
      <i class="fas fa-search"></i> Search
    </button>
  </div>
</form>
```
Here's the erb code:
```erb
<%= simple_form_for :search, url: root_path, method: :get do |f| %>
  <div class="search-form-control form-group">
    <input class="form-control string required" type="text" name="search[query]" id="search_query" />
    <button name="button" type="submit" class="btn btn-flat">
      <i class="fas fa-search"></i> Search
    </button>
  </div>
<% end %>
```
The css code.
```css
.search-form-control {
  position: relative;
}

.search-form-control .btn {
  position: absolute;
  top: 8px;
  bottom: 8px;
  right: 8px;
}

.search-form-control .form-control {
  height: 3.5rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
  border: 1px solid #E7E7E7;
}

.search-form-control .form-control:focus {
  border: 1px solid #1EDD88;
  outline: none !important;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
}
```
### Alert <a name="subparagraph12"></a>
#### Lewagon alert
```html
<div class="flash flash-success alert alert-dismissible fade show" role="alert">
  <span><strong>Yay!</strong> 🎉 you successfully signed in to our service.</span>
  <a data-dismiss="alert" aria-label="Close">
    <i class="fas fa-times"></i>
  </a>
</div>

<div class="flash flash-warning alert alert-dismissible fade show" role="alert">
  <span><strong>Mmh</strong> 🤔 seems like you don't have <a href="#">profile picture</a> yet.</span>
  <a data-dismiss="alert" aria-label="Close">
    <i class="fas fa-times"></i>
  </a>
</div>

<div class="flash flash-danger alert alert-dismissible fade show" role="alert">
  <span><strong>Oops!</strong> 😱 a problem has occurred while processing your booking.</span>
  <a data-dismiss="alert" aria-label="Close">
    <i class="fas fa-times"></i>
  </a>
</div>
```
The css:
```css
.flash {
  padding: 16px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: white;
  box-shadow: 0 0 8px rgba(0,0,0,0.2);
  border-radius: 4px;
  margin: 8px;
}

.flash-success {
  border: 2px solid #1EDD88;
}

.flash-warning {
  border: 2px solid #FFC65A;
}

.flash-danger {
  border: 2px solid #FD1015;
}
```
### Avatar <a name="subparagraph13"></a>
#### Lewagon alert
```html
<img class="avatar" alt="avatar" src="https://kitt.lewagon.com/placeholder/users/cveneziani" />
<img class="avatar-large" alt="avatar-large" src="https://kitt.lewagon.com/placeholder/users/arthur-littm" />
<img class="avatar-bordered" alt="avatar-bordered" src="https://kitt.lewagon.com/placeholder/users/sarahlafer" />
<img class="avatar-square" alt="avatar-square" src="https://kitt.lewagon.com/placeholder/users/krokrob" />
```

```erb
<%= image_tag "https://kitt.lewagon.com/placeholder/users/cveneziani", class: "avatar", alt: "avatar" %>
<%= image_tag "https://kitt.lewagon.com/placeholder/users/arthur-littm", class: "avatar-large", alt: "avatar-large" %>
<%= image_tag "https://kitt.lewagon.com/placeholder/users/sarahlafer", class: "avatar-bordered", alt: "avatar-bordered" %>
<%= image_tag "https://kitt.lewagon.com/placeholder/users/krokrob", class: "avatar-square", alt: "avatar-square" %>
```

```css
.avatar {
  width: 40px;
  border-radius: 50%;
}

.avatar-large {
  width: 56px;
  border-radius: 50%;
}

.avatar-bordered {
  width: 40px;
  border-radius: 50%;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}

.avatar-square {
  width: 40px;
  border-radius: 0px;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}
```


### What is href="#" and why is it used? <a name="subparagraphhref"></a>
Putting the "#" symbol as the href for something means that it points not to a different URL, but rather to another id or name tag on the same page. For example:
```html
<a href="#bottomOfPage">Click to go to the bottom of the page</a>
  blah blah
  blah blah
  ...
<a id="bottomOfPage"></a>
```
### Reading Margins <a name="subparagraphmargin"></a>
Reading margins is really important:
```css
margin: 5px 0px 100px; /*reads margin top is 5px, margin to sides is 0px, margin below is 0px*/
```
another example:
```css
.container {
  width: 900px;
  margin: 24px auto;
}
```



## Ruby <a name="ruby"></a>
Basic Ruby concepts.
```irb``` 
use the terminal ruby environment
```ri split```
decribes method split 

## Rails MVP <a name="paragraph2"></a>

Basic Ruby concepts.
### The Model
It maintains the relationship between the objects and the database and handles validation, association, transactions, and more.

This subsystem is implemented in ActiveRecord library, which provides an interface and binding between the tables in a relational database and the Ruby program code that manipulates database records. Ruby method names are automatically generated from the field names of database tables.
### The View
It is a presentation of data in a particular format, triggered by a controller's decision to present the data. They are script-based template systems like JSP, ASP, PHP, and very easy to integrate with AJAX technology.

This subsystem is implemented in ActionView library, which is an Embedded Ruby (ERb) based system for defining presentation templates for data presentation. Every Web connection to a Rails application results in the displaying of a view.
### The Controller
The facility within the application that directs traffic, on the one hand, querying the models for specific data, and on the other hand, organizing that data (searching, sorting, messaging it) into a form that fits the needs of a given view.

This subsystem is implemented in ActionController, which is a data broker sitting between ActiveRecord (the database interface) and ActionView (the presentation engine).

## Debugging <a name="subparagraphpry"></a>
Install 
```ruby
  gem 'pry-byebug'
  gem 'pry-rails'
  gem 'pry'
```
Within the code being debugged
```require 'pry' ```
Put binding.pry where its required, for example:
```ruby
def some_method
  puts 'Hello World' # Run 'step' in the console to move here
end

binding.pry
some_method          # Execution will stop here.
puts 'Goodbye World' # Run 'next' in the console to move here.
```
The output is:
```ruby
    2: 
    3: def some_method
    4:     puts 'Hello World' # Run 'step' in the console to move here
    5:   end
    6:   binding.pry
 => 7:   some_method          # Execution will stop here.
    8:   puts 'Goodbye World' # Run 'next' in the console to move here.
```
### Rails Console
```rails console```
```ruby
Running via Spring preloader in process 31298
Loading development environment (Rails 6.0.0)
[1] pry(main)> Rails.env.production?
=> false
[2] pry(main)> Rails.env.development?
=> true
```
https://medium.com/rubyinside/powering-your-ruby-rails-development-with-pry-3d5dbd2a8b80

### Rails Lines of Code
rails stats 

### Rails Generate <a name="railsgenerate"></a>

```ruby
$ rails generate controller Greetings hello
     create  app/controllers/greetings_controller.rb
      route  get 'greetings/hello'
     invoke  erb
     create    app/views/greetings
     create    app/views/greetings/hello.html.erb
     invoke  test_unit
     create    test/controllers/greetings_controller_test.rb
     invoke  helper
     create    app/helpers/greetings_helper.rb
     invoke    test_unit
     invoke  assets
     invoke    scss
     create      app/assets/stylesheets/greetings.scss
```

Check out the controller and modify it a little (in ```app/controllers/greetings_controller.rb```):

```ruby
class GreetingsController < ApplicationController
  def hello
    @message = "Hello, how are you today?"
  end
end
```

Then the view, to display our message (in ```app/views/greetings/hello.html.erb```):
```html
<h1>A Greeting for You!</h1>
<p><%= @message %></p>
Fire up your server using rails server.
```
The URL will be http://localhost:3000/greetings/hello.

With a normal, plain-old Rails application, your URLs will generally follow the pattern of http://(host)/(controller)/(action), and a URL like http://(host)/(controller) will hit the index action of that controller.

### Rails Routes <a name="railsroutes"></a>
```ruby
       Prefix Verb URI Pattern        Controller#Action
  pages_about GET  /about(.:format)   pages#about
pages_contact GET  /contact(.:format) pages#contact
         root GET  /                  pages#home
```

### Rails Basics <a name="railsbasics"></a> 
For every user action in Rails, we need to code **(i) a route, (ii) an action, and (iii) a view**.
#### Route ####
Write a simple route to serve the GET /ask HTTP request to the ask action of the questions controller. As a reminder, here is the pattern of a route coded in Rails:
```ruby
verb "url", to: "controller#action"
```
For example:
```ruby
get "ask", to: "questions#ask"
```


So its really simple, if we do a GET for ask we end up going to the QuestionsController which is ```questions_controller.rb``` with the action of ```ask```.
#### Controller ####
Run the controller for this 
```rails generate controller QuestionsController```

```rails routes``` gives:
```ruby
Prefix Verb URI Pattern       Controller#Action
   ask GET  /ask(.:format)    questions#ask
```

#### View ####
Setup the following within the view.
Not the *form does this*.
**GET method.** by default. 
**action*** URL triggered by submit is ```action="/answer"```.
**name** allows setting of the parameter, in this case ```question``` 

```
<form action="/answer">
    <input type="text" name="question" >
    <input type="submit" value="Ask">
</form>
```
The above will give a ```No route matches [GET] "/answer"```
To fix this follow the same methodology: **route, action, view**.

Now we want to keep this logic going to explain Rails basics. So lets consider the response to the question above (stupid coaching) by understanding answer as **route, controller and view**.
#### Route again !####
```ruby
get 'answer',    to: 'questions#answer' 
```

#### Controller again! ####
Whats important here is we're calling the ```question``` parameter from the view and passing into the controller. Uses *params* really important. 
Notice instance variable ```@question``` for the view to display is computed. This is important and needs to be initialised.

```ruby
class QuestionsController < ApplicationController
  def ask
  end

  def answer
    @question = params[:question]
    if @question.blank?
      @answer = "I can't hear you!"
    elsif @question =~ /i am going to work/i
      @answer = "Great!"
    elsif @question.ends_with?("?")
      @answer = "Silly question, get dressed and go to work!"
    else
      @answer = "I don't care, get dressed and go to work!"
    end
  end
end
```
#### View again! ####
The only thing worth mentioning is otice ```@question``` is initialised form controller and passed in here. Also notice ```@answer``` comes from the controller. Not so stupid huh?
```html
<h1>Stupid Coaching</h1>

<blockquote>
  <p>
    <% if @question.blank? %>
      😶
    <% else %>
      <%= @question %>
    <% end %>
  </p>
  <cite>You</cite>
</blockquote>

<blockquote class="coach">
  <p><%= @answer %></p>
  <cite>Your coach</cite>
</blockquote>

<%= link_to "Ask a new question", ask_path %>
```

## Object Oriented Programming <a name="oop"></a>
OOP = Data + Behavior
```String```
We already have used built-in classes like String
```ruby
name = String.new("John Lennon")  # (same as) name = "John Lennon"
name.split # => [ "John", "Lennon" ]
```
- Data (or State) = the list of characters.
- Behavior = the set of methods which can act on the list of characters.
### Class and Instances <a name="class"></a>
A class is like a cake mold. It helps to create a cake, but is not a cake
An instance of a class is a cake created from a given cake mold
Create a Class
```ruby
# car.rb
class Car
end
```
Convention: filename is in lower snake case, class name in upper camel case.

For example: ```sports_car.rb → class SportsCar```
### Instantiation <a name="instance"></a>
```ruby
my_car = Car.new
your_car = Car.new
```
We just created two new instances of the class Car.
### Constructor
```ruby
Car.new # => Instantiates the class, then calls the method `initialize`.
```
```ruby
class Car
  def initialize
  end
end
```
### Instance variable - DATA
```ruby
class Car
  def initialize
    @engine_started = false
  end
end
```
### Instance methods - BEHAVIOR 1/2
```ruby
class Car
  def initialize
    @engine_started = false
  end

  def engine_started?
    return @engine_started
  end
end
```
```ruby
my_car = Car.new
my_car.engine_started?
# => false
```
### Instance methods - BEHAVIOR 2/2
```ruby
class Car
  def initialize
    @engine_started = false
  end

  def engine_started?
    return @engine_started
  end

  def start_engine
    @engine_started = true
  end
end
```
```ruby
my_car = Car.new
my_car.engine_started? #=> false
my_car.start_engine
my_car.engine_started? #=> true
```
### Setting and accessing state
```ruby
class Car
  def initialize(color)
    @color = color
  end
end
```
```ruby
red_car = Car.new("red")
green_car = Car.new("green")
```
### Explicit reader
```ruby
class Car
  def initialize(color)
    @color = color
  end

  def color
    return @color
  end
end
```
```ruby
red_car = Car.new("red")
puts red_car.color
# => "red"
```
```attr_reader```
```ruby
class Car
  def color
    return @color
  end
end
```
equivalent to
```ruby
class Car
  attr_reader :color
end
```
```attr_reader```convenient shortcut
```ruby
class Car
  def color
    return @color
  end

  def brand
    return @brand
  end
end
```
equivalent to
```ruby
class Car
  attr_reader :color, :brand
end
```
Explicit writer
```ruby
class Car
  attr_reader :color

  def initialize(color)
    @color = color
  end

  def color=(new_color)
    @color = new_color
  end
end
```
```ruby
my_car = Car.new("red")
my_car.color
#=> "red"
my_car.color = "green" # (same as) my_car.color=("green")
my_car.color
#=> "green"
```
```attr_writer```
Again there is a shortcut method
```ruby
class Car
  attr_writer :color

  def initialize(color)
    @color = color
  end
end
```
```ruby
my_car = Car.new("red")
my_car.color = "green" # car color has been updated
```
```attr_accessor```
```attr_reader + attr_writer = attr_accessor```
```ruby
class Car
  attr_accessor :color  # Can read and write the color property
end
```
```ruby
my_car = Car.new
my_car.color = "red"
my_car.color
# => "red"
```


### Private interface
```ruby
class Car
  def start_engine
    start_fuel_pump
    init_spark_plug
  end

  private

  def start_fuel_pump
  end

  def init_spark_plug
  end
end
```
External world does not know about both private methods.

- Everything in ruby is an object.
- OOP is about data (or state) and behavior.
- State is stored in instance variables (@foo)
- Behavior is defined by instance methods (def bar in class definition)

Pay attention to your class file and your class name. 
Remember, lower_snake_case(.rb) for file name,
UpperCamelCase for class name in the class definition. 
Both must be singular! 
Remember, the class is the structure that allows you to create lots of different restaurants (with .new).

So first we add data to a class and then behaviour.
We have a class created, then addd some date to a class and then add behaviour

### Object Orientated Oriented Programming in a Nutshell <a name="OOBsummary"></a>
- First make the class
- Add the data 
- Then the behaviour

The class
```ruby
class Restaurant
    def initialize(name, address, foodtype)
      @name = name
      @address = address
      @mealprice = mealprice
    end
end

#this is the class, then we add data to the class and then behaviour
```

Data and behaviour
```ruby
require_relative "restaurant"

# Okay its really easy, first we create a class (restaurant.rb lass above) and add data to it
best_indian = Restaurant.new("kebabmahal", "calle fuertes", 100)
classic_spanish    = Restaurant.new("cochio", "calle san juan", 50)

#Then we add behaviour 

restaurant = Restaurant.new("T", "Ford", 0)
p restaurant
```
### attr_accessor in Ruby <a name="attr_accessor"></a>
Say we have a class ```Person``. Then we get a ```undefined method `name'```error here.
```ruby
class Person
end

person = Person.new
person.name # => no method error
```
Obviously we never defined method name. Let's do that.
```ruby
class Person
  def name
    @name # simply returning an instance variable @name
  end
end

person = Person.new
person.name # => nil
person.name = "Dennis" # => no method error
```
Aha, we can read the name, but that doesn't mean we can assign the name. Those are two different methods. The former is called **reader** and latter is called **writer**. We didn't create the writer yet so let's do that.
```ruby
class Person
  def name
    @name
  end

  def name=(str)
    @name = str
  end
end

person = Person.new
person.name = 'Dennis'
person.name # => "Dennis"
```
Awesome. Now we can write and read instance variable @name using reader and writer methods. Except, this is done so frequently, why waste time writing these methods every time? We can do it easier.

```ruby
class Person
  attr_reader :name
  attr_writer :name
end
```
Even this can get repetitive. When *you want both reader and writer just use accessor*!
```ruby
class Person
  attr_accessor :name
end

person = Person.new
person.name = "Dennis"
person.name # => "Dennis"
```
Works the same way! And guess what: the instance variable @name in our person object will be set just like when we did it manually, so you can use it in other methods.
```ruby
class Person
  attr_accessor :name

  def greeting
    "Hello #{@name}"
  end
end

person = Person.new
person.name = "Dennis"
person.greeting # => "Hello Dennis"
```


### Super Common Error with Class
```uninitialized constant Car (NameError)```
Above just means why are you trying to use a class on data when you have no Class setup such as an actual restaruant.rb file with ```class Restaurant```
The following line of code would give this error is used in the code block above. Basic problem is 
```ruby
restaurant = car.new("T", "Ford", 0)
``` 
does not have ```car.rb``` Class coded.
That's it. In order to understand how **attr_reader, attr_writer, and attr_accessor** methods *actually generate methods for you*!
