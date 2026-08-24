<div align="center">

# gautam.raj — portfolio

*A single-page developer portfolio, designed and coded from scratch — no template.*

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](#)

**[🌍 Live Site](https://gautamraj1234.github.io/portfolio/)**

</div>

---

## What this is

A static, single-page portfolio site. No framework, no build step — just
semantic HTML, hand-written CSS, and vanilla JS for interactivity. It's meant
to load instantly, work with JavaScript disabled (content is visible by
default; JS only adds scroll-reveal as an enhancement), and hold up on a
phone as well as a desktop.

## Design

The visual identity is built around one idea: I don't just build projects, I
**ship and run them in production** — and fix what breaks. The signature
element is a live status strip in the hero showing real project URLs with
status indicators (`● live` / `● building`), styled the way a real deploy
dashboard would show it — not a decorative stat counter.

| Token | Choice |
|---|---|
| Palette | Ink-charcoal background, amber (`#E8A54B`) primary accent, signal-green (`#4FD1AE`) reserved specifically for "live" status |
| Type | [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (display) + [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) (body) + [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (metadata — dates, tech stacks, status labels) |
| Structure | Section eyebrows styled as directory paths (`~/about`, `~/projects`) instead of decorative icons |
| Motion | Scroll-reveal via `IntersectionObserver`, respects `prefers-reduced-motion`, one restrained blinking-cursor accent in the hero |

## Sections

- **Hero** — headline, live project status strip, résumé download
- **About** — who I am, in four quick facts
- **Skills** — grouped by category (languages, AI/ML, backend, frontend, data, DevOps)
- **Experience** — internship timeline
- **Projects** — SmartHire (flagship), PlantSathi AI, AI Resume Screening System
- **Credentials** — education + certifications
- **Contact** — email, GitHub, LinkedIn

## Project structure

```
portfolio/
├── index.html
├── style.css
├── script.js
├── Gautam_Raj_Resume.pdf   # linked from the hero + nav "résumé" buttons
└── .gitignore
```

## Running locally

No build step — just open it:

```bash
git clone https://github.com/GautamRaj1234/portfolio.git
cd portfolio
open index.html          # macOS
# or: python3 -m http.server 8000   →  http://localhost:8000
```

## Deployment

Hosted on **GitHub Pages**, served directly from `main`:

1. Repo → **Settings** → **Pages**
2. Source: **Deploy from a branch** → Branch: `main`, folder: `/ (root)`
3. Live at `https://gautamraj1234.github.io/portfolio/` within about a minute of any push to `main`

## Updating content

Everything is plain HTML — no CMS, no data file. To update:
- **Projects** — edit the `<article class="project-card">` / `.project-flagship` blocks in `index.html`
- **Skills** — edit the `.skill-chips` lists
- **Status strip** — edit `.status-row` blocks; swap `dot-live`/`dot-build` and `tag-live`/`tag-build` classes to reflect a project's real deployment status
- **Résumé** — replace `Gautam_Raj_Resume.pdf` with an updated export, keeping the same filename

## Accessibility notes

- Content is visible by default; `.reveal` animations are a progressive
  enhancement, not a requirement for content to appear
- `prefers-reduced-motion` disables all transitions and the blinking cursor
- No focus outlines are suppressed — keyboard navigation keeps the browser's
  default focus rings throughout

## License

Personal portfolio — feel free to use the structure/code as a reference, but
please don't republish the content (copy, projects, résumé) as your own.
