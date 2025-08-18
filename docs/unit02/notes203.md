---
layout: notes
title: "📓2.3: Animations" 
parent: "2️⃣ Advanced HTML & CSS"
nav_order: 3
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---
<div style="text-align: center;">
<span class="highlighter-green"> 
<strong>✴✴✴ NEW UNIT/SECTION! ✴✴✴</strong><br>Create a blank website program to take your class notes in for the next few lessons.<br><em>Click on the collapsed heading below for GitHub instructions</em> ⤵  
</span>
</div>

<html>
  <details>
    <summary>📓 <strong class="text-green-200">NOTES PROGRAM SETUP INSTRUCTIONS</strong></summary>

<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Unit2Lesson3-Notes`
4. For the **description**, write: `CSS transforms and animations)`
5. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 📂
6. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
7. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
8. 📝 Take notes in this Codespace during class, writing **code** & **comments** along with the instructor.

</div>

<br>

<div class="warn" markdown="block">

🛑 When class ends, don't forget to **SAVE YOUR WORK**! **Codespaces** are TEMPORARY editing environments, so you need to COMMIT changes properly in order to update the main **repository** for your program. 

_There are multiple steps to saving in GitHub Codespaces:_

1. Navigate to the `Source Control` menu on the _LEFT_ sidebar
2. Click the <button type="button" name="button" class="btn btn-green">commit changes</button> button on the _LEFT_ menu
3. Type a brief **commit message** at the top of the file that opens, for example: `updated index.html`
4. Click the small `✔️` **checkmark** in the _TOP RIGHT_ corner
5. Click the <button type="button" name="button" class="btn btn-green">sync changes</button> button on the _LEFT_ menu
6. _Finally you can close your Codespace!_

</div>

</details>

</html>

---

## CSS Transforms

The `transform` **property** is a powerful tool to *change the appearance of elements* without affecting the natural document flow.

You have likely seen it in action on many of your favorite websites! Transforms are very commonly used for animated effects. While we are sure you'll like to create sleek **animations** of your own, we first need to understand how transforms work. 

![image](https://miro.medium.com/v2/resize:fit:960/1*R2IxrEjMVm6QiRYdEo-lvQ.png)

#### 📖 Learning goals:
{:.no_toc}

- How to use 2D transforms.
- How to use 3D transforms.
- How to chain multiple transforms.
- The benefits of using the `transform` property.


<div class="imp" markdown="block">

The `transform` property takes in one or more CSS transform **functions** as its values, with those functions taking in their own **value**, usually an angle or a number.

```css
element {
    transform: function(value);
}
```

Almost all HTML elements can have the `transform` property applied to it, with the exceptions being _non-replaced inline elements_. 
> "Non-replaced" refers to elements whose content is contained directly within the HTML document (`<span>`, `<b>`, and `<em>`, for example), as opposed to a "replaced" element's content being contained outside of the document (`<a>` and `<img>`, for example).

</div>

### 2-dimensional transforms

In this section, we'll go through **2D transforms** with the following transform **functions**: `rotate`, `scale`, `skew`, and `translate`.

#### Rotate
{:.no_toc}

This is the transform function value to **rotate** an element on a 2D plane:

```css
.element {
  transform: rotate();
}
```

Below is a CodePen that shows how the value affects the target element.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="GRMgKeE" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/GRMgKeE">
2D Rotate | CSS Transform</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Scale
{:.no_toc}

These are the transform function values to **scale** (adjust the size of) an element on a 2D plane:

```css
.element {
  transform: scaleX();
  transform: scaleY();
  transform: scale();
}
```

Below is a CodePen that shows how each value affects the target element.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="XWeJrGL" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/XWeJrGL">
2D Scale | CSS Transform</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Skew
{:.no_toc}

These are the transform function values to **skew** an element on a 2D plane:

```css
.element {
  transform: skewX();
  transform: skewY();
  transform: skew();
}
```

Below is a CodePen that shows how each value affects the target element.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="mdBybgm" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/mdBybgm">
2D Skew | CSS Transform</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Translate
{:.no_toc}

These are the transform function values to **translate** (move) an element on a 2D plane:

```css
.element {
  transform: translateX();
  transform: translateY();
  transform: translate();
}
```

Below is a CodePen that shows how each value affects the target element.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="PoJwYrO" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/PoJwYrO">
2D Translate | CSS Transform</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

### Chaining multiple transforms

Now that you have a grasp of 2D transforms, we will learn how to **chain** them. Chaining multiple transforms is done by adding more transform functions with a _space between each one_. Take a look at the code below:

```html
<div class="red-box"></div>
<div class="blue-box"></div>
```

```css
.red-box,
.blue-box {
  position: absolute;
  width: 100px;
  height: 100px;
}

.red-box {
  background: red;
  transform: rotate(45deg) translate(200%);
}

.blue-box {
  background: blue;
  transform: translate(200%) rotate(45deg);
}
```

There are two boxes located at the same position. We chained `rotate` and `translate` function values to both boxes, but in **different orders**. Make a guess on what will happen to each box, then run it in a code window.

If you guessed correctly, congratulations! But this is a tricky concept. MDN's transform docs state that "[composite transforms are effectively applied in order from right to left](https://developer.mozilla.org/en-US/docs/Web/CSS/transform#values)".

> The blue box rotates 45 degrees on the spot, then translates on the X axis by 200%, moving it directly to the right. The red box translates by 200% first, so moves to the right, but the transform origin is still where it used to be. Therefore, it rotates 45 degrees around that original point, making the red box "swing down" to end up diagonally from where it started.

While you can generally chain multiple transforms in any order for various results, there is one exception: `perspective`. This brings us nicely to the next section where `perspective` is involved.

### 3-dimensional transforms

The `rotate`, `scale`, and `translate` transform functions aren't limited to just 2D planes. They also work for 3D planes as well! However, to perceive a 3D effect on some of these function values, `perspective` is required.

#### Perspective
{:.no_toc}

This is the transform function value to set the **distance** from the user to the `z = 0` plane:

```css
.element {
  transform: perspective();
}
```

Essentially, by setting a `perspective` value, we are telling the object to render as if we were _viewing it from a specific distance_ on the z-axis.

{:.highlight}
Unlike other transform function values, `perspective` must be declared first (leftmost) when there are multiple transform function values. In the upcoming examples for `rotate`, `scale`, and `translate`, we will be able to see how it affects the target element.

#### Rotate specific axis
{:.no_toc}

These are the additional transform function values to **rotate** an element in a 3D space:

```css
.element {
  transform: rotateX();
  transform: rotateY();
  transform: rotateZ();
  transform: rotate3d();
}
```

Below is a CodePen that shows how the first three values affects the target element.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="PoJwozR" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/PoJwozR">
3D Rotate | CSS Transform</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### Scale specific axis
{:.no_toc}

These are the additional transform function values to **scale** an element in a 3D space:

```css
.element {
  transform: scaleZ();
  transform: scale3d();
}
```

{:.highlight}
See MDN's 3D cube in action with [`scaleZ`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/scaleZ()) and [`scale3d`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/scale3d()).

#### Translate specific axis
{:.no_toc}

These are the additional transform function values to **translate** an element in a 3D space:

```css
.element {
  transform: translateZ();
  transform: translate3d();
}
```

`translateZ` doesn't do much without `perspective`. Instead, `perspective` and `translateZ` work together to create the _illusion of 3-dimensional distance_ from the rendered object, as shown in the example below.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="MWEYWpN" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/MWEYWpN">
TranslateZ | CSS Transform</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

#### 🧠 Knowledge check
{:.no_toc}

The following questions are an opportunity to reflect on key topics in this lesson. If you can't answer a question, click on it to review the material.

- [What are the four main functions of the `transform` property?](#two-dimensional-transforms)
- [Which function can be used to move an object through space on the X, Y, or Z axis?](#translate)
- [Which function can be used to make an object larger or smaller on the X, Y, or Z axis?](#scale)
- [What additional function is required for 3D transforms?](#three-dimensional-transforms)

#### 📚 Additional resources
{:.no_toc}

- Take a look at this [MDN demonstration of `rotate3d`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/rotate3d()) then read more about the property in this [Quackit article on `rotate3d`](https://www.qhmit.com/css/functions/css_rotate3d_function.cfm).
- Learn more about [the `perspective` property on CSS Tricks](https://css-tricks.com/how-css-perspective-works/).
- MDN has another great [demonstration using `translate3d`](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function/translate3d()).
- Go through [The World of CSS Transforms](https://www.joshwcomeau.com/css/transforms/) by Josh Comeau.
- For a full reference, there’s always [MDN's documentation on CSS transform functions](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-function).
- For more on the 3D transform functions, [W3Schools' page on CSS transforms](https://www.w3schools.com/css/css3_3dtransforms.asp) is a good article demonstrating how they work.

---

## CSS Animations

Now let's explore CSS animations using `keyframes`. Animations let you animate elements from one style configuration to another. Once you have your elements in place and CSS defined, an animation will start running immediately if that's what you told it to do!

#### 📖 Learning goals:
{:.no_toc}

- How to **configure** animation sub-properties.
- How to **sequence** an animation using `@keyframes`.

![image](https://freefrontend.com/assets/img/css-fire-animation/CSS-Fire.gif)

### Animation sub-properties

Let's see an animation in action to see what we've been talking about.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="jOGENZz" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

  <span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/jOGENZz">
  keyframes 1 longhand</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Note how the animation is already running and how it keeps repeating itself. We'll cover that `@keyframes` rule at the bottom of our example in a bit, so for now focus on the actual `animation` **properties** used in the example above.

<div class="imp" markdown="block">

The code below is known as the **configuration stage** where we _define animation properties_ to be applied on the element, and it is only the first half of defining an animation.

```css
#ball {
  /* ... other CSS properties ... */
  animation-duration: 2s;
  animation-name: change-color;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

In our example, we have:

- An `animation-duration` of two seconds. This means that it will take two seconds for the `#ball` element to _complete one animation cycle_.
- Defined the `animation-name` to be "change-color" which is essential for the `@keyframes` section coming up next.
> This is just a custom name that is not a particular CSS value. We could have called it "pineapples" if we so wished, but for our purposes "change-color" suits us well.
- Set the `animation-iteration-count` to `infinite`, which means this animation will run forever. You could set this to `1`, `2`, or as many _iterations_ as you wish.
- Set the `animation-direction`  to `alternate`. This property decides if our animation should _alternate direction on the completio_n of one cycle, or reset to the start point and repeat itself.
> Here it means that the `#ball` will smoothly change back to its original color instead of "jumping" straight back to red.

</div>

### Animation keyframes

Now it's time to tackle the second half of our animation definition by exploring the `@keyframes` **at-rule**.

```css
@keyframes change-color {
  from {
    background-color: red;
  }

  to {
    background-color: green;
  }
}
```

The `@keyframes` at-rule references the 'change-color' name we defined earlier. Then, we use the `from` and `to` properties to change the `background-color` of `#ball` from red to green.

{:.highlight}
It's important to know that keyframes use a percentage to _indicate the times for an animation to take place_ and that the `from` and `to` statements are actually aliases for `0%` and `100%`, respectively. You can read `from/0%` as meaning '_at zero seconds_' and `to/100%` as '_at 2 seconds_' according to our `animation-duration` in our example from above. There is no hard and fast rule on whether or not you should use `from/to` or `0%/100%`. Just pick a style and be consistent with it!

The `@keyframes` at-rule also **defines one animation cycle**. So if we were to change our `animation-iteration-count` from earlier to 2 then the ball would change its `background-color` from red to green, then from green to red, and then the animation would stop. Be careful not to think of one iteration as a complete loop, but rather a **single cycle** from beginning to end (or end to beginning when alternating the direction).

Now it's time to introduce the **shorthand notation** for our animation properties and glimpse a little into the added flexibility of the keyframe notation. Check out the live example below then have a look at the notation:

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="zYExOLQ" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

  <span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/zYExOLQ">
  keyframes 2 shorthand</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

```css
#ball {
  /* ... other CSS properties ... */
  background-color: red;
  animation: 2s change-color infinite alternate;
}

@keyframes change-color {
  from {
    background-color: red;
  }
  
  50% {
    transform: scale(2);
    background-color: blue;
  }

  to {
    background-color: green;
  }
}
```

Here we added another keyframe for when the `animation-duration` is at 50%, or 1 second. This means as well as the `background-color` changing to an additional value, we have also specified that the ball double in size. Just be aware that additional keyframes are always defined in percentages. Only the `0%/100%` values may use the `from/to` alias.

Hopefully, this gives you a glimpse into the power the `@keyframes` syntax provides to you when it comes to controlling the animation of an element's properties. You can add keyframes whenever you want, control whatever CSS-animatable properties you want, and have the control to add some real creative flair to your website elements.

#### 🧠 Knowledge check
{:.no_toc}

The following questions are an opportunity to reflect on key topics in this lesson. If you can't answer a question, click on it to review the material.

- [What are the long and short-hand notations for CSS animations?](https://developer.mozilla.org/en-US/docs/Web/CSS/animation)
- [How do you add keyframes to an animation?](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations#defining_the_animation_sequence_using_keyframes)
- [When would you use an animation over a transition (and vice versa)?](#animations-vs-transitions)

#### 📚 Additional resources
{:.no_toc}

- [Video from DevTips on CSS Animations and Keyframes](https://www.youtube.com/watch?v=f1WMjDx4snI&list=PLqGj3iMvMa4LvJ8VctoXnPI0dtE40wfid&index=2&ab_channel=DevTips).
- Code along with this [MDN article for using CSS animations](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations).
- Read the [@keyframes reference](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) to gain a deeper understanding of how keyframes are implemented.
- Read this [interactive guide to keyframes](https://www.joshwcomeau.com/animation/keyframe-animations/).

---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [The Odin Project](https://www.theodinproject.com/) and most images are from [Interneting is Hard](https://internetingishard.netlify.app/).

{: .fs-2 }

