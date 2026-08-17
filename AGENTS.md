# AGENTS.md — read this before writing anything into this repository

**This repo is output, not source of truth.** The standards that govern every page here —
content rules, quality gates, voice, visual standards, research requirements — live in the
**sibling `venture-os` repo** (`../venture-os`), not in this one. A file that looks correct here
tells you nothing about whether it was allowed to be written.

Applies to every tool and session equally: Claude Code, Antigravity, Gemini, Cursor, Copilot,
any other agent, or a human. "I was only asked to write one page" is not an exemption.

## Before creating or editing any page

1. Read **`../venture-os/AGENTS.md`** in full — the canonical framework (`CLAUDE.md` and
   `GEMINI.md` there are thin pointers to it, not separate rulesets).
2. Read **`../venture-os/principles.md`** — 7 non-negotiable principles; every page must pass all 7.
3. Read **`../venture-os/ventures/homeservicesorted/`** — `config.json`, `context.md`,
   `voice-guide.md`, `visual-standards.md`, `learnings.md`.
4. Read the research file for the relevant cluster,
   **`../venture-os/ventures/homeservicesorted/research-{cluster}-cluster.md`**.

If you cannot access those files, **stop and say so.** Do not infer the standards by copying a
neighbouring page. Cloning the template correctly is the easy half; it proves nothing about
whether the content is true, needed, or non-duplicative.

## Hard requirement for any NEW page

A new `src/**/*.html` may not be committed unless the cluster research file already contains,
for that specific page:

- **the target keyword and a real demand signal** (volume or observed evidence — not "this seems
  like something people search for"), plus a SERP/competition note;
- **a source for every factual claim** on the page — every vendor capability, price, statistic,
  date and number, traced to vendor documentation, a help centre, a regulator, or a named review
  platform. A model's recollection is not a source;
- **a verification date.**

Missing or partial trail → **stop and flag it. Do not commit.**

## Site-specific basics (the full set is in venture-os)

- **US/Canadian English.** No British spellings, no "whilst", no "licences".
- USD primary, note CAD where the content targets Canadian readers.
- Every page: mobile-first at the 680px breakpoint, JSON-LD schema, footer affiliate disclosure
  referencing FTC (US) and CASL/ASC (Canada).
- Design tokens are fixed and documented in `visual-standards.md` — do not improvise colours,
  fonts, or components.
- Do not claim commission in the footer on a page that carries no vendor links.

## Why this file exists

On 2026-08-13 a page was generated into `src/hvac/` by a tool that had never read any of the
above. It cloned the template near-perfectly and read fluently — and inverted the offline
capability of all four vendors it reviewed, invented a company history and a dollar figure, and
contradicted itself twice. It had no research trail. The polish is precisely what made it
dangerous: nothing on the surface signalled that the substance was unverified.
