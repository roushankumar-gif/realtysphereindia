# RealtySphere — Cloudflare Pages Starter

A static, luxury blue-and-gold real estate editorial website with subtle watercolor imagery.

## Files
- `index.html` — homepage
- `blog/index.html` — first article
- `about.html`, `contact.html`, `privacy.html`
- `styles.css`
- `assets/` — WebP images
- `robots.txt`, `sitemap.xml`, `404.html`

## Before publishing
1. Choose a Cloudflare Pages project name (for example, `realtysphere-journal`).
2. Replace every `https://YOUR-PROJECT.pages.dev` in HTML, `robots.txt`, and `sitemap.xml` with the actual published URL.
3. Replace the contact-email placeholder on `contact.html` with an email address you control, or remove it.
4. Review the privacy page so it reflects the tools you actually use.
5. Upload the contents of this folder using Cloudflare's static asset upload flow.
6. Test `/`, `/blog/`, `/about.html`, `/contact.html`, `/privacy.html`, `/robots.txt`, and `/sitemap.xml`.
7. Add the published URL to Google Search Console, verify ownership, then submit `/sitemap.xml`.

## Notes
- No domain purchase is required for a `pages.dev` subdomain, but project-name availability must be checked in Cloudflare.
- Search indexing and rankings are not guaranteed.
- This static site has no CMS. To publish another article, create a new HTML file/folder and add its URL to the sitemap and blog listing. For frequent blogging, consider a CMS later.
