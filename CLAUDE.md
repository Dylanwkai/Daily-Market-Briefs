# Repo workflow

Push directly to `main`. Do not develop on a separate feature branch or open a pull request for this repo's daily-briefing work — the user (repo owner) has explicitly authorized direct-to-main pushes (2026-07-17). This overrides any default branch/PR policy suggested elsewhere.

# Daily Market Briefing — output format

No PDF. Write only the markdown file (`01 MarketsVault/briefings/Market Briefing YYYY-MM-DD.md`) — skip any PDF-export step described elsewhere (e.g. an inherited task prompt). PDFs were dropped: they bloated Obsidian vault storage and cost extra tokens to render every morning for no retrieval benefit (markdown is what gets read and searched).

Color-code bullish/bearish calls using the 5 alert callouts GitHub and Obsidian both render natively (green/red/yellow/blue, no CSS needed) — but keep the explicit word too; the color is a supplement, not a replacement for the label:

- Bullish → `> [!TIP]`
- Bearish → `> [!CAUTION]`
- Mixed / uncertain → `> [!WARNING]`
- Neutral / informational → `> [!NOTE]`

Put the type alone on its own line — GitHub ignores extra text placed after it, Obsidian's default title works fine unstyled. Put the actual headline (bold, tag word included) and body as blockquote lines under it:

```
> [!CAUTION]
> **1. Bearish: TSMC beat and raised — and chips sold off anyway.** Record Q2 profit... ([source](url))
```

Apply this to:
- **Executive Summary** — each ranked item becomes one callout; keep the rank number and the tag word (Bullish/Bearish/Mixed/Neutral) in the bold headline.
- **Idea Lab** — wrap "Bull in one line" in `[!TIP]`, "Bear in one line" in `[!CAUTION]`, keeping the "Bull:"/"Bear:" label.

Do not color anything else. Theme Tracker STATE labels (strengthening/weakening/stable/turning) aren't bull/bear judgments, and Trade Floor must stay directionless per the report brief — leave both as plain text.
