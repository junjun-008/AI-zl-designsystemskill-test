---
name: stock-trading-design-system
description: 用于创建或审核股票交易 App 页面、移动端金融原型、Figma 更新、组件规范、页面规范、产品经理输出和实现提示词，并确保结果遵循从 Figma 文件 OHAU7JaTYZ1uNsITyPhvIF 提取的 Stock Trading 设计系统。
---

# Stock Trading 设计系统 Skill

当设计师、产品经理或开发人员处理 Stock Trading App，并且需要让输出符合当前设计系统时，使用本 Skill。

这个 Skill 不只是用于 AI 生成，也是团队共用的规则手册，覆盖：

- Figma 页面扩展
- 新功能原型输出
- 组件和设计 token 治理
- 页面审查与质量检查
- 产品经理到设计的交接
- 设计到代码的提示词

## 权威来源

- Figma 源文件：`Stock Trading App - UI Concept (Community)` / 文件 Key `OHAU7JaTYZ1uNsITyPhvIF`
- 设计文件中的核心页面：
  - `Aktivitas`
  - `Trending`
  - `Detail Saham`
  - `Topup Buying Power 1`
  - `Topup Buying Power 2`
  - `Topup Buying Power 3`
- 设计系统页面：
  - `Design System / Components`
  - `Design System / Examples`
  - `Design System / Sections`
  - `Design System / Handbook`
  - `Design System / Color Palette`

## 阅读顺序

按任务逐层读取，不要一开始读取全部文件，除非任务确实需要。

### 第一层：入口文件

每次都先读取：

1. `SKILL.md`
2. `GLOSSARY.md`

### 第二层：工作规范

按任务类型选择：

- 组件任务：`components.md`
- 页面任务：`page-list.md`
- 布局尺寸和测量：`docs/layout-and-component-specs.md`
- 图标或 Logo 使用：`assets/icon-index.json`
- 代码或原型变量：`tokens.json`、`design-tokens.css`、`component-variables.css`

### 第三层：扩展参考

只在需要时读取：

- 可复用页面骨架：`page-shells/`
- 业务领域规则：`product-lines/`
- 常见错误和审查模式：`case-studies/`
- 安装和团队使用：`INSTALL.md`
- 术语和治理变更：`CHANGELOG.md`

## 强制规则

### 必须做到

1. 产品页面始终以 `375px` 为移动端基准。
2. 新值优先使用现有 token，不要直接发明裸值。
3. 创建独立 Frame 之前，先复用已有组件。
4. 保持当前深色金融产品风格：信息密集、任务导向、数据优先。
5. 页面、组件、token 和状态使用当前命名体系。
6. 保持股票涨跌语义一致：
   - 正向 = 绿色
   - 负向 = 红色
   - 中性 = 弱化文字
7. 按钮、Tab、列表行、支付控件和导航必须组件化。
8. 业务列表使用本地 icon/logo 组件，不使用粘贴的位图占位符。
9. 为导航、操作、自选、持仓、盯盘、触发器、行情、支付和 Logo 位置选择图标前，先读取 `assets/icon-index.json`。
10. HTML 原型先通过 `assets/icons/icon-map.json` 和公共 SVG Sprite 解析已批准的通用图标，再考虑绘制新的 SVG 路径。
11. 字体样式使用 `Display`、`Headline`、`Title`、`Body`、`Label` 等角色命名。
12. 交接前对照 Figma Handbook 页面检查新输出。

### 禁止做到

1. 不要因为单个页面显得空而引入新的视觉风格。
2. 项目内部不要用 `H1 / H2 / body1 / body2` 作为工作命名体系。
3. 不要拆离 Button、Bottom Navigation、Segment Tab、Stock Row、Payment Method Item 等核心控件。
4. 不要用空白圆形或随机图标替代股票 Logo。
5. 不要只因为图形相似就使用通用图标，图标含义必须符合 `assets/icon-index.json`。
6. 不要在 App 页面中加入浅色主题界面、营销 Hero 或装饰性渐变。
7. 不要在同一页面混用多套页面级间距体系。
8. 除非当前 token 无法表达需求且已明确批准，否则不要创建新的颜色、阴影、圆角或字号。
9. 如果 `tokens.json` 已存在 Figma 组件 API，不要使用临时属性名描述组件。

## 任务路由

### 页面生成或页面审查

读取：

- `page-list.md`
- `page-shells/` 中的一个文件
- `product-lines/` 中的一个文件
- `docs/layout-and-component-specs.md`
- 当页面包含导航、工具栏、股票 Logo、盯盘、触发器、支付图标或其他纯图标操作时，读取 `assets/icon-index.json`
- HTML 原型的可复用图标读取 `assets/icons/icon-map.json` 和 `assets/icons/common-icons/icon-sprite.svg`

### 组件生成或组件审查

读取：

- `components.md`
- `tokens.json`
- `docs/layout-and-component-specs.md`
- 当组件包含图标、Logo、前置图标、尾部图标、方式图标或实例替换插槽时，读取 `assets/icon-index.json`
- HTML 原型中的图标插槽读取 `assets/icons/icon-map.json`
- 相关 `case-studies/` 案例

### 原型或实现输出

读取：

- `tokens.json`
- `design-tokens.css`
- `component-variables.css`
- `components.md`
- `assets/icon-index.json`
- `assets/icons/icon-map.json`
- `assets/icons/common-icons/icon-sprite.svg`

### 安装、团队同步或协作治理

读取：

- `INSTALL.md`
- `GLOSSARY.md`
- `CHANGELOG.md`

## 交付标准

输出必须满足：

- 使用当前组件名称和状态名称
- 使用当前间距、圆角和颜色 token
- 符合现有移动端深色股票交易视觉语言
- 产品经理、设计师和开发人员无需额外翻译即可理解
- 可以在后续页面中复用，而不是只解决一个局部 Frame

## 文件说明

### 元数据

- `SKILL.md`：入口、路由和强制规则
- `CHANGELOG.md`：治理变更记录
- `GLOSSARY.md`：共用术语
- `INSTALL.md`：安装和使用指南

### 资产

- `tokens.json`：结构化 token 权威来源
- `design-tokens.css`：面向原型和代码的 CSS token 导出
- `component-variables.css`：包含组件变量的兼容导出
- `page-shells/`：可复用页面组合骨架
- `product-lines/`：业务领域覆盖规则

### 参考资料

- `components.md`：组件规则和 API
- `page-list.md`：页面规则和模块组合
- `docs/layout-and-component-specs.md`：详细尺寸规范
- `assets/icon-index.json`：图标和 Logo 的语义使用表，含中文含义、业务分类、推荐用法和回退规则
- `assets/icons/icon-map.json`：HTML 原型的通用图标注册表
- `assets/icons/common-icons/icon-sprite.svg`：公共 SVG 图标资源
- `case-studies/`：真实失败模式和审查案例

## 最终自检

交付前确认：

- 页面是否仍以 `375px` 为移动端基准？
- 是否复用了正确组件，而不是绘制脱离组件体系的副本？
- 所有颜色和圆角是否来自现有 token？
- 正负数据的颜色语义是否正确？
- Button、Tab 和导航的状态是否完整？
- 本地图标和股票 Logo 是否保留？
- 页面结构是否符合已批准的页面骨架？
- 产品经理和设计师是否无需额外解释就能理解输出？
