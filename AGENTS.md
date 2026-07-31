# Instructions for AI agents

This is the website for Wellness Worthy Counseling
(www.wellnessworthycounseling.com), a small counseling practice. It is
deliberately the simplest possible kind of website, and the owner is **not a
programmer**. Your job is to help her without making the site more
complicated. Read this whole file before changing anything.

## The prime directive: keep it simple

The entire architecture is: plain HTML files + one CSS file + an images
folder, served by GitHub Pages straight from the `main` branch. There is no
build step, no framework, no package.json, no tests, no CI. **This is a
feature, not an oversight.**

Do NOT introduce, even if it would be "better":

- npm / node_modules / any package manager
- React, Astro, Jekyll, Tailwind, or any framework/generator
- Build steps, bundlers, minifiers, or GitHub Actions
- A JavaScript file (the only JS on the site is tiny inline `onerror`
  attributes on images — leave it that way)
- New top-level folders or config files

If she asks for something that genuinely needs those (a blog, a booking
system), explain the trade-off in plain English first and suggest an
external service (Calendly, etc.) linked from the site instead.

**Her courses live on Teachery** (her account at teachery.co). Requests
like "link to my Digital Awareness course" are exactly right for this
site: just point a button or link (e.g. the ones on
`digital-awareness.html`) at the course's Teachery URL — ask her for the
URL if she hasn't given it. Same goes for scheduling: the "I am ready"
buttons currently use a placeholder `mailto:`; swapping in her real
scheduler or email link is a one-line edit, not a rebuild.

## How the site is organized

| File | What it is |
|---|---|
| `index.html`, `services.html`, `digital-awareness.html`, `resources.html`, `about.html` | The five pages. Nav menu is duplicated in each — a nav change means editing all five. |
| `css/style.css` | ALL look-and-feel. Colors are CSS variables at the top. Never put styling inline in the HTML. |
| `images/` | One optional image per page, **named after the page** (`about.html` → `images/about.jpg`). Plus optional `background.jpg`, shown faintly site-wide via `body::before`. |
| `EDITING.md` | Her plain-English editing manual. |
| `README.md` | Her one-time GitHub Pages + DNS setup guide. |
| `CNAME` | Custom domain for GitHub Pages. **Never delete or rename it.** |

## Conventions to preserve

1. **Per-page images.** Every page has at most one image, at
   `images/<pagename>.jpg`. Each `<img>` has an `onerror` handler so a
   missing file hides the image (and collapses the photo column on
   two-column pages). If you add a page, follow this pattern exactly.
2. **Friendly comments.** Editable spots in the HTML are marked with
   `<!-- ✏️ ... -->` and photo instructions with `📷`. Keep them accurate —
   they are the owner's user interface. If you change behavior, update the
   comments and `EDITING.md` in the same commit.
3. **Docs in plain English.** `EDITING.md` and `README.md` are written for a
   non-technical reader. No jargon; keep that voice.
4. **Content placeholders.** Much of the text is placeholder (Calvin &
   Hobbes jokes). Placeholders say so explicitly. When she gives you real
   text, just swap it in — don't rewrite her words without being asked.
5. **Design.** Taupe (#a99f8f) nav and banner, Playfair Display headings,
   Poppins body. It mirrors her chosen design — don't restyle uninvited.

## Hard rules

- **No PII, ever.** This is a counseling site. Never add client names,
  testimonials with real names, intake forms, or anything that collects or
  stores visitor data. Contact goes through `mailto:` links or an external
  scheduler.
- Keep the 988 Suicide & Crisis Lifeline link on the Resources page unless
  she explicitly removes it.
- Don't force-push, rewrite history, or delete `CNAME`.
- Test by opening `index.html` in a browser (or `python -m http.server`).
  If it needs more than that to preview, you've overcomplicated it.
