# UT Canoe & Hiking Club Website

UTCH site frontend (Vite) + Cloudflare Worker backend.

## Project Structure

- `src/`: frontend source (pages, partials, JS, CSS, assets)
- `worker/`: Cloudflare Worker API and integrations
- `.github/workflows/deploy-pages.yml`: GitHub Pages deploy workflow

## Frontend Development

Install and run:

```bash
npm ci
npm run dev
```

Create a production build:

```bash
npm run build
```

Vite outputs compiled files to `dist/`.

## Frontend Config

Edit `src/public/assets/config.js`:

```javascript
window.UTCH_CONFIG = {
  calendarEmbedUrl: "https://calendar.google.com/calendar/embed?src=...",
  calendarIcsUrl: "",
  apiBaseUrl: "https://your-worker.workers.dev"
};
```

## GitHub Pages Deployment

Deployment is handled by GitHub Actions.

1. In GitHub repo settings, go to `Settings` -> `Pages`.
2. Set `Build and deployment` source to `GitHub Actions`.
3. Push to `main` to trigger deploy.

## Backend

See `worker/README.md` for Worker setup and secrets.
