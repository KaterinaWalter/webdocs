---
layout: project
title: "💻 Unit 3 Project"
projectname: "Personal Website"
parent: "3️⃣ Bootstrap"
nav_order: 5
---


### Overview

In this project, you will create a **responsive one-page personal website** that demonstrates your mastery of Bootstrap and the concepts covered in the tutorials. The project is open-ended to encourage creativity while giving you the opportunity to practice building a responsive and visually appealing website.

#### Project Goal
Design and develop a **one-page personal website** using Bootstrap classes and UI components. Your website should reflect your _personality_, _interests_, or _goals_ and include well-organized sections with responsive layouts.

<html>
<details>
<summary>📥 <strong class="text-green-200">PROJECT SETUP & SUBMISSION INSTRUCTIONS</strong></summary>
  
<div class="setup" markdown="block">

1. Go to the `CS1 Unit 3 Project` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Unit 3 Project` assignment on Blackbaud.

</div>

</details>
</html>

--- 

### Instructions

#### Plan Your Personal Website

<div class="task" markdown="block">
  
🧠 **BRAINSTORMING CONTENT:**
- **Hero Section**: A welcoming section with your name, a title, and a short tagline.
  - Think about how you want to introduce yourself. Consider a tagline or quote that represents your values or aspirations.
- **About Me**: A section describing who you are, your interests, or your goals.
  - What makes you unique? Share your hobbies, favorite activities, or personal story. Include a profile picture or avatar.
- **Portfolio/Showcase**: If you have completed projects, hobbies, achievements, or any creative work, showcase them here. If not, create placeholders for future content.
- _Other ideas for sections:_
  - **Skills**: Highlight your technical or personal skills. 
  - **Testimonials**: Add quotes from your peers, or feedback from others.
  - **Photo Gallery**: Display your favorite photos in a grid layout. 

💡 **DESIGN INSPIRATION:** 
- [Developer Portfolio Websites](https://github.com/emmabostian/developer-portfolios)
  - Scroll down to the list of links, open random pages, and make notes of _design choices_ that resonate with you, such as interesting layouts or font styles
- Explore [Coolors - Trending Color Palettes](https://coolors.co/palettes/trending) and [SheCodes - Color Palette Ideas](https://www.shecodes.io/palettes)

</div>

#### Create Your Layout
1. Start with an eye-catching **Hero Section**:
   - Create a `<div class="container-fluid"></div>` at the top of your page. 
   - Use a Bootstrap background color, or a full-width background image or custom gradient.
   - Add a large heading with your name and a short tagline centered in the section.
1. Build out a variety of **Grid-Based Layouts**:
   - Organize _every section_ of content in at least one outer `<div>`, and decide whether you want it to be a fixed `.container` or full-width `.container-fluid`.  
   - Within some sections, use Bootstrap's [grid system](https://getbootstrap.com/docs/5.3/layout/grid/) to create interesting layouts for your content.
     - Remember that grids must follow the pattern: `.container` → `.row` → `.col` → CONTENT
     - Experiment with different column sizes for each section (e.g., `.col-6`, `.col-md-4`).
1. Include **UI Components**:
   - Use [Bootstrap UI Components](https://coderina.dev/webdocs/docs/unit03/notes302.html) like cards, buttons, badges, or carousels to make your site visually appealing.

#### Fill in Content & Images
1. Write meaningful **text** content for each section.
2. Use **images** that reflect your personality, work, or interests.
3. Add **decorations** like icons, emojis, or clipart (transparent background pictures).

#### Style with Bootstrap Classes & Custom CSS
1. Use [Bootstrap Formatting Classes](https://coderina.dev/webdocs/docs/unit03/notes301.html) to quickly add style to your page.
2. Write your own styling rules in a `style.css` file to personalize your website. Apply custom styles to make the website uniquely yours, such as changing fonts/colors or adding special CSS effects/animations. 
  > _Example:_
  ```css
  /* Override a Bootstrap class */
  .bg-primary {
    background-color: #ff5733 !important;
  }
  ```

{:.warning}
Overriding Bootstrap's pre-defined class names DOES NOT ALWAYS work! In this case, just add your own `id` or `class` attribute to the HTML element and select for it in CSS as usual. 

--- 

### Minimum Requirement Checklist

Before submitting, ensure your website includes the following:

1. **Hero Section**:
   - [ ] Full-width background (color, image or gradient).
   - [ ] Large heading and a short tagline.
   > You can deviate from the suggestions above as long as you still have an _eye-catching_ section at the top.

2. **About Me Section**:
   - [ ] Text content describing who you are, your interests, or your goals.
   - [ ] A profile image styled with Bootstrap classes (e.g., `rounded-circle`).

3. **Portfolio/Showcase Section**:
   - [ ] At least three items displayed.

4. **Responsive Design**:
   - [ ] Use Bootstrap's **grid system** to ensure your website adapts to different screen sizes.
   - [ ] Use Bootstrap **UI components** like cards or buttons.

5. **Custom CSS**:
   - [ ] Include a `style.css` file with at least five custom styles.

#### Bonus Challenges
- Add a **carousel** to showcase images or testimonials.
- Add a responsive **navigation bar** at the top of your website using Bootstrap's navbar component. Ensure links scroll to the corresponding sections of the page.
- Use Bootstrap's **scrollspy** to highlight the current section in the navbar as users scroll.
- Experiment with more interactive Bootstrap components like modals or alerts.


{:.highlight}
**RESOURCES:** While working on this project or attempting the bonus features, you are encouraged to look up any Bootstrap `classes` or starter code! Refer to the [📖 Bootstrap Documentation](https://www.w3schools.com/css/), review our [📓 Unit 3 Notes](https://coderina.dev/webdocs/unit03). 

