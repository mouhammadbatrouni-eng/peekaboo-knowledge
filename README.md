# Peekaboo — Client Training Site

Training material for nursery teams using the Peekaboo portal.
A static site: plain HTML plus markdown, no build step, no dependencies.

**Live portal it documents:** https://peek.peek-a-boo.app

---

## What's here

| File | Contents |
|---|---|
| `index.html` | The site — sidebar, role picker, search. The only code in the project. |
| `01-welcome.md` | What Peekaboo is, signing in, finding your way around, first 30 minutes |
| `02-role-tracks.md` | Learning tracks for all 7 roles, each with a competency checklist |
| `03-how-to.md` | 115 step-by-step tasks across 13 groups |
| `04-faq.md` | 339 questions in staff's own words |
| `05-getting-unstuck.md` | 59 entries for when something looks wrong |
| `06-module-guides.md` | All 27 areas of the portal explained |
| `07-glossary-and-statuses.md` | 124 terms, 34 statuses, quick-lookup table |
| `08-all-links.md` | Every page, one click away |

## Running it locally

No build step. Serve the folder with any static server:

```bash
python3 -m http.server 4800
```

Then open http://localhost:4800

## Deploying

Connected to Vercel — pushing to `main` deploys automatically.
`vercel.json` sets security headers and marks the site `noindex`, and
`robots.txt` keeps it out of search results. The site is still readable by
anyone with the link; add Vercel password protection if that matters.

## Editing the content

Every page is plain markdown. Edit the `.md` files directly — no rebuild
needed, the site renders them in the browser. To add a new page, add the file
and add one line to the `DOCS` array near the top of the `<script>` block in
`index.html`.

---

## House style — please keep to these

This material goes to customers, so it follows strict rules:

1. **No technical references.** No filenames, code, database fields or API details.
2. **No fault language.** Never "bug", "broken", "known issue". Where the portal
   behaves unexpectedly, the text gives calm, positive guidance on what to do instead.
3. **Only document what customers actually have.** The portal in production does
   **not** include the Forms module, and Incidents, Health (as a page), Schedule,
   Complaints, Classrooms and Early Childhood Objectives are not available. None of
   these are taught.
4. **Safety guidance is deliberate.** Daily-report health status and temperature
   selections are not retained by the form, so staff are told to record illness,
   injury or temperature in the **Note to parents** box *and* tell the room lead in
   person. Do not weaken or remove this.
5. **Write for a busy reader.** One action per step, exact on-screen labels in bold,
   no assumed knowledge, a direct link to the page wherever there is one.

## Status

Content is derived from a full read of the portal's source code. It has **not yet
been verified against the running portal** — button labels in particular should be
confirmed against a demo or staging environment before wide release.
