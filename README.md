# Photos by MP

A fast, responsive home for my photography. I won my high school's Arts Fest photography award in Grades 10 and 11, and this is where that work will live.

**Status:** coming soon at https://photos.marcantoniopovolo.com · [About the project](https://marcantoniopovolo.com/projects/photos.html) · Open source (MIT)

Built by [Marcantonio Povolo](https://marcantoniopovolo.com), a Computer Engineering student at Toronto Metropolitan University. I decide what it does and review and test each change; AI coding tools help write the code.

## How I'm building it

1. Choose a small set of photos worth showing.
2. Design a layout that works on phones first, then larger screens.
3. Keep every image sharp but fast, with location data removed.

## Layout

| Path | What it is |
|---|---|
| `site/` | The website at photos.marcantoniopovolo.com: the coming-soon page (`index.html`, `style.css`), icons and favicons. `about/` and `_redirects` send the old project page to [marcantoniopovolo.com/projects/photos.html](https://marcantoniopovolo.com/projects/photos.html) |
| `worker.js` | The API: anything under `/api/` (for now `/api/status`). Everything else is served from `site/` |
| `wrangler.jsonc` | Cloudflare settings: `site/` plus `worker.js` at photos.marcantoniopovolo.com |
| `LICENSE` | MIT: free to use, change and share |
| `AGENTS.md` | Rules for AI coding tools working in this repo |

## Publishing

Pushing to GitHub saves the code. To put `site/` online at photos.marcantoniopovolo.com, run this in the repo folder:

```
npx wrangler deploy
```

## API

The app and its API share one address. The website is served from `site/`; requests under `/api/` go to `worker.js`. While the app is coming soon there is one endpoint:

```
curl https://photos.marcantoniopovolo.com/api/status
```

## Open source

This project is open source under the [MIT License](LICENSE). Fork it, change it and make your own version; just keep the license notice. Issues and pull requests are welcome.
