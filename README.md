# IntentDockWelcom

The "under construction" welcome page for [intentdock.io](https://intentdock.io).

It's one static `index.html` file with no build step and no dependencies.

## Deploying with Cloudflare Pages

1. In the Cloudflare dashboard, go to **Workers & Pages → Create → Pages → Connect to Git**.
2. Choose this repository.
3. Build settings: set **Framework preset** to *None*, leave **Build command** empty, and set **Build output directory** to `/`.
4. Deploy. Then go to **Custom domains** and add `intentdock.io` (and `www.intentdock.io` if you want it).

Every push to `main` redeploys the site automatically.
