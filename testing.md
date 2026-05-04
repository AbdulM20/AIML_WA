# testing.md

**Module:** Web Authoring 5N1910  
**Student:** Abdul Mohaimin  
**Date:** April 2026  

---

## 1. Testing Procedures

Testing was done manually throughout development using Safari on a MacBook. The main tool was Safari DevTools — specifically the responsive design mode for checking layouts at different screen widths, and the console for spotting any errors.

The general approach was to test after every significant change rather than leaving everything to the end. This caught layout problems early, before they had time to compound.

---

## 2. W3C Validation

All eight pages were run through the W3C HTML Validator at https://validator.w3.org and the W3C CSS Validator at https://jigsaw.w3.org/css-validator/.

**HTML results:** No errors on any page. A small number of informational warnings were returned, mostly about the use of `type="text/plain"` on the contact form's enctype attribute and the use of `aria-label` on elements that already have visible text. These were reviewed and left as-is since they do not affect functionality or accessibility.

**CSS results:** No errors. The validator flagged the SVG noise texture in the body background as an unknown value, which is expected behaviour — it is a valid inline SVG data URI that the validator does not recognise. Everything else passed cleanly.

---

## 3. Browser Compatibility

| Browser | Version | Result |
|---|---|---|
| Safari | macOS latest | All pages pass |
| Chrome | Latest | All pages pass |
| Firefox | Latest | All pages pass |

The `<details>` and `<summary>` elements used for the collapsible code sections are supported in all three browsers. The CSS `clamp()` function used for fluid heading sizes is also supported. No polyfills were needed.

One minor difference: Safari and Firefox render the `<details>` marker triangle slightly differently. This does not affect usability. The marker is hidden with CSS anyway (`list-style: none` and `::-webkit-details-marker { display: none }`).

---

## 4. Responsive Design Testing

Tested at three widths using Safari DevTools responsive mode:

| Width | Layout | Result |
|---|---|---|
| 1200px+ (desktop) | Two-column grids, full intro strip | Pass |
| 768px (tablet breakpoint) | Single column, stacked grids | Pass |
| 375px (iPhone SE) | Single column, reduced padding | Pass |

Specific things checked at each breakpoint:

- Navigation links stay on one line and do not wrap or overflow
- The intro grid on the homepage stacks vertically — name above, description below
- The about and contact grids collapse to single column
- Project cards stack to single column
- Code blocks scroll horizontally rather than breaking the layout (`overflow-x: auto`)
- Data tables reduce font size and padding at 768px
- The overview TOC description text is hidden at 480px to avoid overflow on very small screens

---

## 5. Navigation and Link Verification

Every internal link on every page was clicked manually. Tested from:

- Homepage cards to all five project pages
- Back link on each project page to overview.html
- Table of contents links on overview.html to each project page
- Header navigation across all pages
- Footer links across all pages

All links resolved correctly. No 404 errors.

External links tested:
- GitHub profile link in footer — opens correct profile in new tab
- GitHub profile link on contact page — opens correct profile in new tab
- Contact form mailto — opens mail client with correct address pre-filled

---

## 6. Accessibility Testing

Tested with Safari's built-in VoiceOver screen reader on the homepage and one project page (neuron.html).

Things that were confirmed:
- Page landmark regions (`<header>`, `<main>`, `<footer>`, `<nav>`) are announced correctly
- All images have descriptive `alt` text
- Form inputs on contact.html are correctly linked to their labels via `for`/`id` pairs
- Table headers use `scope="col"` so screen readers announce column context
- All tables have a `<caption>` that is read before the table data
- The `<details>` element announces its expanded/collapsed state
- `aria-label` attributes on `<nav>` and `<section>` elements give screen readers useful context

One thing noted: the `<summary>` element inside `<details>` announces as "button" in VoiceOver, which is acceptable behaviour.

---

## 7. User Feedback

The site was reviewed by a classmate before final submission. Feedback received:

- The collapsible full code sections were useful — they do not clutter the page but the code is there if needed
- The overview page table of contents made it easy to navigate between projects
- The contact form worked correctly on their machine

No layout or link issues were reported.

---

## 8. Issue Log

| Issue | Where found | How fixed |
|---|---|---|
| Project cards not linking to pages | index.html | Updated href attributes to correct filenames |
| `nn-multi.html` and `nn-single.html` not tracked by Git | WebStorm | Ran `git add .` in terminal |
| Contact form data arriving as unformatted string | Live site | Known limitation of mailto — left as-is, noted in maintenance.md |
| `<details>` marker visible in some browsers | All project pages | Hidden with `list-style: none` and `::-webkit-details-marker { display: none }` |
| Code blocks overflowing on narrow screens | Project pages | Added `overflow-x: auto` to `pre` in styles.css |
| Git push failing with no upstream branch | Terminal | Ran `git push --set-upstream origin main` once to set remote |
