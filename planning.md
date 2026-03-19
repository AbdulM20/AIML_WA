# Web Authoring Assignment 1 — Planning Document

**Student Name:** Abdul Mohaimin  
**Assignment:** Web Authoring Assignment 1  
**Module:** Web Authoring 5N1910  
**Date:** 18.02.2026  

---

## 1. Portfolio Purpose and Audience

### What is the purpose of this portfolio landing page?

The purpose of this portfolio is to showcase my abilities and educational journey as part of my AIML Foundations course. The page creates an impression of professionalism, curiosity, and technical competence while remaining accessible to non-technical viewers.

### Who is my target audience?

My primary audience includes my lecturers, classmates, potential mentors, and potential future employers in the tech and AI fields. This affects my design choices. I prioritise readability, structure, and logical organisation over decorative design, and I keep the layout professional at all times.

---

## 2. Content Planning

### What is included on the landing page?

**Header section:**
- My name: Abdul Mohaimin
- Tagline: "Machine Learning Student — Aspiring AI Specialist"
- Navigation links to Home, About, and Contact

**Introduction section:**
A large typographic display of my name alongside a short description of who I am and what I do. Includes my location and availability.

**Skills section:**
An unordered list of core skills displayed as tags — Python, HTML & CSS, Machine Learning, Data Visualisation, Git & GitHub, and Linear Algebra. Includes a custom code icon image created in Canva, stored in the `images/` folder.

**Projects section:**
A placeholder section indicating that project documentation is in development.

**Navigation:**
Navigation appears in the header (top right) and links to Home, About, and Contact.

**Footer section:**
Copyright notice, name, year, and links to GitHub and Contact.

### What is included on the About page?

A two-column layout with a biography on the left and structured information blocks on the right. The biography covers my background, interests, and direction. The info blocks cover skills, tools and technologies, education, and contact details including a mailto link.

### What is included on the Contact page?

A contact form with name, email, subject, and message fields alongside a GitHub profile link and location information.

---

## 3. Design Decisions

### Colour Scheme

| Role | Colour | Hex |
|---|---|---|
| Background | Off-white / cream | `#f5f2ec` |
| Surface (cards) | White | `#ffffff` |
| Primary text | Near-black | `#111111` |
| Muted text | Dark grey | `#666666` |
| Borders | Near-black | `#111111` |
| Accent | Deep red | `#c0392b` |

**Why these colours?**  
The cream background is easier on the eyes than pure white for extended reading. The near-black text on cream creates high contrast without being harsh. The deep red accent creates clear focal points on labels, links, and active states without competing with the content. The overall palette follows an editorial brutalism direction : stark, structural and professional.

### Typography

| Role | Font | Fallback |
|---|---|---|
| Display headings | Playfair Display | Georgia, serif |
| Body copy | IBM Plex Mono | Courier New, monospace |

**Source:** Google Fonts loaded via @import in styles.css

**Why these fonts?**  
Playfair Display is a high-contrast serif that creates an editorial, authoritative feel for large headings. IBM Plex Mono is a technical monospace font that reinforces the coding and data theme of the portfolio. Together they create a clear visual hierarchy.

### Layout

- Single-column structure for main content sections
- CSS Grid for the two-column layouts on About and Contact pages
- CSS Flexbox for header and footer alignment
- Maximum content width: 1200px, centred with auto margins
- Generous section padding using CSS custom properties
- Sticky header so navigation stays visible while scrolling

### Image

A custom code icon was created in Canva and exported as a PNG with a transparent background. It is stored in the `images/` folder and placed inline next to the "What I Work With" heading on the homepage. Sized to 40x40px via CSS with `border-radius: 50%` to appear circular.

---

## 4. Navigation Structure

**Location:** Top right of header, horizontal layout  
**Links:** Home → index.html, About → about.html, Contact → contact.html  
**Active page indicator:** Current page link displayed in accent colour with a bottom border underline  

**Why this structure?**  
Simple and predictable. Users immediately see what pages are available without confusion. Clear labelling makes navigation intuitive for both technical and non-technical visitors.

---

## 5. Wireframes

**Format:** Hand-drawn (see submitted sketch)

**Desktop layout structure:**
1. Header — name left, navigation right
2. Intro section — large name left, tagline and description right (2:1 grid)
3. Skills section — icon and horizontal tag list
4. Projects placeholder section
5. Footer — copyright left, links right

**Responsive considerations:**  
On smaller screens the intro stacks vertically, grids collapse to a single column, and spacing reduces. Navigation links remain visible at all breakpoints.

---

## 6. Technologies and Tools

| Tool | Purpose |
|---|---|
| WebStorm | Code editor |
| Safari | Browser testing and DevTools inspection |
| GitHub | Version control |
| GitHub Pages | Live deployment |
| Google Fonts | Web typography |
| Canva | Icon creation |
| Hand drawing | Wireframing |

---

## 7. HTML Elements Planned and Used

| Element | Purpose | Why Appropriate |
|---|---|---|
| `<header>` | Site header with name and navigation | Semantic landmark, improves accessibility |
| `<nav>` | Navigation menu | Identifies navigation region for screen readers |
| `<main>` | Primary page content | Semantic landmark |
| `<section>` | Groups thematic content | Organises content logically with headings |
| `<aside>` | Supplementary info on About and Contact pages | Tangentially related content |
| `<footer>` | Site footer | Semantic landmark for closing content |
| `<h1>`–`<h3>` | Heading hierarchy | Communicates document structure |
| `<p>` | Body paragraphs | Standard prose content |
| `<ul>` | Skills list, tech tags | Unordered grouped items |
| `<a>` | Navigation and external links | Standard hyperlink element |
| `<img>` | Code icon image | Visual content with alt text |
| `<form>` | Contact form | User input collection |
| `<input>` | Text and email fields | Form data entry |
| `<textarea>` | Message field | Multi-line text input |
| `<label>` | Form field labels | Accessibility — links label to input |

---

## 8. CSS Properties and Techniques

### CSS Grid
Used for the two-column layouts on the About and Contact pages, and the intro strip on the homepage.

### CSS Flexbox
Used for the header (logo left, nav right), footer, and navigation link alignment.

### CSS Custom Properties (Variables)
All colours, fonts, spacing, and border values stored as variables in `:root`. This means the entire site's appearance can be updated by changing a single value.

### ID Selectors
Used on landmark elements: `#site-header`, `#main-nav`, `#main-content`, `#site-footer`.

### Class Selectors
Used for reusable components: `.container`, `.label`, `.btn`, `.info-block`, `.skills-icon` etc.

### Element Selectors
Used for base styles: `body`, `h1`, `p`, `ul`, `img`, `label`, `input`, `textarea`.

### Combination Selectors
Used to scope styles precisely: `.site-nav a`, `.info-block ul li`, `input:focus`, `a.btn:link`.

### Link Pseudo-classes
All four states defined: `a:link`, `a:visited`, `a:hover`, `a:active`.

### Media Queries
Two breakpoints: 768px (tablet) and 480px (mobile). Grids collapse to single column, spacing reduces, navigation gap tightens.

### Hover Effects
Navigation links, footer links, and buttons all change colour on hover. 

---

## 9. Implementation Plan

1. Create basic HTML structure with semantic elements  
2. Add header and navigation  
3. Add intro section with name and tagline  
4. Build skills section with unordered list and icon image  
5. Add contact page with form  
6. Add about page with biography and info blocks  
7. Write styles.css with all required properties  
8. Implement Grid and Flexbox layouts  
9. Add responsive media queries  
10. Test in Safari DevTools  
11. Deploy to GitHub Pages  

### Anticipated Challenges
- Making layouts responsive without breaking at different screen widths
- Ensuring proper spacing and alignment across pages
- Keeping the design minimal while remaining visually engaging

These were addressed by testing frequently in Safari DevTools and adjusting CSS step by step.
