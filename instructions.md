*Portland Code School*
### Web Development Primer Class
# Exercise
## Update a web site with modern HTML & add pages

In this exercise, you will take a template file and modify it to meet a client's specifications in several iterations.

A web design brief with the client's specs is included below.

Wireframes are in the "wireframes.pdf" file.


##Iterations

1. Template code, wireframes, and design brief walk-through
2. Create page structure by adding navigation and content elements
3. Create main page with client color palette and content
  	* Header and footer divs
  	* Navigation div
  	* Dummy articles
4. Create "About and "Contact" page with form
5. (Optional) Make the design responsive
 
##The Template

The template file comes from some fictional previous client. It provides you with a framework and some hopefully helpful comments. Most work is rework -- reading existing code and learning how to modify it is a primary skill in coding. 

You will find some of the existing code and HTML / CSS techniques useful. You replace others to bring the page up to date.

No navigation panel is included in the template, but your client design brief requires it. You will have to add this and several other structural elements (`<div>`, `<section>`, `<article>` and other elements)

The color palette is primarily shades of gray with some uncontrolled elements. You'll have to change these colors and get all the elements under control as part of the exercise.

***

#Web Design Brief

Our client today is a massage therapist. She wants a "brochure" site -- a small, static site that highlights her philosophy, presents her business, and invites the visitor to make an appointment by contacting her through the web. 

You'll give the site a consistent look and feel by repeating the header, navigation panel, and filter elements on all pages.

**Note:** In our Front End class, we cover site generators and dynamic websites; we show you how to automatically place headers on every page of the website. However, in this class, just create the HTML code when you design the main page and then duplicate it for the other pages. Consider this editing practice. :-)


##Color Palette

The client wants a subtle color palette. She would prefer soothing, tranquil colors. Use [kuler](https://kuler.adobe.com/create/color-wheel/) to find a color palette and modify the CSS file to reflect your changes. We suggest a "triad" color scheme with a base color that references the colors in the logo image.

##Body Text Copy

The client does not have the body text copy ready yet. Show at least two articles on the front page and use all the titles shown in the wireframes. Use *lorem ipsum* gibberish as body text. You can find a generator at [this Mashable article](http://mashable.com/2013/07/11/lorem-ipsum/).

##The Container

The contents of the site go in a `<container>` div. The container should float in the center of the page by using automatic margins in the CSS file, and should have the lightest background color of the site. For a schematic view of the page structure, see the wireframe document.

**Question for discussion:**

*Is an HTML5 [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section) element appropriate for this full page container or is the `<div>` element the right choice?* To answer, consider [the specification](http://www.w3.org/TR/html5/sections.html#the-section-element) where it says, "The section element is not a generic container element. When an element is needed only for styling purposes or as a convenience for scripting, authors are encouraged to use the `div` element instead. A general rule is that the section element is appropriate only if the element's contents would be listed explicitly in the document's outline."

The background of the page (everything outside the container div) should be either white, black, or the darkest color of the color palette. 

Notice that there are healthy margins around all of the elements inside the container. This provides negative space (or, what print designers used to call "whitespace") among the content that opens up the design, lets it "breathe", and leads to a more engaging customer experience.

##The Header

The header div now contains the site title in an `<h1>` container, the site tagline in an an `<h2>` container, and the logo. The logo should float to the right. The header should appear on every page. Use an HTML5 [`<header>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header) element to define this section.

##The Navigation Panel

The navigation panel should be on the left-hand side of the page. It should contain three links, one to each page in the site. The links should highlight when the cursor hovers over them. It should also contain the client's headshot. Use small rounded corners and a subtle but distinct background color taken from the color palette to separate it from the main container. Use an HTML5 [`<nav>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav) element for this panel.

##The Content Panel

The main content of each page is in the right-hand side of the page. The proportions of the navigation panel to the main content panel should be close to the [golden ratio](http://en.wikipedia.org/wiki/Golden_ratio). 

**Questions for discussion:**

*	*Is an HTML5 [`<section>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section) element appropriate for this panel?*

*	*Should an [HTML5 `<article>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article) element be used for each blog article?*

*	*Or are `<div>` elements more appropriate?*

##The Form

You can use the form code from the template in the client site. It connects to a simple app that just echoes the form contents so that you can check that the form works. We won't be discussing how forms work in this class, so it doesn't matter if the form itself actually gathers information! In our Front End and Full Stack Ruby on Rails courses, we dive deep into working with forms and the server-side code needed to process them. For this class, just make sure it looks the way the client wants and sends data correctly.

##The Footer

Use an HTML5 [`<footer>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer) element to define this section.

Put the copyright notice in the footer. Use the "C in a circle" copyright mark. Use a [named character reference](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Introduction#Named_character_references) to create the copyright symbol.

Make sure that you provide attribution on the photos. You can do this in the footer of the page. Make the text small and use a unobtrusive color. Each attribution should link back to the original location.

**Note:** all of these images are used through a Creative Commons commercial license.

For the headshot, the photographer is "Pat David" and the link is:
[http://www.flickr.com/photos/39707801@N00/10214643804](http://www.flickr.com/photos/39707801@N00/10214643804)

For the logo the photographer is "The Tedster" and the link is:
[http://www.flickr.com/photos/14648291@N04/8353617707/](http://www.flickr.com/photos/39707801@N00/10214643804)


#Detailed instructions

##Iteration 1

0. Clone the repository to the ~/Documents/pcs folder on your machine that is not in a repository. We will walk through this in class. 
0. Use the commands:
```
git clone git@github.com:portlandcodeschool/pcs-primer-exercise.git
``` 

Next, you will make a copy of the template files.  (We keep the template files around so you can refer to them if you make changes that don't work and you want to refer to the original.)

```
cp -r template site
```

0. In the *css* folder, copy ```template.css``` to ```main.css``` file.  
0. Change the *<link>* tag in the HTML file to point to the renamed CSS file.
0. Verify that the link works by opening up your index.html file in the Chrome browser.

Next, we start making modifications.

0. Examine the your new CSS file.
0. Look for CSS rules that control color.
0. Look for color definitions.
0. Choose new color definitions from [kuler](https://kuler.adobe.com/create/color-wheel/) and choose a new color palette.
0. Substitute the new colors into your CSS file.
0. Check to make sure they look the way they need to look by opening your *index.html* file in the Chrome browser.
0. Use `git add .` to stage your changes
0. Use `git commit -m"Copied template files and modified color palette"` to store your changes in your local repository.


##Iteration 2

In this iteration, we add a nav panel and use "floats" to put the nav panel and the content panel side by side, and start playing with the confusing, wonderful world of HTML validation.

Note: After each iteration, stage and commit your changes to your local repository. We won't list the explicit commands to do so any more. Also, you'll note that the overall instructions will become more and more high level. No more "type this" kind of instructions. Towards the end, you'll be told, "Use a media query" as if you know what this means (because you will!). In order to progress, you will have to become familiar with online documentation and learn how to learn on your own. If you have trouble, please do not hesitate to ask for help from your instructors or classmates.

#####HTML Structure

1. Convert the current `<div class='header'>` and `<div class='footer'>` elements into appropriate `<header>` and `<footer>` HTML5 elements.
2. Create a `<div>` after the "header" and before the "footer". Assign it a class="main". 
2. Create a section *inside* the main section that contains all the articles. Assign it a class="articles". This represents the actual article content.
3. Replace each `<div class="article">` div with an `<article>` element.
3. Create a `<nav>` element *inside* the `<div class='main'>` div but *before* the `<section class='articles'>` section. 
4. Put a non-breaking space in the `<nav>` __OR__ make a set of one-sentence paragraphs `<p>` __OR__ create an unordered list `<ul>` of one-sentence list items `<li>`. This will become our site menu. NOTE: If you'd like to learn a little about the wonders of HTML nesting rules, try putting *flow content* inside *phrasing content* (ie a `<ul></ul>` element inside a `<p></p>` element). This a common thing you might think is possible, and most browsers might let you get away with it, but any self-respecting validator will toss it right out because it's against [the rules](http://www.w3.org/TR/html5/dom.html#phrasing-content-1). 
5. As you make your changes, [validate your code](http://validator.w3.org) to catch any errors

#####CSS

7. Change the `<article_heading>` div to be 80% so that it flexes inside the new containing divs
0. Add a "clear:both" rule to both the header and footer so the floats don't apply to them.
5. Make `<nav>` 30% wide and float it to the left using the appropriate CSS rules (look them up: "width", "min-width", "max-width" and "float").
6. Make the articles section 70% wide. Float it to the left also, so it snugs up against `<nav>`.
7. Make sure there's lots of negative space between the nav panel and the main content panel.
0. Notice that the containing element collapses as you float the inner elements. This is because, by floating the elements, you are telling the browser you are taking over the decision-making on how packing is going to work in this div. Use an `overflow: auto;` property in the containing element to tell it how to manage the interior elements. This is an example of how CSS has lots of implicit rules that you have to learn as you go.
8. As you make your changes, [validate your code](http://jigsaw.w3.org/css-validator/) to catch any errors


While you are playing with your new sections and divs, keep this in mind:

* You can set the margin and background color of your divs to something bright and garish as you work so they are easier to see

* Use Chrome Developer Tools to adjust the properties until you like them, then edit the CSS files with the resulting values.

* As you add margin and padding, be aware of how that changes the width of your side-by-side div containers.

**Question for discussion:**

*The [box model](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model) has this way of changing the size of the box depending on the margin and padding settings. See also [this simplified description](http://www.w3schools.com/css/css_boxmodel.asp). What technique can you use to eliminate this annoying phenomenon? Hint: read what noted web guru and lead Googler Paul Irish [has to say about it](http://www.paulirish.com/2012/box-sizing-border-box-ftw/)*

##Iteration 3

Here we create the header & footer.

1. Change the `<h1>` entry to match the design brief/wireframes. Style the h1 (and only the h1 inside `<header>`) to fit with the site color palette. [See SEO note, below.]
2. Create the site tag line using your choice of tags and styling
3. Put in an image tag `<img>` for the logo, float it right. Look at the badges to understand how to do this.
4. Replace the badge placeholders with the code snippets awarded by the validators upon successful validation. Do not create the badges with some image you find on the net. Do not write the validator code by hand. *Only the code snippets you earn by successful validation will be accepted.* If you have trouble getting your page to validate, leave the placeholders as they are and get assistance from your instructors.
5. Move the contact link to the footer
6. Change the page title (in the "title" container in the "head" of the page) to match the `<h1>`1 contents.
7. Make sure `<header>`  behaves well when you squish and stretch your browser. *(What does this mean? We'll discuss.)*
8. The footer is similar. Make sure it flexes and contains all the information specified above.

#####SEO note

Google and other robot spiders expect one -- and *only one* -- h1 on each page that "tells the story" for that page. They pay special attention to contents, and thus meaning. Given that using an h1 for the company name makes sense on this page. However, does it make sense on any other page of the site? Probably not.

**Therefore:**

*How would you change the header so that it looks the same but doesn't use an h1 container?*

*What would the h1 on the main page be?*

##Iteration 4

1. Create the other two pages. (Simple, huh? Copy the page you just made and modify its contents.)  
2. Make sure the header and footer are exactly the same on the new pages even if the rest of the content is different.
2. Modify the nav panel on the main page to include links to the other pages. Use [*relative addressing*](http://www.w3schools.com/tags/att_a_href.asp)
0. Make sure the nav panel appears in the same position on the othe pages
3. Make the links on the other pages link back to the main page.


## Iteration 5 - optional extra credit
Use a [media query](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries) to make the following modifications when the screen width is less than 600 pixels.

1. The logo image should be smaller and in line with the header information.
1. The nav panel should be smaller and in line after the header.
2. The headshot should disappear.

We will cover responsive design next week, so don't worry too much about this if you don't have time.

<hr />
Copyright © 2013-2014 Alan Zimmerman <br />
Used by permission by Portland Code School
