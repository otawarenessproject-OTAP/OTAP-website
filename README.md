# OTAP UI fix starter

This starter contains CSS and JavaScript for styling the highlighted controls to match the approved mockup. It does **not** replace `index.html` or deploy changes to GitHub Pages.

## Important image path
Keep the already-uploaded hero image. If the HTML uses an `<img>`, the expected relative path is:

`assets/image/otap-hero-silhouette-10-ot.png`

If the hero image is a CSS background, update that existing `url(...)` instead. Do not create or regenerate another image.

## How to integrate
1. Add `otap-ui-fix.css` to the repository, then link it from `index.html`:
   `<link rel="stylesheet" href="otap-ui-fix.css">`
2. Add `otap-ui-fix.js` and load it with `defer`:
   `<script src="otap-ui-fix.js" defer></script>`
3. Add the CSS classes and `data-otap-*` attributes from the files to the matching existing controls.
4. Replace placeholder section IDs with the **actual** IDs used by the current page. Every navigation link must point to an existing section.
5. Connect BM/EN buttons to the site's existing translation logic. The included JS only manages pressed-state accessibility; it does not translate the page by itself.
6. Verify all links and buttons on mobile before deploying.

## Classes / attributes
- Language buttons: `.otap-language-toggle` and `data-otap-language="bm"` / `"en"`
- Hamburger: `.otap-menu-toggle` and `data-otap-menu-toggle`
- Menu panel: `.otap-menu-panel` and `data-otap-menu-panel`
- Close menu button: `data-otap-menu-close`
- Main CTA: `.otap-cta .otap-cta--primary`
- Secondary CTA: `.otap-cta`
- Bottom navigation: `.otap-bottom-nav`
- Floating contact wrapper: `.otap-contact-float` and `data-otap-contact-float`
- Existing loading element (if any): `data-otap-loading`

The code is a safe starter, not a verified patch against the live site, because the current `index.html` source was not available to inspect. It must be integrated against the actual HTML rather than pasted blindly.
