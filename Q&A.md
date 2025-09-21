# HTML & CSS Exam Preparation Guide

## 📝 Table of Contents
1. [HTML Theory Questions & Answers](#html-theory-questions--answers)
2. [CSS Theory Questions & Answers](#css-theory-questions--answers)
3. [Practical HTML Questions](#practical-html-questions)
4. [Practical CSS Questions](#practical-css-questions)
5. [Table Creation Examples](#table-creation-examples)
6. [Form Creation Examples](#form-creation-examples)
7. [Layout & Positioning](#layout--positioning)
8. [Unexpected/Tricky Questions](#unexpectedtricky-questions)
9. [Code Output Questions](#code-output-questions)
10. [Quick Reference & Cheat Sheet](#quick-reference--cheat-sheet)

---

## HTML Theory Questions & Answers

### 1. What is HTML? Explain its features.
**Answer:**
HTML (HyperText Markup Language) is the standard markup language for creating web pages.

**Features:**
- Platform Independent
- Case Insensitive (but lowercase recommended)
- Easy to learn and use
- Markup language, not programming language
- Supports multimedia (images, audio, video)
- Hyperlink support
- Free and open standard

### 2. Difference between HTML and XHTML
| HTML | XHTML |
|------|-------|
| Flexible syntax | Strict syntax |
| Tags can be unclosed | All tags must be closed |
| Case insensitive | Case sensitive (lowercase) |
| Attributes don't need quotes | Attributes must be quoted |
| `<br>` allowed | Must be `<br />` |

### 3. What is DOCTYPE? Why is it used?
**Answer:**
DOCTYPE declaration tells the browser which version of HTML the document is written in.
```html
<!DOCTYPE html>  <!-- HTML5 -->
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">  <!-- HTML 4.01 -->
```

### 4. Difference between Block-level and Inline elements
| Block-level | Inline |
|-------------|--------|
| Takes full width available | Takes only necessary width |
| Starts on new line | Doesn't start on new line |
| Can contain block and inline elements | Can only contain inline elements |
| Examples: `<div>`, `<p>`, `<h1>-<h6>`, `<ul>`, `<ol>` | Examples: `<span>`, `<a>`, `<img>`, `<strong>`, `<em>` |

### 5. What are semantic elements? Give examples.
**Answer:**
Semantic elements clearly describe their meaning in a human and machine readable way.

**Examples:**
- `<header>` - Page/section header
- `<nav>` - Navigation links
- `<main>` - Main content
- `<article>` - Self-contained content
- `<section>` - Thematic grouping
- `<aside>` - Sidebar content
- `<footer>` - Page/section footer

### 6. Difference between `<div>` and `<span>`
| `<div>` | `<span>` |
|---------|----------|
| Block-level element | Inline element |
| Used for larger sections | Used for small portions of text |
| Takes full width | Takes only necessary width |
| Can contain block and inline elements | Should only contain inline content |

### 7. What are void/empty elements?
**Answer:**
Elements that don't have closing tags and don't contain content.
**Examples:** `<br>`, `<hr>`, `<img>`, `<input>`, `<meta>`, `<link>`, `<area>`, `<base>`

### 8. Difference between `id` and `class` attributes
| `id` | `class` |
|------|---------|
| Unique identifier | Can be used multiple times |
| Should be used once per page | Can be applied to multiple elements |
| CSS: `#idname` | CSS: `.classname` |
| Higher specificity | Lower specificity |
| Used for JavaScript targeting | Used for styling groups |

---

## CSS Theory Questions & Answers

### 1. What is CSS? Explain its advantages.
**Answer:**
CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of HTML documents.

**Advantages:**
- Separation of content and presentation
- Reduced file size and bandwidth
- Easy maintenance
- Multiple device compatibility
- Better accessibility
- Consistent styling across pages

### 2. Types of CSS
**1. Inline CSS:**
```html
<p style="color: red; font-size: 16px;">Text</p>
```

**2. Internal CSS:**
```html
<head>
<style>
  p { color: red; font-size: 16px; }
</style>
</head>
```

**3. External CSS:**
```html
<head>
<link rel="stylesheet" href="style.css">
</head>
```

### 3. CSS Selectors Types
**1. Element Selector:**
```css
p { color: blue; }
```

**2. Class Selector:**
```css
.highlight { background: yellow; }
```

**3. ID Selector:**
```css
#header { font-size: 24px; }
```

**4. Attribute Selector:**
```css
input[type="text"] { border: 1px solid black; }
```

**5. Pseudo-class Selector:**
```css
a:hover { color: red; }
```

**6. Pseudo-element Selector:**
```css
p::first-line { font-weight: bold; }
```

### 4. CSS Box Model
**Answer:**
The CSS box model describes how elements are structured:
- **Content** - The actual content
- **Padding** - Space inside the element
- **Border** - Line around padding and content
- **Margin** - Space outside the border

```css
.box {
  width: 200px;
  padding: 10px;
  border: 2px solid black;
  margin: 15px;
}
```

### 5. CSS Positioning Types
**1. Static (default):**
```css
position: static;
```

**2. Relative:**
```css
position: relative;
top: 10px;
left: 20px;
```

**3. Absolute:**
```css
position: absolute;
top: 0;
right: 0;
```

**4. Fixed:**
```css
position: fixed;
bottom: 0;
right: 0;
```

**5. Sticky:**
```css
position: sticky;
top: 0;
```

### 6. CSS Display Property
- `block` - Takes full width, new line
- `inline` - Takes necessary width, same line
- `inline-block` - Inline but can set width/height
- `none` - Element not displayed
- `flex` - Flexible layout
- `grid` - Grid layout

### 7. CSS Units
**Absolute Units:**
- `px` - Pixels
- `pt` - Points
- `cm` - Centimeters
- `mm` - Millimeters
- `in` - Inches

**Relative Units:**
- `%` - Percentage
- `em` - Relative to parent font size
- `rem` - Relative to root font size
- `vw` - Viewport width
- `vh` - Viewport height

---

## Practical HTML Questions

### Q1: Create a basic HTML5 document structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Web Page</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

### Q2: Create a navigation menu
```html
<nav>
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="services.html">Services</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

### Q3: Create different types of lists
```html
<!-- Unordered List -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<!-- Ordered List -->
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>

<!-- Definition List -->
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>
```

### Q4: Create semantic HTML5 layout
```html
<!DOCTYPE html>
<html>
<head>
    <title>Semantic Layout</title>
</head>
<body>
    <header>
        <h1>Website Title</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <article>
            <h2>Article Title</h2>
            <p>Article content goes here...</p>
        </article>
        
        <section>
            <h2>Section Title</h2>
            <p>Section content...</p>
        </section>
        
        <aside>
            <h3>Sidebar</h3>
            <p>Sidebar content...</p>
        </aside>
    </main>
    
    <footer>
        <p>&copy; 2023 My Website</p>
    </footer>
</body>
</html>
```

---

## Practical CSS Questions

### Q1: Style a navigation menu
```css
nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    background-color: #333;
}

nav li {
    display: inline-block;
}

nav a {
    display: block;
    color: white;
    text-decoration: none;
    padding: 15px 20px;
}

nav a:hover {
    background-color: #555;
}
```

### Q2: Create a CSS grid layout
```css
.container {
    display: grid;
    grid-template-columns: 1fr 3fr 1fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas: 
        "header header header"
        "sidebar main aside"
        "footer footer footer";
    gap: 20px;
    min-height: 100vh;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.aside { grid-area: aside; }
.footer { grid-area: footer; }
```

### Q3: Create a responsive design
```css
/* Mobile First */
.container {
    width: 100%;
    padding: 10px;
}

.column {
    width: 100%;
    margin-bottom: 20px;
}

/* Tablet */
@media (min-width: 768px) {
    .column {
        width: 48%;
        display: inline-block;
        vertical-align: top;
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .column {
        width: 30%;
    }
}
```

### Q4: Create a card design
```css
.card {
    background: white;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    padding: 20px;
    margin: 20px;
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 20px rgba(0,0,0,0.2);
}

.card h3 {
    color: #333;
    margin-top: 0;
}

.card p {
    color: #666;
    line-height: 1.6;
}
```

---

## Table Creation Examples

### Q1: Simple Table with Border
```html
<table border="1" cellpadding="10" cellspacing="0">
    <tr>
        <th>Name</th>
        <th>Age</th>
        <th>City</th>
    </tr>
    <tr>
        <td>John</td>
        <td>25</td>
        <td>New York</td>
    </tr>
    <tr>
        <td>Jane</td>
        <td>30</td>
        <td>London</td>
    </tr>
</table>
```

### Q2: Complete Table Structure
```html
<table border="1" cellpadding="8" cellspacing="0">
    <caption>Student Grades</caption>
    <thead>
        <tr>
            <th>Student Name</th>
            <th>Math</th>
            <th>Science</th>
            <th>English</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Alice</td>
            <td>85</td>
            <td>92</td>
            <td>78</td>
        </tr>
        <tr>
            <td>Bob</td>
            <td>76</td>
            <td>84</td>
            <td>88</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <th>Average</th>
            <th>80.5</th>
            <th>88</th>
            <th>83</th>
        </tr>
    </tfoot>
</table>
```

### Q3: Table with Colspan and Rowspan
```html
<table border="1" cellpadding="10" cellspacing="0">
    <tr>
        <th colspan="3">Employee Information</th>
    </tr>
    <tr>
        <th>Name</th>
        <th>Department</th>
        <th>Salary</th>
    </tr>
    <tr>
        <td rowspan="2">John Smith</td>
        <td>IT</td>
        <td>$60,000</td>
    </tr>
    <tr>
        <td>Security</td>
        <td>$45,000</td>
    </tr>
</table>
```

### Q4: Styled Table with CSS
```html
<style>
table {
    border-collapse: collapse;
    width: 100%;
    font-family: Arial, sans-serif;
}

th, td {
    border: 1px solid #ddd;
    padding: 12px;
    text-align: left;
}

th {
    background-color: #f2f2f2;
    font-weight: bold;
}

tr:nth-child(even) {
    background-color: #f9f9f9;
}

tr:hover {
    background-color: #f5f5f5;
}
</style>

<table>
    <tr>
        <th>Product</th>
        <th>Price</th>
        <th>Stock</th>
    </tr>
    <tr>
        <td>Laptop</td>
        <td>$999</td>
        <td>15</td>
    </tr>
    <tr>
        <td>Mouse</td>
        <td>$25</td>
        <td>50</td>
    </tr>
</table>
```

---

## Form Creation Examples

### Q1: Basic Contact Form
```html
<form action="/submit" method="POST">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="50"></textarea>
    
    <input type="submit" value="Send Message">
</form>
```

### Q2: Registration Form with Various Inputs
```html
<form action="/register" method="POST">
    <fieldset>
        <legend>Personal Information</legend>
        
        <label for="fname">First Name:</label>
        <input type="text" id="fname" name="firstname" required>
        
        <label for="lname">Last Name:</label>
        <input type="text" id="lname" name="lastname" required>
        
        <label for="dob">Date of Birth:</label>
        <input type="date" id="dob" name="dateofbirth">
        
        <label>Gender:</label>
        <input type="radio" id="male" name="gender" value="male">
        <label for="male">Male</label>
        <input type="radio" id="female" name="gender" value="female">
        <label for="female">Female</label>
    </fieldset>
    
    <fieldset>
        <legend>Account Details</legend>
        
        <label for="username">Username:</label>
        <input type="text" id="username" name="username" required>
        
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>
        
        <label for="country">Country:</label>
        <select id="country" name="country">
            <option value="">Select Country</option>
            <option value="usa">United States</option>
            <option value="uk">United Kingdom</option>
            <option value="canada">Canada</option>
        </select>
        
        <input type="checkbox" id="newsletter" name="newsletter">
        <label for="newsletter">Subscribe to newsletter</label>
    </fieldset>
    
    <input type="submit" value="Register">
    <input type="reset" value="Clear Form">
</form>
```

### Q3: Styled Form with CSS
```css
form {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="password"],
textarea,
select {
    width: 100%;
    padding: 8px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 3px;
    box-sizing: border-box;
}

input[type="submit"] {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 3px;
    cursor: pointer;
}

input[type="submit"]:hover {
    background-color: #45a049;
}
```

---

## Layout & Positioning

### Q1: Create a Fixed Header Layout
```css
body {
    margin: 0;
    padding-top: 60px; /* Height of fixed header */
}

.header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 60px;
    background-color: #333;
    color: white;
    z-index: 1000;
}

.content {
    padding: 20px;
    min-height: 100vh;
}
```

### Q2: Create a Flexbox Layout
```css
.container {
    display: flex;
    min-height: 100vh;
    flex-direction: column;
}

.header {
    background-color: #333;
    color: white;
    padding: 20px;
}

.main-content {
    display: flex;
    flex: 1;
}

.sidebar {
    background-color: #f4f4f4;
    width: 250px;
    padding: 20px;
}

.content {
    flex: 1;
    padding: 20px;
}

.footer {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}
```

### Q3: Centering Elements
```css
/* Horizontal centering */
.center-horizontal {
    margin: 0 auto;
    width: 300px;
}

/* Vertical and horizontal centering with flexbox */
.center-flexbox {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

/* Absolute positioning centering */
.center-absolute {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

---

## Unexpected/Tricky Questions

### Q1: What will be the output of this HTML?
```html
<p>This is <strong>bold <em>and italic</strong> text</em></p>
```
**Answer:** The code has improper nesting. The `<em>` tag should close before `</strong>`. Browsers will try to fix it, but it's invalid HTML.

### Q2: Which CSS rule will be applied?
```css
p { color: red !important; }
#myid { color: blue; }
.myclass { color: green; }
<p id="myid" class="myclass" style="color: yellow;">Text</p>
```
**Answer:** Red color will be applied because of `!important` declaration.

### Q3: What's the difference between `margin: 10px;` and `margin: 10px 10px 10px 10px;`?
**Answer:** Both are the same. The first is shorthand for all four sides having 10px margin.

### Q4: What happens if you don't close a `<div>` tag?
**Answer:** Modern browsers will automatically close it at the end of the document, but it's invalid HTML and can cause layout issues.

### Q5: Can you use same ID on multiple elements?
**Answer:** No, IDs must be unique. Using the same ID multiple times is invalid HTML and can cause JavaScript and CSS issues.

### Q6: What's the default position value in CSS?
**Answer:** `static` - the element follows normal document flow.

### Q7: Which has higher specificity?
```css
#header .menu a { color: red; }
.navigation ul li a:hover { color: blue; }
```
**Answer:** The first rule (red) has higher specificity: ID selector has higher specificity than class selectors.

### Q8: What's the difference between `display: none` and `visibility: hidden`?
**Answer:**
- `display: none` - Element is completely removed from layout
- `visibility: hidden` - Element is invisible but still takes up space

### Q9: Box model calculation question:
```css
.box {
    width: 200px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
}
```
**What's the total width?**
**Answer:** 250px (200px content + 20px padding left + 20px padding right + 5px border left + 5px border right)

### Q10: CSS Inheritance Question
```css
body { color: blue; }
p { font-size: 16px; }
```
```html
<body>
    <p>What color is this text?</p>
</body>
```
**Answer:** Blue - color is inherited from the body element.

---

## Code Output Questions

### Q1: What will this CSS produce?
```css
.box {
    width: 100px;
    height: 100px;
    background: red;
    position: relative;
    left: 20px;
    top: 10px;
}
```
**Answer:** A red box moved 20px from its normal left position and 10px down from its normal top position.

### Q2: What's wrong with this HTML?
```html
<ul>
    <p>This is a paragraph</p>
    <li>List item 1</li>
    <li>List item 2</li>
</ul>
```
**Answer:** `<p>` tag cannot be a direct child of `<ul>`. Only `<li>` elements should be direct children of `<ul>`.

### Q3: CSS Float behavior:
```css
.left { float: left; width: 50%; }
.right { float: right; width: 50%; }
.clear { clear: both; }
```
**Answer:** Two elements side by side, with the third element below them (due to clear).

### Q4: Pseudo-class question:
```css
a:link { color: blue; }
a:visited { color: purple; }
a:hover { color: red; }
a:active { color: green; }
```
**What's the correct order and why?**
**Answer:** LOVE-HATE order (Link, Visited, Hover, Active) - this is the correct specificity order.

---

## Quick Reference & Cheat Sheet

### HTML5 Essential Tags
```html
<!-- Document Structure -->
<!DOCTYPE html>
<html>, <head>, <body>
<meta>, <title>, <link>

<!-- Text Content -->
<h1>-<h6>, <p>, <br>, <hr>
<strong>, <em>, <mark>
<small>, <del>, <ins>
<sub>, <sup>

<!-- Lists -->
<ul>, <ol>, <li>, <dl>, <dt>, <dd>

<!-- Links and Media -->
<a>, <img>, <audio>, <video>
<iframe>, <embed>, <object>

<!-- Tables -->
<table>, <tr>, <td>, <th>
<thead>, <tbody>, <tfoot>
<caption>, <colgroup>, <col>

<!-- Forms -->
<form>, <input>, <textarea>
<select>, <option>, <button>
<label>, <fieldset>, <legend>

<!-- Semantic HTML5 -->
<header>, <nav>, <main>
<article>, <section>, <aside>
<footer>, <figure>, <figcaption>
```

### CSS Essential Properties
```css
/* Text Styling */
color, font-family, font-size, font-weight
text-align, text-decoration, line-height

/* Box Model */
width, height, margin, padding, border
box-sizing, overflow

/* Background */
background-color, background-image
background-position, background-repeat, background-size

/* Positioning */
position, top, right, bottom, left
z-index, float, clear

/* Display and Layout */
display, visibility, opacity
flex, grid, justify-content, align-items

/* Styling */
border-radius, box-shadow, transform
transition, animation
```

### Important Shortcuts & Values
```css
/* Margin/Padding Shorthand */
margin: 10px;                    /* all sides */
margin: 10px 20px;              /* top/bottom left/right */
margin: 10px 20px 30px;         /* top left/right bottom */
margin: 10px 20px 30px 40px;    /* top right bottom left */

/* Border Shorthand */
border: 1px solid #000;         /* width style color */

/* Font Shorthand */
font: italic bold 16px/1.4 Arial, sans-serif;
/* style weight size/line-height family */

/* Background Shorthand */
background: #fff url(bg.jpg) no-repeat center/cover;
/* color image repeat position/size */
```

### Common Exam Formulas
- **Total Width** = width + padding-left + padding-right + border-left + border-right + margin-left + margin-right
- **CSS Specificity**: Inline(1000) > ID(100) > Class(10) > Element(1)
- **Responsive Breakpoints**: Mobile(<768px), Tablet(768px-1024px), Desktop(>1024px)

---

## 🎯 Last-Minute Tips for Exam

1. **Remember DOCTYPE**: Always start with `<!DOCTYPE html>`
2. **Close all tags**: Especially `<p>`, `<div>`, `<span>`
3. **Table structure**: `<table>` → `<tr>` → `<td>`/`<th>`
4. **Form labels**: Always associate labels with form inputs
5. **CSS specificity**: ID > Class > Element
6. **Box model**: Content → Padding → Border → Margin
7. **Semantic HTML**: Use appropriate semantic tags
8. **Validation**: Check for proper nesting and closed tags

### Common Mistakes to Avoid:
- Forgetting to close tags
- Wrong nesting of elements
- Using same ID multiple times
- Incorrect CSS syntax (missing semicolons, colons)
- Not using quotes around attribute values
- Mixing up `class` and `id` selectors in CSS

