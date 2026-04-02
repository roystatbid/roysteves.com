# roysteves.com

Static HTML site hosted on GitHub Pages. No build step, no frameworks — Claude is the build tool.

## Site structure

- `/blog/` — blog posts, each as standalone HTML files
- `/blog/_template.html` — reference template for new posts (full SEO markup, structured data)
- `/projects/` — browser-based hobby/art projects, each in its own subfolder
- `/assets/css/style.css` — shared stylesheet
- `/assets/img/` — images
- `/feed.xml` — RSS 2.0 feed (manual, no build step)
- `/sitemap.xml` — sitemap for search engines
- `/robots.txt`

## New content checklist

Every new blog post requires all of these steps:

1. Create HTML file from `blog/_template.html` — fill in all SEO fields (title, description, canonical, OG, structured data)
2. Add entry to `blog/index.html` listing
3. Add entry to `sitemap.xml`
4. Add entry to `feed.xml`

## Rules

- **SEO is a top priority.** Every page needs: canonical URL, meta description, Open Graph tags, structured data (JSON-LD) where applicable. Add every new page to `sitemap.xml`. Use semantic HTML. Clean URL slugs.
- **No Twitter/X.** No Twitter card meta tags, no links to Twitter/X, no integration of any kind. Ever.
- **External links** must always use `target="_blank" rel="noopener"`.
- **No italic in UI/chrome** (nav, headings, captions). Body content may use italic, bold, and other inline formatting at Roy's direction.
- **Typography:** Palatino Linotype stack for serif (headlines, wordmark), system-ui stack for sans (body, nav, UI).
- **Color roles:** teal (`#7eb8c9`) for links, tags, active states. Gold (`#dfc98a` / `#eddfa8`) for callouts, borders, highlights. No visited/unvisited link distinction.

## Workflow

Roy drafts content in any format, pastes it into conversation. Claude applies the template, formats as HTML, handles SEO meta, and commits. No markdown-to-HTML pipeline needed.
