---
title: "Overflow"
summary: "Bulk prompt automation extension for Google Flow image generation."
repo: "https://github.com/SwiftScripters/Overflow"
license: "Apache-2.0"
language: "JavaScript"
date: 2026-07-30
---

Overflow is a Chrome extension that automates repetitive image-generation workflows in
Google Flow. Instead of babysitting a browser tab, queue up multiple prompts and let
Overflow work through them unattended, with human-like typing speed and genuine click
interactions.

## Features

- Bulk prompt queuing with pause/resume controls
- Auto-pause when the Flow tab loses focus
- Character consistency through reference image uploads
- Automatic result downloading with sequential naming
- Safety guardrails preventing use outside Flow projects
- Manual queue clearing and error recovery

## Status

Alpha release (v1.0.0.1) — functional end-to-end but still getting polished and tested.

## Installation

```bash
git clone https://github.com/SwiftScripters/Overflow
```

Then load the extension unpacked via `chrome://extensions`. See the repo README for
full setup steps.
