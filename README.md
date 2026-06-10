# K Audiovisual — Website

Placeholder landing page for **kaudiovisual.ca**. Plain static HTML — no build step.

---

## One-time setup: push to GitHub

Run these in the VS Code terminal **from inside this folder** (`kaudiovisual-site`).

```bash
git init
git add .
git commit -m "Hello World: K Audiovisual landing page"
git branch -M main
git remote add origin https://github.com/claude-richard-5/kaudiovisual-site.git
git push -u origin main
```

> Before the `push`, create the empty repo on GitHub: go to https://github.com/new,
> name it **kaudiovisual-site**, leave it empty (no README, no .gitignore), and create it.

---

## Connect to Cloudflare (one time)

1. Cloudflare dashboard → **Workers & Pages** → **Create application** → **Pages** tab.
2. **Import an existing Git repository** → authorize GitHub → pick **kaudiovisual-site** → **Begin setup**.
3. Build settings: **no framework**, **no build command**, output directory **`/`** (root). This is plain HTML.
4. **Save and Deploy.** Live in ~30–60s at `https://kaudiovisual-site.pages.dev`.
5. Project → **Custom domains** → **Set up a domain** → `kaudiovisual.ca`. DNS is auto-added (your domain is already on Cloudflare); HTTPS turns on automatically.

---

## The publish loop (every change after that)

```bash
# edit index.html in VS Code, then:
git add .
git commit -m "describe your change"
git push
```

Cloudflare redeploys automatically on every push to `main`. Live in about a minute.

**Try it:** open `index.html`, find the line marked `EDIT THIS LINE`, change the tagline,
then run the three commands above. Watch it go live.
