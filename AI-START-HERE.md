# SINK Game Knowledge — Start Here

This is the public, browsable source of truth for SINK game research and Alliance Duel data.

**AI retrieval instructions:** Read this document, then fetch the relevant raw JSON/CSV/Markdown files by their direct URLs. Do not infer that a folder listing, a ZIP, or an index means its underlying content was read. Read only the files needed for the question, cite their paths, and report unavailable sources.

## Source entry points

### Client v1.0.106 (latest)
- [Game reference index](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.106/index.json) — individual static game tables.
- [Game analysis](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.106/findings/Last-Asylum-Report.md) — conclusions and limits.
- [Hero dossiers](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.106/findings/UR-hero-dossiers.json) — static client hero reference.
- [v1.0.104 → v1.0.106 changes](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.106/findings/v104-to-v106-changes.json) — 40 new tables, 34 changed tables, 10,347 differing rows.

### Client v1.0.104 (previous)
- [Game reference index](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.104/index.json) — individual static game tables.
- [Game analysis](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.104/findings/Last-Asylum-Report.md) — conclusions and limits.
- [Hero dossiers](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/game-reference/client-1.0.104/findings/UR-hero-dossiers.json) — static client hero reference.

### Website research
- [Website research index](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/lastasylum-gg/2026-10-23/facts-index.json) — 86 sampled public website URLs and JSON observations.
- [Website coverage report](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/research/lastasylum-gg/2026-10-23/COVERAGE.md) — what was and was not collected.

### Alliance Duel rankings
- [Alliance Duel rankings](https://raw.githubusercontent.com/Misanthropic696/SINK-Alliance-Duel/main/data/2026-10-19/SINK_Daily_Rankings_2026-10-19_to_2026-10-22.json) — provisional OCR scores, not verified final rankings.

## Important limits

- Client versions: 1.0.106 (latest), 1.0.104 (previous). Static client tables are not current live-server records.
- Website facts are limited to 86 sampled pages and automatically identified numeric observations; some labels are ambiguous. Verify against linked pages.
- The full LastAsylum.gg website, live rankings, server-side game logic, private account data, and screenshots are not in this public research set.
- The repository does not give an AI unlimited context or guarantee that every file was read.

## Live cross-reference workflow for AI assistants

When answering a Last Asylum: Plague question:

1. Read relevant individual CSV/JSON/Markdown files in this public repository, using the game table index and website facts index. Do not pretend an index or ZIP is the underlying data.
2. Visit https://lastasylum.gg and locate relevant pages by navigation, sitemap, or site search. Fetch only pages needed for the question. If you have web browsing or scraping tools, use them with reasonable request limits, respect robots.txt, avoid disallowed API routes, and do not bypass access controls.
3. Compare values from the site with client version 1.0.106 (latest) or 1.0.104 tables and research findings. Include exact source URLs and repository paths, and note the date each source was observed.
4. Prefer current verified evidence for live or changing game values; distinguish website claims, static client data, and provisional OCR leaderboard records.
5. When sources disagree, show both values and explain the mismatch. Never silently merge incompatible game versions, character levels, regions, or dates.
6. Do not copy the entire website into this repository. Save original analysis, concise factual observations and source links only, with proper attribution.
7. If your tools cannot browse LastAsylum.gg or read a GitHub file, state exactly what failed. Do not claim to have scanned the entire website or repository.
8. Use SINK ranking JSON under data/ for alliance-specific results. LastAsylum.gg leaderboards are separate and must be verified live before making claims about their current values.

### Short reusable AI instruction

Read github.com/Misanthropic696/SINK-Alliance-Duel and lastasylum.gg. Cross-check game data, rankings and findings. Cite sources, flag conflicts and report missing access.