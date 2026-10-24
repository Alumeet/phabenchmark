# PHA Benchmark

A public directory of personal health agents — agents that coach, triage, and make
sense of personal health data. Anyone can list theirs. Listed never means tested.

This repository holds the site source: a static, single-file page (`index.html`).
No build step, no dependencies, no backend.

## Status

- The site is **live** at https://alumeet.github.io/phabenchmark/ (GitHub Pages,
  no custom domain). phabenchmark.com only *appeared* unregistered (RDAP 404 /
  NXDOMAIN) at check time on 2026-10-24; buying a domain is still the
  operator's call.
- **Submissions are open** through a Google Form whose responses are visible only
  to the operator (a private review queue). Nothing is published automatically;
  a person reviews every listing. The submitter's contact email is used only to
  reply about the listing and is never published.
  Submit here: https://forms.gle/fmSvj6DW53ssBnKo8
- Seed entries are editorial (added from public sources) and labeled as such per
  card. The Vital OS entry is an illustrative example of a listing, flagged on the
  card and in the footer, because the operator is its maker.
- Everything on the page that reads as policy (benchmark ground rules, review
  process) is the operator's draft proposal, and the page says so.

## Intake configuration

The submission section is driven by `SUBMISSIONS` at the top of the inline script:

    const SUBMISSIONS = { mode: "google-form", url: "https://forms.gle/fmSvj6DW53ssBnKo8" };

- `mode: "google-form"` (current) — private queue, no Google sign-in required to
  submit, public response summary disabled.
- `mode: "github"` — requests as issues via `.github/ISSUE_TEMPLATE/listing.yml`.
  Issues on a public repo are public, so the template deliberately has no
  contact-email field and warns submitters not to include private details; the
  issue thread is the reply channel. Submitters need a GitHub account.
- `mode: "preview"` — disabled, non-submitting on-page demo.

## Still the operator's calls

- Buying a domain and pointing it at the site.
- Moderation owner and the bar for accepting a listing.
- A fuller privacy note (the form currently states its minimal stance: the
  contact email is used only to reply about the listing).
- Publish the benchmark protocol before any benchmark results.
