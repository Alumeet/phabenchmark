# PHA Benchmark - Admin guide

How the directory's data flows, and how to operate it safely.

## Architecture

| Piece | What it is | Who can see it |
| --- | --- | --- |
| Public sheet "PHA Benchmark - Directory data" | Google Sheet shared **anyone with the link can view**. The live site reads it directly (gviz JSON). | **The world.** Everything in every tab is public, including "hidden" tabs. |
| Tab `agents` | The directory listings shown on the site. | Public. |
| Tab `reviews_published` | Approved community reviews, copied here field by field after moderation (see below). | Public. |
| Review intake form ("Review a personal health agent") | Google Form. Responses go only to the form's response list. | **Private.** Only you (form owner). Never link to the Responses page or its response sheet from the site. |
| Maker submission form | The original "list your agent" form. | Private responses; only the public form link is shared. |

## The one rule that matters

**Anything you type into the public sheet is world-readable the moment you type it.**
Hidden tabs are not private. Formatting tricks are not private. The sheet is the publication boundary: only content that is ready to be on the public website belongs in it.

Never put in the public sheet:
- pending or unmoderated reviews
- reviewer contact emails or any personal data
- admin notes, flags, or internal comments

## Editing listings

1. Open the sheet, tab `agents`.
2. Edit rows directly; each row is one card. Keep `addedBy` and the "not independently tested" wording intact. Listed never means tested.
3. The site picks up changes within about 5 minutes (Google's gviz cache). Hard-refresh to check.

## Moderating community reviews

Reviews arrive in the **review form's Responses tab** (Google Forms UI). Each respondent affirmed: their review, rating and chosen display name may be published after moderation, and that their email (if given) stays private and is never published.

To publish a review:

1. Read it in the form Responses. Reject spam, abuse, or anything you don't want on the site. Delete junk responses from the form.
2. In the public sheet, tab `reviews_published`, add one row with **exactly these columns and nothing else**:
   - `agent` - the listed agent's name, spelled exactly as on its card
   - `rating` - the star rating (1-5)
   - `review` - the review text
   - `display_name` - the name/handle the reviewer chose, or `Anonymous` if blank
   - `submitted` - date the review was submitted
   - `published` - date you published it
3. **Never copy the email column into the sheet.** The public projection has no email column on purpose.
4. The review appears on the agent's card under "Community reviews", labeled as individual experiences, not tests or benchmark results.

Until you set a firm moderation policy, leaving reviews unpublished in the form is the safe default.

## Methodology

`REVIEWING.md` (and the site's How we review page) documents the review model and the draft structured-review rubric. The rubric is a draft, not a validated benchmark; keep that wording when you talk about it.
