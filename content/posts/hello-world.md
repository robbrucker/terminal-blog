---
title: "Hello, World!"
date: 2026-03-03
draft: false
tags: ["intro", "meta"]
categories: ["general"]
description: "First post. Testing the terminal theme with some mixed markdown."
---

Welcome to my corner of the internet. This blog runs on [Hugo](https://gohugo.io/) with a custom terminal theme inspired by the tools I use every day.

## Why a terminal theme?

I spend most of my waking hours in a terminal. VS Code, iTerm2, tmux — the dark backgrounds and monospace fonts feel like home. So when it came time to build a blog, I wanted something that felt familiar.

> "Any sufficiently advanced technology is indistinguishable from magic."
> — Arthur C. Clarke

## Some things I'll write about

- **Software engineering** — architecture, debugging, and the craft of writing code
- **Tools and workflows** — the stuff that makes developers productive
- **Projects** — things I'm building and lessons learned along the way

## A quick code test

Here's a simple Go function, because why not:

```go
func greet(name string) string {
    if name == "" {
        return "Hello, World!"
    }
    return fmt.Sprintf("Hello, %s!", name)
}
```

And some inline code: `hugo server -D` starts the dev server.

## A table for good measure

| Tool | Purpose | Been using since |
|------|---------|-----------------|
| Neovim | Editor | 2020 |
| tmux | Multiplexer | 2019 |
| Hugo | Static sites | 2026 |
| Go | Backend | 2021 |

---

That's it for now. More posts coming soon.
