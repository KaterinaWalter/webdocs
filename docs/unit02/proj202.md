---
layout: project
title: "💻PROJECT #2.2"
projectname: "Design a Town"
parent: "2️⃣ Advanced HTML & CSS"
nav_order: 6
---


### Overview & Setup

In this creative project, you will use **CSS positioning** to place elements creatively on a webpage. Your goal is to design a unique **townscape** with icons, backgrounds, and `div` boxes styled into different shapes.

> 🧠 **BRAINSTORM:** Pick a fun theme! (city, rural, suburbs, island, fantasy, etc). 

<div class="setup" markdown="block">

1. Go to the `CS1 Project 2.2` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Project 2.2` assignment on Blackbaud.

</div>

--- 

### Instructions

<div class="task" markdown="block">

1. 🖼️ **Add a Background Image:**
	* Find an image to use for the **ground**, such as grass, bricks, or a texture (check out this [Seamless Textures](https://architextures.org/textures) website). Feel free to experiment with different images to find one that fit your vision for the town.
	* In your CSS file, set the `background` to the image's `url`.
```css
body {
    background: url(" ");
    background-size: 20%;
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
2. 🌈 **Create a Gradient Background:**
	* In your `HTML` file, add a `<div>` with an `id="sky"` to represent the **sky**.
	* In your `CSS` file, style the sky with a `linear-gradient` of your choice. Experiment with different combinations of colors to create your ideal sky!
```css
#sky {
    background: linear-gradient(DeepSkyBlue, LightSkyBlue, AliceBlue);
    width: 100%;
    height: 60%;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 0;
}
```
3. ⭐️ **Add a Symbol/Emoji:**
	* Add a symbol or emoji to represent something in the sky. It could be a ☀️ (sun), 🌙 (moon), ☁️ (cloud), or any other symbol of your choice!
	* In your `HTML` file, add a `<span>` element (inline container) to hold your symbol:  `<span id="sky-symbol">☀️</span>`
	* In your `CSS` file, select your symbol to adjust the `size` and `position` it in the sky. Adjust the `top` and `left` properties to place the symbol exactly where you’d like.
```css
#sky-symbol {
    font-size: 150px;
    position: absolute;
    top: 5%;
    left: 10%;
}
```
4. 🟪 **Make Rectangles with Divs:**
	* In your `HTML` file, add a `<div>` with an `id="building-1"` to represent a **structure** in your town (like a house, store, or office building).
	* In your `CSS` file, style it to give it a unique color and position it on the page.
	* Feel free to choose a different color, size, or position for your building.
```css
#building-1 {
    background-color: lightgray;
    width: 100px;
    height: 80px;
    position: absolute;
    top: 50%;
    left: 15%;
}
```
5. 🔺 **Make Triangles with Divs:**
	* INSIDE the **building** `<div>`, add another `<div>` with an `id` of `"roof-1"` or a name of your choice.
	* Style it to look like a triangular roof, as in the code snippet below. 
	* Adjust the colors, shapes, and sizes to fit your design. You could even use another symbol, like 🏠 or 🏛️, to create a roof effect.
```css
#roof-1 {
    position: relative;
    bottom: 60px;
    width: 0; 
    height: 0; 
    border-left: 60px solid transparent;
    border-right: 60px solid transparent;
    border-bottom: 60px solid brown;
}
```
6. 🎨 **Customize your Town:**
	* Get creative! Add more buildings, symbols, or decorative elements to make the town your own.
	* Experiment with shapes, colors, and different icons to add personality to your town.
	* See below for a **checklist of minimum requirements** for this project. 

</div>

### Minimum Requirements

#### Buildings or Structures:
- [ ] Include at **least 3 buildings or structures** (e.g., houses, stores, towers) created using `<div>` elements.
	* Each building should have a distinct style, size, or color to add variety to your townscape.

#### Symbols or Emojis:
- [ ] Use at least 10 [symbols](https://copychar.cc/symbols/) or [emojis](https://copychar.cc/emoji/) to represent elements of your **town**.
	* Icons or emojis can be added in the sky (e.g., ☁️ or 🌙), as landmarks (e.g., 🏛️ or 🏫), or as decorations (e.g., 🏠 or 🚗).
	* Ensure that these icons are positioned and sized appropriately to fit into the overall design.

#### Sky Design:
- [ ] The **sky** must include a [gradient background](https://gradients.shecodes.io/).
	* You can customize the colors to create a sunrise, sunset, daytime, or nighttime feel.
- [ ] Include at least one emoji or icon in the sky (e.g., ☀️, 🌙, or ☁️).

#### Extra Decorative Element(s):	
- [ ] Add at least one extra **decoration** to each building or structure, such as a roof, door, window, or tree.
	* Each extra element should be styled differently from the main building, using unique colors, shapes, or positioning.

#### Creative Positioning:
- [ ] Use **CSS positioning** (like `absolute` or `relative`) to place elements creatively around the town.
	* Experiment with different `top`, `left`, `right`, or `bottom` values to arrange your buildings and icons in a way that resembles a town layout.

{:.highlight}
📖 **RESOURCES:** While working on this project, you are encouraged to look up CSS `properties` on Google or [W3Schools](https://www.w3schools.com/css/), review our [Unit 1 Notes](https://coderina.dev/webdocs/unit01) or [Unit 2 Notes](https://coderina.dev/webdocs/unit02), and make use of the helpful [SheCodes CSS Tools](https://generators.shecodes.io/). 

