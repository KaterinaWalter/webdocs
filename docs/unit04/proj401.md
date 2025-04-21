---
layout: project
title: "💻PROJECT #4.1"
projectname: "Light & Dark Mode"
parent: "4️⃣ JavaScript"
nav_order: 5
---


### Overview

To demonstrate how **JavaScript** can be implemented in HTML/CSS webpages, we will create a usable **light/dark mode toggle** button using _variables_, _functions_, _conditionals_, and JavaScript's [DOM (Document Object Model)](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) library. 

<html>
<details>
<summary>📥<strong>PROGRAM SETUP & SUBMISSION INSTRUCTIONS</strong></summary>
  
<div class="setup" markdown="block">

1. Go to the `CS1 Project 4.1` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Project 4.1` assignment on Blackbaud.

</div>
 
</details>
</html>

--- 

### Tutorial Instructions

#### 🧱 Part A: Build a Simple HTML Page

1. In `index.html` add the following starter code inside the `<body>` section:
  
  ```html
  <div class="container">
    <h1 id="main-heading">Welcome to My Page</h1>
    <p id="description">This page supports light and dark mode!</p>
    <button id="toggle">Switch to Dark Mode</button>
  </div>
  ```
  > - We give the `<div>` a `class` called `container` so we can _select_ it in **CSS**.
  > - There’s a `<button>` element with an `id` called `toggle` so we can _target_ it in **JavaScript**.
  > - Note that the other elements have their own `id` values as well...

#### 🎨 Part B: Add Basic Styles in CSS

1. In `styles.css` apply the following styling rules to the whole page:
  ```css
  body {
      font-family: sans-serif;
      margin: 0;
      padding: 5px;
  }
  ```
  > - Leave out the **colors** so we can set them via JavaScript!
2. Center the div that contains the main content: 
  ```css
  .container {
      width: 60%;
      margin: auto;
      text-align: center;
  }
  ```
3. Style the button:
  ```css
  button {
      padding: 2px;
      margin-top: 5px;
      font-size: 24px;
  }
  ```

#### 💡 Part C: Write JavaScript for Theme Toggling

1. Create a **boolean** (`true`/`false`) variable to remember if we’re in dark mode or not:
  ```javascript
  let isDarkMode = false;
  ```

2. Before you can change anything on the page, you need to *select* the **HTML elements** you want to work with.
  ```javascript
  const body = document.querySelector('body');
  const heading = document.querySelector('#main-heading');
  const description = document.querySelector('#description');
  const toggleButton = document.querySelector('#toggle');
  ```
  > - The `querySelector()` function lets you select any element using its **tag**, `class`, or `id`.
  > - We’re selecting the button, the body (for background), the heading, and the paragraph. All of these "_selections_" are stored in named **variables** to be accessed later.
  > - `const` (_constant_) is used as the keyword to **declare variables** here instead of `let`, because `querySelector` returns just a _REFERENCE_ to the element's **location**, which does not change. 

3. Define a **function** that toggles the color theme mode:
  ```javascript
  function toggleMode() {
      // Code statements that modify the page for each mode
  }
  ```

4. Inside the function, start by flipping the value of `isDarkMode`:
  ```javascript
  // Flip the boolean with the NOT (!) operator
  isDarkMode = !isDarkMode; 
  ```

5. Next inside the function, add **conditional statements** to handle each mode depending on whether `isDarkMode` is `true` or not:
  ```javascript
  if (isDarkMode) {
      // Apply DARK MODE styles and text
  }
  else {
      // Apply LIGHT MODE styles and text
  }
  ```

6. In the `if (isDarkMode)` block, change the **style properties** and **text content** of the elements we selected earlier:
  ```javascript
  // Apply DARK MODE styles and text
  body.style.backgroundColor = 'black';
  body.style.color = 'white';
  heading.style.color = '#ffcc00';
  description.textContent = 'Dark mode is now enabled!';
  toggleButton.textContent = 'Switch to Light Mode';
  ```

7. In the `else` block, change the **style properties** and **text content** for light mode:
  ```javascript
  // Apply LIGHT MODE styles and text
  body.style.backgroundColor = 'white';
  body.style.color = 'black';
  heading.style.color = '#003366';
  description.textContent = 'Light mode is now enabled!';
  toggleButton.textContent = 'Switch to Dark Mode';
  ```

8. When the user clicks on the button, we want to trigger the `toggleMode()` function. AFTER the function definition, include this statement that adds an **event listener** to register button clicks:
  ```javascript
  toggleButton.addEventListener('click', toggleMode);
  ```
  > - This tells the browser: _"When the button is clicked, call the `toggleMode()` function."_
  > - We don’t use parentheses here (`toggleMode()` → ❌). Just pass the **function name** so it runs when clicked.

---

### 🆕 JavaScript Skills

| Concept                | Example                              | What It Does                                      |
|------------------------|---------------------------------------|---------------------------------------------------|
| `querySelector()`      | `const element = document.querySelector('#btn');`      | Function that _selects_ an **HTML element**                          |
| Event Listener         | `element.addEventListener('click', function);`       | Runs a **function** when something is clicked        |
| `.style.property`      | `element.style.color = 'red';`         | Changes a **CSS property** with JavaScript           |
| `.textContent`         | `element.textContent = 'Hello!';`      | Changes what **text** is displayed in an element     |
| Boolean Toggle         | `isDarkMode = !isDarkMode;`           | Switches `true` ↔ `false`                          |

{:.highlight}
Refer to the notes page for detailed explanations: [📓 Notes 4.4: HTML DOM](https://coderina.dev/webdocs/docs/unit04/notes404.html)

---

### Extension Tasks

{:.important}
You are required to attempt _at least TWO_ of the **creative features** suggested below to earn full credit on this project! 

1. **Change Images Based on the Mode**
  - 🖼️ Add an image of a sunny landscape to the HTML:
    ```html
    <img id="image" src="day.jpg">
    ```
  - Since you added a **new HTML element** to the document, you should create a JavaScript **named variable** for it as well. Call it `imageElement` and **select** it from the `document` the same way we selected the `heading`, `toggleButton`, etc. at the top of your script.
    > _HINT:_ Scroll up and look for all the `const` declarations. Follow the same pattern to select your image!
  - Inside your `toggleMode` function, switch the image's `src` attribute:
    ```javascript
    if (isDarkMode) {
      imageElement.src = 'night.jpg';
    }
    else {
      imageElement.src = 'day.jpg';
    }
    ```
    > _HINT:_ You already have an `if` and `else` block, so do not just copy-paste the code above. Figure out where you need to add the specific line that changes the `src` for each mode.

2. **Customize the Page's Appearance**
  - 🎨 If you loved the CSS unit, dive back into it and enhance the overall **style** of your page!
  - First, refine the base styles in `style.css` by setting more **properties** (`border`, `text-shadow`, `box-shadow`, `font-family`, etc.) 
  - Next, add **JavaScript statements** in the `script.js` toggle function to make even _more visual differences_ between the two themes. Refer here: [HTML DOM Style Object Properties](https://www.w3schools.com/jsref/dom_obj_style.asp) to see what else you can change inside your `toggleMode` function. 
  - Decorate with **emojis/icons**, for example, you could replace text with 🌞 and 🌙 icons for a fun visual toggle. _BONUS:_ Animate the icons using CSS `@keyframes`.
  - Make the background and text color changes **fade smoothly** by adding this `transition`:
  ```css
  body {
      transition: background-color 0.4s ease, color 0.4s ease;
  }
  ```

3. **Provide Multiple Color Themes**
  - Design and enable more than two color theme options. ⚠️ Note that every additional theme will _require its own_ HTML `<button>` and JavaScript `function`!
  - Check out trending **color palettes** on [Coolors.co](https://coolors.co/palettes/trending) to use as inspiration.
  - Pick **gradients** from [SheCodes.io](https://www.shecodes.io/gradients) to use for `background` instead of a plain color.  

4. **Keyboard Shortcut to Toggle Theme**
  - ⌨️ Add an event listener for _keyboard input_:
    ```javascript
    function handleKeydown(event) {
      if (event.key == 't') {
          toggleMode();
      }
    }
    document.addEventListener('keydown', handleKeydown);
    ```
    
5. **Save User’s Preference with `localStorage`**
  - 📥 When a user selects dark mode, _save their preference_ so it stays even after a refresh.
  - Try this:
    ```javascript
    localStorage.setItem('theme', 'dark'); // or 'light'
    ```
  - And on page load:
    ```javascript
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme == 'dark') {
      toggleMode(); // or set dark styles manually
    }
    ```

