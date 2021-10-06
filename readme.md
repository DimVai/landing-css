# landing.css
## A small CSS for composing minimalist landing pages without using classes

### By Dimitris Vainanidis (c) 2021. #



This is to be used when writing a **new** landing page using plain HTML.
 This is "invasive" and formats the basic HTML Elements (headings, links, buttons, inputs etc) so don't use it if your HTML has style already. This is a basic style to start writing your HTML page. 

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

Look at the live example (link above) for how they look.

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

input textarea select (forms)


code, kbd, pre, samp, code,

sub, sup

blockquote (formatted also as to be used for a "standing-out" paragraph)

aside

```

<hr>

##  Header with navigation bar

The `landing-css` formats nicely your header if you use the following standard format (use `header` as the first element of body to have the navigation bar *stick* on top of page):
```html
<body>

    <!-- header should be the first element inside body -->
    <header>
        
        <div>  <!-- header's first element (div) goes on the left --> 
            <a href="#">
                <img src="optional.png" height="30px"/>
                <h2>Logo and/or Brand</h2>
            </a>
        </div> 
        </nav>  <!-- header's second element (nav) goes on the right -->
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

#  **Classes to add additional style and layout**

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
```

##  Classes for formatting text
Basic formatting classes (with usual meaning):
```css
.bold 
.italics 
.underlined 
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

## Have fun!
