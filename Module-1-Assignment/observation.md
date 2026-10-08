# Observation — FDE Landing Page (Module 1)

Task: build a single landing page for an FDE (Forward Deployed Engineer) service.
Both outputs were viewed in the browser at desktop width (1568px) and their source code was reviewed.

---

## Model 1 — Claude Opus 5.5 (auto mode)

**Process**
- Asked me no clarifying questions. It just built the page.

**Output** — brand name "Fieldwork"
- Hero: "We send engineers to sit next to your problem." The headline, the subtext and both CTAs (*Book a scoping call*, *See how an engagement runs*) all fit in the first screen.
- Hero visual: a "deployment log" card (Day 01 → Day 17) that tells the FDE story from pilot to production.
- Sections: Why → How it works → Capabilities → Field reports (case studies) → Engagements (pricing, e.g. "Embedded pod, from $65k / month") → FAQ → Contact.
- Visual style: warm off-white background with topographic lines, dark green, and yellow accents. It's consistent and looks like a real agency site.
- The data is dummy (made-up company, prices, and metrics).

**Code**
- One file, `index.html`, **657 lines**. CSS, HTML and JS are all in the same file.
- No frameworks. Plain HTML, CSS and JS. The only external resource is Google Fonts.
- Responsive: 3 breakpoints (960 / 720 / 420px) plus `prefers-reduced-motion`.
- Accessibility: every section has `aria-labelledby`, and the FAQ uses native `<details>` (6 items).

**Verdict:** Excellent and professional.

---

## Model 2 — Grok 4.5 Medium (free)

Prompt: *"Create a single-landing page website for an FDE (Forward Deployed Engineer) Service"*

**Process**
- Asked for permission before acting.

**Output** — brand name "Nearfield"
- Hero: "The system ships when you're close enough to feel it fail." At desktop width the headline wraps to about 8 lines, which pushes the subtext and CTA below the first screen.
- Hero visual: a "Proximity" widget with two circles ("Your floor" / "FDE desk") and a distance slider. It's creative, but less clear than Claude's deployment log.
- Sections: Problem → Work → Method ("Four beats") → Compare ("Not a consultancy. Not staff aug.") → People → CTA ("Request a scout week").
- Visual style: dark navy with pink/magenta accents.
- It has no pricing section and no FAQ, so it's thinner on content than Claude's page.

**Code**
- One file, `index.html`, **614 lines**. CSS, HTML and JS are all in the same file.
- No frameworks. Plain HTML, CSS and JS. The only external resource is Google Fonts.
- Responsive: 2 breakpoints (900 / 620px) plus `prefers-reduced-motion`.
- Some inline styles (`style="padding-top: 0;"` on sections), and no `aria-labelledby` on sections.

**Verdict:** It works, but it doesn't look as good as Opus.

---

## Side-by-side

| | Claude Opus 5.5 | Grok 4.5 Medium |
|---|---|---|
| Asked questions / permission | No questions (auto mode) | Asked permission |
| File split | Single file | Single file |
| Lines of code | 657 | 614 |
| Framework | None | None |
| Responsive breakpoints | 3 | 2 |
| Pricing / FAQ | Yes / Yes | No / No |
| Hero fits first screen | Yes | No (headline too tall) |
| Data | Dummy | Dummy |
| Overall look | Excellent, professional | Decent, weaker than Opus |

**Common to both:** single-file output, no framework, dummy content, Google Fonts only, a mono "technical" accent font (IBM Plex Mono), and support for reduced motion.
