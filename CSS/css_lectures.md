# CSS Lectures #

## Intro to CSS

**1. What's CSS?**

CSS, or Cascading Stylesheets, hold all the code that makes your webpage beautiful! If HTML is the skeleton and JavaScript is the muscular system, CSS is the skin! It is the outer appearance of our program. The following are some really beautiful web pages:

<img src="/assets/woven.gif">

- <a href="https://wovenmagazine.com">Woven Magazine</a>


<img src="/assets/amanda.gif">

- <a href="https://amandamartocchio.com/">Amanda Martocchio Architecture</a>


<img src="/assets/mikiya.gif">

- <a href="https://www.mikiyakobayashi.com/">Mikiya Kobayashi</a>


<img src="/assets/planet1.gif">

- <a href="https://www.onepercentfortheplanet.org/issues">1% For the Planet</a>


<img src="/assets/welcom.gif">

- <a href="https://www.franshalsmuseum.nl/nl/?gclid=EAIaIQobChMIgcWyzbLm6AIVtz6tBh3v0gr1EAAYAiAAEgKRWfD_BwE">Frans Hals Museum</a>


You can be as creative as you want with CSS, the sky is the limit. But first, let's start with the basics.

## Module 2: CSS Syntax ##

The syntax for a CSS file is as follows:

```css
body {                          /* A reference to the section you are styling followed by opening brace */
  background-color: #fff88f;    /* Styling written in key:value pairs, followed by a semicolon */
  color: pink                   
}                               /* Closing brace */
```
Here we are saying, "Every element in the `body` tag will have a yellow background color and pink font color." But what the heck is a `key:value` pair?? A _key:value_ pair in CSS code is a protected keyword (such as `color`, which represents font color) followed by a colon, and the value you'd like to apply (in this case, the protected color word `pink`).

Like HTML, there are a ton of styling referneces to use in your key:value pairs and they do not need to be memorized. Here's a list of them!

<a href="https://www.w3schools.com/cssref/">CSS Styling References</a>

Don't worry too much on the content of the CSS styling here. Just know that this basic syntax will apply to all of the elements that you end up styling. You can have as many lines of styling code as you'd like within the curly braces. 

## Module 3: Targeting Elements ##

**1. Styling HTML Classes and ID's**

Remember _HTML attributes_? The attributes _class_ and _id_ will be paramount when it comes to styling your webpages. 

- A _class_ attribute should be applied to multiple HTML elements that you'd like to all be styled to same way
- An _id_ attribute should be applied to a single HTML element that will have unique styling

For example:
```
<body>

  <h1>Fun with colors!</h1>

  <ul>
    <li class="purple">Purple 1</li>
    <li class="purple">Purple 2</li>
    <li class="purple">Purple 3</li>
    <li id="blue">Blue</li>
    <li id="orange">Orange</li>
    <li id="green">Green</li>
  </ul>

</body>
```
Inside of our `body` tag, we have a header followed by a list of colors. We want all of our purple items to have the same styling, but the rest of the colors should be more unique. For our purples, we have added the attribute `class` and assigned all of them the same thing `"puple"`. For blue, orange, and green, we have added the attribute `id` and assigned them unique values. An `id` value can only be used once in an HTML markup.

So what does the correlating CSS file look like then?

```css
.purple {
  color: purple
}


#blue {
  color: rgb(52, 81, 227)
}
#orange {
  color: #ffaf2e
}
#green {
  color: #45bf53
}
```

Here's the result:

<img src="https://i.ibb.co/bsYDyYj/Screen-Shot-2020-04-14-at-11-20-52-AM.png" alt="Screen-Shot-2020-04-14-at-11-20-52-AM" border="0">

Classes tags are targeted with the syntax above. A `.` then the name of the class. ID's are targeted with a `#` then the name of the ID. Notice how we have started to group all of the id's being targeted and separating them from the class. This helps us to stay organized. 

As we mentioned to earlier, in this example we are altering the font colors of these sections of HTML. There are multiple ways to refer to a color in CSS. 
- A protected word like purple, pink, or blue. While there are a lot of protected color words in CSS, the perfect color you are looking for may not be included and you'll probably need to be more specific. <a href="https://www.w3schools.com/cssref/css_colors.asp">CSS Colors</a>
- The hex code for a color
<img src="/assets/hex.gif">

- The RGB code for a color
<img src="/assets/rgb.gif">

**2. Style by Tag**

You can also style your HTML by its tag. Like in the example on CSS sytnax:

```css
body {                      
  background-color: #fff88f;     
  color: pink                   
}                               
```
We are targeting the entire `body` tag of our HTML markup. Maybe we want all of our paragraphs to have the same styling? It would be a waste of time to write out a class for each `p` tag if we can just target the tag itself:
```css
p {
  background-color: LemonChiffon;
  color: LightSeaGreen;
  border: 1px dotted RosyBrown;
  border-radius: 25px;
  font-size: 150%;
  text-align: center;
}                          
```
The code above would produce paragraphs that look like this:
<img src="https://i.ibb.co/s6m1fFw/Screen-Shot-2020-04-14-at-11-22-31-AM.png" alt="Screen-Shot-2020-04-14-at-11-22-31-AM" border="0">

## Module 4: Divs and Spans ##

Divs and spans are both tags in HTML that are used as containers for information. Neither are visible on their own on a page.
- A `div` is a _block-level_ element, meaning that a div will take up the entire width of the page.
- A `span` is an _in-line_ element, meaning that it can contain information without taking up the width of the page.

Here's some code for a basic HTML page complete with a header and some paragraphs. The paragraphs are broken into `div`s which are assigned ID's. Inside of the divs, see if you can find the `span` tags:

```
<body>

  <h1>I am the header!</h1>

  <div id="intro">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation <span>this part is unique</span> ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </div>

  <div id="bodyParagraphs">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate <span>this part is unique</span> velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </div>

  <div id="conclusion">
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt <span>this part is unique</span> ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </div>

</body>
```
Without any styling, our page looks like this:

<img src="https://i.ibb.co/P67xqBL/Screen-Shot-2020-04-14-at-11-36-51-AM.png" alt="Screen-Shot-2020-04-14-at-11-36-51-AM" border="0">

Let's add some styling in our CSS file:

```css
#intro {
  background-color: #bcff40;
  color: #2f62a8
}
#bodyParagraphs {
  background-color: #e1c2f0;
  color: #713f8a
}
#conclusion {
  background-color: #ffc34a;
  color: #d12626
}

span {
  color: #4f8ff0;
  font-weight: bold
}
```
Now look at our page:

<img src="https://i.ibb.co/gZYXyM0/Screen-Shot-2020-04-14-at-11-42-46-AM.png" alt="Screen-Shot-2020-04-14-at-11-42-46-AM" border="0">

Notice the background on the block-level `div` takes up a whole block of real estate on the page, while the `span` styling falls in-line.

## Module 5: Pseudo-Classes ##

A pseudo-class is used to define a special state of an element. For example, it can be used to:
- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

Here's the syntax of a Pseudo-Class:

```css
selector:pseudo-class {
  property:value;
}
```

For example, this code will make the color of my text white when I hover over it:
```css
p:hover {
  color: white
}
```

<img src="/assets/hover.gif">

Adding effects to your hover, etc. creates dimension for your site and improves user experience! 

## Module 6 Flexbox ##

Something to note: centering things in CSS can be a real pain in the behind! Luckily we have flexbox to help us out! Flexbox is used on a conatiner of elements (such as a div) and organizes the elements within. 

The first thing you have to do to have access to all of the great flexbox features is to add the following code to your styling:

```css
#id {
  display: flex;
}
```

Let's go through some flexbox basics! Look at these dots:

<img src="/assets/original.png">

- Flex direction: Let's add the following code:

```css
#dots {
  border: 2px solid black;             /* The border allows us to see the entire area of the div */
  display: flex;                       /* gives us access to flex abilities */
  flex-direction: column;              /* direction -> column */
}
```
<img src="/assets/column.png">

- Flex direction reverse:

```css
#dots {
  border: 2px solid black;
  display: flex;
  flex-direction: column-reverse;       /* direction -> column reverse */
}
```
<img src="/assets/column-reverse.png">

- Flex direction row looks like the original

```css
#dots {
  border: 2px solid black;
  display: flex;
  flex-direction: row;                  /* direction -> row */
}
```
<img src="/assets/original.png">

- But flex direction row _reverse_ looks like this:

```css
#dots {
  border: 2px solid black;
  display: flex;
  flex-direction: row-reverse;          /* direction -> row reverse */
}
```
<img src="/assets/row-reverse.png">

- To center in row we can use justify content

```css
#dots {
  border: 2px solid black;
  display: flex;
  justify-content: center;
}
```
<img src="/assets/justify-center.png">

- Now let's reverse it!

```css
#dots {
  border: 2px solid black;
  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
}
```
<img src="/assets/row-reverse-justify.png">

- To center the column, we will have to align items

```css
#dots {
  border: 2px solid black;
  display: flex;
  flex-direction: column;
  align-items: center;
}
```
<img src="/assets/column-align.png">

Check out <a href="https://flexboxfroggy.com/">Flexbox Froggy </a> for lots of practice in flexbox!

<a href="https://github.com/rachaelstanislaw/learn-pre-work/blob/master/CSS/css_challenges.md">Go to challenges</a>

<a href="https://github.com/rachaelstanislaw/learn-pre-work">Back to Table of Contents</a>
