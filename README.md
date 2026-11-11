# ASA Parts – Landing Page

A responsive landing page for ASA Parts, a business selling used and new car parts, specializing in engines.

**Live site:** https://asa-parts-landing.netlify.app/

## Built With

- HTML5 (semantic markup)
- CSS3 (Flexbox, Grid, custom properties)
- Netlify (hosting + form handling)

## Features

- Fully responsive, mobile-first design
- Self-hosted variable fonts and WebP images sized to their real dimensions
- Whole-card links, a native `<details>` FAQ and scroll-reveal animations, all without JavaScript
- Sticky header with frosted glass effect
- Working contact form via Netlify Forms, with spam protection and its own thank-you page
- Accessible: semantic HTML, labels, skip link, keyboard focus styles, reduced-motion support

## Changelog

### v2 – November 2026

**Layout and content**

- Moved the engine photo into the hero, with a badge on top, so the first screen shows what the shop sells
- Rebuilt the Engines section: the checklist is now a grid of four tiles next to the text
- Parts cards show two per row on phones instead of one, which makes the mobile page much shorter
- Every part card is now a link to the contact form (the whole card is clickable)
- Added an icon to each "Why Us" card and a dashed line joining the "How It Works" steps
- Added a FAQ section built with native `<details>` / `<summary>`
- Added "How It Works" and "FAQ" to the navigation (shown on wide screens) and "FAQ" to the footer
- Added a `thanks.html` page shown after the form is sent, instead of Netlify's default one
- Added scroll-reveal animations in pure CSS (`animation-timeline: view()`)

**Performance**

- Fonts are self-hosted as two variable `.woff2` files and preloaded, replacing Google Fonts
- All photos converted from JPG to WebP, with their real `width` and `height` set to stop layout shift
- The hero image uses `srcset` / `sizes` so phones download a smaller file, and `fetchpriority="high"` so it loads first

**Accessibility**

- Added a skip link and screen-reader-only text so the six card links don't all read the same
- Fixed three contrast problems: input borders, placeholder text and link hover color
- Form fields only turn red after the user has interacted with them (`:user-invalid`)
- Marked required and optional form fields, and added a hint in the message field
- Bigger tap targets on the nav links, and a shorter header on mobile
- Hover effects moved into `@media (hover: hover)` so they don't stick on touch screens

**SEO and sharing**

- New 1200×630 Open Graph image, plus `twitter:card`, `canonical`, `theme-color` and `color-scheme` meta tags

**CSS cleanup**

- Replaced hard-coded colors with variables and added fluid section spacing with `clamp()`
- "Why Us" and "How It Works" now use explicit Grid columns instead of `flex-basis` and `auto-fit`
- Merged duplicate classes (`hero__tagline` into `section-tag`) and replaced a fragile selector with a class
- Added three numbered sections to `style.css` (Fonts, FAQ, Thank-you page) and moved the old "Polish" rules into the sections they belong to
- Fixed a typo in the contact text

### v1 – November 2026

- Initial release

## What I Learned

- Structuring a page with semantic HTML and BEM class naming
- When to use Flexbox vs Grid
- Mobile-first responsive design with `clamp()`, `min()` and media queries
- Deploying a static site with continuous deployment from GitHub

## Code Organization

- I split `style.css` into numbered sections with comment headers (Variables, Reset, Base, Header, Hero, and so on), roughly in the same order the sections appear on the page. As the file grew past 700 lines, scrolling to find things got slow, so the headers let me jump straight to the part I need with Ctrl+F. It also keeps the file organized from general (variables, reset, base styles) to specific (individual sections), with the responsive media queries grouped near the end.
