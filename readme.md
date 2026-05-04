# Abdul Mohaimin — ML Portfolio

**Module:** Web Authoring 5N1910  
**Assignment 1:** Web Authoring Assignment 1  
**Assignment 2:** Web Authoring Project — ML Project Documentation  
**Live Site:** https://abdulm20.github.io/AIML_WA/  
**Repository:** https://github.com/abdulm20/AIML_WA  

---

## 1. Overview

This portfolio is a static website built with HTML and CSS as part of the Web Authoring module at Dublin College of Further Education. Assignment 1 built the landing page, about page, and contact page. Assignment 2 extends the site with five documentation pages covering the machine learning projects completed during the course.

The site uses an editorial brutalist aesthetic — cream background, near-black text, Playfair Display headings, IBM Plex Mono body copy, and a deep red accent. It is aimed at lecturers, classmates, and potential employers in the tech and AI fields.

---

## 2. Page Descriptions

### `index.html` — Homepage (updated)
The main landing page. Updated in Assignment 2 to replace the projects placeholder with five linked project cards, one per skills demo.

### `about.html` — About
Two-column layout with biography and info blocks. Covers background, interests, direction, skills, tools, education, and contact details.

### `contact.html` — Contact
Contact form with name, email, subject, and message fields. GitHub profile link and location information.

### `styles.css` — Stylesheet (extended)
Single shared stylesheet across all pages. Assignment 2 appended a new section (section 16) adding styles for code blocks, data tables, ordered/unordered doc lists, aside callouts, and the overview page layout. All Assignment 1 rules preserved unchanged.

### `planning.md` — Planning Document (updated)
Sections 1–9 cover Assignment 1. Sections 10–18 added for Assignment 2: updated site map, content planning per page, wireframes, design decisions, technical planning, new HTML elements, new CSS techniques, and anticipated challenges.

---

### `neuron.html` — Artificial Neuron
Documents Skills Demo 1. Covers the purpose of the project, a conceptual explanation of ReLU, weighted sum, and bias, the full implementation with three code blocks, a results table for all three test cases, and a reflection on bugs encountered. The simplest project — one input, one weight, one neuron.

### `language.html` — Language Detector
Documents Skills Demo 2 (Programming Design Principles). Covers the five-step classification pipeline, the design decision to normalise raw counts to percentages, two distance methods (compare_statistics and MSE), results tables for language pair distances and minimum sample size testing, and a reflection. Key finding: English and Portuguese are hardest to distinguish (distance 0.44 on the basic method). Minimum reliable sample: 500 characters.

### `nn-single.html` — Neural Network: Single Class
Documents Skills Demo 2 (Computer Maths module). Covers the NeuralNetwork class built across three days — forward pass, cross-entropy loss, and backpropagation. Three architectures compared on 800 MNIST training examples: tiny (6,370 params, 84.5% test accuracy), medium (52,650 params, 86% test accuracy), and large (535,818 params, 89% test accuracy). The large network overfits; medium recommended for deployment.

### `nn-multi.html` — Neural Network: Multiple Classes
Documents Skills Demo 3. Covers the full OOP redesign — three inheritance trees (Layer, Activation, OutputFunction), the Model class, and the make_network factory function. Two architectures compared on 2,000 MNIST examples: Model A (64 hidden nodes, 89.7% test accuracy) and Model B (128 hidden nodes, 90.7% test accuracy). Key insight: depth adds power only with non-linear activations.

### `overview.html` — Portfolio Overview
Table of contents linking all four project pages with descriptions. Project summary cards with tag lists. Progression timeline table showing how each project built on the last. Technologies overview. Overall learning reflection.

---

## 3. Technical Implementation

### HTML
All pages use semantic HTML5 elements throughout: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`. Assignment 2 added `<pre>`, `<code>`, `<table>` with `<thead>`, `<tbody>`, `<caption>`, `<th scope="col">`, and both `<ol>` and `<ul>` lists with custom CSS counters and markers.

### CSS
Single external stylesheet. Custom properties for the full design system. Grid and Flexbox layouts. All four link pseudo-class states. Media queries at 768px and 480px. Assignment 2 extended the stylesheet with: `counter-reset`/`counter-increment` for custom list numbering, `nth-child(even)` for table striping, `transform: translateX()` for hover animations, and `overflow-x: auto` for responsive code blocks.

### Accessibility
All images have descriptive alt text. All form inputs have associated labels via `for`/`id` pairs. Navigation landmarks use `aria-label`. Tables use `<caption>` and `scope="col"` on header cells. Heading hierarchy is consistent across all pages.

---

## 4. Special Features

- **Live code blocks** — all code on project pages is presented in styled `<pre><code>` blocks with a red left border accent, dark background, and warm off-white text
- **Data tables** — results tables on all project pages use `<caption>`, `<thead>`, `<tbody>`, `scope` attributes, and zebra striping
- **Overview TOC** — large full-width linked entries with Playfair Display index numbers that animate on hover
- **Aside callouts** — highlighted insight blocks on language.html and nn-multi.html using a 4px red left border
- **Project cards on homepage** — five cards now link directly to each documentation page

---

## 5. Deployment

**GitHub Pages URL:** https://abdulm20.github.io/AIML_WA/

Deployed from the `main` branch, root directory. All Assignment 2 files committed to the same repository as Assignment 1. Updates go live within approximately 60 seconds of each push.

---

## 6. File Structure

```
AIML_WA/
├── index.html           — Homepage (updated with project cards)
├── about.html           — About page
├── contact.html         — Contact page
├── neuron.html          — Artificial Neuron documentation
├── language.html        — Language Detector documentation
├── nn-single.html       — Neural Network: Single Class documentation
├── nn-multi.html        — Neural Network: Multiple Classes documentation
├── overview.html        — Portfolio Overview
├── styles.css           — Shared stylesheet (extended for Assignment 2)
├── planning.md          — Planning document (updated for Assignment 2)
├── readme.md            — This file
├── maintenance.md       — Maintenance and future development notes
├── testing.md           — Testing procedures and results
└── Images/
    └── code-icon.png    — Custom icon used on homepage skills section
```

---

## 7. Resources and Attributions

| Resource | Use |
|---|---|
| [Google Fonts](https://fonts.google.com) | Playfair Display and IBM Plex Mono |
| [Canva](https://canva.com) | Custom code icon image |
| [MDN Web Docs](https://developer.mozilla.org) | HTML and CSS reference |
| [W3C Validator](https://validator.w3.org) | HTML validation |
| [W3C CSS Validator](https://jigsaw.w3.org/css-validator/) | CSS validation |
| MNIST dataset | Used in Skills Demo 2 (CM) and Skills Demo 3 |
| Dewey, Montessori, Freire texts | Used in Skills Demo 2 (PDP) — public domain |

All HTML, CSS, and Python code is my own work unless referenced above.

---

## 8. Learning Reflection

### Assignment 1

Building this portfolio gave me a much clearer understanding of how HTML and CSS work together. Starting with semantic HTML using `<section>`, `<aside>`, `<nav>`, and `<footer>` instead of just `<div>` everywhere forced me to think about the structure and meaning of each part of the page before touching any styling.

CSS custom properties were something I hadn't used before and they made a big difference. Storing all the colours, fonts, and spacing values as variables in `:root` meant I could make site-wide changes in seconds rather than hunting through the file for every individual value.

Grid and Flexbox took some trial and error to get right. Understanding which one to use and why was one of the bigger things I took away from Assignment 1.

### Assignment 2

Documenting the ML projects was a different kind of challenge. The hardest part was not the code — the code was already written and tested. The challenge was deciding how much detail to include, how to explain concepts clearly without being condescending, and how to present raw output (training logs, distance numbers) in a way that actually communicates something.

Writing the language detector page made me notice things about the project I hadn't articulated before. The decision to convert raw counts to percentages before comparing texts sounds obvious in retrospect, but documenting it forced me to explain *why* it matters, which deepened my understanding of the design.

The neural network pages were the most technically demanding to document. Explaining backpropagation in prose, without the scaffolding of the original notebook, required me to understand it well enough to summarise it — not just copy the code.

The `<pre><code>` blocks and data tables required careful attention to HTML structure. Learning about `scope="col"` on table header cells and `<caption>` for accessibility was a small but meaningful addition to my understanding of semantic HTML.

The biggest thing I took from Assignment 2 is that documentation is part of the work — not a separate task done after. A project you cannot explain clearly is a project you do not fully understand yet.
