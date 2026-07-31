---
title: "QwenVideoFactory"
summary: "Bulk prompt automation extension for chat.qwen.ai video generation."
repo: "https://github.com/SwiftScripters/QwenVideoFactory"
license: "Apache-2.0"
language: "JavaScript"
date: 2026-07-01
---

QwenVideoFactory is a Chrome extension that automates video-generation workflows on
chat.qwen.ai. Load a batch of prompts, let it process them in an unattended queue, and
download the results — all within your own account's daily generation limit.

## Features

- Batch prompt processing with configurable delays
- Automatic account rotation when daily limits are reached
- Pause, resume, and stop controls for queue management
- Auto-pause when the browser tab loses focus
- Automatic video downloading with sequential naming
- Support for multiple account credentials to extend processing capacity

## Installation

```bash
git clone https://github.com/SwiftScripters/QwenVideoFactory
```

Then load the extension unpacked via `chrome://extensions`. See the repo README for
full setup steps.
