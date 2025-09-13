# Nobel — HTML/CSS Single-Page Site

A lightweight, no-JS* (except optional “ding” on subscribe) site about the Nobel Prize.  
Uses semantic HTML5, fixed header/footer, and the CSS `:target` trick so only one section is visible at a time.

## How to run
Open `index.html` in any modern browser. All assets are under `/resources`.

## What’s inside
- **Fixed header & footer** pinned to top/bottom.
- **Hash navigation** (`#home`, `#about`, `#winners`, `#categories`, `#newsletter`) toggles sections with CSS only.
- **Tables** listing recent laureates by category.
- **Form** with `text`, `email`, `password`, and a `datalist`.
- **Media**: image inside `figure/figcaption`, video with `poster`, and an (invisible) audio element for autoplay on **Home** *(or optional “ding” when Subscribe is clicked)*.
- **Contact** links: `mailto:` and `tel:` in the footer.

\* If you enable the optional “ding” on subscribe, there’s a 6-line script; the site otherwise works fully without JS.

---

## Tag index (all HTML tags used + short descriptions)

| Tag | Description / How used |
|---|---|
| `html` | Root element of the document |
| `head` | Metadata container (title, fonts, favicon, styles) |
| `meta` | Charset & viewport configuration |
| `title` | Page title shown in browser tab |
| `link` | External resources (stylesheet, Google Fonts, favicon) |
| `body` | Page content wrapper |
| `header` | Top site header with logo and navigation |
| `nav` | Primary navigation list |
| `main` | Main content region |
| `section` | Page sections (`home`, `about`, `winners`, `categories`, `newsletter`, etc.) |
| `article` | Independent content blocks (definition card; news/winner cards) |
| `aside` | Pull-quote beneath the hero |
| `footer` | Site footer with contact links |
| `h1` | Site logo/title |
| `h2` | Section headings |
| `h3` | Subheadings (e.g., winners subtitle/cards) |
| `h4` | Card titles in the news grid |
| `p` | Paragraph text |
| `strong` | Strong emphasis in the definition text |
| `em` | Emphasis (italic) in definition text |
| `br` | Line break in the quote |
| `ul` | Unordered lists (nav, quick links, categories grid) |
| `li` | List items for nav/links/categories |
| `a` | Hyperlinks (hash links, external articles, `mailto:`, `tel:`) |
| `figure` | Image with caption wrapper |
| `figcaption` | Caption for the figure |
| `img` | Images (icons, thumbnails, category icons) |
| `video` | Embedded video with `poster`, `autoplay`, `muted`, `controls` |
| `source` | Media sources for `<video>` (and `<audio>` if used) |
| `details` | FAQ accordion container |
| `summary` | Toggle title for the FAQ |
| `table` | Tabular data for laureates |
| `thead` | Table header row group |
| `tbody` | Table body rows |
| `tr` | Table row |
| `th` | Table header cell |
| `td` | Table data cell |
| `form` | Newsletter signup form |
| `label` | Accessible labels (visually hidden with `.sr-only`) |
| `input` | Form fields (`text`, `email`, `password`, `list`) |
| `datalist` | Autosuggest options for the “Area of interest” input |
| `option` | Individual datalist options |
| `button` | Submit button (“Subscribe”) |
| `div` | Neutral grouping (containers, wrappers) |
| `audio` | *Invisible* background audio on **Home** or optional click “ding” |
| `script` | *(Optional)* tiny handler to play a sound on subscribe click |

> Note: `<!DOCTYPE html>` and HTML comments `<!-- ... -->` also appear, but they are a declaration/comment, not tags.

---

## Files & folders

