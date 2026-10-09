# HTML Email Templates

A collection of responsive HTML email templates, hand-coded with email-client-safe techniques. Built as a portfolio piece demonstrating email development skills: table-based layouts, bulletproof buttons, inline CSS, and mobile-first thinking for the inbox.

## Templates

**Faithful HTML recreations of real client designs** (original email designs by Shaheryar Butt, rebuilt as responsive HTML for portfolio purposes):

- **plaxic-welcome.html** — Plaxic eco-movement welcome email: "Welcome To Plaxic / Joining the movement to Clean the Earth" hero, earth-in-hands imagery, green $1.99 contribution band, explore-the-app section, Plaxic Team sign-off.
- **neurogan-wellness.html** — Neurogan CBD wellness email: "Wellness / On Us" hero with product bottle, "With Neurogan's Lab-Tested, Full-Spectrum Free Samples", FULL SPECTRUM CBD OIL feature rows (Tastes Like / Feels Like / Harmonizes Like), star-rated testimonial card, pill CTAs, "You May Also Like" product row.

**Generic placeholders** (being replaced with real client work over time):

- **black-friday.html** — Bold Black Friday sale email: dark theme, giant discount headline, red urgency bar, 3-product grid, countdown-style timer block, and stacked CTAs.
- **eco-brand.html** — Clean eco/sustainable brand email: light greens and earth tones, hero image, brand-story card, 2-column product feature, and impact stats row.
- **sale.html** — Bright, energetic e-commerce sale email: colorful hero banner, dashed-border discount-code box (`SUNNY25`), 2x2 product grid with add-to-cart buttons.
- **pet-store.html** — Playful pet-store email: warm amber/brown palette, friendly rounded type pairing, 3 featured products, pet-care tips panel, and first-order discount CTA.

## Techniques used

- **Table-based layouts** — nested tables with `role="presentation"`; no div-based layout for content, so templates render in Outlook, Gmail, and Apple Mail alike.
- **600px centered container** — `max-width:600px` with an `<!--[if mso]>` fixed-width wrapper for desktop Outlook.
- **All CSS inline** — every visual style lives in `style` attributes; the only `<style>` block in `<head>` holds the mobile media query plus email resets (`mso-table-lspace`, `-webkit-text-size-adjust`, etc.).
- **Mobile responsive** — `@media (max-width:480px)` collapses multi-column rows into stacked blocks, scales hero type, and expands buttons to full width.
- **Outlook conditionals** — `<!--[if mso]>...<![endif]-->` wrappers around the outer container; VML namespaces declared on `<html>` for future background-image support.
- **Bulletproof buttons** — padded table cells with background colors instead of CSS-styled anchors, so CTAs render even where padding on `<a>` is stripped.
- **Email-safe images** — `https://placehold.co` placeholders with explicit `width`, `display:block`, and descriptive `alt` text on every image.
- **Accessibility & compliance** — hidden preheader text, `role="article"` on the email body, `lang`/`dir` attributes, physical mailing address and unsubscribe link in every footer.
- **Web-safe fonts** — Arial/Helvetica, Georgia, Trebuchet MS, Courier New, with generic fallbacks; no webfont dependencies.
- **No JavaScript, no external stylesheets.**

## How to preview

1. **In a browser** — open any `.html` file directly; the 600px centered layout previews exactly as it will render in most inboxes. Resize the window below 480px to see the mobile stacking kick in.
2. **With an email testing tool** — paste the HTML into [Litmus](https://www.litmus.com) or [Email on Acid](https://www.emailonacid.com) to screenshot it across 90+ real email clients (Outlook, Gmail, Apple Mail, Yahoo, etc.).
3. **Send a test** — most ESPs (Mailchimp, Klaviyo, Customer.io) accept raw HTML paste; send yourself a test to check dark-mode and image-blocking behavior.

> Note: placeholder links (`https://example.com/...`) and addresses are fictional. Swap in real URLs, brand assets, and your company's physical address before sending.
