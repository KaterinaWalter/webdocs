---
layout: notes
title: "📓2.2: Positioning" 
parent: "2️⃣ Advanced CSS"
nav_order: 2
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---
#### New Unit! Use a GitHub Template for class notes:
{:.no_toc}

<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Unit-2-Notes-Positioning`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Take notes in this Codespace during class, coding along with the instructor.

</div>

---

## CSS Positioning Modes

By now you have had quite a bit of practice moving elements around the screen using things like `margin`, `padding`, and `flex`box. These techniques have all relied on CSS's default **positioning-mode**: `static`. Static means the elements go along with the "normal flow" of the HTML document, much like a balloon with stored static electricity will stick to your sweater as you move:

![image](https://coolscienceexperimentshq.com/wp-content/uploads/2015/12/Make-Your-Hair-Stand-on-End-Science-Experiment-Step-2.jpg)

This default positioning-mode is intuitive, and you'll continue using it for almost all of your layout needs. However, there are other methods at your disposal that can be very useful in some situations.

#### Lesson overview
{:.no_toc}

This section contains a general overview of topics that you will learn in this lesson.

- You'll learn how to use `relative` positioning.
- You'll learn how to use `absolute` positioning.
- You'll learn how to use `fixed` positioning.
- You'll know the difference between each property and how to combine them.

![image](figures/positioned-elements-terminology.png)

<iframe width="560" height="315" src="https://www.youtube.com/embed/Sm1ORyc2Qao?si=8KWBw7jWXsXrtqbe" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

### Relative Positioning

The default positioning mode that you've gotten used to is **static**. The difference between static and relative is fairly simple:
* `position: static` is the default position of every element, and unless this `position` property is changed from `static`, the properties `top`, `right`, `bottom`, and `left` do not affect the position of the element. 
* `position: relative` on the other hand is pretty much the same as static, but properties `top`, `right...(etc.)` **displace** the element _relative to its normal position_ in the flow of the document.

![image](figures/css-relative-positioning.png)

<div class="imp" markdown="block">
  
`position: relative` moves elements around **relative** to where they would _normally appear in the static flow_ of the page. This is useful for **nudging boxes around** when the default flow is just a little bit off. Using any positioning scheme (other than `static`) enables specifying the location anywhere on the screen with the  `top`, `right`, `bottom`, and `left` properties: 

```css
.item-relative {
  position: relative;
  top: 30px; 
  left: 30px; 
}
```
> The `position: relative`; line makes it a **positioned element**, and the `top` and `left` properties let you define how far the element is offset from its static position. 

</div>

![image](figures/relative-positioning-offsets.png)

{:.highlight}
Note that these properties accept **negative values**, which means there’s two ways to specify the same offset. We could just as easily used `top: -30px;` in place of the `bottom: 30px;` declaration above.

### Absolute Positioning

**Absolute positioning** is just like relative positioning, but the **offset** is _relative to the entire browser window_ instead of the original position of the element. Since there’s no longer any relationship with the static flow of the page, consider this the most **manual** way to lay out an element.

<div class="imp" markdown="block">
  
`position: absolute` allows you to **position something at an exact point** on the screen without disturbing the other elements around it. Using an absolute positioning scheme enables specifying the location anywhere on the screen with the  `top`, `right`, `bottom`, and `left` properties: 

```css
.item-absolute {
  position: absolute;
  top: 100px; /* 100px AWAY from TOP edge of page */
  left: 50%; /* 50% AWAY from LEFT edge of page */
}
```
> The `position: absolute`; line makes it a **positioned element**, and the `top` and `left` properties let you define how far the element is offset from its static position. This is sort of like setting an **(x, y) coordinate** for the element.

</div>

> More specifically, using absolute positioning on an element will **remove that element** from the **normal document flow** while being positioned _relative to an ancestor element_. To put it in other words: elements that are removed from the normal flow of the document _do not affect other elements_ and are also not affected by other elements.

![image](figures/css-absolute-positioning.png)

{:.highlight}
This property is really useful when you want to position something at an **exact point** on the screen, without disturbing any of the other elements on the page. A couple of good use cases for absolute positioning are: **modals** (pop up windows), image with a **caption** on it, icons **on top** of other elements, or if you're making **CSS art** (_our next project!_ 🎨)

In the following example, we are using absolute positioning to display text _over_ an image.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="poWyWeJ" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/poWyWeJ">
Absolute Position | CSS Positioning</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

{:.warning}
**Disclaimer:** Absolute positioning has very specific use cases and if possible, using `flex` or `grid` layout schemes should be prioritized. Absolute positioning should NOT be used to do entire page layouts.

#### "Relatively-Absolute" Positioning

Absolute positioning becomes much more practical when it’s **relative to some other element that IS in the static flow** of the page. Fortunately, there’s a way to _change the coordinate system_ of an absolutely positioned element. Coordinates for absolute elements are always **relative to the closest container** that is a positioned element. It only falls back to being relative to the browser when none of its ancestors are positioned. 

![image](figures/css-relatively-absolute-positioning.png)

So, if we change `.item-absolute`’s **parent element** (let's call it `.container`) to be relatively positioned, it should appear in the top-left corner of that element instead of the browser window:

```css
.container {
  position: relative;
}
```
> The `.container` div is still laid out with the normal flow of the page, and we can manually move around our `.item-absolute` element inside that div wherever we need to. This is great, because if we want to alter the normal flow of the container, say, for a mobile layout, any absolutely positioned elements will _automatically move_ with it.

### Fixed Positioning

Elements with `position: fixed` have a lot in common with absolute positioning: the fixed positioning scheme is very manual, the element is removed from the normal flow of the page, and the coordinate system is relative to the `viewport` (the entire browser window). The key difference is that **fixed elements don’t scroll** with the rest of the page. You can still use `top`, `right`, `bottom`, and `left` properties to position it, and it will _stay in place as the user scrolls_. 

{:.highlight}
Fixed positioning is especially useful for things like **navigation bars** and **floating chat buttons** that you ALWAYS want displayed, regardless of where the user is on your page. 

![image](figures/css-fixed-positioning.png)

#### Sticky Positioning

Elements with `position: sticky` will act like normal **static** elements until you _scroll past them_, then they start behaving like **fixed** elements. They are also _not taken out of the normal flow_ of the document. It might sound confusing, so check out this [sticky positioning example](https://codepen.io/theanam/pen/MPLBYy) that might clear things up for you. 

{:.highlight}
Sticky positioning is useful for things like **section-headings**. Remember being able to still see what category you're looking at while scrolling through a shop? This is how it's done!


### Z-Index

We’ve never had to deal with “depth” issues before. Until now, all our HTML elements rendered above or below one another in an intuitive way. But, since we’re doing advanced stuff, relying on the browser to determine which elements appear on top of other ones isn’t going to cut it.

<div class="imp" markdown="block">
  
The `z-index` property lets you control the **depth** of elements on the page. If you think of your screen as 3D space, **negative** z-index values go farther **INTO** the page, and **positive** ones come **OUT** of the page. The default `z-index` value is `0`.

```css
.front-item {
  position: relative;
  z-index: 2;
}
.back-item {
  position: relative;
  z-index: 1;
}
```
>Take note of that `position: relative;` line. It’s required because only positioned elements pay attention to their z-index property. This is easy to forget, so make a mental note for the next time you’re having depth issues and your CSS rules don’t seem to have any effect.
</div>

![image](figures/css-z-index.png)

---

#### Knowledge check
{: .no_toc }

<div class="task" markdown="1">

💬 **DISCUSS:** The following questions are an opportunity to reflect on key topics in this lesson. _If you can't answer a question, click on it to review the material._

- [What is the difference between static and relative positioning?](#static-and-relative-positioning)
- [What is absolute positioning useful for?](#absolute-positioning)
- [What is the difference between fixed and sticky positioning?](https://www.kevinpowell.co/article/positition-fixed-vs-sticky/)

</div>

#### Additional resources
{: .no_toc }

- Web Dev Simplified's [Learn CSS Position](https://www.youtube.com/watch?v=jx5jmI0UlXU) video is fast-paced but provides a good visual representation of different positioning behaviors. Go ahead and watch it.
- [MDN's docs on `position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position) covers all of the conceptual details about positioning.
- CSS trick's page [Absolute, Relative, Fixed Positioning](https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/) should give you a different insight on the topic. You should read it as well.
- Finally, Kevin Powell's article discusses the [difference between fixed and sticky positioning](https://www.kevinpowell.co/article/positition-fixed-vs-sticky/). It’s a great read to understand the difference better.
- [Understand the CSS Position Property With Practical Examples](https://www.makeuseof.com/css-position-property-practical-examples/) provides some different CSS methods for positioning elements.
- You can check out this helpful video resource on [CSS positioning from Slaying the Dragon](https://www.youtube.com/watch?v=MxEtxo_AaZ4&t=2s) for clear explanations and practical examples.

---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [The Odin Project](https://www.theodinproject.com/) and most images are from [Interneting is Hard](https://internetingishard.netlify.app/).

{: .fs-2 }

