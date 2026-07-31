# Wellness Worthy Counseling 💐

This is the website for **www.wellnessworthycounseling.com**. There are only
two things to know:

- **Editing your site day-to-day** (changing words, swapping photos) →
  see [EDITING.md](EDITING.md)
- **Getting it live the first time** → that's the rest of this page, below.

## Getting Your Website Live 🚀

This is the one-time setup that connects your website files to your domain.
You only ever do it once.

There are two halves: turning the website **on** (GitHub's side) and pointing
your **domain name** at it (your domain company's side).

> **📌 One rule that matters for every step below:** wherever these
> instructions say `mtgiguere`, that's the GitHub username of the account
> this website lives under. If this repository moves to **your** GitHub
> account, use **your username** instead — e.g. the address becomes
> `yourusername.github.io` — and it's *your* copy's Settings → Pages that
> must be turned on. Everything else stays exactly the same.

> ### ⚠️ Read this first: your old site stays up until Part 2
>
> Right now, www.wellnessworthycounseling.com shows your **existing Teachery
> site**. It will keep showing it until you do Part 2 below — and the moment
> you do Part 2, visitors see **this new site instead**. There's no
> in-between.
>
> So the smart order is:
>
> 1. Do **Part 1** now. That publishes a *preview* of the new site at
>    **https://mtgiguere.github.io/wellnessworthycounseling** without
>    touching your real domain.
> 2. Take your time replacing the placeholder text and photos
>    (see [EDITING.md](EDITING.md)) until the preview looks right.
> 3. Do **Part 2** when you're ready to go live for real.
>
> And if you ever regret it: Part 2 is fully reversible (see the last
> section of this page).

### Part 1 — Turn the website on (GitHub)

1. Log in at **github.com** and open the `wellnessworthycounseling` repository.
2. Click **Settings** (the gear tab at the top of the repository).
3. In the left sidebar, click **Pages**.
4. Under **"Build and deployment" → "Source"**, choose **"Deploy from a
   branch"**. Set the branch to **`main`** and the folder to **`/ (root)`**,
   then click **Save**.
5. The **"Custom domain"** box should already show
   `www.wellnessworthycounseling.com` (it reads that from a file in the
   website). If it's empty, type it in and click **Save**.
6. Leave this tab open — you'll come back after Part 2.

### Part 2 — Point your domain at it (your domain company)

Log in to the company where you bought the domain (GoDaddy, Namecheap,
Squarespace Domains, etc.) and find the **DNS settings** (sometimes called
"DNS records", "Manage DNS", or "Advanced DNS") for
wellnessworthycounseling.com.

The names and buttons vary a little by company, but every one of them has
these same fields.

**Step 1 — Edit your existing `www` record (this is the switch-over moment).**
In your DNS records you'll find one that looks like this — it's what points
your domain at Teachery today:

| Type | Host / Name | Value (currently) |
|---|---|---|
| `CNAME` | `www` | `www.teachery.co` |

Click edit on that record and change **only the value** to:

| Type | Host / Name | Value (new) |
|---|---|---|
| `CNAME` | `www` | `mtgiguere.github.io` |

That single edit is the whole switch. Saving it takes your Teachery site
off the domain and puts the new site on it (within the hour).

**Step 2 — Add four records so wellnessworthycounseling.com (without the
www) also works.** These are brand new — the "Add record" button. All four
are type `A`, with Host/Name set to `@` (which means "the bare domain"),
one for each of these values:

| Type | Host / Name | Value |
|---|---|---|
| `A` | `@` | `185.199.108.153` |
| `A` | `@` | `185.199.109.153` |
| `A` | `@` | `185.199.110.153` |
| `A` | `@` | `185.199.111.153` |

(If there are already other `A` or `CNAME` records sitting on `@`, delete
those old ones — they'll fight with the new ones.)

### Part 3 — Wait, then flip on the padlock

1. DNS changes take anywhere from a few minutes to a day to spread across
   the internet. Usually it's under an hour. Go have a coffee. ☕
2. Back on the GitHub **Settings → Pages** tab, it will run a check on your
   custom domain. When it shows a green check, tick the
   **"Enforce HTTPS"** checkbox. That's the padlock 🔒 browsers show —
   it may take another hour to become available. If the checkbox is greyed
   out, wait and refresh; it sorts itself out.
3. Visit **www.wellnessworthycounseling.com** — that's your website!

### If something's not working

- **"Domain's DNS record could not be retrieved"** on GitHub → the DNS
  records from Part 2 haven't spread yet, or a Host/Name field has a typo.
  Wait an hour and re-check Part 2.
- **The old parking page still shows** → your browser is remembering it.
  Try a private/incognito window, or a different device.
- **Site shows but looks broken / no padlock** → "Enforce HTTPS" isn't on
  yet. See Part 3, step 2.
- Anything else → text Matt. This setup only happens once; nothing you do
  while editing the site day-to-day can undo it.

### Changed your mind? Going back to Teachery

The switch is not a one-way door. To put your old Teachery site back on the
domain, edit that same `www` record from Part 2 and change its value from
`mtgiguere.github.io` back to **`www.teachery.co`**. The old site returns
within the hour. (This only works while your Teachery account is still
active, so don't cancel Teachery until you're sure you're happy.)
