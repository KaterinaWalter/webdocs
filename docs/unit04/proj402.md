---
layout: project
title: "💻PROJECT #4.2"
projectname: "Light & Dark Mode"
parent: "4️⃣ JavaScript"
nav_order: 6
---


## Overview

### **Project Goal**
Create a fun and interactive **simulation of a real-life process** using JavaScript and the DOM. Your simulation should allow users to interact with buttons or other inputs on a webpage and see changes appear on screen. This is your chance to turn your code into a mini-world where things come to life when clicked!

#### **Example Project: Coffee Drink Maker**
Imagine a blank coffee cup on the screen. The user can click buttons like "Add Milk," "Add Caramel Syrup," or "Add Ice." Each click changes how the drink looks or adds a new visual layer. You’ll use **DOM methods** like `querySelector`, `style`, `textContent`, `addEventListener`, and possibly `createElement` and `appendChild` to make this happen.

<html>
<details>
<summary>📥<strong>PROGRAM SETUP & SUBMISSION INSTRUCTIONS</strong></summary>
  
<div class="setup" markdown="block">

1. Go to the `CS1 Project 4.2` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Project 4.2` assignment on Blackbaud.

</div>
 
</details>
</html>

--- 

## Instructions

### **Step 1: Plan Your Simulation**

🧠 Start by choosing a theme. Here are some ideas:
- **Build a Sandwich** (add bread, cheese, lettuce, meat…)
- **Dress a Character** (change outfit colors, add hats, accessories…)
- **Assemble a Pizza** (choose toppings and watch them appear…)
- **Weather Simulator** (toggle between sunny, rainy, snowy visuals…)
- **Tiny Garden** (plant seeds, grow flowers, change the background…)

📝 Sketch or list:
- What _elements_ are on screen when the page loads?
- What _buttons_ (or keyboard controls) can the user interact with?
- What _changes_ will happen on screen?

### **Step 2: Set Up Your HTML**

🏗️ Create a simple HTML page with:
- A descriptive title/header (in an `h1` element)
- A **display area** (like a `div` or `section`) to show your simulation
  ```html
  <div id="cup-display" class="coffee">[ Coffee ]</div>
  ```
- At least **three buttons** that trigger different actions
  ```html
  <div class="container text-center m-auto">
    <button id="add-milk">Add Milk</button>
    <button id="add-ice">Add Ice</button>
    <button id="reset">Reset</button>
  </div>
  ```

### **Step 3: Style Your Display (`style.css`)**

🎨 Use CSS to format your starting display area. For example:

```css
#cup-display {
  width: 200px;
  height: 250px;
  text-align: center;
  font-size: 22px;
  margin: auto;
  border: 10px solid black;
}
```

➕ You can also create “layer” classes to add visual effects:
```css
.coffee {
  background: #6F4E37;
}

.milk {
  background: #b89d8a;
}
```
> The intention here is to _switch_ between the **class** names! 

### **Step 4: Add Interactivity with JavaScript (`script.js`)**

Now, make the buttons actually do something! Use:
- `const element = document.querySelector("selector");`
- `element.addEventListener("click", function);`
- `.style` or `.classList.add()`
- `.textContent` or `.innerHTML`
- `createElement` and `appendChild`

```js
const cup = document.querySelector("#cup-display");

const milkBtn = document.querySelector("#add-milk");
milkBtn.addEventListener("click", addMilk);

function addMilk() {
  cup.classList.remove("coffee");
  cup.classList.add("milk");
  cup.textContent = "[ Coffee with Milk ]";
}

const iceBtn = document.querySelector("#add-ice");
iceBtn.addEventListener("click", addIce);

function addIce() {
  const iceCube = document.createElement("span");
  iceCube.textContent = "🧊";
  cup.appendChild(iceCube);
}
```

### **Step 5: Customize Your Simulation**

Replace the coffee drink example with your own theme and style! You must include:
- A **display area**
- At least **3 buttons or interactive elements**
- At least **3 visible DOM changes**, such as:
  - Changing styles or background colors
  - Changing text on screen
  - Adding new elements to the display (`createElement`, `appendChild`)

### Extension Challenges (Optional)

Try adding one or more:
- A **Reset** button that clears the display area
- Use `setTimeout` to create a delay before a change happens
- Add sound effects using the `<audio>` tag and `.play()`
- Use a **dropdown menu** or **checkboxes** instead of buttons

### ✅ Project Checklist

Before you submit:
- [ ] My simulation has a clear theme
- [ ] I used at least 3 types of DOM operations (`style`, textContent, createElement, etc.)
- [ ] I included at least 3 user interactions (buttons or controls)
- [ ] My HTML, CSS, and JS are organized into separate files
- [ ] I had fun and made something cool!

---

### 📚 Resources & JS Cheatsheet

| Concept                | Example                              | What It Does                                      |
|------------------------|---------------------------------------|---------------------------------------------------|
| `querySelector()`      | `const element = document.querySelector('#btn');`      | Function that _selects_ an **HTML element**                          |
| Event Listener         | `element.addEventListener('click', function);`       | Runs a **function** when something is clicked        |
| `.style.property`      | `element.style.color = 'red';`         | Changes a **CSS property** with JavaScript           |
| `.textContent`         | `element.textContent = 'Hello!';`      | Changes what **text** is displayed in an element     |

{:.highlight}
Refer to the notes page for detailed explanations: [📓 Notes 4.4: HTML DOM](https://coderina.dev/webdocs/docs/unit04/notes404.html)

