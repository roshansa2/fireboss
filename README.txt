FIRE BOSS WEBSITE — deployment & editing guide
==============================================

PAGES
  index.html      Home
  about.html      About
  products.html   Product catalogue (filter, search, enquiry list)
  services.html   Services + FAQ
  gallery.html    Gallery with lightbox
  contact.html    Enquiry form, map, contact details
  404.html        Error page

DEPLOY ON HOSTINGER
  1. hPanel > Websites > File Manager > public_html
  2. Upload the CONTENTS of this folder (not the folder itself) — index.html must sit directly in public_html.
  3. Make sure .htaccess is uploaded too (it may be hidden — enable "show hidden files").
  4. Once SSL is active, uncomment the HTTPS redirect lines in .htaccess.

CHANGE THE WHATSAPP NUMBER / PHONE / EMAIL
  - assets/js/config.js  ->  whatsapp, phones, email, defaultMessage
    (drives every WhatsApp button, the sticky button, the enquiry list and the contact form)
  - The phone numbers/email/address text in the header, footer and contact page are plain HTML —
    search & replace them across the .html files if they ever change.
  - The WhatsApp number 918249957373 is also written into each button's fallback link in the HTML;
    do a search & replace for 918249957373 if you change the number.

IMPORTANT ASSUMPTION
  The WhatsApp number is set to the FIRST mobile in the brochure (8249957373).
  Confirm which of the three numbers the client wants on WhatsApp.

HOW THE ENQUIRY FORM WORKS
  No server needed: "Send on WhatsApp" opens WhatsApp with the enquiry pre-filled;
  "Send by email" opens the visitor's mail app addressed to the client.
  Products added to the "Enquiry list" are included automatically.

IMAGES
  All photos were cut from the client's brochure (assets/img). They are low resolution (~100-300px for products).
  Replace files with the same file names (e.g. assets/img/products/abc.jpg) for sharper photos — no code changes needed.
  The logo (assets/img/logo.jpg) is the raster JPG from the brand kit; swap in a vector/PNG master when available.

BRAND
  Colours: Charcoal #2D2D2F, Safety Red #ED1C24, Safety Orange #F58220, Safety Yellow #FFD400, White #FFFFFF
  Fonts: Montserrat (headings) + Poppins (body) — self-hosted in assets/fonts (no Google Fonts call).
