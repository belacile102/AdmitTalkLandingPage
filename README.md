# AdmitTalk — Landing Page

A static, single-purpose landing page for AdmitTalk, a community forum for
college admissions discussion (students, parents, and counselors). No
build step, no framework — plain HTML, CSS, and JS.

## Files

- `index.html` — page content and structure
- `styles.css` — all styling (light + dark mode via `prefers-color-scheme`)
- `script.js` — mobile nav toggle, smooth-scroll, footer year (progressive enhancement only)
- `favicon.svg` — browser tab icon

Every "Join the forum" button links to `https://forum.admittalk.com`. Update
that URL in `index.html` (four places) if the forum address changes.

## Preview locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy to Cloudflare Pages

**Option A — dashboard, no git:**
1. Cloudflare dashboard → Workers & Pages → Create → Pages → Upload assets.
2. Drag in this folder's contents (or a zip of them).
3. Deploy — Cloudflare gives you a `*.pages.dev` URL immediately.
4. Add your custom domain (e.g. `admittalk.com` or `www.admittalk.com`)
   under the project's Custom domains tab.

**Option B — connect a git repo:**
1. Push this folder to a GitHub/GitLab repo.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git.
3. Build settings: no framework preset, build command empty, output
   directory `/` (root).
4. Deploy. Every push to the connected branch redeploys automatically.

**Option C — Wrangler CLI:**
```bash
npx wrangler pages deploy . --project-name=admittalk-web
```

No environment variables, redirects, or server-side code are required.
