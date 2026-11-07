# ASA Parts – Landing Page

A responsive landing page for ASA Parts, a business selling used and new car parts, specializing in engines.

**Live site:** https://asa-parts-landing.netlify.app/

## Built With

- HTML5 (semantic markup)
- CSS3 (Flexbox, Grid, custom properties)
- Netlify (hosting + form handling)

## Features

- Fully responsive, mobile-first design
- Responsive grids without media queries (`auto-fit` + `minmax`)
- Sticky header with frosted glass effect
- Working contact form via Netlify Forms, with spam protection
- Accessible: semantic HTML, labels, keyboard focus styles, reduced-motion support

## What I Learned

- Structuring a page with semantic HTML and BEM class naming
- When to use Flexbox vs Grid
- Mobile-first responsive design with `clamp()`, `min()` and media queries
- Deploying a static site with continuous deployment from GitHub

## Code Organization

- I split `style.css` into numbered sections with comment headers (Variables, Reset, Base, Header, Hero, and so on), roughly in the same order the sections appear on the page. As the file grew past 700 lines, scrolling to find things got slow, so the headers let me jump straight to the part I need with Ctrl+F. It also keeps the file organized from general (variables, reset, base styles) to specific (individual sections), with the responsive media queries grouped near the end.
