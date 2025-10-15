---
layout: project
title: "💻 Unit 1 Project"
projectname: "Recipe Blog"
parent: "1️⃣ Web Dev Foundations"
nav_order: 6
---


### Project Setup & Overview

It's time to practice all of the `HTML` and `CSS` knowledge you have acquired! In this project, you are going to build a **basic recipe blog website**. The website will consist of one page which will have links to a few recipes. 

<html>
<details>
<summary>📥 <strong class="text-green-200">PROJECT SETUP & SUBMISSION INSTRUCTIONS</strong></summary>
  
<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Recipe-Blog`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Write code in this Codespace during class.

</div>

</details>
</html>

### PART A: Build the HTML Structure 🧱

#### 1. Create Initial Structure
<div class="task" markdown="block">

1. Within the project, navigate to the `index.html` file.
1. Ensure that it is already filled out with the usual **boilerplate HTML**, with a `head` and `body` section inside the opening & closing `html` tags.
2. Add an `h1` heading inside the `body` section that describes the main title of the website (like _"My Favorite Recipes"_ or _"Sweet Treats for Fall"_).

</div> 

#### 2. Start Recipe Section

<div class="task" markdown="block">
 
1. Create a **new `div` element** to _group together_ the information for your first recipe on the page.
2. Specify a **unique identifier** within the `div` opening tag, like this: `<div id="recipe-name">`
  > You can use the name of your favorite dish or, if you need some inspiration, you can find a recipe to use at [Allrecipes](https://www.allrecipes.com/).
3. Include a **class name** within the `div` opening tag, like this: `<div id="lasagna" class="recipe-section">`
  > This will help with _styling_ all **recipe sections** later on! 
4. For now, just include an `h2` **heading** inside the `div`, with the recipe's name as its content.

</div>

#### 3. Fill in Recipe Content

<div class="task" markdown="block">
 
Your new recipe `div` section must include the following content:
1. An **image** of the finished dish under the `h2` heading that you added earlier.
  > You can find images of the dish on Google or [Allrecipes](https://www.allrecipes.com/).
1. Under the image, it should have an appropriately sized **heading** (_HINT: smaller than the recipe title heading_) with the words "Description".
1. Following the heading, include a **paragraph** or two describing the recipe.
1. Under the description, add an "Ingredients" **heading**, followed by an **unordered list** of the ingredients needed for the recipe.
1. Finally, under the ingredients list, add a "Steps" **heading**, followed by an **ordered list** of the steps needed for making the dish.

</div>

{:.highlight}
Forgot how to write `HTML` code for **images**, **headings**, **paragraphs**, or **lists**? Refer to your `Unit-1-Notes` repository on GitHub or review the [📓 Notes 1.2: HTML Foundations](https://coderina.dev/webdocs/docs/unit01/notes102)!


#### 4. Add More Recipes

<div class="task" markdown="block">

1. Add **two more recipes** with identical structures to the recipe `div` section you've already created, but replace the inner **text content**.
  > _TIP:_ You can **copy-paste** your own code! Select from the opening `<div>` tag until the closing `</div>` tag. 
1. Don't forget to change **attributes** for certain elements, such as the `id` of the `div` and the `src` of the `img`. 
  > Each `div` section must have a **unique** `id`, but you can leave their `class` names the same.

</div>

#### 5. Add In-Page Navigation Links

<div class="task" markdown="block">
  
1. Back at the TOP of the `body` section, under the first `h1`, add an **anchor** link to jump to each recipe `div` section.
  > _Example:_ `<a href="#recipe-name"> Recipe Name </a>`. 
  > * The `href` **attribute** is _directing_ the anchor to the `div` on the page that has `id="recipe-name"`. Replace `recipe-name` with your own identifier for that recipe.
  > * The _text_ of the link (between the `a` tags) should again be replaced with the actual recipe name.
2. **Repeat** to add links for the other two recipe sections.
  > Make sure to replace the `href` to match that recipe's `id`, and replace the _text_ to match that recipe's name.

</div>

---

### PART B: Style with CSS 🎨

#### 1. Apply general styles to the whole page

<div class="task" markdown="block">

1. In `style.css`, write a **selector** for the whole page. Remember that the `body` tag contains _all the content_:
   ```css
   body {
   
   }
   ```
2. _Inside_ the curly brackets for that selector, change the `background` **property** to any color you like:
   ```css
     background: pink;
   ```
3. Set the **text color** for the whole page:
   ```css
     color: purple;
   ```
4. Pick a `font-family` for your page:
   ```css
     font-family: sans-serif;
   ```
   > 🔡 Use one of the [web-safe fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php) to start out, but to _really_ make your page stand out, you can **import a custom font** by following my [Google Font Tutorial](https://coderina.dev/webdocs/docs/ref/fonts.html)!

</div>

#### 3. Style Your Headings

<div class="task" markdown="block">

1. **Select** your main title (the `h1` tag) and make it stand out by changing the following **properties**:
   * `color`
   * `text-align`
   * `font-size`
2. **Select** & style your recipe names (`h2`) so they look different from the page title. Change the following **properties**:
   * `color`
   * `font-size`
3. Give smaller headings (`h3`) a bold look. Change the following **properties**:
   * `font-weight`
   * `font-size`
     
</div>

#### 4. Add Borders and Spacing with the Box Model

<div class="task" markdown="block">

1. Give each recipe section (the `<div>` that holds the recipe) a border, padding, and margin.
   Example if your recipe `div`s use the `class` name `recipe-section`:
   ```css
   .recipe-section {
     border: 2px solid black;
     padding: 15px;
     margin: 20px 0;
   }
   ```
   > * **Border** adds a line around the box.
   > * **Padding** adds space between the text and the border.
   > * **Margin** adds space outside the border.
2. Change the border `width`, `style`, and `color` to experiment with different looks.

</div>

#### 5. Style Links

<div class="task" markdown="block">

1. Make your navigation links (`a` tags) look nicer by adding some simple styles:
   ```css
   a {
     color: purple;
     text-decoration: none;
     font-weight: bold;
   }
   ```

</div>

#### 6. Style Images

<div class="task" markdown="block">

1. Add a border to your recipe images. _Example:_
   ```css
   img {
     border: 2px solid black;
   }
   ```
2. Add some space _around_ them so they don’t touch the text.
   > Would this be `margin` or `padding`?
   
</div>

---

### Minimum Requirements Checklist

By the end of **PART A**, your `index.html` file should include, in this order:
* [ ] A `h1` heading that describes the theme of the blog
* [ ] 3 links (`a` tags) that anchor to different sections on the page (referencing `id` names)
* [ ] 3 recipes, each contained in a `div` section with a **unique** `id` name and a **shared** `class` name
  > _Each recipe section includes the following elements:_
  > * `h2` with the recipe's name
  > * `img` of the finished dish
  > * "Description" `h3` followed by a `p` (paragraph)
  > * "Ingredients" `h3` followed by a `ul` (unordered list) of ingredients
  > * "Steps" `h3` followed by an `ol` (ordered list) of steps

By the end of **PART B**, your `style.css` file should include:

* [ ] A background color for the page
* [ ] A custom text color and font family for the `body`
* [ ] Styled headings (`h1`, `h2`, `h3`) with different sizes and/or colors
* [ ] Borders, padding, and margins on your recipe sections
* [ ] Styles for links
* [ ] At least one set of styling rules for images

---

### Extension Challenges

If you finish the required checklist, try adding some of these extras to make your recipe site more creative:

* Add **even more recipes** by repeating the `<div>` structure you used for the other recipes. 
* Incorporate **emojis** 🍝 to embellish your text content, if you like the way they look. 
* Design a **header image** or **logo** for your recipe blog on [Canva](https://www.canva.com/). After you've finished the design, follow these steps to include it on your page:
   > 1. **Download** it from Canva as a `.png`, `.jpeg`, or `.jpg` file onto your computer.
   > 2. Drag it from your computer into your `File Explorer` tab in the Codespace to **upload** it to your project.
   > 3. In your `HTML` code, add an `img` element at the top of your page, before the `h1` heading. The `src` **attribute** should be set to the name of the image file. 
* **Background Gradients or Images:**
   * Instead of one solid background color, use a **gradient**. You can copy and paste a gradient from [SheCodes Gradients](https://www.shecodes.io/gradients).
   > _Example CSS Rule:_ `background: linear-gradient(to right, #ffecd2, #fcb69f);`
   * Another option is to use an **image**. For best results, search _"Seamless Pattern"_ on [Google Images](https://images.google.com/).
   > _Example CSS Rule:_ `background: url("image-name.png");`
* **Different Fonts for Headings:**
   * You can set your `h1`, `h2`, or `h3` to use a different `font-family` than the body text.
   * _Example:_
     ```css
     h1, h2, h3 {
       font-family: "Georgia";
     }
     ```
     > 🔡 Use one of the [web-safe fonts](https://www.w3schools.com/cssref/css_websafe_fonts.php) to start out, but to _really_ make your page stand out, you can **import a custom font** by following my [Google Font Tutorial](https://coderina.dev/webdocs/docs/ref/fonts.html)!

* **Rounded Corners on Boxes and Images:**
   * Use `border-radius` property to soften the look of divs or images.
* **Create “Button-Like” Links:**
   * Add background colors and padding to your `<a>` tags so they look more like buttons:
     ```css
     a {
       background: lightgray;
       padding: 5px 10px;
       border: 1px solid black;
     }
     ```
* **Centering Images:**
   * Wrap your image in a `<div>` with a class, then use `text-align: center` on the container.
   * _Example in HTML:_
     ```html
     <div class="centered">
       <img src="lasagna.jpg" alt="Lasagna">
     </div>
     ```
   * _Example in CSS:_
     ```css
     .centered {
       text-align: center;
     }
     ```

