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

#### **Example Project: Coffee Drink Maker**
Imagine a blank cup on the screen. The user can click buttons like "Add Coffee" or "Add Milk." Each click changes how the drink looks or adds a new visual layer. You’ll use **DOM methods** like `querySelector`, `style`, `textContent`, `addEventListener`, and possibly `createElement` and `appendChild` to make this happen.

<html>
<p class="codepen" data-height="300" data-theme-id="light" data-default-tab="result" data-slug-hash="vEEWVMO" data-pen-title="Covfefe" data-user="katerinawalter" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/katerinawalter/pen/vEEWVMO">
  Covfefe</a> by Katerina Walter (<a href="https://codepen.io/katerinawalter">@katerinawalter</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://public.codepenassets.com/embed/index.js"></script>
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

Now, make the buttons actually _do something_! Use the last project to help you. Here are two additional ways to use **JavaScript to change the page**:

* Button that changes the **CLASS NAME** attached to an element:
  ```js
  const cup = document.querySelector("#cup-display");
  
  const milkBtn = document.querySelector("#add-milk");
  milkBtn.addEventListener("click", addMilk);
  
  function addMilk() {
    cup.classList.remove("coffee");
    cup.classList.add("milk");
    cup.textContent = "[ Coffee with Milk ]";
  }
  ```
  > This strategy is useful for applying larger _sets of styling rules_, as an alternative to setting individual style properties like we did in the last project with `element.style.cssProperty = "value"`.
* Button that **CREATES** and **ADDS** a new HTML element to the document: 
  ```
  const iceBtn = document.querySelector("#add-ice");
  iceBtn.addEventListener("click", addIce);
  
  function addIce() {
    const iceCube = document.createElement("span");
    iceCube.textContent = "🧊";
    cup.appendChild(iceCube);
  }
  ```

### **Step 5: Customize Your Simulation**

<div class="task" markdown="block">
  
Replace the example with a simulation of your own unique **theme** and style! Use [JavaScript DOM operations](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/DOM_scripting) to manipulate the **HTML and CSS** of the document.

#### 📖 JS CHEATSHEET:

| Syntax Example                                | Description |
|-----------------------------------------------|----------------|
| `const element = document.querySelector();`    | Selects the first **HTML element** that matches the provided **CSS selector** (`tag`, `.class`, or `#id`) |
| `element.textContent = "text";`                      | Sets the **text** inside an element like `<h1>`, `<p>`, or `<span>` |
| `element.src = "source";`                               | Sets the **source attribute** of an `<img>` element |
| `element.style.property = "value";`               | Changes an **inline style** of the selected element by setting a [CSS property](https://www.w3schools.com/jsref/dom_obj_style.asp) (_ex:_ `element.style.border = "2px solid black";`) |
| `element.classList.add();`          | **Adds a class name** (set of _styling rules_ defined in CSS) |
| `element.classList.remove();`       | **Removes a class name** from the element (therefore removing that set of _styling rules_) |
| `element.addEventListener('click', functionName);` | Attaches an _event listener_ to an element (usually a `<button>`) to **trigger a function** in response to **user actions** |
| `function functionName() {}` | Defines a new **function** (_process_) that executes a set of JavaScript **statements** (_instructions_) when activated |
| `const newElement = document.createElement('tag');` | Creates a **new HTML element** in the DOM |
| `element.appendChild(newElement);`                 | Adds a new _child element_ to a _parent element_ (usually a `<div>`) in the document |

#### 🎯 REQUIREMENTS:
- [ ] One **display area** (or more) that can change with user interaction
  - Include appropriate HTML elements to _build the scene_ of your simulation
    > _Examples:_ `<p>`, `<div>`, `<span>`, `<img>`
  - Design the initial layout/appearance of the elements with CSS rules
- [ ] At least **3 buttons** (or other interactive controls, like key presses)
  - Use `document.querySelector` to select the button elements in JavaScript
  - Use `addEventListener` to connect each button element to a function
  - Define a `function` for each button that handles **changes** in your simulation
- [ ] At least **10 visible DOM changes** handled in JavaScript, such as:
  - Changing individual `style` properties 
    > _Reference:_ [HTML DOM Style Object Properties](https://www.w3schools.com/jsref/dom_obj_style.asp)
  - Apply **class names** dynamically for larger sets of styling rules (`classList.add`, `classList.remove`)
  - Changing the `textContent` of **text elements**
  - Modifying the `src` attribute of **image elements**
  - Adding **new elements** to the display area (`createElement`, `appendChild`)
    > _Reference:_ [JavaScript Document Object Model](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/DOM_scripting)

</div>

#### Extension Ideas:

We have only just scratched the surface of what JavaScript can do! Try to implement one or more of the following features:

- A **RESET** button that clears the display area _back to the starting appearance_.
  > See the JavaScript code for `resetBtn` and `resetCup()` in my example here: [Wk32 CodeCollab](https://github.com/BWL-CS/cs1-wk32-codecollab)
- Use the `classList.add()` function to attach an **ANIMATION** to an element.
  > See the CSS code for `.milk-animation` and `@keyframes pour-milk`, and the JavaScript code for `addMilk()` in my example here: [Wk32 CodeCollab](https://github.com/BWL-CS/cs1-wk32-codecollab)
- Use `.setTimeout()` to create a **delay** before a change happens
  > _Reference:_ [W3 Schools - Window setTimeout Method](https://www.w3schools.com/jsref/met_win_settimeout.asp)
- Add **sound effects** using the `<audio>` tag in HTML and `.play()` in JS
  > _Reference:_ [HTML Audio](https://www.w3schools.com/html/html5_audio.asp) and [JavaScript play Method](https://www.w3schools.com/tags/av_met_play.asp)
- Use **checkboxes** or other types of **HTML form input** instead of buttons
  > _Reference:_ [How to Submit a Form with JavaScript](https://www.freecodecamp.org/news/how-to-submit-a-form-with-javascript/)
