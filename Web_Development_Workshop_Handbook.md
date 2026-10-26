# Web Development Workshop Handbook

### HTML, CSS, JavaScript, DOM and Practical Website Building

**Level:** Beginner to Beginner--Intermediate\
**Duration:** 1 Hour (Day 1)\
**Technology:** HTML, CSS, JavaScript, DOM, VS Code and a web browser\
**Mini Project:** Tech Club Website

---

# Table of Contents

1.  Introduction to Web Development
2.  How a Website Works
3.  Setting Up the Project
4.  HTML Fundamentals
5.  Building the Tech Club Website
6.  CSS Fundamentals
7.  JavaScript Fundamentals
8.  Events and DOM Manipulation
9.  Complete Project Code
10. Common Mistakes
11. Practice Challenges
12. Quick Questions and Answers
13. Practical Assessment
14. Quick Revision Sheet

---

# 1. Introduction to Web Development

## What is web development?

Web development is the process of creating websites and web applications
that run in a web browser.

Examples include:

- Personal portfolio websites
- College and student club websites
- News websites
- Online stores
- Event registration pages
- Student portals

## The three main technologies

| Technology | Main purpose              | Examples                                     |
| ---------- | ------------------------- | -------------------------------------------- |
| HTML       | Structure and content     | Headings, paragraphs, links, lists, buttons  |
| CSS        | Appearance and layout     | Colors, fonts, spacing, responsive layouts   |
| JavaScript | Behaviour and interaction | Click actions, changing text, adding content |

A simple way to remember them:

- **HTML:** What is on the page?
- **CSS:** How does it look?
- **JavaScript:** What can it do?

## What participants will build

In this workshop, we will create a small **Tech Club website**
containing:

- A navigation bar
- A welcome section
- An activities list
- A button that changes text
- A button that adds a new activity

The aim is to understand the building blocks rather than create a large
website in one hour.

---

# 2. How a Website Works

A browser reads HTML, applies CSS styling, and runs JavaScript.

1.  HTML describes the content and structure.
2.  CSS controls the presentation and layout.
3.  JavaScript responds to actions and can change the page.
4.  The browser displays the result.

## What is the DOM?

DOM stands for **Document Object Model**.

When a browser loads HTML, it creates a structured representation of the
page called the DOM. JavaScript can find elements in this structure and
change their text, attributes, styles, or children.

For example, JavaScript can change a heading after a button is clicked
without reloading the page.

---

# 3. Setting Up the Project

## Requirements

- A computer with a modern web browser
- A code editor such as Visual Studio Code
- No framework or build tools are required

## Step 1: Create a folder

Create a folder named `tech-club-website`.

Inside it, create these three files:

```text
tech-club-website/
├── index.html
├── style.css
└── script.js
```

- `index.html` contains the page structure.
- `style.css` contains the styling.
- `script.js` contains the interactions.

## Step 2: Open the project

Open the folder in VS Code. Start by editing `index.html`.

You can open `index.html` directly in a browser. After editing and
saving HTML or CSS, refresh the browser to see the changes.

---

# 4. HTML Fundamentals

## What is HTML?

HTML stands for **HyperText Markup Language**. It describes the
structure and meaning of web content.

HTML uses elements, usually written with an opening tag and a closing
tag.

```html
<p>This is a paragraph.</p>
```

Here, `<p>` is the opening tag and `</p>` is the closing tag.

## Basic HTML document

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tech Club</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1>Welcome to Tech Club!</h1>
    <p>Learn, build, and innovate together.</p>

    <script src="script.js"></script>
  </body>
</html>
```

## Important parts

- `<!DOCTYPE html>` tells the browser to use modern HTML standards.
- `<html>` is the root element.
- `<head>` contains page information and links to resources.
- `<title>` sets the browser-tab title.
- `<body>` contains visible page content.
- `<link>` connects the CSS file.
- `<script>` connects the JavaScript file.
- The viewport meta tag helps the page scale correctly on mobile
  screens.

## Common HTML elements

| Element    | Purpose               | Example                                   |
| ---------- | --------------------- | ----------------------------------------- |
| `h1`--`h6` | Headings              | `<h1>Welcome</h1>`                        |
| `p`        | Paragraph             | `<p>Hello!</p>`                           |
| `a`        | Link                  | `<a href="#about">About</a>`              |
| `img`      | Image                 | `<img src="club.jpg" alt="Club members">` |
| `ul`       | Unordered list        | `<ul>...</ul>`                            |
| `ol`       | Ordered list          | `<ol>...</ol>`                            |
| `li`       | List item             | `<li>Workshop</li>`                       |
| `nav`      | Navigation section    | `<nav>...</nav>`                          |
| `section`  | Thematic page section | `<section>...</section>`                  |
| `button`   | Interactive button    | `<button>Click</button>`                  |
| `div`      | Generic container     | `<div>...</div>`                          |
| `footer`   | Footer content        | `<footer>...</footer>`                    |

## Links and navigation

A link can navigate to another website:

```html
<a href="https://example.com">Visit website</a>
```

A link can also jump to a section on the same page:

```html
<a href="#activities">Activities</a>

<section id="activities">
  <h2>Our Activities</h2>
</section>
```

The `href="#activities"` value matches the `id="activities"` attribute.

## Lists

An unordered list uses bullet points:

```html
<ul>
  <li>Web Development</li>
  <li>Hackathons</li>
  <li>Coding Workshops</li>
</ul>
```

An ordered list uses numbers:

```html
<ol>
  <li>Plan the page</li>
  <li>Write the HTML</li>
  <li>Style the page</li>
</ol>
```

## Attributes, IDs and classes

Attributes provide additional information to elements.

```html
<p id="intro" class="highlight">Welcome to the club.</p>
```

- `id` identifies one particular element and should be unique within
  the page.
- `class` can be shared by multiple elements.
- JavaScript can find an element using its ID.
- CSS can select elements by tag, ID, or class.

## Exercise

Add a heading, a paragraph, a navigation link, and a list containing
three activities.

---

# 5. Building the Tech Club Website

Add the following content inside the `<body>` element of `index.html`.
Keep the stylesheet link in `<head>` and the script link near the end of
`<body>`.

```html
<nav>
  <h2>Tech Club</h2>
  <a href="#home">Home</a>
  <a href="#activities">Activities</a>
</nav>

<section id="home">
  <h1 id="heading">Welcome to Tech Club!</h1>
  <p>Learn, build, and innovate together.</p>
  <button id="welcomeBtn">Say Hello</button>
  <p id="message"></p>
</section>

<section id="activities">
  <h2>Our Activities</h2>
  <ul id="activityList">
    <li>Web Development</li>
    <li>Hackathons</li>
    <li>Coding Workshops</li>
  </ul>
  <button id="addBtn">Add Activity</button>
</section>

<footer>
  <p>Made by the Tech Club</p>
</footer>
```

## Concepts to explain while coding

- `nav` groups navigation links.
- `section` groups related content.
- `h1` is the main heading; `h2` introduces a subsection.
- `ul` and `li` create a bullet list.
- `button` creates a control that can respond to a click when
  JavaScript is added.
- IDs such as `welcomeBtn` and `activityList` make specific elements
  easy to target.

---

# 6. CSS Fundamentals

## What is CSS?

CSS stands for **Cascading Style Sheets**. It controls the visual
presentation of HTML elements.

CSS rule structure:

```css
p {
  color: blue;
  font-size: 18px;
}
```

- `p` is the selector.
- `color` and `font-size` are properties.
- `blue` and `18px` are values.

## Selectors

```css
/* Select all paragraph elements */
p {
  color: #334155;
}

/* Select an element by ID */
#heading {
  color: #173b70;
}

/* Select all elements with this class */
.highlight {
  background: #e0f2fe;
}
```

## Margin and padding

- **Margin** creates space outside an element.
- **Padding** creates space between an element's content and its
  border.

## Style the website

Add this to `style.css`:

```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f1f5f9;
  color: #1e293b;
}

nav {
  display: flex;
  align-items: center;
  gap: 20px;
  padding: 12px 24px;
  background: #173b70;
}

nav h2 {
  margin-right: auto;
  color: white;
}

nav a {
  color: white;
  text-decoration: none;
}

nav a:hover {
  text-decoration: underline;
}

section {
  padding: 24px;
}

button {
  padding: 10px 16px;
  border: none;
  border-radius: 6px;
  background: #2563eb;
  color: white;
  cursor: pointer;
}

button:hover {
  background: #1d4ed8;
}

footer {
  padding: 16px 24px;
  background: #173b70;
  color: white;
}
```

## Concepts to explain

- `font-family` changes the text font.
- `background` sets the background color.
- `padding` adds internal spacing.
- `display: flex` arranges the navigation content in a row.
- `gap` adds space between flex items.
- `:hover` applies styling when the pointer is over an element.
- `border-radius` rounds the button corners.

## Optional challenge

Ask participants who finish early to change the theme color, adjust the
spacing, or add a CSS class to highlight an activity.

---

# 7. JavaScript Fundamentals

## What is JavaScript?

JavaScript is a programming language that can add behaviour to a
webpage. It can respond to user actions, calculate values, and work with
the DOM.

## Variables

Variables store values.

```javascript
let clubName = "Tech Club";
const activityCount = 3;

console.log(clubName);
console.log(activityCount);
```

- `let` declares a variable that can be reassigned.
- `const` declares a binding that cannot be reassigned.
- `console.log()` prints a value in the browser console.

## Functions

A function groups instructions that can be run when needed.

```javascript
function greetStudent() {
  alert("Welcome to the workshop!");
}

greetStudent();
```

## Events

Events occur when users interact with the page. Examples include
clicking a button, typing in an input, or submitting a form.

In JavaScript, an event listener can run a function when an event
occurs.

```javascript
const button = document.getElementById("welcomeBtn");

button.addEventListener("click", function () {
  alert("Button clicked!");
});
```

`addEventListener("click", ...)` runs the provided function when the
button is clicked.

## Important distinction

Use:

```javascript
button.addEventListener("click", greetStudent);
```

Do not use this when you want the function to run only after a click:

```javascript
button.addEventListener("click", greetStudent());
```

The second version calls the function immediately instead of passing the
function itself as the event handler.

---

# 8. Events and DOM Manipulation

## Find an HTML element

```javascript
const heading = document.getElementById("heading");
```

This finds the element whose ID is `heading`.

## Change text

```javascript
heading.textContent = "Welcome to Our Coding Community!";
```

The visible heading changes without reloading the page.

## Create and add an element

```javascript
const list = document.getElementById("activityList");

const item = document.createElement("li");
item.textContent = "AI Workshop";

list.appendChild(item);
```

This creates a new list item and adds it to the existing list.

## Complete JavaScript for the project

Add this to `script.js`:

```javascript
const welcomeBtn = document.getElementById("welcomeBtn");
const message = document.getElementById("message");

welcomeBtn.addEventListener("click", function () {
  message.textContent = "Welcome to our Tech Club!";
});

const addBtn = document.getElementById("addBtn");
const activityList = document.getElementById("activityList");

addBtn.addEventListener("click", function () {
  const item = document.createElement("li");
  item.textContent = "New Coding Activity";
  activityList.appendChild(item);
});
```

## What happens when a button is clicked?

1.  JavaScript finds the button and the relevant page element.
2.  The browser detects the click event.
3.  The registered function runs.
4.  JavaScript changes text or creates a new element.
5.  The browser displays the updated DOM.

## DOM methods summary

Method or property Purpose

---

`document.getElementById()` Find an element by its ID
`addEventListener()` Run a function in response to an event
`textContent` Read or change text
`document.createElement()` Create a new element
`appendChild()` Add a child element
`console.log()` Print debugging information in the console

## Exercise

1.  Change the welcome message.
2.  Add a new activity to the list when the button is clicked.
3.  Change the main heading using JavaScript.

---

# 9. Complete Project Code

Use this section as the final reference after participants have built
the page step by step.

## `index.html`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tech Club</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <nav>
      <h2>Tech Club</h2>
      <a href="#home">Home</a>
      <a href="#activities">Activities</a>
    </nav>

    <main>
      <section id="home">
        <h1 id="heading">Welcome to Tech Club!</h1>
        <p>Learn, build, and innovate together.</p>
        <button id="welcomeBtn">Say Hello</button>
        <p id="message" aria-live="polite"></p>
      </section>

      <section id="activities">
        <h2>Our Activities</h2>
        <ul id="activityList">
          <li>Web Development</li>
          <li>Hackathons</li>
          <li>Coding Workshops</li>
        </ul>
        <button id="addBtn">Add Activity</button>
      </section>
    </main>

    <footer>
      <p>Made by the Tech Club</p>
    </footer>

    <script src="script.js"></script>
  </body>
</html>
```

## `style.css`

```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f1f5f9;
  color: #1e293b;
}

nav {
  display: flex;
  align-items: center;
  gap: 20px;
  padding: 12px 24px;
  background: #173b70;
}

nav h2 {
  margin-right: auto;
  color: white;
}

nav a {
  color: white;
  text-decoration: none;
}

nav a:hover {
  text-decoration: underline;
}

section {
  padding: 24px;
}

button {
  padding: 10px 16px;
  border: none;
  border-radius: 6px;
  background: #2563eb;
  color: white;
  cursor: pointer;
}

button:hover {
  background: #1d4ed8;
}

footer {
  padding: 16px 24px;
  background: #173b70;
  color: white;
}

@media (max-width: 480px) {
  nav {
    flex-wrap: wrap;
    gap: 12px;
  }

  nav h2 {
    width: 100%;
    margin: 0;
  }

  section {
    padding: 18px;
  }
}
```

## `script.js`

```javascript
const welcomeBtn = document.getElementById("welcomeBtn");
const message = document.getElementById("message");

welcomeBtn.addEventListener("click", function () {
  message.textContent = "Welcome to our Tech Club!";
});

const addBtn = document.getElementById("addBtn");
const activityList = document.getElementById("activityList");

addBtn.addEventListener("click", function () {
  const item = document.createElement("li");
  item.textContent = "New Coding Activity";
  activityList.appendChild(item);
});
```

## Test the finished website

- The navigation links jump to the correct sections.
- The welcome button displays a message.
- The add button inserts a new activity.
- The CSS file styles the navbar, buttons, and page.
- The layout adapts to narrower screens.

---

# 10. Common Mistakes

| Mistake | Solution |
|---|---|
| CSS file does not load | Check `href="style.css"` and the filename |
| JavaScript does not run | Check `src="script.js"` and the browser console |
| Button click causes an error | Check the element ID and event listener |
| `getElementById()` returns `null` | Ensure the ID matches and the script runs after the HTML element exists |
| Link does not jump to a section | Match the link's `href="#id"` to the section's `id` |
| New list item does not appear | Check that the list was found and `appendChild()` is called |
| CSS rule has no effect | Check selector spelling, braces, property names, and values |
| Elements are too close together | Adjust margin, padding, or gap |
| Page looks small on mobile | Add the viewport meta tag |

## Debugging tip

In the browser, open Developer Tools and check the **Console** for
JavaScript errors. Read the first error carefully; it often points to
the problem.

---

# 11. Practice Challenges

Complete the basic project first. Participants with prior experience can
try the optional challenges.

## Beginner challenges

1.  Change the heading to a club name of your choice.
2.  Add two more activities in HTML.
3.  Change the background and button colors in CSS.
4.  Change the message displayed by the welcome button.

## Extra challenges

1.  Add a third navigation link and a matching section.
2.  Create a CSS class called `.highlight` and apply it to an element.
3.  Change the heading when the welcome button is clicked.
4.  Add a different activity name each time the add button is clicked.
5.  Add a button hover effect.
6.  Make the navigation wrap neatly on a mobile screen.

---

# 12. Quick Questions and Answers

### 1. What is HTML?

HTML describes the structure and content of a webpage.

### 2. What is CSS?

CSS controls how HTML elements look and how they are laid out.

### 3. What is JavaScript?

JavaScript adds programming logic and interaction to a webpage.

### 4. What is an HTML element?

An element is a piece of HTML, often made up of an opening tag, content,
and a closing tag.

### 5. What is the difference between `id` and `class`?

An ID identifies one element; a class can be applied to multiple
elements.

### 6. What is the DOM?

The Document Object Model is the browser's structured representation of
a webpage that JavaScript can access and modify.

### 7. What does `getElementById()` do?

It finds the element with the specified ID.

### 8. What does `addEventListener()` do?

It registers a function to run when a specified event occurs.

### 9. What is the difference between margin and padding?

Margin is outside an element's border; padding is inside the border
around its content.

### 10. What is `textContent` used for?

It reads or updates the text content of an element.

### 11. What is `createElement()` used for?

It creates a new HTML element in the DOM.

### 12. Do HTML and CSS alone make a website interactive?

They can provide links and some native browser interactions, but
JavaScript is commonly used for custom behaviour such as updating text
or adding list items dynamically.

---

# 13. Practical Assessment

## Task: Customize the Tech Club Website

Requirements:

- Change the website title and main heading.
- Add at least one activity.
- Customize a CSS color or spacing value.
- Modify the welcome button's message.
- Demonstrate that the add-activity button works.

---

# 14. Quick Revision Sheet

- **HTML:** Structure and content of a webpage.
- **CSS:** Styling and layout.
- **JavaScript:** Logic and interaction.
- **Element:** A unit of HTML content.
- **Attribute:** Additional information on an HTML element.
- **`id`:** Identifier for a particular element.
- **`class`:** Reusable grouping for styling or selection.
- **`nav`:** Groups navigation links.
- **`ul` / `ol`:** Unordered and ordered lists.
- **Selector:** Chooses which HTML elements a CSS rule styles.
- **Margin:** Space outside an element's border.
- **Padding:** Space inside an element's border.
- **Function:** Reusable block of JavaScript instructions.
- **Event:** Something that happens, such as a click.
- **`addEventListener()`:** Registers a function for an event.
- **DOM:** Structured representation of the webpage.
- **`getElementById()`:** Finds an element by ID.
- **`textContent`:** Reads or changes text.
- **`createElement()`:** Creates an element.
- **`appendChild()`:** Adds a child element.

---

## Final Advice

The objective of Day 1 is not to memorize every tag or property. It is
to understand how HTML, CSS, JavaScript, and the DOM work together.
Build the page incrementally, test each change in the browser, and
encourage participants to experiment.
