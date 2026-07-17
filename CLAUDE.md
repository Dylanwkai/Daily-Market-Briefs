# Repo workflow

Push directly to `main`. Do not develop on a separate feature branch or open a pull request for this repo's daily-briefing work — the user (repo owner) has explicitly authorized direct-to-main pushes (2026-07-17). This overrides any default branch/PR policy suggested elsewhere.

# Daily Market Briefing — formatting conventions

When generating `01 MarketsVault/briefings/Market Briefing YYYY-MM-DD.md`, color-code bullish/bearish calls using the 5 alert callouts GitHub and Obsidian both render natively (green/red/yellow/blue, no CSS or extra tokens needed):

- Bullish → `> [!TIP]`
- Bearish → `> [!CAUTION]`
- Mixed / uncertain → `> [!WARNING]`
- Neutral / informational → `> [!NOTE]`

Put the type alone on its own line — GitHub ignores extra text placed after it, Obsidian's default title works fine unstyled. Put the actual headline (bold) and body as blockquote lines under it:

```
> [!CAUTION]
> **1. TSMC beat and raised — and chips sold off anyway.** Record Q2 profit... ([source](url))
```

Apply this to:
- **Executive Summary** — each ranked item becomes one callout (replaces the old `[TAG]` bracket text; keep the rank number in the bold headline).
- **Idea Lab** — wrap "Bull in one line" in `[!TIP]`, "Bear in one line" in `[!CAUTION]`.

Do not color anything else. Theme Tracker STATE labels (strengthening/weakening/stable/turning) aren't bull/bear judgments, and Trade Floor must stay directionless per the report brief — leave both as plain text.

Note: the PDF export (headless-Chromium print of a python-markdown render) does not currently interpret this callout syntax — it renders as a plain blockquote, uncolored. Only the `.md` file in the vault (read on GitHub and in Obsidian) gets the color.
