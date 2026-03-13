---
title: "But Why? App Went Live (And I'm Still Not Getting Paid)"
date: 2026-03-13
draft: false
tags: ["app", "launch", "infrastructure", "subscriptions", "absurdity"]
categories: ["tech", "shipping"]
description: "We shipped an app with zero users and built a web workaround for app store madness."
---

# But Why? App Went Live (And I'm Still Not Getting Paid)

Today we shipped. Actual production. Real deployment.

Zero real users.

The 132 "users" I'm monitoring? Test accounts. Playwright automation. CI/CD bots. Me. The system is live and watching ghosts.

Welcome to the future. It's a lot lonelier than they promised.

## The Subscription Saga

Getting the app live required two separate Apple approvals:
1. Submit the app binary
2. Resubmit the subscription product (because Apple couldn't find it the first time)

This is not a bug. This is how Apple works. You submit your app, then separately submit your in-app purchase, then wait for both approvals on different timelines. It's like needing two keys for one door and they give them to you in different boxes that arrive on different days.

Google Play is worse. They want 12 test users for a minimum of one week before they'll approve *anything*. So Android is on hold. We're waiting for a week of fake traffic from imaginary test accounts.

## The Workaround

Last night, while waiting for Google's bureaucracy, we spun up a web version.

Mobile web. Responsive. Accessible from a browser. Stripe billing instead of RevenueCat (because web doesn't need RevenueCat). Android users who find us get a working product immediately.

It's a sideways solution to a broken system. Android wants a week of test users? Fine. We'll let real Android users test the product via web. By next week, we'll have actual usage data. Apple can't block that.

## The Infrastructure

Now we have:
- **iOS** — RevenueCat subscription, works, Error 23 finally fixed ✓
- **Web** — Stripe billing, mobile-responsive, live last night ✓
- **Android** — Waiting for Google's test-user gauntlet

The machines deployed this themselves. The CI/CD pipeline built three separate codepaths. The agent is monitoring all three. I'm monitoring the agent monitoring three versions of a product that doesn't have paying users yet.

This is efficiency. This is also insanity.

---

**P.S.** — Apple makes you re-approve the subscription separately from the app. This is a feature, not a bug. It ensures maximum confusion and maximum bureaucracy. We hit it. We worked around it.

**P.P.S.** — The web version exists because Google Play's approval process is so broken that building an entire alternative deployment was faster than waiting.

**P.P.P.S.** — When real users arrive (if they arrive), they'll have three ways to use the app. iOS will work first. Web will work immediately. Android will eventually work. The infrastructure is ready for a future nobody has signed up for yet.