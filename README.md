# AdmitTalk — Website

Static site for AdmitTalk, a community forum for college admissions
discussion (students, parents, and counselors). No build step, no
framework — plain HTML and CSS.

## Current state: coming-soon placeholder

`index.html` is a self-contained placeholder page (inline CSS, no JS
dependency beyond a one-line year stamp). It is up while the forum at
`forum.admittalk.com` is still being built, so visitors are not sent to
an empty forum.

It is set to `noindex`. Remove that meta tag when you want it indexed.

## Restoring the full landing page

The complete landing page — hero, topic boards, trust section, CTAs — is
preserved at the `landing-page-v1` tag:

```bash
git show landing-page-v1:index.html > index.html
```

`styles.css` and `script.js` are still in the repo and are what that page
needs; the placeholder does not use them.

Before putting it back, resolve the open items:

- The six topic boards must exist on the forum and have real threads
- Flarum's default welcome text must be replaced
- Privacy policy and terms need to exist and be linked from the footer
  (the audience includes minors)
- The "real names" identity claim and the moderation claims need to be
  true or softened
- The footer "Guidelines" link points at an on-page marketing section,
  not actual guidelines

## Files

- `index.html` — the live placeholder page
- `styles.css` — styling for the full landing page (unused by the placeholder)
- `script.js` — nav toggle and smooth scroll for the full landing page (unused by the placeholder)
- `favicon.svg` — browser tab icon

## Preview locally

Open `index.html` in a browser directly — there is nothing to serve.

## Deploy

The site is hosted on Cloudflare Pages. Confirm whether the Pages project
is connected to this repo; if it is not, pushing here does not deploy.
