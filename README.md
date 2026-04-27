# Lake Morey 2026 — Dashboard

A single-file static site for the fall 2026 Lake Morey charity golf weekend. Built for the planning crew (Mike, Bob, Jim) to track progress, with a recruitment CTA for prospective golfers.

**Live target URL:** `https://fructifyme.github.io/lake-morey-2026/`

## What's here
- `index.html` — the entire dashboard (single file, no build step, no dependencies beyond Google Fonts)
- `README.md` — this file

That's it. Drop it in a repo, turn on Pages, done.

## Deploy to GitHub Pages

### One-time setup
1. Create a new public repo at **`github.com/fructifyme/lake-morey-2026`** (the URL the site will live at).
2. Push these two files (`index.html`, `README.md`) to `main`.
3. In the repo: **Settings → Pages → Source: Deploy from a branch → Branch: `main` → `/ (root)`**. Save.
4. Wait ~30 seconds. The site will be live at `https://fructifyme.github.io/lake-morey-2026/`.

### Updating
Edit `index.html`, commit, push. GitHub rebuilds within ~30 seconds.

## Things to update as the project moves

Search `index.html` for these markers when you need to change them:

| What | How to find it | When to update |
|---|---|---|
| **Days countdown** | Auto — calculates from `2026-09-25` | Update target date if W2 Sep 25–27 changes |
| **Golfers committed** | `3 / 16` in the stats grid | Each time someone commits |
| **Charity raised** | `$0` in stats + `raise-amount` + `raise-fill` width % | When donations come in |
| **Quote status** | `⏳ Inquiry sent to Lake Morey` | When the quote arrives, change to ✅ + tier |
| **What's happening right now** | Inside `.what-now` box in Progress section | Each phase milestone |
| **Checklist** | `.checklist` ul | Tick items off as they happen |
| **Recommended weekend** | Look for `class="date-card recommended"` | If the group votes a different weekend |

## Things to add later (when ready)

- **Real Lake Morey hero photos** — the current hero uses a CSS gradient + SVG pattern. When Lake Morey grants image permission (we asked in the outreach), drop their photos in. Suggested: add an `assets/` folder and reference local files. Use a `<picture>` element with the gradient as a fallback.
- **Open Graph image** — once you have a hero photo, add `<meta property="og:image" content="...">` so the link previews nicely when shared.
- **Live donation page** — when MFNE confirms a campaign page or P2P fundraising URL, link the charity tracker section directly to it.
- **Roster table** — once we have 8–10 committed, a small "who's coming" section is nice (optional — some people would rather not be listed publicly).
- **Past trip photos** — add a small gallery once permission is set.
- **Favicon** — `<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,...">` with a golf flag SVG.

## Maintaining the email CTA

The "Count Me In" button uses a `mailto:` link to `fructifyme@gmail.com` with a pre-filled subject/body. If you want to switch to:
- A different email — search for `fructifyme@gmail.com` and replace.
- A real form (Google Form, Tally, etc.) — replace the `mailto:` href with the form URL.

## Charity goal & numbers

The page currently shows:
- **$5,000 goal** — change in `.raise-goal` and the supporting copy if the group decides differently.
- **$0 raised** — update `.raise-amount` and the inline `width: 0%` on `.raise-fill` as donations roll in.

## Browser support

Modern evergreen browsers. The `backdrop-filter: blur(...)` on the nav and charity card is the only fancy thing — older browsers will just show a slightly less polished blur, which is fine.

## License / use

Private project page for the planning team. Not affiliated with Lake Morey Resort or MFNE. Mike's call on whether to publicize the URL or keep it lightly shared with the network.
