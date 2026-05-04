# Web Authoring — Planning Document

**Student Name:** Abdul Mohaimin  
**Module:** Web Authoring 5N1910  
**Assignment 1 Date:** 18.02.2026  
**Assignment 2 Date:** 29.04.2026  

---

## Assignment 1 Planning

*Original planning document content preserved below.*

---

### 1. Portfolio Purpose and Audience

The purpose of this portfolio is to showcase my abilities and educational journey as part of my AIML Foundations course. The page creates an impression of professionalism, curiosity, and technical competence while remaining accessible to non-technical viewers.

My primary audience includes my lecturers, classmates, potential mentors, and potential future employers in the tech and AI fields. This affects my design choices. I prioritise readability, structure, and logical organisation over decorative design, and I keep the layout professional at all times.

---

### 2. Content Planning (Assignment 1)

**Header section:** My name, tagline, and navigation links.  
**Introduction section:** Large typographic display of my name with a short description.  
**Skills section:** Unordered list displayed as tags with a custom code icon.  
**Projects section:** Placeholder for Assignment 2.  
**Footer section:** Copyright notice and links.

**About page:** Two-column layout — biography on the left, info blocks on the right.  
**Contact page:** Contact form with name, email, subject, and message fields alongside a GitHub link.

---

### 3. Design Decisions

**Colour scheme:**

| Role | Colour | Hex |
|---|---|---|
| Background | Off-white / cream | `#f5f2ec` |
| Surface (cards) | White | `#ffffff` |
| Primary text | Near-black | `#111111` |
| Muted text | Dark grey | `#666666` |
| Borders | Near-black | `#111111` |
| Accent | Deep red | `#c0392b` |

The cream background is easier on the eyes than pure white. The deep red accent creates clear focal points without competing with content. The palette follows an editorial brutalism direction.

**Typography:**

| Role | Font | Fallback |
|---|---|---|
| Display headings | Playfair Display | Georgia, serif |
| Body copy | IBM Plex Mono | Courier New, monospace |

Playfair Display creates an editorial, authoritative feel. IBM Plex Mono reinforces the coding and data theme. Together they create a clear visual hierarchy.

**Layout:** Single-column for main content; CSS Grid for two-column pages; CSS Flexbox for header and footer. Maximum content width 1200px.

---

### 4. Navigation Structure

Top right of header, horizontal layout. Links: Home → index.html, About → about.html, Contact → contact.html. Active page link displayed in accent colour with a bottom border underline.

---

### 5. Wireframes (Assignment 1)

Hand-drawn sketches submitted separately. Desktop layout: header → intro → skills → projects → footer. Responsive: grids collapse to single column on mobile.

---

### 6. Technologies and Tools (Assignment 1)

| Tool | Purpose |
|---|---|
| WebStorm | Code editor |
| Safari | Browser testing |
| GitHub | Version control |
| GitHub Pages | Live deployment |
| Google Fonts | Web typography |
| Canva | Icon creation |
| Hand drawing | Wireframing |

---

### 7. HTML Elements Planned and Used (Assignment 1)

| Element | Purpose | Why Appropriate |
|---|---|---|
| `<header>` | Site header | Semantic landmark |
| `<nav>` | Navigation menu | Identifies navigation region |
| `<main>` | Primary page content | Semantic landmark |
| `<section>` | Groups thematic content | Logical content organisation |
| `<aside>` | Supplementary info | Tangentially related content |
| `<footer>` | Site footer | Semantic landmark |
| `<h1>`–`<h3>` | Heading hierarchy | Document structure |
| `<p>` | Body paragraphs | Standard prose content |
| `<ul>` | Skills list, tech tags | Unordered grouped items |
| `<a>` | Navigation and external links | Standard hyperlink |
| `<img>` | Code icon | Visual content with alt text |
| `<form>` | Contact form | User input collection |
| `<input>` | Text and email fields | Form data entry |
| `<textarea>` | Message field | Multi-line text input |
| `<label>` | Form field labels | Accessibility |

---

### 8. CSS Properties and Techniques (Assignment 1)

CSS Grid, CSS Flexbox, CSS Custom Properties, ID and class selectors, combination selectors, link pseudo-classes, media queries at 768px and 480px, hover effects.

---

### 9. Implementation Plan (Assignment 1)

Standard build order: HTML structure → header → sections → stylesheet → grid/flexbox → responsive → test → deploy.

---

---

## Assignment 2 Planning

### 10. Assignment 2 Purpose and Scope

Assignment 2 extends the portfolio with five documentation pages covering the machine learning programming projects completed during the course. The goal is to document each project clearly enough that a reader with no prior knowledge of the code can understand what was built, why, and what the results were.

---

### 11. Site Map — Updated

```
index.html (updated — project cards now link to all five pages)
├── about.html
├── contact.html
└── Projects
    ├── neuron.html        — Artificial Neuron
    ├── language.html      — Language Detector
    ├── nn-single.html     — Neural Network: Single Class
    ├── nn-multi.html      — Neural Network: Multiple Classes
    └── overview.html      — Portfolio Overview
```

---

### 12. Content Planning (Assignment 2)

**neuron.html** — Artificial Neuron  
Purpose, conceptual explanation (ReLU, weighted sum, bias), implementation code blocks, test results table, reflection on bugs found.

**language.html** — Language Detector  
Purpose, five-step pipeline explanation, two distance methods (compare_statistics and MSE), results tables for language pair distances and minimum sample size, reflection.

**nn-single.html** — Neural Network: Single Class  
Purpose and three-day structure, conceptual explanation (forward pass, loss, backprop), NeuralNetwork class code blocks, three-architecture experiment with training results and train/test accuracy table, reflection on overfitting.

**nn-multi.html** — Neural Network: Multiple Classes  
Purpose, OOP design explanation (inheritance trees, polymorphism), key code blocks (base classes, softmax, make_network), two-architecture experiment results, reflection on design shift.

**overview.html** — Portfolio Overview  
Table of contents (linked list of all four projects), project summary cards, progression timeline table, technologies list, overall learning reflection.

---

### 13. Wireframes (Assignment 2)

**Documentation page template (all four project pages follow this structure):**

```
[Header — same as all pages]
[Page hero — project title and label]
[Back link — overview.html]
[Purpose & Context — prose]
[Conceptual Explanation — ordered list or prose + aside callout]
[Implementation — code-label + pre/code blocks]
[Results/Testing — data table(s)]
[Reflection — prose]
[Footer — same as all pages]
```

**Overview page:**

```
[Header]
[Page hero]
[Table of contents — large linked list with index numbers]
[Project summary cards — 2-column grid]
[Timeline table]
[Technologies — tag list]
[Overall reflection — prose]
[Footer]
```

---

### 14. Design Decisions (Assignment 2)

The Assignment 2 pages extend the existing editorial brutalist aesthetic without changing anything from Assignment 1. New visual elements added:

**Code blocks:** Near-black background (`#111111`) with warm off-white text and a red left border. Consistent with the site's use of red as an accent. IBM Plex Mono is already the site's body font, so code looks native.

**Data tables:** Clean, minimal — borders only on header row and between rows. Small uppercase column headers in muted grey, matching the `.label` style used elsewhere.

**Aside callouts:** White background with a 4px red left border. Used for key insights on project pages (e.g. why percentages matter in the language detector, the linear activation insight).

**Overview TOC:** Large Playfair Display index numbers in muted grey that turn red on hover. Each entry spans the full content width, similar to editorial magazine link styles.

---

### 15. Technical Planning (Assignment 2)

**Development tools:** WebStorm, Safari DevTools, GitHub.

**GitHub Pages:** Deployed from the same repository as Assignment 1. All new files committed to `main` branch, root directory.

**Code generators:** No AI was used to generate the Python code in the skills demos — all code was written and tested during class sessions. The HTML and CSS for this assignment was structured by hand, building on the existing stylesheet rather than generating from scratch.

**W3C Validation:** All five new pages will be validated against the W3C HTML validator before final submission. The existing CSS will be re-validated with the new rules appended.

---

### 16. HTML Elements Added (Assignment 2)

| Element | Page(s) | Purpose |
|---|---|---|
| `<article>` | All project pages | Wraps the full project documentation |
| `<pre>` | All project pages | Preformatted code blocks |
| `<code>` | All project pages | Inline and block code |
| `<table>`, `<thead>`, `<tbody>`, `<tr>`, `<th>`, `<td>`, `<caption>` | All project pages, overview | Data tables for results |
| `<ol>` | neuron.html, language.html, nn-multi.html | Ordered lists for steps and concepts |
| `<aside>` | language.html, nn-multi.html | Callout blocks for key insights |
| `<nav>` (overview) | overview.html | Table of contents navigation |

**HTML character entities used across new pages (selection):**  
`&mdash;` `&rarr;` `&times;` `&ndash;` `&ldquo;` `&rdquo;` `&lsquo;` `&rsquo;` `&hellip;` `&copy;` `&amp;` `&#10003;` `&#10007;`

---

### 17. CSS Techniques Added (Assignment 2)

**New selectors:**  
`.code-label`, `pre`, `code`, `pre code`, `.doc-table`, `.doc-table caption`, `.doc-table thead th`, `.doc-table tbody td`, `.doc-table tbody tr:nth-child(even) td`, `.doc-list`, `ol.doc-list li::before`, `ul.doc-list li::before`, `.doc-aside`, `.overview-toc`, `.overview-toc-link`, `.toc-index`, `.toc-title`, `.toc-desc`, `.toc-arrow`, `.overview-grid`, `.overview-card`, `.tag-list`

**New techniques introduced:**  
- CSS `counter-reset` and `counter-increment` for custom ordered list numbers  
- `nth-child(even)` pseudo-class for table zebra striping  
- `transform: translateX()` on hover for the TOC arrow animation  
- `border-collapse: collapse` for the data tables  

**Existing techniques extended:**  
All Assignment 1 variables (`--clr-accent`, `--font-display`, `--border`, etc.) reused throughout. No new custom properties needed. New media query rules added within the existing `@media (max-width: 768px)` and `@media (max-width: 480px)` blocks.

---

### 18. Anticipated Challenges (Assignment 2)

- Keeping code blocks readable on narrow screens without breaking the layout — addressed with `overflow-x: auto` on `pre`
- Table responsiveness on mobile — addressed by reducing font size and padding at the 768px breakpoint
- Consistent visual weight between code-heavy pages and prose-heavy pages — addressed by using the same `.project-article` max-width container on all documentation pages
