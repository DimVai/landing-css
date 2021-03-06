# landing.css
## A small CSS for composing minimalist landing pages without using classes

### By Dimitris Vainanidis (c) 2021. #



This is to be used when writing a **new** landing page using plain HTML.
 This is "invasive" and formats the basic HTML Elements (headings, links, buttons, inputs etc) so don't use it if your HTML has already been styled. This is a basic style to start writing your HTML page. 

<hr>


## Live example here: 

https://dimvai.github.io/landing-css/

<hr>
<hr>

# **How to use:**

Load style as the first (or only) stylesheet in your HTML `<head>`:

 ```html
 <link rel="stylesheet" href="landing.min.css">
 ```

<hr>

## **This CSS formats all the basic HTML Elements**

Check out the live example (link above) to see how they look.

```css
p

h1,h2,h3,h4


a (links)

button (buttons are customizable with classes - read below)

img, figure

nav (the color is customizable with classes)


ol, ul, dd, li (lists)

table, td, th, tr (tables)

hr


fieldset, legend, label (forms)

input, textarea, select (forms)


code, kbd, pre, samp, code,

sub, sup

blockquote (formatted also as to be used for a "standing-out" paragraph)

aside


header, footer

```

<hr>

##  **Header with navigation bar**

The `landing-css` formats nicely your header if you use the following recommended format for: body,header,main. Use `header` as the first element of body (to have the navigation bar *stick* on top of page) like this:
```html
<body>

    <header> 
        <!-- header's first element (logo) goes on the left --> 
        <a class="logo" href="/">  
            <img src="optional.png" height="35px"/>
            <span>Logo and/or Brand</span>
        </a>
        <!-- header's second element (nav) goes on the right -->
        <nav>  
            <ul>   
                <li><a href="pricing.html">Pricing</a></li>
                <li><a href="about.html">About Us</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- main body content -->
    </main>

</body>
```
Notes. Use `class="logo"` or `class="brand"` on an `a`, `h1`, `div` or any other HTML tag, in order to give it a responsive font size. 

#  **Classes to add additional style and layout**

##  Classes for sizes

Use these classes (you must not use h2,h3 for formatting purposes) to set custom size. 
```CSS
.s12{font-size:1.2rem}
.s15{font-size:1.5rem}
.s20{font-size:2rem}
.s25{font-size:2.5rem}
.s30{font-size:3rem}
.s40{font-size:4rem}
```

For example:
```html
<p class="s30">This text is 3 times bigger than the text of the paragraphs</p>
```

##  Classes for colors

If you want a red part of a sentence, you can use `class="red"` in a span:
```html
<h2>This is an heading <span class="red">that is important</span></h2>
```

Similarly, this is a green button: 
```html
<button class="green">Go inside</button>
```

You can use the following classes for coloring **text** (p, h1-h4, span) elements:
```css
.red 
.blue 
.green 
.grey
.white
```

and these classes for coloring **buttons**, header, th, nav:
```css
.red
.blue
.green
.orange
.purple
.grey
.indigo
.teal
.cyan
.pink
.navy
.brown
.maroon
.violet
```

General background color classes (use anywhere):
```css
.silver
.lavender
.sand
.snow
.pale-blue
.pale-red
.pale-yellow
.pale-green
```

##  Classes for formatting text
Basic formatting classes (with usual meaning):
```css
.bold 
.italics 
.underlined 
```
If you want a paragraph to have columns in large screens, use `columns` class:
```HTML
<p class="columns">Text in columns...</p>
```

##  Links & Buttons
Ways to format an `a` link as a button:
```HTML
<a href="#" class="button">Click me</a>
<a href="#" type="button">A "link" button</a>
```
Tou can use `small` if you want a smaller button (only in `button` or `button`-ish element)
```HTML
<button class="small">A smaller button</button>
```

##  Centering things
These classes (small, medium, large) are used to limit the width of an html element (e.g. a `div`, or an `img`) and maybe center it (in some cases):
```css
.sm 
.md 
.lg 
```
**Warning**: do not use the above classes on head, body, main etc. Instead, create a new div inside those, having the desired class. 

Use `center` to center a text element (p, h1-h4):
```css
.center
```
But `.center` only works on text elements. If you want to center something **in the general case** (like a table, a form etc), use 
```css
.center-content
``` 
in the **parent** element. For example, to center a table, wrap in in a div with the `center-content` class:
```HTML
<div class="center-content">
    <table>
        <!-- tr,td and other table elements -->
    </table>
</div>
```
<hr>



##  Skip Navigation (Accesibility)
In order to have an accessibility "skip" button appear when you press "tab":

```HTML
    <a href="#main-content" class="skip">Skip Navigation</a>
```
You can put this, for example, before the `<header>` part of your HTML.

<hr>

## **Have fun!**
<hr>
