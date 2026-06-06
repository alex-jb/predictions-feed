# predictions-feed

个人 Orallexa 量化栈每天自动 sync 出来的 JSONL feed, 给 [vibexforge.com/predictions](https://vibexforge.com/predictions) 公开预测面板用。

所有预测在 settlement 时做 Brier 校准审计。MIT 协议。

[English version](./README.md)

## 文件清单

| 文件 | 内容 |
|---|---|
| `sports_history.jsonl` | 体育预测 (NBA / MLB / NHL / MLS / 2026 World Cup) 实时 JSONL |
| `sports_settled.jsonl` | T+1 已结算行, 用于 Brier 审计 |
| `polymarket_history.jsonl` | Polymarket 每个 event 最新 snapshot |
| `series_state.json` | NBA / Stanley Cup Finals 当前系列赛比分 |
| `contrarian/YYYY-MM-DD.json` | 每日 contrarian regime overlay (Tom Lee / Howard Marks / Burry 信号) |

## 工作方式

每天 2 次 sync (12:30 ET + 21:00 ET), 通过 launchd cron 从本地量化栈自动推送, 没有手动编辑。纯只读 feed。

## 相关链接

- 公开 dashboard: https://vibexforge.com/predictions
- 源码: https://github.com/alex-jb/orallexa-ai-trading-agent
- Solo Founder OS (11-agent 开源栈): https://github.com/alex-jb/solo-founder-os
