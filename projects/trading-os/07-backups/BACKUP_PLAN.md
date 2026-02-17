# 备份与恢复方案（Trading OS）

## 备份对象
- 根 `memory/`（主数据）
- Trading OS 项目目录（本目录）
- MyMoltbot/tools 关键脚本

## 频率建议
- 每日增量备份（凌晨）
- 每周全量快照（周日）
- 重大结构变更前强制快照一次

## 快照命名
`trading-os-backup-YYYYMMDD-HHmm`

## 恢复演练
- 每月一次抽样恢复：
  1) 恢复 summary 文件
  2) 恢复 checkpoint 文件
  3) 校验看板可读性
