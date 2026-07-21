# Session Summary — Schedule Library & Survey in a Box

<!--
NOTES (keep at top; update with each change and date it):
- 2026-07-20 — Created. Running summary of the work completed in this chat:
  the standardized schedule families, the Master Library, the catalog data
  format, the interactive Schedule Catalog prototype, and the 10-Hour family.
-->

**Date:** 2026-07-20
**Scope:** Standardizing Shiftwork Solutions' schedule patterns into a consistent premium format, assembling them into a master library, and building the data + interactive catalog for the Survey in a Box product.

## What we built

### 1. Standardized schedule families (premium card format)

Every schedule pattern was rebuilt in one consistent, modern card format (Space Grotesk / JetBrains Mono / Inter; gold = day, navy = night, slate = generic, red dividers between crews). Each family holds its basic pattern plus rotating, fixed, and modified variants where they apply. Coverage math was verified programmatically for every multi-crew schedule (exactly one day crew and one night crew present each day), and weekly hours were checked for balance.

Families completed this session and added to the collection:

- **4-3** — basic, fixed (4 crews), rotating (4 crews).
- **3-on / 3-off** — basic, rapid rotation, fixed 24/7.
- **3-on / 3-off Modified** — clean full-weekend version (basic + fixed).
- **4-on / 4-off** — basic, rapid rotation, medium rotation, fixed 24/7.
- **4-on / 4-off Modified** — clean-weekend version (four weekends off, then four worked).
- **10-Hour** — basic 4×10 (Mon–Thu), two-crew stagger, and five-sub-crew rotation.

These joined the earlier families already in the repo: **5-Day / 24-5, 2-2-3, 5 and 2, Six-Day Coverage,** and the **DuPont** reference card.

### 2. Master Schedule Library (one file)

All standardized families were combined into a single self-contained **Master Schedule Library.html** — a cover page, a clickable table of contents, and every family embedded as its own isolated section so each keeps its exact styling. Currently **11 families**, covering 8-, 10-, and 12-hour patterns. Nothing from the older 40-schedule Word catalog was mixed in.

### 3. Schedule data format

We designed the standard data block that accompanies each schedule: a **Key Statistics** panel (scheduled work days/year, days off/year, average hours/week, full and half weekends off/year, most and fewest days of work in a row), a **Key Feature** write-up, and a two-part **How It Works** (where the crews go, then a week-by-week walk-through for one crew). All figures use the 364-day / 52-week basis and are computed from the actual pattern.

### 4. Interactive Schedule Catalog (prototype)

A working prototype of the browsable, ratable catalog for Survey in a Box: a table of contents (family → schedule), an in-page detail overlay showing the schedule picture, its statistics, key feature, and how-it-works, plus a 1–5 star rating and Back / Next navigation. Two families (4-3 and 3-on/3-off, six schedules) are fully wired as a data-driven sample; the architecture is built so the remaining families drop in as data records.

## Repository contents (D:\Survey and Schedules Temp Repo)

Family cards: 5-Day and 24-5, 10-Hour, 2-2-3, 5 and 2, 4-3, Six-Day Coverage, 3-on/3-off, 3-on/3-off Modified, 4-on/4-off, 4-on/4-off Modified, DuPont. Plus the **Master Schedule Library**, the earlier **Master Schedule Catalog** (40-schedule Word archive), and the **Survey in a Box** app.

## Decisions and conventions established

- Everything traces to real dictated patterns — nothing invented.
- 24/7 patterns drawn Sunday-start; weekday patterns (Six-Day, 10-Hour) Monday-start.
- "Modified" = relocate one Saturday shift to guarantee whole weekends.
- Statistics computed per individual worker on the 364/52 basis; most/fewest runs shown as separate tiles labeled "days of work in a row."
- Catalog detail view is an in-page overlay (not a separate window) so survey state is preserved.

## Open / next steps

1. Generate the full catalog data (stats + key feature + how-it-works) for **every** schedule and variant, including the new 10-Hour three.
2. Wire the catalog into the Survey in a Box flow so a pre-picked schedule opens the detail view, captures the rating, and returns.
3. Decide whether to retire the older 40-schedule Word catalog now that the Master Library supersedes it.

---

*Shiftwork Solutions · Survey in a Box + Schedule Library.*

I did no harm and this file is not truncated.
