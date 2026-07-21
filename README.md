<!--
  README.md — Survey in a Box repository
  Shiftwork Solutions LLC

  NOTES (keep at top; update + date with each change):
    2026-07-21 — Created. Repo index + deploy notes. Describes which files are
                 the deployed site vs. reference material, records the correct
                 (hyphenated) filenames, the correct contact details, and the
                 GitHub -> Render deploy path. Descriptions for files not yet
                 opened in-session are based on their filenames — refine as
                 needed. House rule: use "Hundreds", never a number.
-->

# Survey in a Box

**Survey in a Box** is the employee-survey product from **Shiftwork Solutions LLC** — a professionally designed workforce survey for 24/7 operations that benchmarks every answer against Hundreds of facility surveys and returns a decision-ready report (build → approve → administer → analyze → export).

## Status (as of 2026-07-21)

The **front end is complete and polished**, and both the app and the landing page have been reskinned to match the shift-work.com website scheme (navy `#1F4E79`, orange `#E8610A`, gold, navy-dark footer with correct contact info).

What is **not built yet** is the server side: real persistence, real company accounts, live number-gated employee survey links, real (non-simulated) responses, and a real partner approval step. Today the app runs entirely in the browser and simulates data — a working prototype, not yet operational. See the project roadmap for the full remaining-work list.

## The deployed site

These two files ARE the live product. Everything else in the repo is reference or working material.

| File | Role |
|------|------|
| `survey-landing.html` | Public landing / marketing page. The entry point; its **Sign in** links point to `survey-in-a-box.html`. |
| `survey-in-a-box.html` | The application itself — company sign-in, survey builder, administer, analyze, and PowerPoint export. A single self-contained file (the PptxGenJS library and all schedule-pattern data are embedded inside it). |

> **Filename matters.** The app file is `survey-in-a-box.html` (hyphenated). The landing page links to that exact name — keep it. Do not add a copy named `surveyinabox.html`; that name is linked to nothing and only causes confusion.

## Reference material (standalone; NOT required for the app to run)

The app already has all its schedule data embedded, so these are viewable reference pages, not dependencies of the live product.

| File | Role |
|------|------|
| `Master Schedule Library.html` | Master reference of every schedule family in one page (each family rendered in an embedded frame). |
| `Schedule Catalog (Interactive).html` | Interactive catalog of the schedule families / schedules. Intended to wire into the survey flow in a later phase. |
| `4-on 4-off Schedule Family.html` | Standalone card — 4-on/4-off family. |
| `4-on 4-off Modified Schedule Family.html` | Standalone card — 4-on/4-off modified. |
| `3-on 3-off Schedule Family.html` | Standalone card — 3-on/3-off family. |
| `3-on 3-off Modified Schedule Family.html` | Standalone card — 3-on/3-off modified. |
| `2-2-3 Schedule Family.html` | Standalone card — 2-2-3 family. |
| `4-3 Schedule Family.html` | Standalone card — 4-3 family. |
| `5 and 2 Schedule Family.html` | Standalone card — 5 & 2 family. |
| `5-Day and 24-5 Schedule Family.html` | Standalone card — 5-Day & 24/5 family. |
| `Six-Day Coverage Family.html` | Standalone card — six-day coverage family. |
| `10-Hour Schedule Family.html` | Standalone card — 10-hour family. |
| `DuPont Schedule Format.html` | Standalone card — DuPont 4-crew rotation. |

## Working documents (not part of the deployed site)

| File | Role |
|------|------|
| `Session Summary 2026-07-20.md` | Working session notes. |
| `MyTutor.md` | Project working note. |
| `Master Schedule Catalog.docx` | Legacy Word catalog. Superseded by `Master Schedule Library.html`; candidate to retire. |

## Deploying

The site is plain static HTML — no build step, no server needed for the current front end.

1. Keep this repo on GitHub as the single source of truth. Save the complete files delivered in chat to your drive, then in GitHub use **Add file → Upload files** to add or replace them (a file upload, not copy-paste).
2. On **Render**, connect this repo as a **Static Site**. No build command is needed; the publish directory is the repo root (where the `.html` files live).
3. Every commit to the repo triggers a redeploy on Render.
4. Link the landing page from the shift-work.com **Resources** section (alongside Thomas AI) once it's live.

When the backend (real database + accounts + live employee links) is built, it will be added as a separate Render **Web Service** plus a managed **Postgres** database, and the front end will point at it.

## House details

- Company: **Shiftwork Solutions LLC**
- Phone: **(415) 265-1621**
- Email: **Contact@shift-work.com**
- Web: **shift-work.com**
- Experience is described as "**Hundreds**" of facilities — never a specific number.

---

I did no harm and this file is not truncated.
