# Frontend Mentor - Huddle Landing Page with Single Introductory Section Solution

<div align="center">

![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![NEWBIE](https://img.shields.io/badge/Frontend_Mentor-NEWBIE-3DB8FF?style=for-the-badge)

</div>

A responsive landing page built as part of a Frontend Mentor challenge.

This project focuses on recreating a modern hero section using semantic HTML and CSS while maintaining responsiveness across different screen sizes and preserving the original visual style as closely as possible.

---

## Preview

![Design preview for the Huddle landing page with single introductory section](./preview.jpg)

---

## Live Demo

- Live Site: [https://juansanchezzzzz.github.io/huddle-landing-page/](http://juansanchezzzzz.github.io/Huddle-landing-page-with-a-single-introductory-section/)
- Frontend Mentor Challenge: https://www.frontendmentor.io/challenges/huddle-landing-page-with-single-introductory-section-pts4qJ4

---

# Overview

This project recreates the Huddle Landing Page design provided by Frontend Mentor.

The main objectives were:

- Semantic HTML5 structure
- Responsive layouts
- Flexbox positioning
- SVG background integration
- Typography hierarchy
- Hover interactions
- Responsive images
- Modern CSS architecture

---

# Challenges Faced

### Understanding Relative Units

One of the most valuable lessons from this project was learning when and why to use relative units instead of fixed pixel values.

Initially, many dimensions were defined using `px`, but the layout became more flexible and maintainable after converting most values to:

- `rem` for spacing and sizing
- `%` for fluid widths
- `ch` for text readability
- `clamp()` for responsive typography

For example:

```css
h1 {
  font-size: clamp(2rem, 3vw, 2.75rem);
}
```

This allowed the design to adapt more naturally across different screen sizes.

---

### Background SVG Integration

Another challenge was reproducing the background exactly as shown in the design.

The page combines:

- A solid purple background color
- A decorative SVG overlay

This required configuring both layers correctly:

```css
body {
  background-color: var(--Purple);
  background-image: url("./images/bg-desktop.svg");
}
```

Special care was also needed to switch to the mobile SVG version when the viewport became smaller.

---

### Structuring the Layout with Flexbox

Although the final layout looks simple, organizing the content correctly required several iterations.

The desktop version consists of:

- An illustration section
- A content section

Using Flexbox made it possible to create a clean two-column layout while also allowing it to collapse into a single column on smaller screens.

```css
main {
  display: flex;
  gap: 4rem;
}
```

and later:

```css
@media (max-width: 900px) {
  main {
    flex-direction: column;
  }
}
```

This significantly improved responsiveness and readability.

---

### Social Icons Positioning

Positioning the social media icons was another interesting challenge.

The design required them to appear:

- At the bottom-right corner on desktop
- Centered below the content on mobile

This was solved by combining Flexbox and media queries while changing the positioning strategy depending on the screen size.

---

### Creating a Smooth Button Hover Effect

A smooth hover interaction was added to the call-to-action button.

The button includes:

- Background color transition
- Text color transition
- Slight vertical movement
- Shadow enhancement

```css
button:hover {
  background-color: var(--Magenta);
  transform: translateY(-0.125rem);
}
```

This created a more polished and interactive experience without adding unnecessary complexity.

---

# Built With

- HTML5
- CSS3
- Flexbox
- CSS Custom Properties
- Responsive Design
- SVG Backgrounds
- Relative Units (`rem`, `%`, `ch`)
- CSS Transitions

---

# Responsive Design Approach

The page was designed using a responsive-first mindset.

Desktop devices display the content in two columns:

- Illustration section
- Content section

Mobile devices switch to a single-column layout with centered content and adjusted spacing.

```css
@media (max-width: 900px) {
  main {
    flex-direction: column;
    text-align: center;
  }
}
```

Additional adjustments include:

- Mobile-specific background image
- Responsive illustration scaling
- Centered call-to-action button
- Repositioned social media icons

---

# What I Learned

Through this project I gained more experience with:

- Building responsive landing pages from design mockups
- Using Flexbox for complex layouts
- Working with SVG backgrounds
- Managing responsive typography with `clamp()`
- Choosing appropriate relative units (`rem`, `%`, `ch`)
- Positioning elements differently across breakpoints
- Creating smooth hover interactions
- Organizing CSS into logical sections with clear comments

---

# Author

- Frontend Mentor - https://www.frontendmentor.io/profile/juansanchezzzzz
- GitHub - https://github.com/juansanchezzzzz
