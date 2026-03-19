# Abdul Mohaimin — ML Portfolio

**Module:** Web Authoring 5N1910  
**Assignment:** Web Authoring Assignment 1  
**Live Site:** https://abdulm20.github.io/AIML_WA/  
**Repository:** https://github.com/abdulm20/AIML_WA  

---

## 1. Overview

This portfolio is a static website built with HTML and CSS as part of the Web Authoring module at Dublin College of Further Education. Its purpose is to introduce who I am, present my skills and background, and provide a way for visitors to contact me.

The site is designed with a professional editorial aesthetic, clean, structure and easy to read. It is aimed at lecturers, classmates, and potential employers in the tech and AI fields.

---

## 2. Page Descriptions

### `index.html` — Homepage
The main landing page. Features a large typographic introduction with my name and tagline, a skills section with a custom code icon and tag list, and a placeholder section for projects that will be developed later.

### `about.html` — About
A two-column page with a biography on the left covering my background, interests, and direction. The right column has structured info blocks for skills, tools and technologies, education, and contact details including a mailto link and GitHub profile link.

### `contact.html` — Contact
A contact form with name, email, subject, and message fields alongside a GitHub profile link and location information. Built with semantic form elements including labelled inputs and a textarea.

### `styles.css` — Stylesheet
A single shared external stylesheet used across all pages. Contains CSS custom properties for the full design system, element/class/ID selectors, all four link pseudo-class states, flexbox and grid layouts, form styling, and responsive media queries.

### `planning.md` — Planning Document
Documents the purpose and audience, content planning, design decisions, colour scheme, typography, navigation structure, wireframes, technologies used, HTML elements, CSS techniques, and implementation plan.

---

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and semantic markup |
| CSS3 | Styling, layout, and responsive design |
| Google Fonts | Playfair Display and IBM Plex Mono typefaces |
| Git | Version control |
| GitHub Pages | Static site hosting and deployment |
| WebStorm | Code editor |
| Safari | Browser testing |
| Canva | Custom code icon image |

---

## 4. Viewing Instructions

### View the live site
Open a browser and go to: **https://abdulm20.github.io/AIML_WA/**

### Run locally
1. Clone or download the repository
2. Open the `AIML_WA` folder
3. Open `index.html` in any modern browser

No build tools, server, or dependencies required. All files are plain HTML and CSS.

---

## 5. GitHub Pages URL

**https://abdulm20.github.io/AIML_WA/**

Deployed from the `main` branch, root directory. Updates go live within approximately 60 seconds of each push.

---

## 6. Credits and Resources

| Resource | Use |
|---|---|
| [Google Fonts](https://fonts.google.com) | Playfair Display and IBM Plex Mono typefaces |
| [Canva](https://canva.com) | Custom code icon image |
| [MDN Web Docs](https://developer.mozilla.org) | HTML and CSS reference |
| [W3C Validator](https://validator.w3.org) | HTML validation |
| [W3C CSS Validator](https://jigsaw.w3.org/css-validator/) | CSS validation |

All code is my own work unless referenced above.

---

## 7. Reflection

Building this portfolio gave me a much clearer understanding of how HTML and CSS work together. Starting with semantic HTML using `<section>`, `<aside>`, `<nav>`, and `<footer>` instead of just `<div>` everywhere, forced me to think about the structure and meaning of each part of the page before touching any styling.

CSS custom properties were something I hadn't used before and they made a big difference. Storing all the colours, fonts, and spacing values as variables in `:root` meant I could make site-wide changes in seconds rather than hunting through the file for every individual value.

Grid and Flexbox took some trial and error to get right. I used Flexbox for one-dimensional layouts like the header and footer, and Grid for the two-column sections on the About and Contact pages. Understanding which one to use and why was one of the bigger things I took away from this.

The contact form was interesting to build, learning about the `for` and `id` pairing between labels and inputs, and how `type="email"` changes keyboard behaviour on mobile, were small details that added up to a more polished result.

Testing in Safari DevTools helped me catch a few layout issues at smaller screen sizes that I wouldn't have noticed otherwise, and working through those with media queries gave me a better feel for responsive design.
