# Table of contents
1. [Frontend](#frontend)
    1. [Header](#subparagraph1)
    2. [Banner](#subparagraph2)
    3. [Container](#subparagraph3)
    4. [Button](#subparagraph4)
    5. [Card](#subparagraph5)
    6. [Cards](#subparagraph6)
    7. [Footer](#subparagraph7)
    8. [Navbar](#subparagraph8)
    9. [Tabs](#subparagraph9)
    10. [Search Form](#subparagraph10)
    11. [Alert](#subparagraph11) 
    12. [Avatar](#subparagraph12) 
    12. [What is href="#"](#subparagraphhref)
    13. [Reading Margins](#subparagraphmargin)
    
2. [Ruby](#ruby)

3. [Another paragraph](#paragraph2)

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

### Card <a name="subparagraph5"></a>
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
### Cards <a name="subparagraph6"></a>
This is a separate div for a selection of cards.
Align elements next to each other using flexbox.
.cards {
  display: flex;
  justify-content: space-between;
  margin-bottom: 30px ;
}
### Footer <a name="subparagraph7"></a>
Got o fontawesome and get the code for each font you want to use, for instance for twitter copy `<i class="fas fa-heart"></i>`.
First sort out its background-color, padding and text-align.
```css
.footer {
    background-color: #2c2b2b;
    text-align: center;
    padding: 60px;
}  
```
### Navbar <a name="subparagraph8"></a>
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
### Tabs <a name="subparagraph9"></a>
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
### Search Form <a name="subparagraph10"></a>
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
### Alert <a name="subparagraph11"></a>
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
### Avatar <a name="subparagraph12"></a>
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
