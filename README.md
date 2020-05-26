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
## Ruby <a name="ruby"></a>
Basic Ruby concepts.
