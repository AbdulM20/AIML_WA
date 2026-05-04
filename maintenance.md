# maintenance.md

**Module:** Web Authoring 5N1910  
**Student:** Abdul Mohaimin  
**Date:** April 2026  

---

## 1. Current Functionality

The site has eight pages: index, about, contact, and four project documentation pages plus an overview. All pages share one stylesheet. Navigation works across all pages. The contact form opens the user's mail client. The GitHub link in the footer goes to the correct profile. GitHub Pages is live at https://abdulm20.github.io/AIML_WA/.

Things that work as expected:
- All internal links between pages
- Project cards on the homepage linking to each documentation page
- Collapsible full code sections on all four project pages
- Responsive layout at 768px and 480px breakpoints
- Sticky header on all pages
- Contact form mailto action

---

## 2. Known Limitations

**Contact form.** The mailto action opens the user's email client rather than sending directly. The submitted data arrives in a single unformatted line. It works but it is not clean. Switching to a service like Formspree would fix this without any backend code.

**No JavaScript.** The site is pure HTML and CSS. The collapsible code sections use the native `<details>` element, which works in all modern browsers but has limited styling control. There is no way to add interactivity like syntax highlighting without adding JavaScript.

**One reference text per language.** The language detector was trained on one author per language. This means it may have picked up writing style rather than language patterns. It still works correctly but a proper version would use multiple texts per language.

**No images on project pages.** The documentation pages have no screenshots or diagrams. Adding output visualisations from the training runs would make them easier to read.

**MNIST CSV not in the repo.** The `mnist_train.csv` file used in Skills Demo 2 and 3 is not committed to the repository because of its size. The Python files reference it by local path. This is fine for the portfolio but worth noting.

---

## 3. Future Upgrade Recommendations

**Switch the contact form to Formspree.** Free tier, no backend needed, emails arrive properly formatted. Takes about five minutes to set up.

**Add syntax highlighting to code blocks.** A lightweight library like Prism.js would colour-code the Python snippets and make them much easier to read. It is a single script tag and a stylesheet link.

**Add output images to project pages.** Screenshots of the training loss curves and example digit predictions would add a lot to the neural network pages. The plots exist in the Jupyter notebooks and could be exported and added to the `Images/` folder.

**Add a projects filter or sort on the homepage.** Right now all five cards show at once. If more projects are added later, a simple JavaScript filter by tag would help navigation.

**Add a LinkedIn link.** The about page has a placeholder LinkedIn link pointing to `#`. That should be updated once the profile is set up.

**Add GitHub links to individual project pages.** Each documentation page could link directly to the relevant notebook or Python file in the repository rather than just the profile page.

---

## 4. Maintenance Procedures

**Making a content change** (fixing a typo, updating a result):  
Open the relevant HTML file in WebStorm, make the change, then:
```
git add .
git commit -m "describe what you changed"
git push
```
GitHub Pages updates within about 60 seconds.

**Adding a new project page:**  
1. Copy the structure of an existing project page (e.g. `neuron.html`)
2. Update the label, heading, and all content sections
3. Add a new card to `index.html` in the projects grid
4. Add a new entry to the table of contents in `overview.html`
5. Add a new row to the timeline table in `overview.html`
6. Commit and push

**Updating the stylesheet:**  
All CSS is in `styles.css`. Assignment 1 styles are in sections 1–15. Assignment 2 additions are in section 16 onwards. Add new rules at the bottom and note what they are for in a comment.

**Checking the live site after a push:**  
Open https://abdulm20.github.io/AIML_WA/ and do a hard refresh (`Cmd+Shift+R` on Mac, `Ctrl+Shift+R` on Windows) to clear the cache and see the latest version.

---

## 5. Testing Plan for Updates

Before pushing any change:

1. Open the changed page in Safari and check it looks correct
2. Resize the browser window to confirm the layout does not break below 768px
3. Click every internal link on the changed page to confirm nothing is broken
4. If a CSS change was made, check all pages — not just the one you were working on, since the stylesheet is shared

After pushing:

1. Hard refresh the live site and confirm the change appears
2. Check the page on a phone if the change affected layout or spacing

---

## 6. Long-term Evolution

The site was built as a course portfolio. As my skills develop the natural next steps are:

- Replace placeholder LinkedIn and GitHub links with real ones
- Add more project pages as new skills demos are completed
- Eventually move from GitHub Pages to a proper domain once there is more content worth hosting at a real URL
- The design system (CSS variables, Playfair Display, IBM Plex Mono, cream palette) scales well — adding new pages just means following the same template
