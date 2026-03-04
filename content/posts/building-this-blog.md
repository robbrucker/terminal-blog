---
title: "Building This Blog"
date: 2026-03-02
draft: false
tags: ["hugo", "css", "webdev"]
categories: ["technical"]
description: "How I built a terminal-themed blog with Hugo and plain CSS."
---

I wanted a blog that felt like opening a terminal window. Here's how I built it.

## The stack

The whole thing is surprisingly simple:

- **Hugo** — static site generator, fast builds, great templating
- **Plain CSS** — no frameworks, no build tools, just custom properties and flexbox
- **Google Fonts** — JetBrains Mono for headings/code, Inter for body text

## The terminal chrome

The key visual element is the macOS-style window frame. It's pure CSS:

```css
.terminal {
  background: var(--base);
  border-radius: 10px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
}

.terminal__titlebar {
  display: flex;
  align-items: center;
  background: var(--mantle);
  padding: 12px 16px;
}

.terminal__button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.terminal__button--close { background: #ff5f57; }
.terminal__button--minimize { background: #febc2e; }
.terminal__button--maximize { background: #28c840; }
```

## Color palette

I went with **Catppuccin Mocha** — it's a warm dark theme with soft pastel accents. The contrast ratio between the main text (`#cdd6f4`) and background (`#1e1e2e`) is about 11.5:1, well above the WCAG AAA requirement.

## Syntax highlighting

Hugo has built-in syntax highlighting via Chroma. I generated the Dracula theme CSS:

```bash
hugo gen chromastyles --style=dracula > themes/terminal/static/css/syntax.css
```

Then in `hugo.toml`:

```toml
[markup.highlight]
  noClasses = false
  lineNos = true
```

## JavaScript

Almost none. The only JS is a click handler for the mobile hamburger menu — about 5 lines. Everything else is CSS.

## What I'd add next

1. RSS feed (Hugo generates this out of the box)
2. Search with a `grep`-style interface
3. Dark/light toggle (though let's be honest, it'll stay dark)
