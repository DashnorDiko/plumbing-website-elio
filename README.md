# Local Plumber (plumbing-website-elio)

Mobile-first UK plumber call site. Visitors tap **Call** or **WhatsApp**. We send a plumber to their location.

Contact number: **07806 950180** (`+44 7806 950180`).

## Edit later

In [`index.html`](index.html):

- Business name (title, header, footer) — currently **Local Plumber**
- Hours copy in the hero
- Towns and postcodes in the **Towns and postcodes we cover** section (placeholders until you type the real list)

## Run locally

Open `index.html` in a browser, or from this folder:

```bash
npx wrangler dev
```

Then visit the URL Wrangler prints (usually `http://127.0.0.1:8787`).

## Put it on GitHub

If the repo is not on GitHub yet:

```bash
gh repo create plumbing-website-elio --public --source=. --remote=origin --push
```

Or create an empty repo on GitHub named `plumbing-website-elio`, then:

```bash
git remote add origin https://github.com/YOUR_USER/plumbing-website-elio.git
git push -u origin main
```

## Cloudflare Pages (GitHub)

1. Log in at [Cloudflare Dashboard](https://dash.cloudflare.com/).
2. **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Authorise GitHub and pick **plumbing-website-elio**.
4. Build settings:
   - Framework preset: **None**
   - Build command: leave empty
   - Build output directory: `/`
5. Save and deploy.

After the first deploy, every push to `main` updates the live site.

Optional: attach a custom domain under the project’s **Custom domains** tab.

## Deploy with Wrangler instead

```bash
npx wrangler login
npx wrangler deploy
```

This publishes the same static files as a Worker with assets. Git-connected Pages is the usual GitHub workflow.
