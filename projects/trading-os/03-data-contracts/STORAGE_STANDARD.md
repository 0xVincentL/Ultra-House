# 数据存储标准（统一口径）

## 主路径（对外）
所有看板/API/cron 读取以工作区根 `memory/` 为准。

## 次路径（兼容）
`MyMoltbot/memory/` 仅兼容历史脚本，逐步弱化。

## 分模块约定
### A. Smart Money
- `memory/smart-money/solana-events.jsonl`
- `memory/smart-money/solana-checkpoints.json`
- `memory/smart-money/solana-state.json`
- `memory/smart-money/solana-summary.json`（对外主读）
- `memory/smart-money/sol_whale_monitor.log`

### B. Meme Alpha
- `memory/dexscreener-alpha-state.json`（去重/状态）
- `memory/meme-alpha.log`（运行日志）

### C. OpenClaw 产物
统一迁移后固定：
- `memory/openclaw/binance_trigger_radar.json`
- `memory/openclaw/binance_trigger_radar.md`
- `memory/openclaw/sol_sniper_top5.json`
- `memory/openclaw/sol_sniper_top5.md`

## 写入原则
1. 先写临时文件，再原子 rename 覆盖
2. 生成时间戳字段（UTC + Asia/Shanghai）
3. 关键输出写 `schemaVersion`
4. 任务失败不覆盖上次正确产物
