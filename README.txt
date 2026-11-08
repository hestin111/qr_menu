QR MENU - starter project
=========================

Files
  index.html   The menu page (one page that serves every restaurant)
  menus.json   The menu data (one entry per restaurant, key = link name)
  _redirects   Makes /abebe-cafe and /selam-kitfo load index.html
               (works on Cloudflare Pages and Netlify)

Test on your computer
  1. Open a terminal in this folder and run:  python3 -m http.server 8000
  2. Visit:  http://localhost:8000/index.html?r=abebe-cafe
     (The ?r= part replaces the redirect, which only works once deployed.)
  3. Open http://localhost:8000/index.html to see a list of the demo restaurants.

Deploy (free)
  1. Put these files in a GitHub repository.
  2. In Cloudflare Pages or Netlify choose "Import from Git", leave the build
     command empty, and set the output folder to the root.
  3. Your menu is then at  https://YOURPROJECT.pages.dev/abebe-cafe

Add a restaurant
  Copy one block in menus.json, change the key (this becomes the link),
  the names, prices and "accent" colour, then push the change.
  Keys must be lowercase letters, numbers and dashes.

Important JSON rules
  - Every item and category except the last one needs a comma after it.
  - "available": false shows the item as Sold out.
  - Delete the demo restaurant list block in index.html (marked in a comment)
    before real use, so customers cannot browse your other clients.
