# Xi Lambda Brotherhood Survey

A chapter-wide survey for **Xi Lambda Chapter of Alpha Phi Alpha Fraternity, Inc.** (Chicago, IL). It captures brother sentiment, skills, interests, professional background, and committee commitments for the Membership Committee.

## How it works

- `index.html` is a self-contained web page (React loaded from a CDN) published with **GitHub Pages** — no build step and no server to maintain.
- When a brother submits, the responses are sent to a **Google Apps Script** web app, which appends a row to the chapter's **Google Sheet**.

## The live survey

The survey is published via GitHub Pages. To find or re-enable the link: **Settings → Pages**, with the source set to *Deploy from a branch → main → / (root)*. The public link appears at the top of that page and is the address you share with the brotherhood.

## Where responses go

Submissions are recorded in the chapter's Google Sheet through the collector at the `SURVEY_ENDPOINT` near the top of `index.html`. Each question becomes its own column, committee selections are stored together in one cell, and any "Other — please specify" text is saved to its own `_other` column.

## Updating the survey

1. Update the survey and regenerate `index.html`.
2. In this repo, use **Add file → Upload files** to replace `index.html` — keep the name exactly `index.html`.
3. Commit. GitHub Pages redeploys automatically in about a minute.

## Maintainer notes

- The file served by GitHub Pages **must** be named exactly `index.html` and sit at the top level of the repo. If it's named anything else, Pages shows this README instead.
- To change where responses land, redeploy the Apps Script and paste its new `/exec` URL into `SURVEY_ENDPOINT` in `index.html`.

---

*Alpha Phi Alpha Fraternity, Inc. · Xi Lambda Chapter · Chicago, IL · Est. 1924*
