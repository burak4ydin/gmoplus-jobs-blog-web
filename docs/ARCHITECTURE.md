# Architecture — gmoplus-jobs-blog-web

## Folder Structure
```
src/
  app/
    layout.tsx
    globals.css
    [locale]/
      page.tsx              Blog homepage
      [slug]/page.tsx       Article detail
      kategoriler/page.tsx  Category index
      category/[slug]/      Articles by category
      author/[slug]/        Articles by author
      tag/[slug]/           Articles by tag
      search/page.tsx       Search results
```

## Data Flow
Next.js server component -> fetch() to blog-api -> isomorphic-dompurify sanitizes HTML -> @tailwindcss/typography renders prose. No client-side state management. All pages server-rendered.

## Service Communication
- Reads from `NEXT_PUBLIC_BLOG_API_URL` (https://blog-api.gmoplus.com/api/v1)
- No writes; no auth required

## Auth Model
None. Fully public read-only site. Identical architecture to gmoplus-auto-blog-web and gmoplus-realestate-blog-web.