# Hugo Terminal Blog

A static blog built with [Hugo](https://gohugo.io/) using the [Terminal theme](https://github.com/panr/hugo-theme-terminal).

## Project Structure

- `content/` — Markdown content files (posts, about page)
- `themes/terminal/` — The Terminal Hugo theme (bundled)
- `archetypes/` — Hugo content templates
- `hugo.toml` — Main Hugo configuration
- `public/` — Generated static output (created on build, not committed)

## Development

The site is served by the "Start application" workflow using:

```
hugo server --bind=0.0.0.0 --port=5000 --baseURL=/ --appendPort=false
```

Hugo runs in live-reload mode, watching for changes to content and config.

## Configuration

Site settings are in `hugo.toml`:
- `title`: `rob@blog:~$`
- `theme`: `terminal`
- `params.author`: Rob
- Menu items: Home, Posts, About

## Deployment

Configured as a **static** deployment:
- Build command: `hugo --minify`
- Public directory: `public`

## Dependencies

- **Hugo** (v0.147.3 extended) — installed as a Nix system dependency
