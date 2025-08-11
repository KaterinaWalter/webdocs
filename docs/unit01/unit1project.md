---
layout: project
title: "💻 Unit 1 Project"
projectname: "Recipe Blog"
parent: "1️⃣ Web Dev Foundations"
nav_order: 6
---


### Overview

It's time to practice all of the HTML knowledge you have acquired. In this project, you are going to build a basic recipe website. The website will consist of a main index page which will have links to a few recipes. 
> The website won't look very _pretty_ by the time you've finished, unless you're into [brutalist web design](https://brutalistwebsites.com/), that is.

{:.highlight}
It's important to keep in mind that this project is just to build your HTML chops; we will revisit this project in the future to style it up with CSS.

<html>
<details>
<summary>📥 <strong class="text-green-200">PROJECT SETUP & SUBMISSION INSTRUCTIONS</strong></summary>
  
<div class="setup" markdown="block">

1. Go to the `CS1 Unit 1 Project` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Unit 1 Project` assignment on Blackbaud.

</div>

</details>
</html>

### Part A: Build the HTML Structure

#### 1. Create Initial Structure
<div class="task" markdown="block">

1. Within the project, navigate to the `index.html` file.
1. Ensure that it is already filled out with the usual **boilerplate HTML**, with a `head` and `body` section inside the opening & closing `html` tags.
2. Add an `h1` heading in the body section that describes the main title of the website (like _"My Favorite Recipes"_ or _"Sweet Treats for Fall"_).

</div> 

#### 2. Start Recipe Section

<div class="task" markdown="block">
 
1. Create a **new `div` element** to group together the information for your first recipe on the page.
  
2. Specify a **unique identifier** within the `div` opening tag, like this: `<div id="recipe-name">`
> You can use the name of your favorite dish or, if you need some inspiration, you can find a recipe to use at [Allrecipes](https://www.allrecipes.com/).

3. For now, just include an `h2` **heading** inside the `div`, with the recipe's name as its content.

4. Back at the top of the `body` section, under the first `h1`, add a **link** to the recipe `div` section you just created.
> _Example:_ `<a href="#recipe-name">Recipe Name</a>`. 
> * The `href` attribute is directing the anchor to the `div` on the page that has `id="recipe-name"`. Replace `recipe-name` with your own identifier.
> * The _text_ of the link should again be replaced with the actual recipe name.

</div>

#### 3. Add Recipe Section Content

<div class="task" markdown="block">
 
Your new recipe `div` section must include the following content:
1. An **image** of the finished dish under the `h2` heading that you added earlier. You can find images of the dish on Google or [Allrecipes](https://www.allrecipes.com/).
1. Under the image, it should have an appropriately sized (_smaller than the recipe title heading_) "Description" **heading** followed by a **paragraph** or two describing the recipe.
1. Under the description, add an "Ingredients" **heading** followed by an **unordered list** of the ingredients needed for the recipe.
1. Finally, under the ingredients list, add a "Steps" **heading** followed by an **ordered list** of the steps needed for making the dish.

</div>

#### 4. Add More Recipes

<div class="task" markdown="block">

1. Add **two more recipes** with identical structures to the recipe `div` section you've already created.
1. Don't forget to **link** to the new recipes at the top of the page. This will help with **navigation** around your page, so users can click to jump to the recipe they want to see.

Also, consider putting all the links in an unordered list so they aren't all on one line.

_Example:_

```html
 <ul>
    <li><a href="#lasagna">Lasagna Recipe</a></li>
    <li><a href="#pizza">Pizza Recipe</a></li>
    <li><a href="#chicken-milanese">Chicken Milanese Recipe</a></li>
  </ul>
```
  
Your links won't be flashy, but for now, just focus on building them out.

</div>

#### Extensions
* Add even more recipes!
* Incorporate emojis to embellish your text content, if you like the way they look. 
* Create a **header image** or **logo** for your recipe blog on [Canva](https://www.canva.com/) and add it to the top of your page before the `h1` heading.

### Part B: Style with CSS


<!-- TODO: Improve the steps and checklist for this part 

<div class="task" markdown="1">

🎨 Remember the Recipe page you created to practice the HTML topics? Well, it's rather *plain* looking, isn't it? Let's fix that by adding some CSS styling to it!

- How you actually style it is completely open, but you should use the **external CSS method** (for this practice and moving forward).
- You should also try to use several of the properties mentioned in the previous section (**color**, **background color**, **typography** properties, etc).
  - Take some time to play around with the various properties to get a feel for what they do. For now, don't worry at all about making it look *good*. This is just to practice and get used to writing CSS, not to make something to show off on your resume.
- We haven't covered how to use a custom font for the `font-family` property yet, so for now take a look at [CSS Fonts](https://www.w3schools.com/Css/css_font.asp) for a list of generic font families to use, and [CSS Web Safe Fonts](https://www.w3schools.com/cssref/css_websafe_fonts.asp) for a list of fonts that are web safe. Web safe means that these are fonts that are installed on basically every computer or device (but be sure to still include a generic font family as a fallback).
- Apply what you learned about the box model to improve the appearance of your Recipe blog from Part A. Get creative with **layouts**, **colors**, and **styles** to make your page uniquely captivating!

</div>

-->
