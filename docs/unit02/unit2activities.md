---
layout: notes
title: "🎯 Unit 2 Activities" 
parent: "2️⃣ Advanced HTML & CSS"
nav_order: 6
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
3. Specify the **repository name**: `CS1-Unit2-Activity#`
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

## ©️ ACTIVITY #1: Layout Copycat

For this activity you'll be **creating a web page that mimics a provided design**. The design we're providing you comes in the form of 2 images: one is an image of the complete website, and one has some details about some of the fonts and colors we've used.

Get your **project as close as you can to the design**, but do not worry about getting it pixel-perfect. Don't get out your ruler or count pixels to find the exact margins between the various sections. The point of this assignment is to create something from scratch and get the various elements in more or less the right position relative to the rest. It doesn't matter if you use `margin: 24px` when the design actually has `margin: 48px`.

### Instructions & Requirements

{:.highlight}
Do *not* be afraid to use Google or go back to the unit notes to look something up. **In real life, professional developers use Google *constantly* for things that they have been doing for years.** At this point it is not expected that you will have everything memorized, so don't worry about it. Additionally, there are a few small details that you may not have encountered in our lessons yet. *This is on purpose.* These details are minor, and easily 🔍 **searched** (e.g. Google `css rounded corners`).

#### Iteration 1: Mimic the Structure
<div class="task" markdown="block">

1. Download the **design images** and take a look at what you're going to be creating here: [Image One (Full Design)](https://cdn.statically.io/gh/TheOdinProject/curriculum/81a5d553f4073e593d23a6ab00d50eef8620796d/foundations/html_css/project/imgs/01.png), [Image Two (Color and Fonts)](https://cdn.statically.io/gh/TheOdinProject/curriculum/69e40b6fcacf567f77243547b7f89df75dd8c3d0/foundations/html_css/project/imgs/02.png)
> **Hint:** The font that's being used in the images is `Roboto`, which can be found on [Google Fonts](https://fonts.google.com/).
2. There are many ways to tackle a project like this, and it can be overwhelming to look at a blank HTML document and not know where to start. Our suggestion: take it **one section at a time**.
>The website you're creating has 4 main sections (and a footer), so pick one and get it into pretty good shape before moving on. Starting at the TOP is always a solid plan.
3. For the section you're working on, begin by **getting all the content onto the page** before beginning to style it. In other words, code the `HTML` and *then* code the `CSS`. You'll probably have to go back to the HTML once you start styling, but bouncing back and forth from the beginning will take more time and may cause more frustration.
> Many of the elements on this page are very similar to things you saw in our [📓2.1: Flexbox](https://coderina.dev/webdocs/docs/unit02/notes201.html) notes... feel free to go back to those if you need a refresher.

</div>

#### Iteration 2: Add Your Own Content

<div class="task" markdown="block">

*Finally*, you are free to **substitute your own content** into this design. The images just have some meaningless dummy content at the moment.

Make up a **fake business** and personalize this page around that theme:

1. Change all of the **text** (in `p` tags, `h1` tags, _etc_) to reflect that business.
> Feel free to look up landing pages for real businesses for inspiration!
2. Find, upload, & insert actual **images** in the `img` placeholders. 
3. In terms of CSS styling, keep the layout the same, but play around with the **colors** and **fonts** a bit.

</div>

{: .warning }

_A note about images on the web:_ You do not have the legal right to use just any image that you find on the web. There are many free images to be found, but make sure that the image you use is actually free for you to use, and make sure to credit the creator of the image in your project. Some good places to **find free-to-use images on the web** include [Pexels](https://www.pexels.com/), [Pixabay](https://pixabay.com/), [Unsplash](https://unsplash.com/), and [CleanPNG](https://www.cleanpng.com/).

---

## 🏙️ ACTIVITY #2: Build a Town

In this creative activity, you will use **CSS positioning** to place elements creatively on a webpage. Your goal is to design a unique **townscape** with icons, backgrounds, and `div` boxes styled into different shapes.

> 🧠 **BRAINSTORM:** Pick a fun theme! (city, rural, suburbs, island, fantasy, etc). 

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
📖 **RESOURCES:** While working on this activity, you are encouraged to look up CSS `properties` on Google or [W3Schools](https://www.w3schools.com/css/), review our [Unit 1 Notes](https://coderina.dev/webdocs/unit01) or [Unit 2 Notes](https://coderina.dev/webdocs/unit02), and make use of the helpful [SheCodes CSS Tools](https://generators.shecodes.io/). 

---

