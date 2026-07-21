# Donald R. Honeycutt — Personal Site

Static 4-page site: Home, Selected Projects, Publications, Resume.
No build step — open `index.html` directly, or serve the folder with any static host.

## Structure
```
index.html          Home
projects.html        Selected Projects (4 project cards)
publications.html    Full publication list
resume.html          Embedded CV
css/style.css        Design system (colors, type, layout)
js/main.js            Mobile nav toggle + card scroll-reveal
assets/resume/        Honeycutt_CV.pdf (your actual CV, already included)
assets/papers/         Drop individual paper PDFs here (see below)
```

## Action needed: paper PDFs

Two of the four project cards on `projects.html` link to DOIs (they work right now,
no action needed):
- Knowledge Graph Tools for Intelligence Analysis → doi.org/10.3390/analytics2020028
- First Impressions & Trust Calibration (IUI 2021) → doi.org/10.1145/3397481.3450639

One card points to a **local file that doesn't exist yet** — add your own copy of the
paper here:
```
assets/papers/roy-et-al-2021-explainable-activity-recognition.pdf
```
(Applied AI Letters usually allows authors to self-host an accepted manuscript —
check the journal's self-archiving policy before uploading the publisher's PDF.)

The fourth card ("Counterfactual RLHF for Interactive Fairness Correction") is
intentionally unlinked with a "Paper Coming Soon" badge, since that work isn't
published yet. Once it is, change the button in `projects.html` from:
```html
<span class="btn btn-ghost" aria-disabled="true">Paper Coming Soon</span>
```
to:
```html
<a class="btn btn-outline" href="assets/papers/your-file.pdf" target="_blank" rel="noopener">Read the Paper ↗</a>
```

## Updating your CV
Replace `assets/resume/Honeycutt_CV.pdf` with any new version — the filename must
stay the same, or update the two references to it in `resume.html`.

## Adding a new project card
Copy one `<article class="card">...</article>` block in `projects.html`, edit the
icon colors/positions in the inline SVG if you want a unique mark, and update the
status badge class:
- `status-published` (green) — published paper
- `status-award` (amber) — published + won an award
- `status-progress` (grey) — working paper / dissertation chapter

## Hosting
This is a fully static site — works with GitHub Pages, Netlify, Vercel, or any
basic web host. Just upload the whole folder.
