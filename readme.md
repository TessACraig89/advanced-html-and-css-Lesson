
Title: Morning Lesson<br>
Duration: 1.5 hrs<br>
Creator: Alex White <br>
Topics: Advanced HTML and CSS <br>

---
# Advanced HTML and CSS

## Lesson objectives

_After this lesson students will be able to:_

* Learn wireframing
* Have a sense of the scope of HTML and CSS
* Use HTML5 semantic elements
* Use CSS Media Queries, and pseudo-selectors
* Implement class based CSS 

<br>
<hr>

## Wireframes

Wireframes are a sketch of what you want your website to look like. We can use them to make a blueprint for what we will build using HTML and CSS. 

You can draw a wireframe in pencil and paper, on a whiteboard, or using wireframing software like [balsamiq](https://wireframe.cc/).

Examples:

![](https://upload.wikimedia.org/wikipedia/commons/4/47/Profilewireframe.png)

![](https://wireframesketcher.com/samples/YouTube.png)

&#x1F535; **Activity**
```
* For this wireframing activity, please use whiteboard markers on your desk!
* Go to one of your favorite websites in your browser
* Create a wireframe based on the website's design
* Take a picture of your wireframe with your phone and upload it below these instructions
* 10 minutes

```

## HTML Review

&#x1F535; **Activity**
```
* Get into pairs 
* Talk with your partner about some of the most important things you have learned about HTML
* Create a list of the 5 most interesting, or important things you have learned
* Respond in slack with that list in a thread. 
* 6 minutes

```

Let's discuss as a class. 

## HTML5

There have been a number of small changes to HTML from the beginning up until 5, but HTML 5 introduced some bigger changes. 
The main additions were more semantically named elements, and the addition of `<canvas>`, `<video>`, and `<audio>` elements. 

Here's a [big cheatsheet](https://www.wpkube.com/wp-content/uploads/2017/09/html-chatsheet.jpg) for HTML5 and how it compares to HTML4. 

### Semantic Elements

`<div>` is so 2013. (It's still OK to use them, but use the new stuff too!) Now we have these lovely *semantic* html elements. Meaning they are named what we use them for! 

Example:

```html
<header>
  <span>
    <button>home</button>
    <button>login</button>
  </span>
</header>

  <article>Skate ipsum dolor sit amet, chicken wing yeah steps airwalk hip smith grind 540. Trucks hospital flip Burnside stoked 180 helipop powerslide 360. Indy grab concave grab powerslide 270 kickturn pump Burnside. Mike Taylor pogo lipslide slob air impossible hanger concave berm.</article>
  <aside>Smith grind hip boneless griptape casper hand rail gnar bucket. Wax ollie north handplant locals crooked grind bearings nosepicker.</aside>
<footer>
  <address>123 The Moon Ave. The Moon</address>
</footer>
```
### Audio and Video elements

HTML 5 introduced special elements for Audio and Video making it easier than ever to include audio and video in your webpages, and to customize how the player looks and behaves. 
You are all becoming pro googlers, so when you have the need, check out the docs on [audio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) and [video](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video) elements.

### Meta Tags and other good stuff to put on EVERY HTML page

```html
<!doctype html>
<!-- lang helps enables browsers to auto-translate content, and helps with SEO (search engine optimization) !-->
<html lang="en">
    <head>
        <!-- charset specifies what character codes we are using  -->
        <meta charset="utf-8">
        <title>This shows in the browser tab!</title>
        
        <!-- Used by search engines and sometimes is shown below the link to your page in search engines! -->
        <meta name="description" content="">
        
        <!-- Tells the browswer to set the width of the page to the width of the device it is on. Only use this when your page
        is set up to be responsive. It keeps the page from being way zoomed out on small devices. -->
        <meta name="viewport" content="width=device-width">
        
        <!-- Place favicon.ico in the root directory -->
        
        <!-- normalize is a open source set of CSS modifiers that will override the different defaults from different browsers. It will make your site look the same on all browsers -->
        <link rel="stylesheet" href="css/normalize.css">
        
        <!-- Link your CSS here -->
        <link rel="stylesheet" href="css/style.css">
    </head>
    <body>
        <!-- demand that a user upgrade their browser -->
        <!--[if lte IE 9]>
            <p class="browserupgrade">You are using an <strong>outdated</strong> browser. Please <a href="https://browsehappy.com/">upgrade your browser</a> to improve your experience and security.</p>
        <![endif]-->

        <!-- Add your site or application content here -->
        <p>Hello world! This is HTML5 Boilerplate.</p>

        <!-- Your JavaScript here -->
        <script src="js/main.js"></script>

        <!-- Google Analytics: change UA-XXXXX-Y to be your site's ID. -->
        <script>
            window.ga=function(){ga.q.push(arguments)};ga.q=[];ga.l=+new Date;
            ga('create','UA-XXXXX-Y','auto');ga('send','pageview')
        </script>
        <script src="https://www.google-analytics.com/analytics.js" async defer></script>
    </body>
</html>
```

## CSS Review 

&#x1F535; **Activity**
```
* Get into pairs 
* Talk with your partner about some of the most important things you have learned about CSS
* Create a list of the 5 most interesting, or important things you have learned
* Respond in slack with that list in a thread. 
* 6 minutes

```

## CSS3

CSS3 has been around for a while. You probably know a number of its features and just think of it as CSS.

Things like `border-radius` and `box-shadow`. 

It also includes `media-queries`! This powerful feature allows your code to check the width of the device it's being run on and create custom CSS for different sizes. 

Example: 

```css
@media screen and (max-width: 699px) and (min-width: 520px) {
    ul li a {
        padding-left: 30px;
        background: url(email-icon.png) left center no-repeat;
    }
}
```

And it includes `pseudo-selectors` that allow you to change style on `:hover` or `:focus` without the use of JavaScript. 

Example: 

```css
a:hover { 
    background-color: yellow;
}
```

### Class Based CSS

Tomorrow we learn Bootstrap! A class based CSS library open sourced by Twitter. But you can create your own class based CSS library. Many companies do this, and many companies also use a combination of traditional CSS, class based open source libraries, and their own class based libraries all together. 

The idea behind class based CSS is instead of targeting individual elements, you create small classes that do specific things, and add those to your HTML elements. 

Example: 

```HTML
<article class="skate-article">
  <h3 class="center skate-header-green">Skateboarding is rad.</h3>
  <p class="article-text-gray move-down">Boneless Steve Alba hanger dude carve transfer face plant.</p>
</article>
```

```CSS
.skate-article {
  font-family: Griffy, serif, san-serif;
}

.center {
  text-align: center;
}

.skate-header-green {
  color: #7FFF00;
}

.article-text-gray {
  background-color: #FFFFCC;
  color: dark-gray;
}
```

### Cheat Sheets, further reading and references
#### HTML
[HTML Basics Cheatsheet](https://git.generalassemb.ly/WDIplus-ATX/advanced-html-and-css/blob/master/lesson_1_cheat_sheet.pdf)
[HTML Cheatsheet](https://git.generalassemb.ly/WDIplus-ATX/advanced-html-and-css/blob/master/HTML-CHEAT-SHEET-basics.png)
[Ultimate HTML5 Cheatsheet](https://www.wpkube.com/wp-content/uploads/2017/09/html-chatsheet.jpg)
[HTML 5 Semantic Element Flow Chart](https://git.generalassemb.ly/WDIplus-ATX/advanced-html-and-css/blob/master/html5-element-flow-chart.pdf)
[HTML & CSS Layout Cheatsheet](https://git.generalassemb.ly/WDIplus-ATX/advanced-html-and-css/blob/master/css_layout_cheat_sheet.pdf)

#### CSS
[CSS Basics Resource](https://git.generalassemb.ly/WDIplus-ATX/advanced-html-and-css/blob/master/cheat_sheet_lesson_2.pdf)
[Advanced CSS Cheatsheet](https://git.generalassemb.ly/WDIplus-ATX/advanced-html-and-css/blob/master/advanced_css_cheat_sheet.pdf)
[CSS Vocab Checker](http://apps.workflower.fi/vocabs/css/en)
[CSS Media Queries Cheatsheet](https://mac-blog.org.ua/css-3-media-queries-cheat-sheet/)

#### Other Web Related Resources
[Font Icons](http://fontawesome.io/) - Tools for adding ultra-lightweight, scalable icons to your pages. 
[Web Fonts](https://fonts.google.com/) - Google's tool for adding free fonts not available in most browsers via the web
