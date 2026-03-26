# AI Fluency — The Prompting Lab

An interactive training tool built to support our internal AI Fluency session. Designed for Customer Service Officers, Business Development Managers, and Product Managers who are new to Generative AI.

**Live site:** [ai-fluency.vercel.app](https://ai-fluency.vercel.app)

---

## What's inside

A single-page web app with three tabs:

| Tab | What it does |
|-----|-------------|
| **① The Framework** | Explains the CTFC prompting model (Context, Task, Format, Constraints) with a live annotated example from our wire rope business |
| **② Good vs Bad** | Four side-by-side prompt comparisons — weak prompt vs strong prompt — with realistic responses for each |
| **③ Live Builder** | An interactive prompt builder where you fill in the four fields and watch a response stream in real time |

---

## How to use it

### In a presentation
Open the live URL on a projector. Walk through Tab 1 to explain the framework, use Tab 2 to show the contrast, then demo Tab 3 live by loading a preset and hitting Generate with the audience.

### For self-guided learning
Share the URL with your team. Tabs 1 and 2 work fully without any setup. Tab 3 has four presets built in — just load one and hit Generate.

---

## Presets in the Live Builder

| Preset | What it generates |
|--------|------------------|
| Price increase letter | 7% increase justification referencing AUD/EUR and steel rod costs |
| Supplier negotiation | Three leverage points for annual price discussions |
| Customer complaint | Response to a late delivery from a long-term customer |
| Market summary | Steel costs, currency impact, and lead times for the sales team |

---

## How it works technically

- **Pure HTML/CSS/JS** — no framework, no build step, no dependencies
- **Single file** (`index.html`) — the entire app lives in one file
- **Simulated streaming** — the Live Builder streams pre-written responses character by character, mimicking real AI output. Works offline and on any device with no API key required
- **Hosted on Vercel** — connected to this GitHub repo. Any commit to `main` triggers an automatic redeploy within ~30 seconds

---

## Upgrading to a live API (optional)

The Live Builder currently uses simulated responses for reliability. To connect it to Claude in real time:

1. Get an API key from [console.anthropic.com](https://console.anthropic.com)
2. Set a spend limit (e.g. $10) to cap your risk
3. Open `index.html` and find the commented block near the bottom of the `<script>` section — it starts with `// To switch to LIVE mode`
4. Paste your key on the line marked and uncomment the `callRealAPI` function
5. Commit — Vercel redeploys automatically

> ⚠️ Never commit a real API key to a public repository. If this repo is public, switch it to private before adding a key, or use a backend proxy.

---

## Updating the content

All content lives in `index.html`. To update:

1. Go to the file in this repo
2. Click the pencil (Edit) icon
3. Make your changes
4. Commit — the live site updates within 30 seconds

---

## Repo structure

```
ai-fluency/
└── index.html      ← the entire app (do not rename)
└── README.md       ← this file
```

> **Important:** Do not rename `index.html`. Vercel serves it as the site's home page by convention — renaming it will break the live URL for everyone.

---

## Built with

- HTML / CSS / Vanilla JS
- [DM Serif Display + DM Sans + JetBrains Mono](https://fonts.google.com) — Google Fonts
- Hosted on [Vercel](https://vercel.com) (free tier)
- Responses modelled on real wire rope and lifting & rigging industry scenarios

---

*Internal training tool — not for external distribution.*
