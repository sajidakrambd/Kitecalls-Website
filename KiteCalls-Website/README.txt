KITECALLS WEBSITE — READ ME
============================

HOW TO VIEW IT
---------------
Just double-click index.html. That's it — no server, no install, no
internet connection required. Every file uses relative paths (./css/...,
./images/...), so opening it straight from Windows Explorer works
correctly, including all pages, images, the logo, and navigation.

If you ever see broken images or unstyled text again, it almost always
means the "css", "js", or "images" folder got separated from the HTML
files — keep this whole folder together, always.

WHAT WAS WRONG BEFORE, AND WHAT WAS FIXED
-------------------------------------------
The previous version used paths starting with a slash, like
"/css/style.css" and "/images/logo.png". A path starting with "/" tells
the browser "look at the root of the entire drive," not "look inside
this folder" — which only works when a real web server is involved.
Opened directly as a file, the browser was looking for C:\css\style.css
instead of the css folder sitting right next to index.html. That's why
CSS, images, and the logo all failed and text fell back to the browser's
default (Times New Roman).

This version uses only relative paths (./css/style.css, images/logo.png,
about.html, etc.) everywhere — in every one of the 19 pages, the
stylesheet, the script, and the footer/nav links. It's been checked
programmatically: every single href/src across every page resolves to a
real file in this folder, with zero root-absolute paths anywhere.

FOLDER STRUCTURE
-----------------
index.html                                  -> Home
about.html, leadership.html, services.html,
portfolio.html, contact.html, 404.html      -> other pages
<service-slug>.html  (12 files)             -> one page per service
css/style.css                               -> all styling
js/script.js                                -> mobile menu, scroll reveal, header shadow
images/                                     -> logo, favicons, all photography
fonts/README.txt                            -> why there's no font file, and how to add
                                                Futura PT later if you buy a license
sitemap.xml, robots.txt                     -> for search engines once deployed

FONT NOTE
----------
Futura PT is a paid, licensed font - no files for it were supplied, and
none can legally be bundled here. The site uses this fallback stack
instead:

    "Futura PT", Futura, "Century Gothic", Arial, Helvetica, sans-serif

Century Gothic ships with Windows by default, so most Windows users will
see a very close visual match with no setup at all. If you later buy
Futura PT, see fonts/README.txt for how to wire it in.

BEFORE THIS GOES LIVE ON A REAL DOMAIN
-----------------------------------------
- Phone, email and website in the Contact section and footer are
  placeholders (+971 XX XXX XXXX / hello@kitecalls.com / www.kitecalls.com)
  - swap in the real ones.
- sitemap.xml, robots.txt, and every page's canonical/Open Graph tags
  reference https://www.kitecalls.com as a placeholder domain - replace
  with the real domain before submitting to Google Search Console.
- The contact form currently opens the visitor's email client with the
  message pre-filled (a mailto: form). For real inline submission, wire
  it up to a form service (Formspree, etc.) once hosted.
