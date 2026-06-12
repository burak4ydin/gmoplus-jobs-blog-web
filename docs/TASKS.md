# Task Backlog — gmoplus-jobs-blog-web

## P0 — Blocking
(none)

## P1 — High priority / Correctness
- [ ] NEXT_PUBLIC_APP_URL in .env.example is `https://blog.jobs.gmoplus.com` — verify this matches deployed Coolify domain; the domain map does not list a blog subdomain for jobs, likely copy-paste from another blog-web
- [ ] No sitemap.xml — career/HR content pages need sitemap for SEO indexing; add next-sitemap or App Router sitemap.ts

## P2 — Quality
- [ ] @types/react devDependency is `^18.3.0` but runtime React is `^19.0.0` — upgrade to avoid type drift
- [ ] eslint/eslint-config-next on v8/v14 while app runs Next.js 15 — upgrade
- [ ] No error.tsx at [locale] level — failed blog-api fetches silently break the page
- [ ] No loading.tsx skeleton on article list or detail pages

## P3 — Nice to have
- [ ] Add ISR revalidation on article pages
- [ ] Add RSS feed at /feed.xml
- [ ] Add JSON-LD Article schema for rich snippet eligibility in search results
- [ ] Confirm shared blog-api serves jobs-vertical content correctly (category taxonomy may differ from auto blog)