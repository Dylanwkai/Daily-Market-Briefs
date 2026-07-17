# Repo workflow

Push directly to `main`. Do not develop on a separate feature branch or open a pull request for this repo's daily-briefing work — the user (repo owner) has explicitly authorized direct-to-main pushes (2026-07-17). This overrides any default branch/PR policy suggested elsewhere.

# Daily Market Briefing — output format

No PDF. Write only the markdown file (`01 MarketsVault/briefings/Market Briefing YYYY-MM-DD.md`) — skip any PDF-export step described elsewhere (e.g. an inherited task prompt). PDFs were dropped: they bloated Obsidian vault storage and cost extra tokens to render every morning for no retrieval benefit (markdown is what gets read and searched).

Only the Obsidian render matters (that's where this gets read — GitHub-web fidelity is not a goal). Color-code bullish/bearish calls using **custom callout types whose name is the label itself** — `[!bullish]`, `[!bearish]`, `[!mixed]`, `[!neutral]` — never GitHub's generic `[!TIP]`/`[!CAUTION]`/`[!WARNING]`/`[!NOTE]`. Obsidian renders the type name as the callout's title by default, so the colored box literally reads "Bullish"/"Bearish", no duplicate wording needed in the body:

- Bullish → `> [!bullish]`
- Bearish → `> [!bearish]`
- Mixed / uncertain → `> [!mixed]`
- Neutral / informational → `> [!neutral]`

The colors/icons for these four types are defined once in `.obsidian/snippets/market-briefing.css` (enabled in `.obsidian/appearance.json`) — a one-time setup, not a per-morning cost. Put the type alone on its own line, headline (bold, no tag word — the callout title already says it) and body as blockquote lines under it:

```
> [!bearish]
> **1. TSMC beat and raised — and chips sold off anyway.** Record Q2 profit... ([source](url))
```

Apply this to:
- **Executive Summary** — each ranked item becomes one callout. Number items as `1.1`, `1.2`, ... `1.5` (section 1, sub-item N) instead of a bare rank.
- **Idea Lab** — wrap "Bull in one line" in `[!bullish]`, "Bear in one line" in `[!bearish]`.

Do not color anything else — Theme Tracker STATE labels (strengthening/weakening/stable/turning) aren't bull/bear judgments, and Trade Floor must stay directionless per the report brief. Leave both as plain text.

**Numbered sub-pointers:** within every numbered section (1–8), number each sub-item `<section>.<n>` (e.g. Asia Day-Ahead's sub-points are `4.1`, `4.2`, `4.3`, `4.4`) instead of a bare bold lead-in. Skip this for the two tables (Catalyst Calendar, Market Dashboard) and Global Pulse's spec-mandated (a)/(b)/(c) lettering.
