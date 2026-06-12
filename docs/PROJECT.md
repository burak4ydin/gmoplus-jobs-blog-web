# gmoplus-jobs-blog-web

## What It Does
Static blog frontend for the GMOPlus Jobs vertical. Displays career advice, HR guides, and job market news published via the shared gmoplus-blog-api. Read-only; drives SEO traffic to jobs.gmoplus.com.

## Who Uses It
- Public readers (job seekers and HR professionals) arriving from search engines
- Editorial team publishes via admin panel; content appears here automatically

## Key Features
- Multilingual (TR/EN) via next-intl
- Article listing with category, tag, and author filtering
- Full-text search
- DOMPurify-sanitized HTML rendering
- @tailwindcss/typography styled prose

## Business Flow
1. Editor publishes career/HR article in admin panel
2. Article served server-side from blog-api
3. Reader arrives from search or jobs.gmoplus.com blog link
4. CTAs link back to jobs.gmoplus.com listings

## Success Criteria
- Article pages have correct og:title, og:description, og:image meta tags
- No unsanitized HTML in DOM
- Consistent page structure with other blog-web projects