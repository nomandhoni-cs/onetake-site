# OneTake — static site

Three pages, no build step, no dependencies.

- `index.html` — landing page
- `privacy.html` — Privacy Policy  (served at `/privacy`)
- `terms.html` — Terms of Service  (served at `/terms`)
- `_headers` — basic security headers for Cloudflare Pages
- `robots.txt`

## Deploy to Cloudflare Pages

**Option A — drag & drop**
1. Cloudflare dashboard → Workers & Pages → Create → Pages → Upload assets.
2. Drop this whole folder in, name the project, Deploy.

**Option B — Git**
1. Push this folder to a GitHub/GitLab repo.
2. Pages → Connect to Git → pick the repo.
3. Framework preset: **None**. Build command: *(leave empty)*. Output directory: `/`.

Cloudflare Pages automatically serves `privacy.html` at `/privacy` and
`terms.html` at `/terms`, so the nav links work as-is.

**Option C — Wrangler CLI**
```
npx wrangler pages deploy . --project-name=onetake
```

## Customising
Colours live in the `:root` block at the top of each file:
`--accent: #195636`. Headings use Playfair Display (Google Fonts),
body text uses the system UI font.
