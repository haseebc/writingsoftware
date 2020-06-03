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
### Card <a name="subparagraph6"></a>
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
[2] pry(main)> 
```
