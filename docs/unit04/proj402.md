---
layout: project
title: "💻PROJECT #4.2"
projectname: "Simulation"
parent: "4️⃣ JavaScript"
nav_order: 6
---


## Overview

### **Project Goal**
Create a fun and interactive **simulation of a real-life process** using JavaScript and the DOM. Your simulation should allow users to interact with buttons or other inputs on a webpage and see changes appear on screen. This is your chance to turn your code into a mini-world where things come to life when clicked!

#### **Example Project: Coffee Drink Maker**
Imagine a blank coffee cup on the screen. The user can click buttons like "Add Milk" or "Add Ice." Each click changes how the drink looks or adds a new visual layer. You’ll use **DOM methods** like `querySelector`, `style`, `textContent`, `addEventListener`, and possibly `createElement` and `appendChild` to make this happen.

<html>
  <p class="codepen" data-height="300" data-theme-id="light" data-default-tab="result" data-slug-hash="vEEWVMO" data-pen-title="Covfefe" data-user="katerinanavab" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/katerinanavab/pen/vEEWVMO">
  Covfefe</a> by Katerina Navab (<a href="https://codepen.io/katerinanavab">@katerinanavab</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>
  
</html>

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

🎨 Use CSS to format the **initial appearance** of your display area. For example:

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
> Here, setting some general styles that will NOT change later on. 

➕ You can also define **classes** for certain visual effects:
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

Now, make the buttons actually do something! Here are the JavaScript tools we have so far:

<!--
| Concept                | Example                              | What It Does                                      |
|------------------------|---------------------------------------|---------------------------------------------------|
| `.querySelector()`      | `const element = document.querySelector('#btn');`      | Function that _selects_ an **HTML element**                          |
| Event Listener         | `element.addEventListener('click', function);`       | Runs a **function** when something is clicked        |
| `.style.property`      | `element.style.color = 'red';`         | Changes a **CSS property** with JavaScript           |
| `.textContent`         | `element.textContent = 'Hello!';`      | Changes what **text** is displayed in an element     |

{:.highlight}
Refer to the notes page for detailed explanations: [📓 Notes 4.4: HTML DOM](https://coderina.dev/webdocs/docs/unit04/notes404.html)

-->

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

### Customize Your Simulation

<div class="task" markdown="block">
  
🎯 Replace the example with a simulation of your own unique **theme** and style! 

#### REQUIREMENTS:
- [ ] One **display area** (or more) that can change with user interaction
  - Include appropriate HTML elements to _build the scene_ of your simulation
    > _Examples:_ `<p>`, `<div>`, `<span>`, `<img>`
  - Design the initial layout/appearance of the elements with CSS rules
- [ ] At least **3 buttons** (or other interactive controls, like key presses)
  - Use `document.querySelector` to select the button elements in JavaScript
  - Use `addEventListener` to connect each button element to a function
  - Define a `function` for each button that handles changes in your simulation
- [ ] At least **10 visible DOM changes** handled in JavaScript, such as:
  - Changing individual `style` properties
    > _Reference:_ [HTML DOM Style Object Properties](https://www.w3schools.com/jsref/dom_obj_style.asp))
  - Apply **class names** dynamically (`classList.add`, `classList.remove`)
  - Changing the `textContent` of **text elements**
  - Modifying the `src` attribute of **image elements**
  - Adding **new elements** to the display area (`createElement`, `appendChild`)

</div>

#### Extension Ideas:

_"Done"?_ Nope... we've only just scratched the surface of what JavaScript can do! 

🎯 Try to implement one or more of the following features:

- A **reset** button that clears the display area back to the starting appearance
- Use `setTimeout` to create a **delay** before a change happens
- Add **sound effects** using the `<audio>` tag and `.play()`
- Use **checkboxes** instead of buttons (🔍 search _"HTML Form Checkbox"_)

