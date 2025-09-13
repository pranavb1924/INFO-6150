Nobel — HTML/CSS Single-Page Site (readme.txt)
=================================================

A lightweight, no-JS* (except optional “ding” on subscribe) site about the Nobel Prize.
Uses semantic HTML5, a fixed header/footer, and the CSS :target trick so only one
section is visible at a time.

*If you enable the optional “ding” on Subscribe, there is a tiny script. The site
still works fully without JavaScript.

-------------------------------------------------
How to run
-------------------------------------------------
1) Open index.html in any modern browser.
2) Keep all assets in the /resources folder as listed below.

-------------------------------------------------
What’s inside
-------------------------------------------------
- Fixed header and footer pinned to top and bottom.
- Hash navigation (#home, #about, #winners, #categories, #newsletter) toggles sections
  with CSS only (no frameworks).
- Tables listing recent laureates by category.
- Newsletter form with text, email, password, and a datalist for interests.
- Media: image inside figure/figcaption, video with poster, and an (invisible) audio
  element for autoplay on Home OR an optional “ding” when the Subscribe button is clicked.
- Contact links: mailto: and tel: in the footer.

-------------------------------------------------
Tag index (all HTML tags used + short descriptions)
-------------------------------------------------
html            - Root element of the document
head            - Metadata container (title, fonts, favicon, styles)
meta            - Charset and viewport configuration
title           - Page title shown in the browser tab
link            - External resources (stylesheet, Google Fonts, favicon)
body            - Page content wrapper
header          - Top site header with logo and navigation
nav             - Primary navigation list
main            - Main content region
section         - Page sections (home, about, winners, categories, newsletter, etc.)
article         - Independent content blocks (definition card; winner/story cards)
aside           - Pull-quote beneath the hero image
footer          - Site footer with contact links
h1              - Site logo/title
h2              - Section headings
h3              - Subheadings (e.g., winners subtitle/cards)
h4              - Card titles in the news grid
p               - Paragraph text
strong          - Strong emphasis in the definition text
em              - Emphasis (italic) in the definition text
br              - Line break in the quote
ul              - Unordered lists (nav, quick links, categories grid)
li              - List items for nav/links/categories
a               - Hyperlinks (hash links, external articles, mailto, tel)
figure          - Image with caption wrapper
figcaption      - Caption for the figure
img             - Images (icons, thumbnails, category icons)
video           - Embedded video (poster, autoplay, muted, controls as needed)
source          - Media sources for <video> and <audio>
details         - FAQ accordion container
summary         - Toggle title for the FAQ
table           - Tabular data for laureates
thead           - Table header row group
tbody           - Table body rows
tr              - Table row
th              - Table header cell
td              - Table data cell
form            - Newsletter signup form
label           - Accessible labels (visually hidden with .sr-only class)
input           - Form fields (text, email, password, list for datalist)
datalist        - Autosuggest options for the Area of interest input
option          - Individual datalist options
button          - Submit button (Subscribe)
div             - Neutral grouping (containers, wrappers)
audio           - Invisible background audio on Home or click “ding”
script          - (Optional) tiny handler to play a sound on Subscribe click

Note: <!DOCTYPE html> and HTML comments <!-- ... --> also appear, but they are a
declaration/comment, not element tags.

-------------------------------------------------
Files & folders
-------------------------------------------------
/index.html
/styles.css
/resources/
  favicon.png
  bg.png
  thumbnail.jpg
  about.mp4
  madam-curie.png
  albert.png
  mother-theresa.png
  mandela.png
  physics.png
  chemistry.png
  peace.png
  literature.png
  medicine.png
  intro.mp3        (for Home autoplay)
  ding.mp3         (optional subscribe sound)

-------------------------------------------------
How the “one section at a time” works (CSS-only)
-------------------------------------------------
- Navigation links point to #ids for each .page section.
- CSS uses :target to display:block the active .page and keep others display:none.
- #home is shown by default; when any other section is targeted, #home is hidden.

-------------------------------------------------
Optional audio behaviors
-------------------------------------------------
A) Home section autoplay (no controls visible)
   <audio id="home-audio" preload="auto" autoplay loop hidden aria-hidden="true">
     <source src="./resources/intro.mp3" type="audio/mpeg">
   </audio>
   (Hidden attribute keeps it invisible. Some browsers require a user gesture
   before playing audio with sound.)

B) “Ding” when Subscribe is clicked (optional JavaScript)
   1) Add id to the button:
      <button id="subscribe-btn" type="submit">Subscribe</button>
   2) Add hidden audio once near the end of <body>:
      <audio id="ding" preload="auto">
        <source src="./resources/ding.mp3" type="audio/mpeg">
      </audio>
   3) Minimal script:
      <script>
        const btn  = document.getElementById('subscribe-btn');
        const ding = document.getElementById('ding');
        btn.addEventListener('click', () => {
          try { ding.currentTime = 0; ding.play(); } catch (e) {}
        });
      </script>

-------------------------------------------------
Accessibility notes
-------------------------------------------------
- Every input has a <label>; labels are visually hidden with the .sr-only utility
  but remain available to screen readers.
- All images include meaningful alt text.
- Keyboard focus styles are preserved for navigation and form controls.

-------------------------------------------------
Known tiny polish
-------------------------------------------------
- In styles.css, change the font stack token “Sego e UI” to “Segoe UI”.
- Keep only one favicon <link> (recommend: resources/favicon.png).

-------------------------------------------------
Credits
-------------------------------------------------
Public facts and article links reference nobelprize.org pages.
