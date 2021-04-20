---
title: CSS Questions
layout: layouts/page.njk
permalink: /questions/css-questions/index.html
---

- **What is CSS selector specificity and how does it work?**

  - The specificity starts at 0, adds 1000 for style attribute, adds 100 for each ID, adds 10 for each attribute, class or pseudo-class, add 1 for each element name or pseudo-element.
  - **Equal specificity: the latest rule counts** - If the same rule is written twice into the external style sheet, then the lower rule in the style sheet is closer to the element to be styled, and therefore will be applied:
  - **ID selectors have a higher specificity than attribute selectors.**
  - **Contextual selectors are more specific than a single element selector.**
  - **A class selector beats any number of element selectors**
  - **The universal selector and inherited values have a specificity of 0.** _, body _ and similar have a zero specificity. Inherited values also have a specificity of 0.

- **What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?**

  - CSS resets aim to remove all built-in browser styling. Standard elements like h1 - h6, p, strong, em end up looking exactly alike, having no decoration at all. You're then supposed to add all decoration yourself.
  - _Normalize.css_ aims to make built-in browser styling consistent across browsers. Elements like h1 - h6 will appear bold, larger et cetera in a consistent way across browsers. You're then supposed to add only the difference in decoration your design needs.

- **Describe Floats and how they work.**

  - The float CSS property places an element on the left or right side of its container, allowing text and inline elements to wrap around it. The element is removed from the normal flow of the page, though still remaining a part of the flow (in contrast to absolute positioning).

- **Describe z-index and how stacking context is formed.**

  - Here is the default order the browser stacks elements in, when no `z-index` is applied:

    1. Root element (the <html> element)
    2. Non-positioned elements in the order they are defined
    3. Positioned elements in the order they are defined

  - An element with a higher `z-index` will be displayed in front of an element with a lower `z-index`. One thing to note is that `z-index` only works with **positioned elements**.

  - Adding a z-index value to an element forms what is called a stacking context. The fact that it forms a stacking context affects how its child elements are being displayed. The child element may still display behind other elements despite a higher z-index.

- Describe BFC (Block Formatting Context) and how it works.
- What are the various clearing techniques and which is appropriate for what context?
- How would you approach fixing browser-specific styling issues?
- How do you serve your pages for feature-constrained browsers?
  - What techniques/processes do you use?
- What are the different ways to visually hide content (and make it available only for screen readers)?
- Have you ever used a grid system, and if so, what do you prefer?
- Have you used or implemented media queries or mobile specific layouts/CSS?
- Are you familiar with styling SVG?
- Can you give an example of an `@media` property other than `screen`?
- What are some of the "gotchas" for writing efficient CSS?
- What are the advantages/disadvantages of using CSS preprocessors?
  - Describe what you like and dislike about the CSS preprocessors you have used.
- How would you implement a web design comp that uses non-standard fonts?
- Explain how a browser determines what elements match a CSS selector.
- Describe pseudo-elements and discuss what they are used for.
- Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.
- What does `* { box-sizing: border-box; }` do? What are its advantages?
- What is the CSS `display` property and can you give a few examples of its use?
- What's the difference between inline and inline-block?
- What's the difference between the "nth-of-type()" and "nth-child()" selectors?
- What's the difference between a relative, fixed, absolute and statically positioned element?
- What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
- Have you used CSS Grid?
- Can you explain the difference between coding a web site to be responsive versus using a mobile-first strategy?
- Have you ever worked with retina graphics? If so, when and what techniques did you use?
- Is there any reason you'd want to use `translate()` instead of _absolute positioning_, or vice-versa? And why?
- How is clearfix css property useful?
