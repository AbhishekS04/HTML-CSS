# HTML Complete Study Guide

## Table of Contents
1. [Introduction to HTML](#introduction-to-html)
2. [HTML Document Structure](#html-document-structure)
3. [HTML Elements and Tags](#html-elements-and-tags)
4. [HTML Attributes](#html-attributes)
5. [Text Formatting Elements](#text-formatting-elements)
6. [Lists](#lists)
7. [Links and Navigation](#links-and-navigation)
8. [Images and Media](#images-and-media)
9. [Tables](#tables)
10. [Forms](#forms)
11. [Semantic HTML5 Elements](#semantic-html5-elements)
12. [HTML5 New Features](#html5-new-features)
13. [Meta Tags and SEO](#meta-tags-and-seo)
14. [HTML Validation](#html-validation)
15. [Best Practices](#best-practices)
16. [Common Interview Questions](#common-interview-questions)

---

## Introduction to HTML

**HTML (HyperText Markup Language)** is the standard markup language for creating web pages. It describes the structure and content of web documents using markup tags.

### Key Concepts:
- **Markup Language**: Uses tags to define elements
- **HyperText**: Text with links to other texts
- **Static Language**: Describes structure, not behavior
- **Platform Independent**: Works across all browsers and operating systems

### HTML Versions:
- HTML 1.0 (1991)
- HTML 2.0 (1995)
- HTML 3.2 (1997)
- HTML 4.01 (1999)
- XHTML 1.0 (2000)
- HTML5 (2014) - Current standard
- HTML Living Standard (Ongoing)

---

## HTML Document Structure

### Basic HTML5 Document Template:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
</head>
<body>
    <!-- Content goes here -->
</body>
</html>
```

### Document Structure Breakdown:

1. **DOCTYPE Declaration**: `<!DOCTYPE html>`
   - Tells browser which version of HTML to use
   - Must be first line of document
   - HTML5 has simplified DOCTYPE

2. **HTML Element**: `<html>`
   - Root element of HTML document
   - Contains all other elements
   - `lang` attribute specifies language

3. **Head Section**: `<head>`
   - Contains metadata about document
   - Not displayed on page
   - Includes title, meta tags, links to CSS/JS

4. **Body Section**: `<body>`
   - Contains visible content
   - All displayable elements go here

---

## HTML Elements and Tags

### Tag Syntax:
- **Opening Tag**: `<tagname>`
- **Closing Tag**: `</tagname>`
- **Self-closing Tag**: `<tagname />`
- **Content**: Text between opening and closing tags

### Element Types:

#### 1. Container Elements (have opening and closing tags):
```html
<h1>Heading</h1>
<p>Paragraph</p>
<div>Division</div>
<span>Span</span>
```

#### 2. Empty/Void Elements (self-closing):
```html
<br>      <!-- Line break -->
<hr>      <!-- Horizontal rule -->
<img>     <!-- Image -->
<input>   <!-- Form input -->
<meta>    <!-- Metadata -->
<link>    <!-- External resource link -->
```

#### 3. Block-level Elements:
- Take full width available
- Start on new line
- Examples: `<div>`, `<p>`, `<h1>-<h6>`, `<ul>`, `<ol>`, `<li>`

#### 4. Inline Elements:
- Take only necessary width
- Don't start on new line
- Examples: `<span>`, `<a>`, `<img>`, `<strong>`, `<em>`

---

## HTML Attributes

Attributes provide additional information about elements and are always specified in the opening tag.

### Syntax:
```html
<tagname attribute="value">Content</tagname>
```

### Global Attributes (available for all elements):

#### 1. **id**: Unique identifier
```html
<div id="header">Header content</div>
```

#### 2. **class**: CSS class for styling
```html
<p class="highlight important">Text</p>
```

#### 3. **style**: Inline CSS styling
```html
<p style="color: red; font-size: 16px;">Styled text</p>
```

#### 4. **title**: Tooltip text
```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

#### 5. **lang**: Language specification
```html
<p lang="es">Hola mundo</p>
```

#### 6. **data-***: Custom data attributes
```html
<div data-user-id="123" data-role="admin">User info</div>
```

#### 7. **contenteditable**: Makes element editable
```html
<div contenteditable="true">Edit this text</div>
```

#### 8. **draggable**: Drag and drop functionality
```html
<div draggable="true">Draggable element</div>
```

#### 9. **hidden**: Hides element
```html
<div hidden>Hidden content</div>
```

#### 10. **tabindex**: Tab order for keyboard navigation
```html
<button tabindex="1">First</button>
<button tabindex="2">Second</button>
```

---

## Text Formatting Elements

### Headings:
```html
<h1>Main Heading (largest)</h1>
<h2>Sub Heading</h2>
<h3>Sub Sub Heading</h3>
<h4>Minor Heading</h4>
<h5>Small Heading</h5>
<h6>Smallest Heading</h6>
```

### Text Emphasis:
```html
<p>This is <strong>important text</strong> (bold)</p>
<p>This is <em>emphasized text</em> (italic)</p>
<p>This is <mark>highlighted text</mark></p>
<p>This is <small>small text</small></p>
<p>This is <del>deleted text</del></p>
<p>This is <ins>inserted text</ins></p>
<p>This is <sub>subscript</sub> and <sup>superscript</sup></p>
```

### Code and Preformatted Text:
```html
<code>inline code</code>
<pre>
    Preformatted text
    preserves   spaces
    and line breaks
</pre>
<kbd>Ctrl + C</kbd> <!-- Keyboard input -->
<samp>Sample output</samp>
<var>variable</var>
```

### Quotations:
```html
<blockquote cite="source-url">
    Long quotation that will be indented
</blockquote>
<q>Short inline quotation with automatic quotes</q>
```

### Line Breaks and Separators:
```html
<br> <!-- Line break -->
<hr> <!-- Horizontal rule/separator -->
<wbr> <!-- Word break opportunity -->
```

---

## Lists

### 1. Unordered Lists (Bullet Points):
```html
<ul>
    <li>First item</li>
    <li>Second item
        <ul>
            <li>Nested item 1</li>
            <li>Nested item 2</li>
        </ul>
    </li>
    <li>Third item</li>
</ul>
```

### 2. Ordered Lists (Numbered):
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>

<!-- With custom starting number -->
<ol start="5">
    <li>Fifth item</li>
    <li>Sixth item</li>
</ol>

<!-- With different numbering types -->
<ol type="A">  <!-- A, B, C -->
<ol type="a">  <!-- a, b, c -->
<ol type="I">  <!-- I, II, III -->
<ol type="i">  <!-- i, ii, iii -->
```

### 3. Description Lists:
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
    <dt>JavaScript</dt>
    <dd>Programming language for web interactivity</dd>
</dl>
```

---

## Links and Navigation

### 1. Basic Links:
```html
<!-- External link -->
<a href="https://www.example.com">Visit Example.com</a>

<!-- Internal link -->
<a href="page2.html">Go to Page 2</a>

<!-- Link to section on same page -->
<a href="#section1">Go to Section 1</a>

<!-- Email link -->
<a href="mailto:contact@example.com">Send Email</a>

<!-- Phone link -->
<a href="tel:+1234567890">Call Us</a>
```

### 2. Link Attributes:
```html
<!-- Open in new tab/window -->
<a href="https://example.com" target="_blank">External Link</a>

<!-- Download link -->
<a href="document.pdf" download>Download PDF</a>

<!-- Link relationship -->
<a href="help.html" rel="help">Help Page</a>

<!-- Link with title (tooltip) -->
<a href="about.html" title="Learn more about us">About</a>
```

### 3. Navigation Structure:
```html
<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/services">Services</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

---

## Images and Media

### 1. Images:
```html
<!-- Basic image -->
<img src="image.jpg" alt="Description of image">

<!-- Image with attributes -->
<img src="photo.jpg" 
     alt="A beautiful sunset" 
     width="300" 
     height="200"
     title="Sunset at the beach">

<!-- Responsive image -->
<img src="small.jpg" 
     srcset="small.jpg 480w, medium.jpg 800w, large.jpg 1200w"
     sizes="(max-width: 600px) 480px, (max-width: 900px) 800px, 1200px"
     alt="Responsive image">
```

### 2. Figure and Caption:
```html
<figure>
    <img src="chart.png" alt="Sales data chart">
    <figcaption>Sales performance for Q1 2023</figcaption>
</figure>
```

### 3. Audio:
```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>

<!-- With additional attributes -->
<audio controls autoplay loop muted preload="auto">
    <source src="background-music.mp3" type="audio/mpeg">
</audio>
```

### 4. Video:
```html
<video controls width="640" height="360">
    <source src="movie.mp4" type="video/mp4">
    <source src="movie.webm" type="video/webm">
    <track src="subtitles.vtt" kind="subtitles" srclang="en" label="English">
    Your browser does not support the video element.
</video>

<!-- Video with poster -->
<video controls poster="thumbnail.jpg">
    <source src="presentation.mp4" type="video/mp4">
</video>
```

### 5. Embedded Content:
```html
<!-- iframe for external content -->
<iframe src="https://www.youtube.com/embed/VIDEO_ID" 
        width="560" 
        height="315" 
        frameborder="0" 
        allowfullscreen>
</iframe>

<!-- Embed for plugins -->
<embed src="document.pdf" type="application/pdf" width="600" height="400">

<!-- Object for multimedia -->
<object data="animation.swf" type="application/x-shockwave-flash">
    <param name="movie" value="animation.swf">
    Alternative content for browsers that don't support Flash.
</object>
```

---

## Tables

### 1. Basic Table Structure:
```html
<table>
    <caption>Monthly Sales Report</caption>
    <thead>
        <tr>
            <th>Month</th>
            <th>Sales</th>
            <th>Profit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>January</td>
            <td>$10,000</td>
            <td>$2,000</td>
        </tr>
        <tr>
            <td>February</td>
            <td>$12,000</td>
            <td>$2,400</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Total</td>
            <td>$22,000</td>
            <td>$4,400</td>
        </tr>
    </tfoot>
</table>
```

### 2. Table Attributes and Spanning:
```html
<table border="1" cellpadding="5" cellspacing="0">
    <tr>
        <th colspan="2">Header spanning 2 columns</th>
        <th>Regular header</th>
    </tr>
    <tr>
        <td rowspan="2">Cell spanning 2 rows</td>
        <td>Regular cell</td>
        <td>Another cell</td>
    </tr>
    <tr>
        <td>Cell in second row</td>
        <td>Last cell</td>
    </tr>
</table>
```

### 3. Table Accessibility:
```html
<table>
    <caption>Student Grades</caption>
    <thead>
        <tr>
            <th scope="col">Student Name</th>
            <th scope="col">Math</th>
            <th scope="col">Science</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">John Doe</th>
            <td>85</td>
            <td>92</td>
        </tr>
    </tbody>
</table>
```

---

## Forms

### 1. Form Structure:
```html
<form action="/submit" method="POST" enctype="multipart/form-data">
    <!-- Form controls go here -->
    <input type="submit" value="Submit">
</form>
```

### 2. Input Types:
```html
<!-- Text inputs -->
<input type="text" name="username" placeholder="Enter username" required>
<input type="password" name="password" minlength="8" required>
<input type="email" name="email" placeholder="user@example.com">
<input type="tel" name="phone" pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}">
<input type="url" name="website" placeholder="https://example.com">
<input type="search" name="query" placeholder="Search...">

<!-- Number inputs -->
<input type="number" name="age" min="0" max="120" step="1">
<input type="range" name="volume" min="0" max="100" value="50">

<!-- Date and time inputs -->
<input type="date" name="birthdate">
<input type="time" name="appointment">
<input type="datetime-local" name="meeting">
<input type="month" name="expiry">
<input type="week" name="week">

<!-- File input -->
<input type="file" name="upload" accept=".pdf,.doc,.docx" multiple>

<!-- Color picker -->
<input type="color" name="theme-color" value="#ff0000">

<!-- Hidden input -->
<input type="hidden" name="csrf-token" value="abc123">

<!-- Checkboxes and radio buttons -->
<input type="checkbox" name="newsletter" id="newsletter" checked>
<label for="newsletter">Subscribe to newsletter</label>

<input type="radio" name="gender" value="male" id="male">
<label for="male">Male</label>
<input type="radio" name="gender" value="female" id="female">
<label for="female">Female</label>
```

### 3. Other Form Elements:
```html
<!-- Textarea -->
<textarea name="message" rows="4" cols="50" placeholder="Enter your message"></textarea>

<!-- Select dropdown -->
<select name="country" required>
    <option value="">Choose a country</option>
    <option value="us">United States</option>
    <option value="ca">Canada</option>
    <option value="uk">United Kingdom</option>
</select>

<!-- Multi-select -->
<select name="skills" multiple>
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="js">JavaScript</option>
</select>

<!-- Option groups -->
<select name="food">
    <optgroup label="Fruits">
        <option value="apple">Apple</option>
        <option value="orange">Orange</option>
    </optgroup>
    <optgroup label="Vegetables">
        <option value="carrot">Carrot</option>
        <option value="broccoli">Broccoli</option>
    </optgroup>
</select>

<!-- Datalist (autocomplete) -->
<input list="browsers" name="browser">
<datalist id="browsers">
    <option value="Chrome">
    <option value="Firefox">
    <option value="Safari">
    <option value="Edge">
</datalist>

<!-- Buttons -->
<button type="submit">Submit Form</button>
<button type="reset">Reset Form</button>
<button type="button" onclick="alert('Hello!')">Click Me</button>
```

### 4. Form Grouping and Labels:
```html
<form>
    <fieldset>
        <legend>Personal Information</legend>
        
        <label for="fname">First Name:</label>
        <input type="text" id="fname" name="firstname" required>
        
        <label for="lname">Last Name:</label>
        <input type="text" id="lname" name="lastname" required>
    </fieldset>
    
    <fieldset>
        <legend>Contact Information</legend>
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        
        <label for="phone">Phone:</label>
        <input type="tel" id="phone" name="phone">
    </fieldset>
</form>
```

### 5. Form Validation Attributes:
```html
<input type="text" name="username" 
       required 
       minlength="3" 
       maxlength="20" 
       pattern="[A-Za-z0-9]+"
       title="Username must contain only letters and numbers">

<input type="email" name="email" required>
<input type="url" name="website" required>
<input type="number" name="age" min="18" max="100" required>
```

---

## Semantic HTML5 Elements

Semantic elements clearly describe their meaning in a human and machine readable way.

### 1. Document Structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Semantic HTML Page</title>
</head>
<body>
    <header>
        <h1>Site Title</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <header>
                <h2>Article Title</h2>
                <p>Published on <time datetime="2023-12-01">December 1, 2023</time></p>
            </header>
            
            <section>
                <h3>Introduction</h3>
                <p>Article content...</p>
            </section>
            
            <section>
                <h3>Main Content</h3>
                <p>More article content...</p>
            </section>
            
            <footer>
                <p>Article footer information</p>
            </footer>
        </article>

        <aside>
            <h3>Related Articles</h3>
            <ul>
                <li><a href="#">Related Article 1</a></li>
                <li><a href="#">Related Article 2</a></li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>&copy; 2023 Your Company. All rights reserved.</p>
    </footer>
</body>
</html>
```

### 2. Semantic Elements Explained:

- **`<header>`**: Page or section header
- **`<nav>`**: Navigation links
- **`<main>`**: Main content area (only one per page)
- **`<article>`**: Self-contained content
- **`<section>`**: Thematic grouping of content
- **`<aside>`**: Sidebar content
- **`<footer>`**: Page or section footer
- **`<figure>`**: Images with captions
- **`<figcaption>`**: Caption for figure
- **`<time>`**: Date/time information
- **`<mark>`**: Highlighted text
- **`<details>`**: Collapsible content
- **`<summary>`**: Summary for details element

### 3. Additional Semantic Elements:
```html
<!-- Address information -->
<address>
    Contact us at:
    <a href="mailto:info@example.com">info@example.com</a>
    123 Main Street, City, State 12345
</address>

<!-- Details and summary -->
<details>
    <summary>Click to expand</summary>
    <p>Hidden content that can be toggled.</p>
</details>

<!-- Progress and meter -->
<progress value="70" max="100">70%</progress>
<meter value="6" min="0" max="10">6 out of 10</meter>

<!-- Ruby annotation (for East Asian typography) -->
<ruby>
    漢 <rt>Kan</rt>
    字 <rt>ji</rt>
</ruby>
```

---

## HTML5 New Features

### 1. New Input Types:
Already covered in Forms section above.

### 2. New Semantic Elements:
Already covered in Semantic HTML5 section above.

### 3. Canvas API:
```html
<canvas id="myCanvas" width="400" height="200">
    Your browser does not support the canvas element.
</canvas>

<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');
    ctx.fillStyle = '#FF0000';
    ctx.fillRect(0, 0, 150, 75);
</script>
```

### 4. Web Storage:
```html
<script>
    // Local Storage (persistent)
    localStorage.setItem('username', 'john_doe');
    const username = localStorage.getItem('username');

    // Session Storage (temporary)
    sessionStorage.setItem('temp_data', 'value');
    const tempData = sessionStorage.getItem('temp_data');
</script>
```

### 5. Geolocation API:
```html
<script>
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(function(position) {
            const lat = position.coords.latitude;
            const lon = position.coords.longitude;
            console.log(`Latitude: ${lat}, Longitude: ${lon}`);
        });
    }
</script>
```

### 6. Web Workers:
```html
<script>
    // Create a web worker
    const worker = new Worker('worker.js');
    
    // Send message to worker
    worker.postMessage('Hello Worker');
    
    // Receive message from worker
    worker.onmessage = function(event) {
        console.log('Message from worker:', event.data);
    };
</script>
```

### 7. Drag and Drop:
```html
<div id="drag1" draggable="true" ondragstart="drag(event)">
    Drag me!
</div>

<div id="dropzone" ondrop="drop(event)" ondragover="allowDrop(event)">
    Drop here
</div>

<script>
    function allowDrop(ev) {
        ev.preventDefault();
    }
    
    function drag(ev) {
        ev.dataTransfer.setData("text", ev.target.id);
    }
    
    function drop(ev) {
        ev.preventDefault();
        const data = ev.dataTransfer.getData("text");
        ev.target.appendChild(document.getElementById(data));
    }
</script>
```

---

## Meta Tags and SEO

### 1. Essential Meta Tags:
```html
<head>
    <!-- Character encoding -->
    <meta charset="UTF-8">
    
    <!-- Viewport for responsive design -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Page title (appears in browser tab) -->
    <title>Your Page Title - Brand Name</title>
    
    <!-- Meta description for search engines -->
    <meta name="description" content="A brief description of your page content (150-160 characters max)">
    
    <!-- Keywords (less important now) -->
    <meta name="keywords" content="html, web development, tutorial">
    
    <!-- Author information -->
    <meta name="author" content="Your Name">
    
    <!-- Language -->
    <meta name="language" content="English">
    
    <!-- Robots (search engine instructions) -->
    <meta name="robots" content="index, follow">
    
    <!-- Canonical URL -->
    <link rel="canonical" href="https://example.com/page">
</head>
```

### 2. Open Graph (Social Media):
```html
<!-- Open Graph meta tags for social media -->
<meta property="og:title" content="Your Page Title">
<meta property="og:description" content="Page description for social media">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:url" content="https://example.com/page">
<meta property="og:type" content="website">
<meta property="og:site_name" content="Your Site Name">
```

### 3. Twitter Cards:
```html
<!-- Twitter Card meta tags -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:site" content="@yourusername">
<meta name="twitter:title" content="Your Page Title">
<meta name="twitter:description" content="Page description for Twitter">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

### 4. Additional SEO Meta Tags:
```html
<!-- Refresh/redirect -->
<meta http-equiv="refresh" content="30">
<meta http-equiv="refresh" content="5;url=https://example.com">

<!-- Cache control -->
<meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
<meta http-equiv="Pragma" content="no-cache">
<meta http-equiv="Expires" content="0">

<!-- Theme color for mobile browsers -->
<meta name="theme-color" content="#000000">

<!-- Apple-specific meta tags -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black">
<meta name="apple-mobile-web-app-title" content="App Name">
```

### 5. Link Tags:
```html
<!-- Favicon -->
<link rel="icon" href="/favicon.ico" type="image/x-icon">
<link rel="shortcut icon" href="/favicon.ico" type="image/x-icon">

<!-- Apple touch icons -->
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">

<!-- Stylesheets -->
<link rel="stylesheet" href="styles.css">
<link rel="stylesheet" href="print.css" media="print">

<!-- Alternate versions -->
<link rel="alternate" type="application/rss+xml" title="RSS Feed" href="/feed.xml">
<link rel="alternate" hreflang="es" href="https://example.com/es/">

<!-- Preload resources -->
<link rel="preload" href="font.woff2" as="font" type="font/woff2" crossorigin>
<link rel="preconnect" href="https://fonts.googleapis.com">
```

---

## HTML Validation

### 1. Why Validate HTML?
- Ensures cross-browser compatibility
- Improves SEO
- Better accessibility
- Easier debugging
- Future-proofs your code

### 2. Common Validation Errors:
- Missing DOCTYPE declaration
- Unclosed tags
- Improper nesting of elements
- Missing alt attributes on images
- Invalid attribute values
- Missing required attributes

### 3. Validation Tools:
- W3C Markup Validator (validator.w3.org)
- Browser developer tools
- HTML validation plugins for code editors

### 4. Well-formed HTML Rules:
- All tags must be properly closed
- Tags must be properly nested
- Attribute values must be quoted
- Elements must be lowercase (XHTML)
- Documents must have DOCTYPE

---

## Best Practices

### 1. Document Structure:
- Always include DOCTYPE declaration
- Use proper document structure (html, head, body)
- Include meta charset declaration
- Use semantic HTML5 elements
- Maintain proper heading hierarchy (h1 → h2 → h3)

### 2. Accessibility:
- Always include alt text for images
- Use proper heading structure
- Ensure sufficient color contrast
- Use labels for form inputs
- Provide keyboard navigation support
- Use ARIA attributes when necessary

### 3. SEO Best Practices:
- Use descriptive, unique page titles
- Include meta descriptions
- Use proper heading hierarchy
- Optimize images with alt text
- Create clean, descriptive URLs
- Use structured data markup

### 4. Performance:
- Optimize images (compress, use appropriate formats)
- Minimize HTTP requests
- Use external CSS and JavaScript files
- Implement lazy loading for images
- Minify HTML, CSS, and JavaScript

### 5. Code Organization:
- Use consistent indentation
- Comment complex sections
- Use meaningful class and id names
- Separate content, presentation, and behavior
- Validate your HTML regularly

### 6. Mobile-First Approach:
- Include viewport meta tag
- Use responsive images
- Design for touch interfaces
- Test on multiple devices
- Consider mobile performance

---

## Common Interview Questions

### 1. What is HTML?
HTML (HyperText Markup Language) is the standard markup language for creating web pages. It describes the structure and content of web documents using elements defined by tags.

### 2. What's the difference between HTML elements and tags?
- **Tag**: The markup syntax like `<p>` or `</p>`
- **Element**: The complete structure including opening tag, content, and closing tag: `<p>Hello</p>`

### 3. What is DOCTYPE and why is it important?
DOCTYPE tells the browser which version of HTML to use. It must be the first line of your HTML document. HTML5 uses `<!DOCTYPE html>`.

### 4. Difference between block and inline elements?
- **Block elements**: Take full width, start on new line (div, p, h1-h6)
- **Inline elements**: Take only necessary width, don't start new line (span, a, img)

### 5. What are semantic elements?
Semantic elements clearly describe their meaning to both browser and developer (