# Interview Prep — Hong Kong Financial Services

One site, one GitHub Pages link, everything reachable from a single home page.

## Structure

- `index.html` — the hub. Lists everything below as cards. **This is what loads at your root URL.**
- `insurance.html` — Insurance industry landscape (reusable across any insurance interview)
- `bank.html` — Banking industry landscape (reusable across any banking interview)
- `role-aia-manager-innovation-change.html` — role-specific prep for AIA, Manager Innovation Change Management

Two categories, on purpose:
- **Industry landscapes** (`insurance.html`, `bank.html`) share one neutral design system and a pill-switcher at the top of each ("← All prep · Insurance · Banking") since they're reused across many interviews in that sector. When you learn something new about an industry, these get updated in place rather than duplicated.
- **Role-specific prep** (`role-*.html`) is one page per job application, each free to keep its own look (the AIA page uses AIA's own red/gold branding, for instance) since it's a one-off built for that specific interview. Each just gets a small "← All prep" breadcrumb link added at the top so you can always get back to the hub.

## Publish on GitHub Pages

1. Create a new GitHub repo (public, so Pages is free).
2. Upload all files in this folder to the repo root.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main, folder: / (root) → Save**.
4. You get a URL like `https://<your-username>.github.io/<repo-name>/` within a minute or two — that's your hub page.

## Adding a new role-specific prep page later

When you have a new job application and get a prep page built (in a new Claude chat, or this one):

1. Save the new page as `role-<company>-<short-title>.html` (e.g. `role-manulife-product-manager.html`) — keeps them sorted together and easy to spot in the file list.
2. Add a small "← All prep" breadcrumb link near the top of that page, in whatever style matches its own design (ask Claude to do this — it's a two-line change).
3. Add one card to `index.html`'s "Role-specific prep" section, linking to the new file — ask Claude to do this too, and it'll just be a copy-paste-edit of the existing AIA card.
4. Upload/push both the new file and the updated `index.html`.

No need to touch `insurance.html` or `bank.html` when adding a role-specific page — they're independent.
