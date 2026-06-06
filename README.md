# predictions-feed

Daily JSONL sync from a personal Orallexa markets stack to feed [vibexforge.com/predictions](https://vibexforge.com/predictions).

All forecasts are Brier-audited at settlement. MIT licensed.

[中文版 / Chinese version](./README.zh-CN.md)

## What's in here

| File | Contents |
|---|---|
| `sports_history.jsonl` | Live JSONL of open daily sport picks (NBA, MLB, NHL, MLS, World Cup) |
| `sports_settled.jsonl` | T+1 settled rows for Brier audit |
| `polymarket_history.jsonl` | Latest snapshot per Polymarket event |
| `series_state.json` | NBA Finals / Stanley Cup current series score |
| `contrarian/YYYY-MM-DD.json` | Daily contrarian regime overlay (Tom Lee / Howard Marks / Burry signals) |

## How it works

Synced 2x daily (12:30 ET + 21:00 ET) from a local markets stack via launchd cron. No manual edits. Pure read-only feed.

## See also

- Public dashboard: https://vibexforge.com/predictions
- Source code: https://github.com/alex-jb/orallexa-ai-trading-agent
- Solo Founder OS (11-agent OSS stack): https://github.com/alex-jb/solo-founder-os
