# AI-zl Design System Skill Test

这个仓库用于保存 AI-zl 项目中与设计系统 Skill、PRD、HTML 原型相关的阶段性产物。

## 目录结构

| 目录 | 内容 |
| --- | --- |
| `docs/` | PRD、页面规划、模板等项目文档 |
| `prototypes/` | 已生成的 HTML 原型和预览截图 |
| `skills/` | 当前项目使用和迭代过的 Codex Skills |

## 当前包含的 Skills

| Skill | 中文说明 |
| --- | --- |
| `ai-zl-prdwriting` | PRD 写作与需求结构化 Skill，用于把需求整理成可评审、可执行、可验收的产品文档 |
| `stock-trading-design-system` | 股票交易 App 设计系统规范 Skill，用于约束页面结构、组件命名、视觉规则和设计系统一致性 |
| `stock-trading-prototype-design-system` | 股票交易 App HTML 原型生成 Skill，用于基于 PRD、Figma 截图和设计系统规则生成移动端可交互原型 |

## 使用建议

重做或新增页面原型时，建议按以下顺序使用：

1. 使用 `ai-zl-prdwriting` 明确需求、范围、交互和验收标准。
2. 使用 `stock-trading-design-system` 检查页面是否符合当前 App 设计系统。
3. 使用 `stock-trading-prototype-design-system` 生成 HTML 移动端原型。

## 当前重点文档

- `docs/prd-watchlist-position-analysis-monitoring.md`：自选页持仓分析与智能盯盘 PRD。

