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

Add these records. The names and buttons vary a little by company, but every
one of them has these same fields:

**Record 1 — makes www.wellnessworthycounseling.com work:**

| Field | What to enter |
|---|---|
| Type | `CNAME` |
| Host / Name | `www` |
| Value / Points to | `mtgiguere.github.io` |
| TTL | leave the default |

**Records 2–5 — makes wellnessworthycounseling.com (without the www) work.**
Add four records of type `A`, all with Host/Name set to `@` (which means
"the bare domain"), one for each of these values:

| Type | Host / Name | Value |
|---|---|---|
| `A` | `@` | `185.199.108.153` |
| `A` | `@` | `185.199.109.153` |
| `A` | `@` | `185.199.110.153` |
| `A` | `@` | `185.199.111.153` |

⚠️ If there are already `A` or `CNAME` records on `@` or `www` (domain
companies often pre-fill a "parking page"), delete those old ones — they'll
fight with the new ones.

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
