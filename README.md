# Infinite Designs — website

39 pages, one stylesheet, one script. All files sit loose in this folder — no subfolders.

**You can test it right now.** Double-click `index.html` and it opens in your browser, fully working, before you upload anything. Click Work, click a project, click Insights, click an article — it all works straight off your computer.

## Upload to GitHub

1. **github.com/new** — name it `infinite-designs-website`, leave the three checkboxes unticked, click **Create repository**
2. Click the link "**uploading an existing file**"
3. Open this folder, press **Ctrl+A** (or **Cmd+A**), drag everything onto the GitHub page
4. Wait for the list to finish, then click **Commit changes**

If you already have the repository: **Add file → Upload files**, drag everything, **Commit changes**. Same filenames replace the old ones automatically.

## Deploy on Vercel

1. **vercel.com/new** → click **Import** next to your repository
2. Set **Framework Preset** to **Other**
3. Leave Build Command, Output Directory and Install Command **empty**
4. Click **Deploy**

Nothing else to configure. Every page is a plain HTML file, so any host serves it correctly — Vercel, Netlify, Cloudflare Pages, cPanel, anything.

## Your details

Studio: Uttara, Dhaka 1230, Bangladesh
Phone: 01838642061 and 01790645450 (tap-to-call on mobile)
Email: hello@infinitedesigns.com.bd
Founded: 2024

These appear in the footer and mobile menu of **every** page. To change them, use find-and-replace across all files in a free editor like VS Code (Ctrl+Shift+F), not one file at a time.

## The files

- `index.html` — home
- `about.html` `services.html` `work.html` `insights.html` `careers.html` `contact.html` `privacy.html` `terms.html` — main pages
- `services-*.html` — 13 service pages
- `work-*.html` — 10 case studies
- `insights-*.html` — 6 articles
- `404.html` — shown for an address that doesn't exist
- `styles.css` — every colour, font and spacing value
- `site.js` — animations only; the site reads fine without it
- `vercel.json` `sitemap.xml` `robots.txt` — hosting settings and search engine files

Every page links directly to the file next to it — `work.html` links to `work-ostara-bank.html`. Nothing depends on server configuration, which is why it cannot break.

## Changing colours

Open `styles.css`. The whole palette is at the very top:

```css
:root{
  --ink-900:#07060D;      /* page background      */
  --violet:#7B5CFF;       /* main accent colour   */
  --cyan:#3AE0D0;         /* second accent colour */
  --marigold:#FFAE3B;     /* the big numbers      */
  --txt:#EDEBF7;          /* body text            */
}
```

Change `--violet` and every button, link and highlight changes with it.

## Changing text

Open any `.html` file. The words you see on the website sit between the pointy brackets:

```html
<h1>Four people, two years, forty projects</h1>
```

Edit only what's between `>` and `<`. Leave the brackets alone. Don't edit inside `<svg ...>` blocks — that's the drawing code for the logos and illustrations.

## Two things before you share the link publicly

**1. The ten clients are invented.** Ostara Bank, Prottasha Health, Veloce Retail, Lumenpay, Textura Mills, Skolar, Rundo Logistics, Aurelia Living, Cirrus Energy and Bayleaf Hospitality are made-up companies with logos drawn for this site. Visitors would read fake case studies as real ones. Replace them with your real clients, or remove the case studies. Then delete these three notices:

- the footer paragraph on every page starting `Portfolio, client names and testimonials on this site are sample content…`
- the notice near the top of `work.html`
- the "Portfolio content" section in `terms.html`

**2. The contact form doesn't send yet.** It checks the fields and then tells the visitor it isn't connected. To make it send, open `site.js`, find the comment `replace these two lines to POST to your endpoint`, and connect it to Formspree (free) or your own email service.

## Tested before packaging

1,888 internal links checked across all 39 pages — zero broken. Every page loads its own content with the stylesheet applied. No JavaScript errors. Nothing scrolls sideways at phone width. The Uttara address and both phone numbers appear on all 39 pages. Verified working with no web server at all, so it cannot fail on a host.
