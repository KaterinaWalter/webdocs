---
layout: default
title: "🐞 Debugging Errors" 
parent: "📖 References"
nav_order: 2
---

# 🐞 Debugging Errors
{:.no_toc}

{: .highlight } 
Code not working? Follow the steps in the **debugging process** below _before_ asking a peer or your teacher! Fixing your own errors, no matter how small, is one of the _best_ ways to become a better coder. 

### 🧱 HTML Debugging Process

1. **Check for Proper Tag Structure**

   * Every opening tag needs a closing tag: `<div> ... </div>`
   * Self-closing tags: `<img />`, `<br />`, `<input />`

2. **Check for Typos**

   * Misspelled tags won’t work: `<boddy>` ≠ `<body>`
   * Misspelled attributes: `herf` ≠ `href`, `clas` ≠ `class`

3. **Check Nesting**

   * Tags must be properly nested:
     ✅ `<p><strong>text</strong></p>`
     ❌ `<p><strong>text</p></strong>`

4. **Check File Paths**

   * Are images or stylesheets loading?
     Check: `src="images/cat.jpg"` or `href="style.css"`

5. **Use the Validator**

   * [https://validator.w3.org](https://validator.w3.org) to check for structural errors

---

### 🎨 CSS Debugging Process

1. **Check Selectors**

   * Make sure the selector matches the element:

     * ID: `#main-header` → `<h1 id="main-header">`
     * Class: `.card` → `<div class="card">`

2. **Check Property Spelling and Semicolons**

   * ✅ `color: red;`
     ❌ `colr red` or missing `;`

3. **Check File Links**

   * Did you link the stylesheet?
     `<link rel="stylesheet" href="style.css">`

4. **Check Order and Specificity**

   * Inline styles override external ones
   * More specific selectors override general ones

---

### 🪄 JavaScript Debugging Process

1. **Check the Console for Errors**

   * Read the **first error** and look for:

     * `Uncaught ReferenceError` → variable not defined
     * `Uncaught TypeError` → trying something on the wrong type

2. **Check Capitalization and Spelling**

   * JS is **case-sensitive**: `document` ≠ `Document`
   * Watch for typos like `getElemntById`

3. **Check Syntax**

   * Missing semicolons (`;`)
   * Matching `()` and `{}` and `[]`
   * Strings need quotes: `"text"` or `'text'`

4. **Check If the Script Is Linked Properly**

   * In your HTML:

     * ✅ `<script src="script.js"></script>`
     * Put it **at the bottom** of `<body>`, or use `defer`

5. **Use `console.log()` Often**

   * Print variable values to the console to check what’s happening
   * Example: `console.log(myVar);`

6. **Check DOM Selectors**

   * Does the element exist in the HTML?
   * Use `document.querySelector("#id")` or `.class`
   * If you’re getting `null`, check spelling and that the element is loaded

