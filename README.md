# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page.
- Experience a responsive layout that scales down smoothly on mobile devices without relying on traditional media queries.

### Screenshot

![Blog Preview Card Screenshot](./Solution-screenshot/Blog%20Preview%20Card%20desktop-design%20%20Screenshot.png)

### Links

- Solution URL: [GitHub Repository](https://github.com/roba365/blog-preview-card)
- Live Site URL: [GitHub Pages Live Demo](https://roba365.github.io/blog-preview-card/)

## My process

### Built with

- **Semantic HTML5** markup (`<article>`, `<time>`, `<footer>`, `<a>`)
- **CSS3** with custom properties and flexbox
- **Fluid Typography** using modern CSS `clamp()` functions
- **Google Fonts** - Figtree
- Mobile-first responsive design principles

### What I learned

### What I Learned

During this project, I focused on writing clean, semantic HTML and implementing modern CSS techniques to build an accessible, responsive card component.

1. **Fluid Typography without Media Queries:**
   Instead of using static pixel values and `@media` rules, I used `clamp()` so the typography scales smoothly relative to the viewport size across mobile and desktop screens:

   ```css
   .card-title a {
     font-size: clamp(
       1.25rem,
       4vw,
       1.5rem
     ); /* ~20px on mobile to 24px on desktop */
     font-weight: 800;
   }

   .card-description {
     font-size: clamp(0.875rem, 2.5vw, 1rem); /* ~14px to 16px */
   }
   ```

2. I structured the card using meaningful tags— wrapping content in an <article>, recording dates with <time datetime="...">, and nesting an anchor <a> inside the <h1> title to support full keyboard tab navigation and focus states:

```html
<article class="card">
  <time class="card-date" datetime="2023-12-21">Published 21 Dec 2023</time>
  <h1 class="card-title">
    <a href="#">HTML & CSS foundations</a>
  </h1>
</article>
```
3. Neo-Brutalist Shadow Styling & Hover States:
I created a crisp solid shadow effect and added transition states when users hover over the card and heading link:
```css
.card {
  box-shadow: 8px 8px 0px 0px hsl(0, 0%, 7%);
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}

.card:hover {
  box-shadow: 12px 12px 0px 0px hsl(0, 0%, 7%);
  transform: translate(-2px, -2px);
}

.card-title a:hover {
  color: hsl(47, 88%, 63%);
}
```

### Continued Development

I plan to continue building on these concepts in future Frontend Mentor challenges:
- Implementing advanced web accessibility (a11y) patterns for complex interactive components.
- Utilizing CSS modern layout functions like `min()`, `max()`, and grid auto-fit configurations.
- Transitioning into full-stack web applications by integrating frontend components with backend APIs and state management.

### Useful Resources

- [MDN Web Docs: clamp()](https://developer.mozilla.org/en-US/docs/Web/CSS/clamp) - Essential reference for understanding fluid typography syntax and calculations.
- [A Complete Guide to Flexbox - CSS-Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - A go-to visual guide for building flexible layout structures.
- [Google Fonts - Figtree](https://fonts.google.com/specimen/Figtree) - The official typeface used for this design challenge.

### AI Collaboration

- **AI Collaboration:** Worked alongside Gemini as a pair-programming partner to debug CSS font-weight rendering, optimize semantic HTML structure (`<article>`, `<time>`, `<footer>`), and implement fluid typography with `clamp()` without media queries.

## Author

- Frontend Mentor - [@roba365](https://www.frontendmentor.io/profile/roba365)
- GitHub - [@roba365](https://github.com/roba365)

## Acknowledgments

Thanks to the Frontend Mentor community for providing clean Figma design assets and structured challenges that mimic real-world web development workflows.
