---
layout: default
title: "🧱 HTML Cheatsheet" 
parent: References
nav_order: 4
---

# 🧱 HTML Cheatsheet
{:.no_toc}

### Syntax Structure of an HTML Element

![image](html-element.png)

### Inline Elements
By default, **inline elements** appear next to one another in a webpage. They _take up only as much width as they need_ in a page and fit together horizontally like words in a sentence or books shelved side-by-side in a row. 

| Usage | Tag | Example |
| :---: | :---: | :--- |
| 📦 Inline Container | `<span>` | Used to **group** parts of text, often for styling:<br>`<span class="purple"> Styled text </span>` |
| _Emphasized_ Text | `<em>` | `<em> I am in italics </em>` |
| **Important** Text | `<strong>` | `<strong> I am bold! </strong>` |
| 🔗 Link | `<a>` | `<a href="https://example.org"> Go somewhere </a>` |
| 🖼️ Image | `<img>` | _Self-closing_ tag, but the `src` **attribute** is required:<br>`<img src="profile-pic.png" width="50px">` |

### Block Elements
**Block elements**, on the other hand, _take up the entire width_ of a webpage by default. They also take up a full line of a webpage; they do not fit together side-by-side. Instead, they stack like paragraphs in an essay or toy blocks in a tower.

| Usage | Tag | Example |
| :---: | :---: | :--- |
| 📦 Block Container | `<div>` | Used to **group** elements for organization/layout:<br>`<div id="section-1"> </div>` |
| 💬 Paragraph Text | `<p>` | `<p> I am a paragraph of text. </p>` |
| 📣 Heading Text | `<h1>`...`<h6>` | `<h1> Primary heading </h1>`<br>`<h2> Secondary heading </h2>`<br>... |
| ➖ Horizontal Rule | `<hr>` | _Self-closing_ tag, just insert `<hr>` anywhere for a break with a **border line** |
| ↩ Line Break | `<br>` | _Self-closing_ tag, just insert `<br>` anywhere for a **blank space** break |

<div class="imp" markdown="block">
  
**Inline elements** are usually *nested* inside **block elements**:

```html
<p>
  This is a paragraph block with some inline elements
  like <strong>bold words</strong> or maybe even a
  <a href="www.somewebsite.com">link</a>!
</p>
```

</div>
