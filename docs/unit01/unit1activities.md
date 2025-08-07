---
layout: notes
title: "🎯 Unit 1 Activities" 
parent: "1️⃣ Web Dev Foundations"
nav_order: 5
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---

<html>
  <details>
    <summary>💻 <strong class="text-green-200">ACTIVITY PROGRAM SETUP INSTRUCTIONS</strong></summary>
    
<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Unit1-Activity#`
    > Replace `#` with the specific _activity number_.
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 📂
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!

</div>

<br>

<div class="warn" markdown="block">

🛑 When class ends, don't forget to **SAVE YOUR WORK**! **Codespaces** are TEMPORARY editing environments, so you need to COMMIT changes properly in order to update the main **repository** for your program. 

_There are multiple steps to saving in GitHub Codespaces:_

1. Navigate to the `Source Control` menu on the _LEFT_ sidebar
2. Click the <button type="button" name="button" class="btn btn-green">commit changes</button> button on the _LEFT_ menu
3. Type a brief **commit message** at the top of the file that opens, for example: `updated main.py`
4. Click the small `✔️` **checkmark** in the _TOP RIGHT_ corner
5. Click the <button type="button" name="button" class="btn btn-green">sync changes</button> button on the _LEFT_ menu
6. _Finally you can close your Codespace!_

</div>

  </details>
</html>

---

Based on the attached notes covering foundational HTML concepts (boilerplate structure, text formatting, links, images, and lists), here’s a creative and structured practice activity designed to reinforce key concepts through exploration and personal expression.

---

## ACTIVITY #1: Design Your Own “About Me” Page

Build a creative personal homepage using only the HTML elements you've learned so far. Your page should introduce who you are, highlight your interests, and include some fun or unique touches using links, images, and lists.

This activity will give you a chance to:

* Use semantic tags like **headings**, **paragraphs**, and **lists**
* Embed **links** and **images**
* Experiment with text **emphasis** (bold, italic)
* Explore absolute vs. relative **URL paths**
* Understand element **nesting** and **indentation**

### PART A: Set Up Your Project

<div class="task" markdown="block">

1. Open a new Codespace.
2. Open the `index.html` file.
3. **Delete** any existing code.
4. Rebuild the **HTML boilerplate from scratch**!
  > Try from memory, but peek at the [📓1.2 Notes](https://coderina.dev/webdocs/docs/unit01/notes102.html) if needed.
6. Set the `<title>` **metadata** of your page to something like `About Me - Katerina` (_use your own name!_)

</div>

### PART B: Add a Hero Section

<div class="task" markdown="block">

1. Inside the `<body>`, add an `<h1>` heading that says something like “Welcome to My Webpage!”
2. Add a short introductory `<p>` element with your name and a few fun facts.
3. Use `<strong>` to emphasize one fact and `<em>` to add emphasis to another.
4. Nest your `<strong>` or `<em>` elements inside the paragraph, and make sure everything is indented properly.

</div>

### PART C: Add a Personal Image

<div class="task" markdown="block">

1. Download or select a personal (school-appropriate) image of yourself, a pet, or something you love.
2. Upload the image to your project folder (use drag-and-drop or upload via the file explorer).
3. Add an `<img>` tag to your page that displays the image.
4. Be sure to include:

   * a relative `src` **path** (like `./images/me.jpg`)
   * an `alt` **attribute** that describes the image
   * a `width` and `height` **attribute** to scale it properly (try 200px wide to start)

</div>

### PART D: Add Some Links

<div class="task" markdown="block">

1. Create an `<h2>` section called “My Links”.
2. Add at least two anchor (`<a>`) elements as **absolute links** to websites you like.
  
<!--
   * One **relative link** to a second page in your own project:

     * Create a new file in your project called `fun-facts.html`
     * Add the boilerplate and a simple `<body>` with a fun fact or quote
     * Link to it from your main page using `<a href="fun-facts.html">Fun Facts</a>`
-->

</div>

### PART E: Make Lists of Favorites

<div class="task" markdown="block">

1. Create an `<h2>` heading titled “My Favorite Things”.
2. Add at least **one ordered list** (e.g. favorite movies, songs, books, classes, etc.).
3. Add at least **one unordered list** (e.g. favorite snacks, hobbies, vacation spots).
4. Make sure all `<li>` list items are _nested_ properly inside a set of either `<ol>` or `<ul>` tags.

</div>

---

## 🚊 ACTIVITY #2: Style an NYC Subway Schedule

In this activity, you’ll build a subway schedule page and style it with **CSS selectors, colors, fonts, and the box model**.

Practice:

* External CSS with `<link>`
* Type, class, and ID selectors
* Colors, fonts, and text alignment
* `margin`, `padding`, and `border`
* Display basics

### PART A: Set Up HTML

<div class="task" markdown="block">

1. Open a new Codespace and ensure the **HTML boilerplate** looks correct. 
2. Within the `<head>` section, set the `<title>` to `NYC Subway Schedule`.
3. Inside the `<body>` section, copy in the **starter code**:

```html
  <h1 id="page-title">NYC Subway Schedule</h1>
  <p>Welcome to today’s schedule. Check your train line for the latest stops and updates.</p>

  <h2 class="line-name">A Train</h2>
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/6a/NYCS-bull-trans-A.svg" alt="A Train">
  <ul>
    <li>Inwood – 207 St</li>
    <li>59 St – Columbus Circle</li>
    <li>42 St – Port Authority</li>
    <li>Jay St – MetroTech</li>
    <li>Far Rockaway – Mott Ave</li>
  </ul>

  <h2 class="line-name express">1 Train</h2>
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/13/NYCS-bull-trans-1.svg" alt="1 Train">
  <ul>
    <li>Van Cortlandt Park – 242 St</li>
    <li>96 St</li>
    <li>42 St – Times Sq</li>
    <li>Chambers St</li>
    <li>South Ferry</li>
  </ul>
```

</div>

### PART B: Basic Styling

<div class="task" markdown="block">

1. In `styles.css`, use the **universal selector** to reset the box model:

   ```css
   * {
     box-sizing: border-box;
   }
   ```
2. Style the `body`:

   * Set a background color.
   * Choose a font family (e.g. Arial, sans-serif).
   * Add some padding around the page.
3. ID selector:

   * `#page-title` → large font size, centered text, bold color.
4. Class selector:

   * `.line-name` → background color, white text, padding.
5. Give `.express` a different background or text style.

</div>

### PART C: Lists and Images

<div class="task" markdown="block">

1. Make all station lists (`ul li`) have extra padding and a border-bottom.
2. Make images:

   * A fixed width (e.g. 80px)
   * `height: auto`
   * A border-radius for rounded corners.
3. Use a **descendant selector** so that only images inside `.express` get a colored border.

</div>

### PART D: Box Model Practice

<div class="task" markdown="block">

1. Add `margin` between each train section to create space.
2. Add `padding` inside the `.line-name` headings.
3. Give one section a border to help it stand out.

</div>

---
