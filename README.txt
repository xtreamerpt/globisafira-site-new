GLOBISAFIRA – TRANSPORTES, LDA. — WEBSITE
=========================================

This folder is a complete static website. No server software, database or
build step is needed: upload the whole folder as-is to any web host.

What's inside
  index.html        the website
  favicon.svg       browser tab icon
  robots.txt        lets search engines index the site
  assets/css        styles (site.css) and font setup (fonts.css)
  assets/fonts      the Archivo typeface (self-hosted, no Google requests)
  assets/js         Three.js, GSAP and the map data (geo.js)
  assets/img        photos
  assets/video      the two looping fleet clips

How to put it online (pick one)
  1. Netlify Drop (free, fastest): go to https://app.netlify.com/drop and drag
     this whole folder onto the page. You get a live link immediately and can
     connect your own domain in Site settings > Domain management.
  2. Your existing hosting (cPanel, Plesk, PTisp, Amen, etc.): open the File
     Manager or FTP, go to public_html (or www/htdocs) and upload everything
     in this folder, keeping the folder structure.
  3. GitHub Pages / Cloudflare Pages / Vercel: upload the folder as a project;
     no build command, output directory = the folder root.

Important: keep index.html and the assets folder side by side. Opening
index.html straight from your computer works for a quick look, but upload it
to a host for the real thing (some browsers block video and fonts from local files).

Languages
  The site is translated into 37 European languages (assets/js/i18n.js).
  It opens in the visitor's browser language automatically (English if their
  language isn't available) and the globe menu in the top bar lets them switch.
  Their choice is remembered on that device. You can also link to a specific
  language with ?lang=xx, e.g.  yoursite.pt/?lang=de
  To fix a wording: open assets/js/i18n.js, find the language block (e.g. pt:)
  and edit the text between the quotes. Keep the key names unchanged.

Things to edit later (all in index.html)
  - Phone and email: search for "964 646 911" and "globisafira@gmail.com".
    The quote form sends to the address in QUOTE_EMAIL.
  - Route distances: search for "km:" in the DESTS list in index.html.
    Transit times are translated: keys d3, d34, d45, d4 in assets/js/i18n.js.

Quote form
  The form opens the visitor's own email app with the request filled in and
  addressed to globisafira@gmail.com. To receive requests directly instead
  (without the visitor's email app), connect a form service such as Formspree
  or Netlify Forms and replace the submitTo() function.
