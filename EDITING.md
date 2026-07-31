# How to Edit Your Website 💐

Hi! This is your website. Everything in it is a plain file you can edit
yourself — no coding knowledge needed. Here's the cheat sheet.

(Looking for the one-time setup that puts the site on your domain?
That's on the repository's front page — [README.md](README.md).)

## The 60-second version

1. Go to your website's page on **github.com** and log in.
2. Click the file you want to change (for example `index.html` — that's the home page).
3. Click the **pencil icon** (✏️, top-right of the file view).
4. Change the words you want to change. **Only edit text between `>` and `<` signs** — the stuff inside `< >` angle brackets is the machinery; leave it alone.
5. Click the green **"Commit changes"** button. That's it — the live site updates itself within a minute or two.

If you ever break something, don't panic: GitHub keeps every old version.
Text Matt and he can undo it with one click. You cannot permanently ruin anything.

## Which file is which page?

| File | Page |
|---|---|
| `index.html` | Home ("You are Worthy to be Well.") |
| `services.html` | Services |
| `digital-awareness.html` | Digital Awareness Course |
| `resources.html` | Resources |
| `about.html` | About Me |

Inside each file, look for comments like `<!-- ✏️ EDIT THE TEXT BELOW -->` —
those mark the spots meant for you.

## Changing a photo

You don't have to edit any code. **Every page has one picture, and the
picture's file name matches the page's file name:**

| Page | Its picture | Shape |
|---|---|---|
| `index.html` (Home) | `images/index.jpg` | tall (portrait of you) |
| `services.html` | `images/services.jpg` | wide |
| `digital-awareness.html` | `images/digital-awareness.jpg` | wide |
| `resources.html` | `images/resources.jpg` | wide |
| `about.html` | `images/about.jpg` | tall (portrait of you) |

To swap one:

1. Name your new photo **exactly** as shown above (e.g. `about.jpg`).
2. On GitHub, open the `images` folder → **Add file** → **Upload files**.
3. Upload your photo and commit. It replaces the old one automatically.

**Don't want a picture on some page?** Just delete that file from the
`images` folder (open the file on GitHub → the "..." menu → Delete file).
The page tidies itself up automatically — no empty gap left behind. Upload
a file with that name again later and the picture comes back.

## Optional: a soft background image

Want a gentle texture or photo behind the whole site? Upload a picture named
**`background.jpg`** to the `images` folder. It will appear very faintly
behind every page. Delete the file to remove it. (If it's too faint or too
strong, that's a one-number tweak in `css/style.css` — ask Matt.)

Tip: photos straight off a phone can be huge. If a page loads slowly, resize
the photo to around 1000 pixels wide first (any free online resizer works).

## Adding a link on the Resources page

Open `resources.html`, find the list of links, copy one whole line that starts
with `<li>` and ends with `</li>`, paste it below the others, then change the
web address (the part in quotes after `href=`) and the visible words.

## Things to ask Matt for help with

- Renaming or adding a whole page (the menu appears in all five files)
- Changing colors or fonts (they live in `css/style.css`)
- Anything involving the domain name (www.wellnessworthycounseling.com)
