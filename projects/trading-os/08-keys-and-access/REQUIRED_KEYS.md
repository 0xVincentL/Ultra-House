# 需要的 API / Key 清单（按优先级）

## P0 必需
1. Moltbook API Bearer Key
- 用途：每日情报中的 Moltbook 热议 Top5
- 使用位置：Moltbook 热议抓取任务

2. Telegram 目标权限
- 用途：每日情报定时投递到指定频道/群
- 需要：机器人具备发送权限（管理员）

## P1 建议
3. 稳定行情源 API（可选其一）
- 用途：美股/A股/贵金属/DXY 快照稳定化
- 可选：AlphaVantage / TwelveData / Polygon / Finnhub（按预算）

4. 备用 Solana RPC 节点列表
- 用途：Smart Money 5min 稳定执行，降低 429/超时

## P2 可选
5. 内容源增强 API（如 NewsAPI / GDELT / 自建抓取）
- 用途：宏观与 AI 情报的覆盖率和稳定性增强

---
提供方式建议：
- 仅提供 key 名称与值（不在文档明文长期保存）
- 我会只记录“已配置/未配置”状态，不落盘明文密钥
