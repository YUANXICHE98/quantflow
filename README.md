# QuantFlow 能力总览

> 备份时间: 2026-04-09
> 服务状态: 已关闭 (源码已丢失)

## 能力统计

| 类型 | 数量 | 说明 |
|------|------|------|
| 因子 (factor) | 2 | MACD、RSI 极端值 |
| 策略 (strategy) | 4 | 含 3 个组合策略 |
| 模型 (model) | 1 | LSTM 价格预测 |
| 数据源 (mcp) | 1 | OKX 行情 |
| 技能 (skill) | 1 | 飞书通知 |

## 快速引用

### Chat 模式
```
@factor:macd          # 计算 MACD 指标
@factor:rsi-extreme   # 计算 RSI 信号
@strategy:macd-20ma   # 执行 MACD+均线策略
@model:lstm-predictor # LSTM 价格预测
```

### API 端点
```
GET  /api/capabilities              # 获取所有能力
POST /api/factor/compute            # 计算因子
POST /api/strategy/execute          # 执行策略
```

## 文件结构

```
quantflow/
├── README.md           # 本文件
├── 01_因子库.md        # 因子能力详情
├── 02_策略库.md        # 策略能力详情
├── 03_模型库.md        # 模型能力详情
├── 04_数据与工具.md    # MCP/Skill 能力
├── capabilities.json   # 原始 JSON 备份
└── 因子库规划.md       # 长期规划文档
```

## 恢复说明

源码文件已随会话删除。
重建项目请参考 `capabilities.json` 和各能力文档。