# Table of contents
1. [Frontend](#frontend)
    1. [Components](#subparagraph1)
2. [Ruby](#ruby)

3. [Another paragraph](#paragraph2)

## Frontend <a name="frontend"></a>
HTML
CSS
JS
### HTML&CSS Components <a name="subparagraph1"></a>
Header
#### Header <a name="subsubparagraph1"></a>
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
#### Banner <a name="subsubparagraph2"></a>
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




## Ruby <a name="ruby"></a>
Basic Ruby concepts.
