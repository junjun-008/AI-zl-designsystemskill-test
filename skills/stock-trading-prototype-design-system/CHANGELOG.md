# 变更记录

## 版本兼容

| Generator Skill | Review Skill | 状态 | 说明 |
|---|---|---|---|
| 0.1.0 | - | 仅生成 Skill | MVP 骨架版本 |

## 0.1.1 - 2026-07-09

### 新增

- 新增 `references/screenshot-driven-workflow.md`，作为已有页面修改的默认流程。
- 新增 `assets/icon-index.json`，记录常用 icon 语义、来源优先级和缺失兜底方式。
- 新增 CASE-002，记录自选页原型不像源稿的根因和修正方向。
- 新增截图驱动改页 eval，用于验证“PRD + Figma/截图”的页面修改任务。

### 调整

- `SKILL.md` 的已有页面修改路由改为优先读取截图驱动流程。
- `components-shared.md` 扩展跨页面组件规则：顶部业务 Tab、胶囊筛选、股票列表行、股票状态标签、分时小图、底部弹层、Toast。
- 明确不把具体页面模板写死进 Skill；高频页面也应通过截图或 Figma 节点识别结构。

### 规则引入

| 规则 | 文件 | 来源 | 说明 |
|---|---|---|---|
| 已有页面修改必须先读截图/Figma/当前原型 | `screenshot-driven-workflow.md`, `SKILL.md` | 用户确认 + CASE-002 | 避免凭 PRD 重画页面 |
| 具体页面不写死进 Skill | `SKILL.md`, `case-studies.md` | 用户确认 | Skill 保持轻量、干净、高效 |
| icon 只做语义索引和兜底规则 | `icon-index.json`, `components-shared.md` | 用户反馈 + MVP 边界 | 后续可逐步补真实资产 |
| 跨页面组件优先沉淀 | `components-shared.md` | CASE-002 | 不沉淀具体页面模板 |

## 0.1.0 - 2026-07-09

### 新增

- 创建 `stock-trading-prototype-design-system` MVP Skill。
- 明确默认输出为 390px 亮色 HTML 可交互原型。
- 新增页面模式、模块模式、视觉 token、来源映射资产。
- 新增第一批 eval 测试任务。

### 规则引入

| 规则 | 文件 | 来源 | 说明 |
|---|---|---|---|
| 默认亮色 HTML 原型 | `SKILL.md` | 用户确认 | Figma 输出后置 |
| Page 1 为权威来源 | `BRIEF.md`, `source-principles.md` | 用户确认 + Figma 读取 | Components 页暂不作为权威 |
| 金融红绿语义不可改 | `SKILL.md`, `visual-rules.md` | Figma token + 业务语义 | rise/fall token 固定 |
| 修改类需求不重构整页 | `prototype-flows.md` | 用户场景确认 | 保留原页面壳 |

### 待确认

- 图标库后续是否从 Figma 单独抽取并做成资产。
- HTML 原型是否需要固定技术栈模板。
- 是否需要独立的 review Skill。
