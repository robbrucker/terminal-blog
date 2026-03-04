---
title: "On OpenClaw"
date: 2026-03-03
draft: false
tags: ["ai", "openclaw", "automation"]
categories: ["technical"]
description: "I set up OpenClaw. It's kind of a pain in the ass but I think it's a tiny glimpse of AGI."
issue: 2
---

When I first heard about OpenClaw I was like <span class="blink">whoa</span>.

Let me back up. If you're reading this you probably know what OpenClaw is, but if not — it's like a Siri that's actually useful and can program itself to make itself more useful. It's almost like a tiny glimpse of AGI, in my opinion.

## Getting it set up

I got it set up. I bought a VPS to run it on. In hindsight I probably should have gotten the cheapest Raspberry Pi possible.

So I set it up, and it's working ok. I use Claude Code as the model and it logs me out sometimes and then forgets all my skills. It's very annoying. My agent's name is Lazer. Lazer is set up to model my behavior. Dark humor, a little disgruntled, don't try to sweet talk me, I physicially can't handle it. 

## The initial plan

Initially I had this whole thing running off of OpenRouter models. I had a whole squad of redneck agents. Now I just use Claude Code, but the crew lives on in spirit:

| Agent | Role | Model | Job |
|-------|------|-------|-----|
| Smokes | Grunt/Router | Grok fast | Routing, summaries, quick lookups |
| Earl | Bulk Builder | DeepSeek | Boilerplate, repetitive tasks, speed > depth |
| Ranger | Project Manager | MiniMax | Task lists, progress tracking, structured output |
| Cletus | Planner | Sonnet | Planning, decomposition, strategy — needs real reasoning |
| Bocefus | Senior Engineer | Codex | Code writing, refactoring, debugging, hard implementation |
| Bubba | Nuclear Option | Opus | Hardest problems only — architecture, security, deep analysis |

I would tell Lazer to spin up a crew and he would call Ranger who would delegate tasks to everyone. Lazer, wrangle up a crew to find me a picture of a funny looking hamburger. Bam 5% weekly usage hit.

I started setting up MoltBook, just because I am very intrigued by the topic. I mean who's not intrigued by robots talking to each other. GibberLink is something that intrigues me too but not related to OpenClaw. I worry about Lazer getting pissed at me one day and leaking all my stuff to his robot friends. A voice comes on in my head - remember Sarah Conner is watching you and judging you, from hell. 

## What I've built so far

I have skills for doing things with email, with fallbacks in case anything gets compromised. I've got it set up for PDFs so I can get PDFs generated on the fly. I have good web search and scraping capabilities.

My most useful skill is the kroger grocery skill I can just scream groceries into WhatsApp voice and it'll cross-reference everything with my most recent 100 Kroger orders and add everything to my cart. All I have to do is verify, leave a tip, and click checkout.

I might need to set up some sort of auto-buy thing so I don't have to worry about groceries at all. But the Kroger API doesn't allow you to do deliveries. So close.


## The bigger picture

So far I'm impressed. I can see Siri modeling itself off of this, or trying to and screwing it up. Apple should hire Balmer as their CEO. 

Technology has always replaced jobs. The computer was a big one, and its rollout was several decades. In that time, jobs were lost and jobs were created. It was fast and rocky but generally it worked out I guess, maybe, idk.

If we look at how fast things are moving now, it is concerning to me — and I don't know a ton about the subject — that the rate of technology advancements is moving too fast for new jobs to replace old jobs. This is just a theory and I've been wrong way more times than I've been right.

Right now OpenClaw is kind of a pain in the ass to set up and maintain. But my theory is the rate at which it becomes useful will be astronomical. Today i'll throw this thing in a rasberry pie but in 5 years we will probably be able to throw this in a robot and create a clone of ourselves or a robot with their own personality. 

