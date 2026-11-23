# IntentDockWelcom

The "under construction" welcome page for [intentdock.io](https://intentdock.io).

It's a static site with no build step and no dependencies. The site files are in `public/`, and it's deployed as a Cloudflare Worker with static assets, configured in `wrangler.jsonc`.

```
├── wrangler.jsonc
└── public/
    └── index.html
```

## Deploying with Cloudflare Workers

1. In the Cloudflare dashboard, go to **Workers & Pages → Create → Import a repository** and pick this repo.
2. Build settings: leave **Build command** empty, and set **Deploy command** to `npx wrangler deploy`.
3. Click **Deploy**. The site goes live at `intentdock-welcome.<account>.workers.dev`.
4. Connect the domain: in the Worker, go to **Settings → Domains & Routes → Add → Custom domain**, then add `intentdock.io` and, optionally, `www.intentdock.io`.

Every push to `main` redeploys the site automatically.
