# AdmitTalk — Website

Static site for AdmitTalk, a community forum for college admissions
discussion (students, parents, and counselors). No build step, no
framework — plain HTML and CSS.

## Current state: full landing page

`public/index.html` is the full landing page — hero, topic boards, trust
section, and CTAs — styled by `public/styles.css` with `public/script.js`
for the mobile nav. It is indexable.

The coming-soon placeholder it replaced is in history at commit `13d1850`
if it is ever needed again:

```bash
git show 13d1850:index.html > public/index.html
```

Note: the `landing-page-v1` tag this README used to reference never existed.
The pre-placeholder landing page is at commit `4dde969`.

## Open items

The topic boards on the page were matched to the boards that actually exist
on `forum.admittalk.com`. If you add or rename a board there, update the
`.topic-grid` list in `public/index.html` to match.

Still outstanding:

- **Privacy policy and terms do not exist and are not linked from the
  footer.** The audience includes minors, so this is the significant one —
  it also backs the "nothing sold to advertisers" claim in the trust
  section.
- The trust section previously claimed accounts were "tied to a real
  identity behind the scenes" and that every board had moderators plus
  volunteer counselors. Both were removed or softened because they could
  not be verified. If they become true, the wording can be restored from
  commit `4dde969`.

## Files

- `public/` — everything that gets deployed; set this as the Cloudflare Pages output directory
- `public/index.html` — the live placeholder page
- `public/styles.css` — styling for the full landing page (unused by the placeholder)
- `public/script.js` — nav toggle and smooth scroll for the full landing page (unused by the placeholder)
- `public/favicon.svg` — browser tab icon

## Preview locally

Open `public/index.html` in a browser directly — there is nothing to serve.

## Deploy

The site is hosted on Cloudflare Pages. Confirm whether the Pages project
is connected to this repo; if it is not, pushing here does not deploy.

Only the contents of `public/` are published. This README stays out of the
deployed site — set the Pages output directory to `public`, not the repo root.
