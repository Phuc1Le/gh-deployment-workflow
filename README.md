# Le Hong Phuc — Portfolio Site

A single-page portfolio built with plain HTML, CSS, and vanilla JavaScript —
no build step, no framework, no dependencies beyond two Google Fonts. This
keeps it fast and trivial to deploy on GitHub Pages.

## Files

```
index.html        All content and page structure
css/style.css      All styling (design tokens live at the top of the file)
js/main.js         Mobile nav toggle, scroll-reveal, active nav link
images/            picture1.jpg (profile), picture2.jpg (awards),
                   picture3.jpg (hobbies), favicon.svg
resume.pdf         Current downloadable resume
```

## Content status

The portfolio has been updated from the supplied October 2026 resume, including
HeLab research, the completed VecML internship, projects, technical training,
leadership, education, and technical skills. Profile and project links use the
URLs embedded in the resume. The Resume button opens the included `resume.pdf`.

Photos and personal hobby text are retained from the existing website. Replace
the images if needed. Future resume updates should also replace `resume.pdf`.

## Deploying to GitHub Pages

1. Create a new GitHub repository (or use an existing one).
2. Push these files to the repository root (or to a `/docs` folder — either
   works, you'll just set the source accordingly).
3. In the repo, go to **Settings → Pages**.
4. Under **Source**, choose the branch (usually `main`) and the folder
   (`/root` or `/docs`).
5. Save. GitHub will publish the site at
   `https://<your-username>.github.io/<repo-name>/` within a minute or two.

No build tools, no `npm install` — it's static files GitHub Pages serves
directly.

## Editing content later

Everything is in `index.html`, organized top to bottom in the same order as
the page: Hero, About, Experience, Projects, Skills, Technical Training, Leadership, Awards,
Hobbies, Education, Contact. Each section is clearly commented
(`<!-- ================= PROJECTS ================= -->` etc.) so you can
jump to the right spot and edit text directly — there's no data file or
templating layer to worry about.

To add a new project card, copy an existing `<article class="project-card">`
block in the Projects section and edit its contents. To add a new timeline
entry, copy a `<div class="timeline-item">` block in the Experience section.

## Design notes

- Colors, fonts, spacing, and corner radii are all defined as CSS custom
  properties at the top of `css/style.css` — change a value there and it
  updates everywhere.
- The monospace font (JetBrains Mono) is used deliberately for dates,
  section eyebrows, and tags — a small nod to engineering/documentation
  aesthetics that ties back to the "I care about engineering quality"
  goal, rather than a generic all-Inter treatment.
- Motion is intentionally restrained: a short fade/rise on scroll, subtle
  hover lifts on cards and buttons, and nothing else. Reduced-motion
  preferences are respected automatically.
