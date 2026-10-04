# Photos by MP

A fast, responsive gallery for my photography.

**Status:** coming soon. **Page:** https://photos.marcantoniopovolo.com

Built by [Marcantonio Povolo](https://marcantoniopovolo.com), a Computer Engineering student at Toronto Metropolitan University. I won my high school's Arts Fest photography award in Grades 10 and 11.

## Plan

1. Choose a small set of photos worth showing.
2. Design a layout that works well on phones first, then on larger screens.
3. Keep every image sharp without making the page slow, and measure load time before and after.

## Layout

| Path | What it is |
|---|---|
| `site/` | What Cloudflare serves at photos.marcantoniopovolo.com: the coming-soon page (`index.html`), the project page (`about/`), shared styles (`page.css`), icons and favicon. Built by `build_app_pages.py` in my portfolio folder. |
| `wrangler.jsonc` | Cloudflare Worker settings: serve `site/` at photos.marcantoniopovolo.com. Publish with `npx wrangler deploy`. |
