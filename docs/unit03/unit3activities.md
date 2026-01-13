---
layout: notes
title: "🎯 Unit 3 Activities" 
parent: "3️⃣ Bootstrap"
nav_order: 4
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
3. Specify the **repository name**: `CS1-Unit3-Activity#`
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

## 🖼️ ACTIVITY #1: Art Gallery

We will build a professional-looking webpage for a fictional **art gallery** using ONLY Bootstrap classes for all of the styling and layout. 

### PART A: Design a Hero Section

<div class="task" markdown="block">

1. Decide on a **theme**! Your gallery can be focused on an _art history period_ (Renaissance, impressionist, postmodern, etc.), an _artistic medium_ (photography, sculpture, etc.), or specific _subject_.  

1. In your HTML's `<body>` section, add two `<div>` elements with Bootstrap container classes. One should be a **fluid container**, the other a **fixed container**.

1. In the **fluid** container div, include an `<h1>` element with a title for your gallery, and a `<p>` element with a description of your gallery. 

1. Download an **image** that represents the "storefront" of your gallery and upload it to your repository's File Explorer tab.

1. In the **fixed** container div, include an `<img>` element with the `src` set to your storefront image. Give the image a class of `class="img-thumbnail"`.

</div>

### PART B: Apply Styles with Typography & Color Classes

Now that your page has some opening content, let’s enhance the appearance using Bootstrap’s built-in **typography** and **color utility classes**.

<div class="task" markdown="block">

1. Use **text classes** to change the appearance of your gallery’s title and description. Try adding emphasis with classes like `fw-bold`, `fst-italic`, or `text-uppercase`.
   👉 *Optional challenge*: Use `display-*` classes for oversized titles (e.g., `display-1`, `display-2`...).

2. Choose a **color scheme** for your hero section. Use **text color**, **background color**, and **border** utility classes from Bootstrap. Make sure your colors complement each other!
   👉 Examples: `bg-dark text-light`, `border border-primary`, `bg-warning text-dark`, etc.

3. Try adjusting **spacing** with Bootstrap’s margin (`m-*`) and padding (`p-*`) utility classes to better position your elements on the page.

4. Optional: Use `text-center`, `text-end`, or `text-start` to align your text.

</div>

---

### PART C: Set up a Responsive Grid Structure

Let’s create a layout for your artwork using Bootstrap’s **grid system**.

<div class="task" markdown="block">

1. Inside a `<div class="container">`, add a `<div class="row">` to begin your grid.

2. Create **at least 3 columns** (`<div class="col">`) inside your row. These will hold the featured artwork for your gallery.

3. Explore **responsive column classes** like `col-sm-6`, `col-md-4`, or `col-lg-3` to make your layout adjust on different screen sizes.
   👉 Try mixing column sizes to experiment with how Bootstrap adapts your layout!

4. Give each column a **unique border or background color class** so you can easily see the structure.

</div>

---

### PART D: Populate the Grid with Images

Time to bring your gallery to life by adding some artwork!

<div class="task" markdown="block">

1. Inside each column from Part C, add an `<img>` element to showcase a piece of art. You can find royalty-free artwork online (e.g., [Unsplash](https://unsplash.com), [Pexels](https://www.pexels.com), or [WikiArt](https://www.wikiart.org)).

2. Use the Bootstrap class `img-fluid` on your images so they scale correctly on all screen sizes.

3. Add a **caption** below each image using a `<p>` or `<small>` tag. Style these captions using `text-muted`, `fw-light`, or alignment classes (`text-center`, etc.).

4. Optional: Wrap each image and caption in a `<div class="card">` to give it a framed, elevated look. Try combining with `shadow`, `border`, or `rounded` classes for extra polish.

</div>


---

