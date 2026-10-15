# RealtySphere

Static website for Cloudflare Pages. No build step, no backend.

## Structure
`index.html`, `blog/`, `about/`, `contact/`, `404.html`, `styles.css`, `script.js`, `robots.txt`, `sitemap.xml`, `favicon.svg`, `_headers`, `images/` (your four watercolor images, cropped and converted to WebP).

## 1. Replace the placeholder URL
Every canonical, Open Graph, JSON-LD, `robots.txt` and `sitemap.xml` entry uses the **placeholder** `https://realtysphere.pages.dev`. If your real address differs, run from the site folder:

    grep -rl "realtysphere.pages.dev" . | xargs sed -i 's#https://realtysphere.pages.dev#https://YOUR-REAL-URL#g'

Do not submit the sitemap to Google until this is done and the site is live.

## 2. Deploy (free)
1. Sign in at dash.cloudflare.com, then Workers & Pages, Create, Pages.
2. Choose "Upload assets" (direct upload), name the project (e.g. `realtysphere`; if taken, try `realtysphere-blog` or `realtysphere-india`).
3. Upload the site folder (or the ZIP contents) and deploy. Your address will be `<project-name>.pages.dev`.
4. Apply step 1 with that address, then re-upload.

## 3. Google Search Console
1. Open search.google.com/search-console, click Add property, choose **URL prefix**, enter your live URL.
2. Verify ownership: use the HTML tag method (add the `<meta name="google-site-verification" ...>` tag to the `<head>` of `index.html`, redeploy, click Verify) or the HTML file method (upload the file to the site root).
3. Sitemaps, enter `sitemap.xml`, Submit.
4. URL Inspection, paste the homepage URL, then the first article URL. If "URL is not on Google", click Request indexing.

Search Console is not connected until you complete verification yourself.

## Adding articles
Copy the article folder under `blog/`, edit the content, title, description, canonical, JSON-LD and dates, add a card to `blog/index.html` and `index.html`, and add the URL to `sitemap.xml`.

## Before publishing
- Add real contact details to `contact/index.html` only when you have them.
- Verify any location facts (Sector 16 connectivity, land use) before adding them.
- Local preview: `python3 -m http.server` in this folder (root-relative paths need a server).
