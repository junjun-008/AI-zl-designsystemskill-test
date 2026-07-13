---
name: stock-trading-prototype-design-system
version: 0.1.1
description: 当产品经理或设计师需要为股票交易 App 生成移动端 HTML 原型时使用本 Skill，适用于已有页面修改、功能调整、新增模块、AI 交易页面、行情首页、详情/事件页面和需要评审的可交互原型。不要用于 PRD 写作、营销文案、海报、通用网页、后端工作、数据分析或最终像素级精修交付。
---

# 股票交易 App 原型设计系统 Skill

这个 Skill 用于把业务需求或页面修改需求，快速生成符合当前股票交易 App 视觉风格的移动端 HTML 可交互原型。MVP 阶段以评审可用、风格一致、结构清晰为目标，不承诺一次生成设计师最终精修稿。

入口文件只负责路由和关键约束。详细规则在 `references/`，精确数值在 `assets/`。

## 默认输出

- 输出类型：HTML 可交互原型。
- 默认主题：亮色模式。
- 默认屏宽：390px。
- 必须附带：页面目的、模块说明、交互说明、数据假设、设计自检。
- Figma 输出暂不作为 MVP 默认能力。
- 已有页面修改默认采用“截图/Figma 驱动”：先读取用户提供的截图、Figma 节点或当前页面原型，再做局部改造。

## 权威来源

规则优先级：

1. 用户提供的当前页面截图、Figma 节点截图或当前 HTML 原型截图。
2. Figma `Page 1` 真实页面。
3. `assets/design-tokens.css` 和已确认 Light/Dark token。
4. `assets/page-patterns.json`、`assets/component-patterns.json`、`assets/source-map.json`。
5. 用户确认过的评审问题和修正案例。
6. 明确标注的模型假设。

当前 Components 页只作为参考，不作为权威组件库。

## 路由表

| 用户意图 | 读取 |
|---|---|
| 行情首页、市场概览、行情异动、首页新增模块 | `references/page-patterns.md`, `references/components-shared.md`, `references/mobile.md` |
| AI 持仓诊断、AI 交易、交易优化、自动模拟交易 | `references/page-patterns.md`, `references/prototype-flows.md`, `references/components-shared.md` |
| 事件详情、发展脉络、热点事件、关联 ETF、信息解释页 | `references/page-patterns.md`, `references/components-shared.md`, `references/mobile.md` |
| 已有页面修改、功能调整、新增模块功能、PRD + 截图改页 | `references/screenshot-driven-workflow.md`, `references/prototype-flows.md`, `references/components-shared.md`, `references/mobile.md` |
| 明暗色、视觉 token、颜色/字号/圆角/间距 | `references/visual-rules.md`, `references/dark-mode.md`, `assets/design-tokens.css` |
| 图标、底部导航图标、工具图标缺失处理 | `assets/icon-index.json`, `assets/icons/icon-map.json`, `references/components-shared.md` |
| 术语不清、业务/设计/代码命名冲突 | `GLOSSARY.md` |
| 规则变更、失败案例、是否新增规则 | `references/meta-rules.md`, `references/case-studies.md` |

## 顶层硬规则

1. 默认生成亮色 390px 移动端 HTML 原型。
2. 不允许生成营销页、大屏仪表盘、通用 SaaS 页面或海报风格。
3. 不允许改变金融涨跌红绿语义：上涨/正向使用 rise，下降/负向使用 fall。
4. 不允许随意发明颜色、字体、圆角、阴影、图标、导航结构。
5. 已有页面修改时，必须先识别来源截图或 Figma 节点的页面结构，不把具体页面模板写死进 Skill。
6. 修改类需求默认保持原页面壳和导航，只新增或替换目标模块。
7. 缺少源稿证据时，必须在输出中标注“假设”，不要伪装成规范。
8. 每次输出都必须做简短自检。

## 组件来源边界

1. 业务组件和页面模块由本 Skill 约束，见 `references/components-shared.md`。
2. HTML 实现可使用普通 HTML/CSS/JS，但视觉必须来自本 Skill 的 token 和模式。
3. 图标优先调用项目通用图标包 `assets/icons/icon-map.json` 和 SVG Sprite；只有通用图标包没有覆盖的特殊业务图标，才允许临时绘制并标注“临时图标”。
4. 已存在于通用图标包的图标禁止在页面内重新手写 SVG 路径。

## 输出自检

输出前检查：

- [ ] 如果是已有页面修改，是否先读取并识别了截图/Figma/当前原型结构。
- [ ] 是否使用 `assets/design-tokens.css` 中的 token。
- [ ] 是否保持 390px 移动端风格。
- [ ] 是否避免了营销页、SaaS 仪表盘、大圆角泛化卡片、紫色渐变等非源稿风格。
- [ ] 金融红绿语义是否正确。
- [ ] 修改类需求是否保留原页面壳和导航。
- [ ] 新增内容是否只插入或替换影响区域，而不是重构整页。
- [ ] 通用 icon 是否按 `icon-map.json` 调用，特殊 icon 是否明确标记为临时方案。
- [ ] 交互状态是否足够用于评审。
- [ ] 假设和缺失素材是否明确标注。

## 文件清单

| 文件 | 用途 |
|---|---|
| `BRIEF.md` | MVP 目标和边界 |
| `SKILL.md` | Skill 入口、触发、路由、顶层规则 |
| `GLOSSARY.md` | 中文术语和命名治理 |
| `CHANGELOG.md` | 版本记录 |
| `references/page-patterns.md` | 页面模式规则 |
| `references/screenshot-driven-workflow.md` | 截图/Figma 驱动的已有页面修改流程 |
| `references/prototype-flows.md` | 原型流程和交互规则 |
| `references/components-shared.md` | 共享模块/组件规则 |
| `references/mobile.md` | 移动端布局规则 |
| `references/visual-rules.md` | 视觉 token 使用规则 |
| `references/dark-mode.md` | 暗色模式规则 |
| `references/source-principles.md` | 来源和证据原则 |
| `references/meta-rules.md` | 规则治理 |
| `references/case-studies.md` | 失败案例 |
| `assets/design-tokens.css` | 精确 token |
| `assets/page-patterns.json` | 页面模式结构化资产 |
| `assets/component-patterns.json` | 模块模式结构化资产 |
| `assets/icon-index.json` | icon 语义索引和缺失素材处理规则 |
| `assets/icons/icon-map.json` | 通用 icon ID 与 SVG Sprite 映射 |
| `assets/icons/common-icons/icon-sprite.svg` | 通用 SVG icon 资产 |
| `assets/source-map.json` | Figma 来源映射 |
| `evals/evals.json` | MVP 测试任务 |
