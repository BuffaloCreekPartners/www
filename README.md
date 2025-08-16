Buffalo Creek Partners — Website

Static marketing site for Buffalo Creek Partners, an owner-operator of campgrounds & RV parks in the United States with emphasis on the Midwest and Southeast.
Built as a single, dependency-free HTML file with optimized images, basic SEO, and accessible, responsive layout.

Live site: https://buffalocreekpartners.com

Features

⚡️ Zero-build static site (just open index.html)

🖼 Optimized images with WebP + JPEG fallbacks

🔎 SEO ready: unique <title>, meta description, Open Graph tags, canonical URL

🧭 Structured data: Organization schema (JSON-LD)

♿ Accessibility: semantic headings, descriptive alt text, focus/contrast-friendly styles

📱 Responsive layout

✉️ Contact: simple mailto form (optional: swap to Formspree/Netlify for serverless submissions)

Project Structure
/
├─ index.html                 # Main site
├─ README.md                  # This file
├─ logo_large.webp            # Preferred logo format (small, fast)
├─ logo_large.jpg             # Fallback logo (JPEG)
├─ bright_park.webp           # Hero image (preferred)
└─ bright_park.jpg            # Hero image fallback


⚠️ Case sensitivity: On many hosts Logo_large.jpg ≠ logo_large.jpg.
Keep filenames exactly as above.

Getting Started (Local)

No tooling required.

Option A — open directly

Double-click index.html to preview in a browser.

Option B — run a tiny web server (recommended)
# Python 3
python3 -m http.server 8080
# then visit http://localhost:8080


or

# Node (if installed)
npx http-server -p 8080

Deploy
GitHub Pages

Create a new repo and push these files to main.

In Settings → Pages, choose:

Source: Deploy from a branch

Branch: main (root)

Save. Pages will publish at https://<you>.github.io/<repo>/.

Netlify / Vercel

Drag-and-drop the folder (or connect the repo).

Set the publish directory to the repo root.

Traditional hosting

Upload all files to your site root (e.g., /public_html).

Ensure MIME type for WebP is enabled (see WebP MIME below).

Editing Content

Open index.html and look for these sections:

Hero — headline + hero image (bright_park.webp/jpg)

What we do — acquisition, operations, revenue, safety, events, partnerships

Regions — state chips (Midwest & Southeast)

Types of Properties — table of target assets (RV parks w/ hookups, glamping, tent, snowbird, themed/membership, value-add)

About — positioning

Contact — mailto form to hello@buffalocreekpartners.com

Footer — year + domain

Logo usage

Header logo + favicon use a <picture> element and dual favicon entries:

<link rel="icon" type="image/webp" href="/logo_large.webp">
<link rel="icon" type="image/jpeg" href="/logo_large.jpg">


Header:

<picture>
  <source srcset="/logo_large.webp" type="image/webp">
  <img src="/logo_large.jpg"
       alt="Buffalo Creek Partners logo — rustic-modern campground & RV park operator"
       width="48" height="48">
</picture>

Hero image
<picture>
  <source srcset="/bright_park.webp" type="image/webp">
  <img src="/bright_park.jpg"
       alt="Well-maintained RV park with paved pads, full hookups, picnic tables, and landscaped grounds under a blue sky"
       loading="lazy" decoding="async" style="width:100%;height:auto;border-radius:12px">
</picture>

SEO Notes

Title: “Buffalo Creek Partners — Campgrounds & RV Parks (Midwest + Southeast)”

Meta description: “...Modern amenities meet rustic hospitality.”

Open Graph: includes both hero and logo images for rich previews.

Canonical: set to https://buffalocreekpartners.com/

Schema: Organization with email, areaServed, logo, and image array.

Local SEO ideas (future pages/posts):

State/region landing pages (e.g., /midwest/, /southeast/)

Owner-focused guides (e.g., “Value-Add Playbook for Snowbird Parks”)

Amenity pages (pet-friendly, full hookups, glamping)

Accessibility

All images have meaningful alt text.

Headings are hierarchical (h1 → h2).

Contrast tuned to be readable on cream background.

Add keyboard “skip to content” link if you expand navigation.

Performance

WebP used everywhere with JPEG fallback.

Consider adding explicit width and height on images to reduce CLS.

Keep hero under ~250–350 KB total for snappy loads.

WebP MIME (server config)
If WebP doesn’t render, add:

Apache (.htaccess)

AddType image/webp .webp


Nginx

types { image/webp webp; }

Contact Form Options

Current form opens a prefilled email to hello@buffalocreekpartners.com.
To capture submissions without email clients:

Formspree: replace the <form> action with your endpoint and add a hidden _subject.

Netlify Forms: add data-netlify="true" and a hidden name input.

Ask if you want a wired version included.

Color Palette

Dark Brown (brand): #3A2B21

Cream (bg): #F4EFE6

Light Card: #FFF9F0

Accent Brass: #B08B57

Muted Text: #6B5B4A

Body Text: #2F261D

Roadmap / TODO

 Add sitemap.xml & robots.txt

 Add apple-touch-icon.png (180×180)

 Optional blog/landing pages per region

 Formspree/Netlify integration for contact form

 Add srcset sizes for truly responsive hero

 Basic analytics (privacy-friendly)

Contributing

Create a feature branch: git checkout -b feature/thing

Edit index.html (and image assets).

Commit with concise messages, open a PR.

License

Code: MIT

Brand assets (logo_large.*, wordmarks, photos unless otherwise noted): © Buffalo Creek Partners.
Not for reuse outside Buffalo Creek Partners properties without written permission.

Support

Questions or requests?
hello@buffalocreekpartners.com | https://buffalocreekpartners.com
