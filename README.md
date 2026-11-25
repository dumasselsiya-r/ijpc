# International Journal of Psychological Community (IJPC) — Premium Academic Website

## Overview
This production-ready website is a complete visual, typographic, responsive, and technical rebuild of the **International Journal of Psychological Community (IJPC)** platform (e-ISSN: 2839-5638), published by the **Tamil Nadu Psychology Association (TNPA)** in research collaboration with the **Indian Institute of Psychological Research and Training (IIPRT)**.

## What Was Built
- **All 47 HTML Pages Redesigned**: Homepage, About the Journal, About the Publisher, Editorial Board (19 members with category filtering), Call for Paper, Author Guidelines & Fees, Submission Guidelines (APA 7th), Disclaimer & Submission Policy, Book Publication (ISBN), Special Publication, Published Journals (with search, topic filters & grid/list views), Previous Issues Archive, Blog for Writers, Online Manuscript Submission Portal, Contact Us, Volume 1 Issue 1 Full Reader, all 12 Peer-Reviewed Research Article Reader Pages (with APA 7th & BibTeX citation copy, sticky TOC scrollspy, PDF & certificate downloads, and ScholarlyArticle JSON-LD), and all 19 APA Academic Resource pages.
- **Design System**: Deep Navy (#10243A), Premium Teal (#087F8C), Warm Ivory (#F8F7F3), Pure White (#FFFFFF), Champagne Gold (#C4A46B), Charcoal (#263442), Light Grey Borders (#E2E8F0). Typography powered by Playfair Display, Libre Baskerville, and Inter with fluid CSS `clamp()` scaling.
- **Cinematic 4-Slide Homepage Hero Slider**: Original photorealistic WebP photography, Ken Burns slow zoom, 5.5s auto-playback with progress indicators, Prev/Next, Pause/Play, keyboard navigation, and mobile touch swipe.
- **Genuine Author & Researcher Photo Carousel**: Showcases all 15 genuine editorial & researcher portraits preserved from the existing site (with institutional monograms for the 4 Advisory Board professors without supplied photos — zero fabricated portraits).
- **Complete Image Audit & Fixes**: Fixed all 29 broken `.webp.webp...` figure paths across research articles and APA resources, and replaced missing WordPress slider banners with locally stored optimized WebP editorial photography.
- **Zero External JS Dependencies**: Lightweight vanilla ES6 JavaScript (`assets/site.js`) and modular CSS3 (`assets/style.css`) with `prefers-reduced-motion` support.

## Hosting & Deployment Instructions
1. Upload the entire contents of this folder directly into your web server root (e.g., `public_html/` on cPanel, Apache, Nginx, or any PHP-enabled hosting).
2. All internal links and assets use clean relative paths — no hardcoded domain dependencies.
3. Verify HTTPS is active so copy-to-clipboard buttons and form submissions run over a secure origin.

## Backend Form Configuration (`backend/submit.php`)
All three existing forms (`common-signup/`, `book-publication/`, and `contact-us/`) preserve their exact original `form_fields[...]` input names and submit via `POST` (`multipart/form-data`) to `backend/submit.php`.

Currently, `backend/submit.php` preserves the original safety stub returning HTTP 503 until server mail/storage credentials are configured. Before enabling live online submissions in production:
1. Configure authenticated SMTP (e.g., PHPMailer with SPF/DKIM) to forward submissions to `editor@ijpc.in` / `iiprt2021@gmail.com`.
2. Validate and sanitize uploaded file extensions (`.doc`, `.docx`, `.pdf`, `.jpg`, `.png`) and enforce file size limits (max 20 MB), storing uploads outside the public webroot.
3. Add CSRF protection and rate limiting or server-side honeypot checks.

## Verification Notes
- All 47 HTML pages, internal links, PDF links, and local image references were programmatically audited with 0 broken local images and 0 broken internal links.
- Visual & interactive testing verified across desktop (1440px, 1280px, 1024px) and mobile/tablet (768px, 390px, 375px, 320px) viewports with zero horizontal overflow and zero console errors.
