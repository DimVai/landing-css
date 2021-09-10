# landing.css
## A small CSS for composing minimalist landing pages without using classes

### By Dimitris Vainanidis (c) 2021. #



This is to be used when writing a **new** landing page using plain HTML.
 This is "invasive" and formats the basic HTML Elements (headings, links, buttons, inputs etc) so don't use it if your HTML has style already. This is a basic style to start writing your HTML page. 

<hr>


## Live example here: 

https://dimvai.github.io/landing-css/

<hr>

## Load style as the first style in your HTML <head>
 ```html
 <link rel="stylesheet" href="landing.min.css">
 ```

<hr>

## **This CSS formats all the basic HTML Elements**
```css
p

h1,h2,h3,h4

img, figure

a (links)

ol, ul, dd, li (lists)

code, kbd, pre, samp, code,

sub, sup

blockquote (formatted also as to be used for an important paragraph)

hr

table, td, th, tr (tables)

button

fieldset, legend, label (forms)

input text area select (forms)

aside
```

<hr>

##  Header with navigation bar

The `landing-css` formats nicely your header if you use the following standard format (use `header` as the first element of body to hav the navigation bar stick on top of page):
```html
<body>
    <!-- header should be the first element inside body -->
    <header>
        <!-- the first element (div) contains what goes on the left --> 
        <div>   
            <a href="#"><h2>Logo and/or Brand</h2></a>
        </div> 
        <!-- the second element (nav) contains what goes on the right -->
        </nav>  
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

#  Classes to add additional style

##  Classes for colors

If you want a red part of a sentence, you can use `class="red"` in a span:
```html
<h2>This is an heading <span class="red">that is important</span></h2>
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
```

##  Classes for formatting text
Basic formatting classes (with usual meaning):
```css
.bold .italics .underlined 
```
If you want a paragraph to have columns in large screens, use `columns` class:
```html
    <p class="columns">Text in columns...</p>
```

Ways to format an `a` link as a button:
```html
<a href="#" class="button">Click me</a>
<a href="#" type="button">A "link" button</a>
```
Tou can use `small` if you want a smaller button (only in `button` or `button`-style element)
```HTML
<button class="small">A smaller button</button>
```

##  Classes for layout
With their usual meaning:
```css
.bold .italics .underlined 
```

##  Centering things
These classes (small, medium, large) are used to limit the width of an html element (e.g. a `div`, or an `img`) and also center it:
```css
.sm 
.md 
.lg 
```
Use `center` to center a text element (p,h1-h4):
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
        <!-- tr td and other table elements -->
    </table>
</div>
```

