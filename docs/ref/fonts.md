---
layout: default
title: "🔤 Custom Fonts" 
parent: References
nav_order: 2
---

# 🔤 How to Import Custom Fonts
{:.no_toc}

### Google Fonts - CSS loading method with `@import`

1. Open your web browser and go to [Google Fonts](https://fonts.google.com).
2. Browse or search for the font you want to use.
3. Click on the font to view its details.
4. Select the **styles** (like Regular, Bold, Italic) you want by clicking "Select this style".
5. After selecting your styles, click on the **“View Selected Families”** button at the top-right corner of the page.
6. Find and select the `@import` option under **“Use on the Web”**.
7. Copy part of the generated statement, from `@import` until the semicolon `;`.
   <div class="warn" markdown="block">
     DO NOT include the {% raw %}`<style></style>`{% endraw %} tags, those are for HTML but we are sticking to CSS.
   </div>
8. Open your `style.css` file in your project.
9. Paste the `@import` statement at the very **TOP of your CSS**, above any selectors. _Example:_
   ```css
   @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');
   ```
10. Use the `font-family` property to **apply** the font to your elements. _Example:_
   ```css
   body {
     font-family: 'Roboto', sans-serif;
   }
   ```

#### Full Example:
```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

body {
  font-family: 'Roboto';
}
```
