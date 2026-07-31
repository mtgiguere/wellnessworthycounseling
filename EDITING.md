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

## Optional: putting the website on your own computer ("cloning")

Everything above happens on the GitHub website, and honestly that's all you
ever *need*. But you can also keep a copy of the site on your computer —
useful if you want to preview changes before they go live, edit lots of
things at once, or use an AI assistant. This is called **cloning**, and it
doesn't move anything — GitHub stays the "real" copy; your computer gets a
linked twin.

The friendly way is an app called **GitHub Desktop**:

1. Download it free from **desktop.github.com**, install it, and sign in
   with your GitHub account.
2. Click **File → Clone repository**, pick
   **`wellnessworthycounseling`** from the list, and click **Clone**.
   That's it — the whole website is now in a folder on your computer
   (it tells you where; usually Documents\GitHub).
3. **To preview the site:** open that folder and double-click
   `index.html`. It opens in your web browser, working exactly like the
   real site — photos, pages, everything. No internet required.
4. **To edit:** open any `.html` file in a text editor (Notepad works;
   a free app called VS Code is nicer), change your words, save, and
   refresh the browser to see it instantly.
5. **To publish your changes:** go back to GitHub Desktop. It shows a
   list of everything you changed. Type a short note in the "Summary" box
   (e.g. "updated my bio"), click **Commit to main**, then click
   **Push origin** at the top. A minute later it's on the live site.
6. **Before each editing session**, click **Fetch origin → Pull** in
   GitHub Desktop first, so your computer picks up any changes made
   elsewhere (like edits you did on the GitHub website, or Matt's fixes).

Two nice things about this setup:

- **You can't lose work.** Until you click Push, nothing you do on your
  computer touches the live site. Mess something up? GitHub Desktop has a
  "discard changes" option that puts files back the way they were.
- **AI assistants understand this website.** If you use one on your
  computer (Claude, GitHub Copilot, etc.), just open the website's folder
  and ask for what you want in plain English — there's an instruction file
  in the folder (`AGENTS.md`) that they read automatically, which tells
  them how this site works and what not to break.

## Things to ask Matt for help with

- Renaming or adding a whole page (the menu appears in all five files)
- Changing colors or fonts (they live in `css/style.css`)
- Anything involving the domain name (www.wellnessworthycounseling.com)
