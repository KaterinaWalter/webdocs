---
layout: project
title: "💻 Project #3"
projectname: "Animated Movie Scene"
parent: "2️⃣ Advanced HTML & CSS"
nav_order: 8
---


### Overview

🎥 CSS **animations** and **transforms** are powerful tools that bring life to web pages. With **animations**, we can create smooth transitions, moving objects, or even complex _sequences_ of changes, making websites more interactive and visually appealing. **Transforms** allow us to _manipulate elements_ by rotating, scaling, or repositioning them, enabling unique and dynamic designs.

In this project, you'll practice these techniques by building an **animated scene** inside a defined container. You’ll experiment with movement, resizing, and interactivity to make a creative and engaging display. 

> 🧠 **BRAINSTORM:** Look up on Google Images: _"iconic scenes from..."_ + the title of your favorite **movie**, **show**, or **book**. 

<html>
<details>
<summary>📥 <strong class="text-green-200">PROJECT SETUP & SUBMISSION INSTRUCTIONS</strong></summary>
  
<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Animated-Scene`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Write code in this Codespace during class.

</div>

</details>
</html>


--- 

### Instructions

#### Part A: Setting Up the Starter Code

<div class="task" markdown="block">
  
1. **Add Starter CSS Code**
    * Write the following style rules in `style.css`:
```css
html, body {
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
> These rules basically "reset" the settings of the overall page. 
2. **Set the Background**
    * Add a `body` style rule to include a background image:
```css
body {
    background-image: url("https://wallpaper.dog/large/20552168.jpg");
    background-size: cover;
}
```
3. **Add the Scene Description Section**
    * Inside the `<body>` tag in `index.html`, create a container to describe the scene: `<div id="scene-description"></div>`
    * Inside that `<div>`, include an `<h1>` element with the scene **title** and a `<p>` element with a brief **description** of the scene. 
4. **Style the Scene Description**
    * In `style.css`:
```css
#scene-description {
    width: 600px;
    margin: 20px auto;
    text-align: center;
    font-family: "Trebuchet MS";
    font-size: 0.8em;
    color: white;
}
```
5. **Add the Scene Container Section**
    * Below the `#scene-description` div in HTML, add another container for the main animation area: `<div id="scene-container"></div>`
6. **Style the Scene Container**
    * In `style.css`:
```css
#scene-container {
    width: 600px;
    height: 400px;
    margin: auto;
    border: 5px solid black;
    background-color: white;
    overflow: hidden; /* contain objects "on-screen" */
}
```

</div>

#### Part B: Building & Animating the Scene

<div class="task" markdown="block">

1. **Plan your Scene**
    * Pick an **iconic scene** from a movie, TV show, or book that you'd like to model.
    * Identify several possible animations to make your scene dynamic (_e.g., a bouncing ball, flying objects, spinning elements, people walking, etc._)
2. **Add Elements to the Scene**
    * Inside the `#scene-container`, add HTML elements to represent props, actors, etc.
      >
    * _For example:_
      * `<img id="actor" src=" ">` for **images/clipart**
      * `<div id="ground"></div>` for **blocks/shapes**
      * `<p id="ball">🏈</p>` for **emojis/symbols**
3. **Style the Elements**
    * Define styles for the new elements to position and size them.
    * Example styling for a `p` tag that holds an emoji: 
    ```css
    #ball {
        display: inline-block;
        font-size: 30px;
        position: absolute;
        top: 20%;
        left: 15%;
        z-index: 5;
    }
    ```
4. **Define CSS Animations**
    * Use the `@keyframes` rule to define the frames ("timepoints") of an animation **sequence**.
    * Incorporate movement using `transform` functions like `rotate`, `scale`, `skew`, and `translate` within your sequence.
      > *Reference:* [📖 W3Schools - Transforms](https://www.w3schools.com/css/css3_2dtransforms.asp)
    * _Example:_
    ```css
    @keyframes spin {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
    }
    ```
5. **Attach Animations to Elements**
    * In the selector for an object you want to animate, configure the `animation` property.
      > *Reference:* [📖 W3Schools - Animations](https://www.w3schools.com/css/css3_animations.asp)
    * _Example:_
    ```css
    #ball {
        animation: spin 5s infinite linear;
    }
    ```
    > Remember that this is **shorthand** for the 4 important _sub-properties_ that control the settings of an animation: `animation-name`, `animation-duration`, `animation-iteration-count`, `animation-timing-function`
6. **Test, Edit, Repeat!**
    * Ensure the animations are smooth and work well together, adjusting **durations**, **iteration counts**, and **timing functions** as needed.
      > There are other helpful, but optional, sub-properties like `animation-delay` and `animation-direction` available. _Look them up!_
    * You may also need to adjust your `@keyframes` definitions to include more points (e.g. `0%`, `25%`, `50%`, `75%`,`100%`).

</div> 

--- 

### Minimum Requirement Checklist

- _HTML Content:_
  - [ ] Include at least **6 HTML elements** inside the `#scene-container` with distinct classes or ids, using the appropriate tags (e.g., `<div>`, `<p>`, `<span>`, `<img>`).
- _CSS Base Styles:_
  - [ ] Style all elements to fit your **theme** (e.g., colors, sizes, positioning).
- _CSS Animations:_
  - [ ] Define at least 2 distinct `@keyframes` **animation sequences**. One of these must have _more than 2 points_ in the animation sequence (e.g. `0%`, `50%`, `100%` rather than just `from` and `to`).
  - [ ] In a selector for the **element** to be animated, specify the relevant **animation** **properties** (e.g., `animation-name`, `animation-duration`, `animation-iteration-count`, `animation-timing-function`, along with any optional customizations like `animation-delay` or `animation-direction`).
- _CSS Transforms:_
  - [ ] Apply at least 4 different `transform` functions (e.g., `rotate`, `scale`, `translate`).
- _CSS Positioning:_
  - [ ] Use at least 2 different **positioning techniques** (e.g., `absolute`, `relative`, or `fixed`).
- _CSS Customization:_
  - [ ] Adjust the `background` of the movie scene, or `border` styles for visual appeal.
  - [ ] Ensure that the final product of your movie scene looks **cohesive**.

#### Bonus Features
- Include an **interactive** effect (e.g., `:hover` pseudo-class selector with a `transition` property).
  - See [📖 W3Schools - Pseudoclasses](https://www.w3schools.com/css/css_pseudo_classes.asp) and [📖 W3Schools - Transitions](https://www.w3schools.com/css/css3_transitions.asp)
- Use CSS **variables** for repeated values.
  - See [📖 W3Schools - Variables](https://www.w3schools.com/css/css3_variables.asp) 
- Create a "start" `button` that triggers animations using a `class` toggle (_requires some JavaScript_).
- Experiment with CSS `clip-path` or `filter` for advanced effects.

{:.highlight}
**RESOURCES:** While working on this project or attempting the bonus features, you are encouraged to look up any CSS `properties` on Google or [📖 W3Schools](https://www.w3schools.com/css/), review our [📓 Unit 1 Notes](https://coderina.dev/webdocs/unit01) or [📓 Unit 2 Notes](https://coderina.dev/webdocs/unit02), and make use of the helpful [🎨 SheCodes CSS Tools](https://generators.shecodes.io/). 


