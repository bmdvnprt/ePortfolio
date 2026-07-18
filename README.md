# Brandon Davenport — Capstone Technical Writing ePortfolio

A hand-coded, multi-page static website built for the College Capstone Technical
Writing ePortfolio assignment. No frameworks, no build step — just HTML, CSS, and
a small amount of vanilla JavaScript, ready to host free on **GitHub Pages**.

**Live site:** _add your GitHub Pages URL here after deploying_ →
`https://<your-username>.github.io/eportfolio/`

---

## Pages (labeled tabs)

| Tab | File | Purpose |
| --- | --- | --- |
| Home | `index.html` | Introduction, brand statement, quick facts, audio tour |
| About | `about.html` | Professional biography, values, personality photo |
| Résumé | `resume.html` | Experience, education **table**, skills, PDF download |
| Artifacts | `artifacts.html` | Overview linking to three artifact reflections |
| — | `artifact-tracker.html` | BARAD-DUR Tracker reflection |
| — | `artifact-pta.html` | White Sands PTA website reflection |
| — | `artifact-writing.html` | Technical writing sample reflection |
| Goals | `goals.html` | Near-term and long-term professional goals |
| Contact | `contact.html` | Contact form + direct contact links |

## Design system

- **Backgrounds:** deep navy `#0F1E33` + cream `#F7F4EE`
- **Accent:** warm gold (`#C8A24B` on dark, `#7C6124` on light for AA contrast)
- **Fonts:** Source Serif 4 (headings) + Inter (body) — two fonts only
- All colors verified for WCAG AA contrast; navigation, components, and layout are
  repeated consistently across every page (C.R.A.P. principles).

## Preview locally

```bash
cd eportfolio
python3 -m http.server 8000
# then open http://localhost:8000
```

---

## Before final submission — customization checklist

Everything below is marked in the source with `EDIT ME` comments or a visible
"Placeholder" note.

- [ ] **Photos** — replace the three placeholders in `assets/` with real images
  and update each `<img>` `alt` text:
  - `placeholder-headshot.svg` → your headshot (Home)
  - `placeholder-career.svg` → a career/school photo (available if you want it)
  - `placeholder-personality.svg` → a hobby/interest photo (About)
- [ ] **Résumé PDF** — `assets/Brandon_Davenport_Resume.pdf` is generated; update
  it if your résumé changes.
- [ ] **Contact form** — in `contact.html`, replace `REPLACE_WITH_YOUR_ID` with a
  free [Formspree](https://formspree.io) form ID so the form delivers messages.
- [ ] **Contact links** — update the email, GitHub, and LinkedIn links in
  `contact.html` (the email `hello@brandondavenport.dev` is a professional
  placeholder, which the assignment allows).
- [x] **Writing sample** — `assets/Davenport_Business_Writing_Reflection.pdf` is
  added and linked from `artifact-writing.html` (ENC 2210 business-writing reflection).
- [ ] **Audio tour** — record a 3–5 minute tour (see `AUDIO_TOUR_SCRIPT.md`),
  export it as `assets/audio/tour.mp3`; the player on the Home page is already
  wired to it.

---

## Deploy to GitHub Pages

1. Create a **public** repository on GitHub (e.g., `eportfolio`).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial ePortfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/eportfolio.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment →** Source: *Deploy from a
   branch*, Branch: `main` / `root`, then **Save**.
4. Wait ~1 minute, then visit `https://<your-username>.github.io/eportfolio/`.
5. Test the link in a private/incognito window (or send it to a friend) to confirm
   it's publicly accessible.

## Accessibility

Skip-to-content link, semantic landmarks, one `<h1>` per page with logical heading
order, descriptive `alt` text, meaningful link text, visible focus states,
`aria-current` on the active tab, and AA color contrast throughout.
