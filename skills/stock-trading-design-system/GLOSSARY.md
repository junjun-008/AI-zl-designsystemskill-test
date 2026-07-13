# 术语表

## 核心术语

### 设计系统（Design System）

用于约束 token、组件、页面结构和文档的一整套规则，确保新输出与现有 Stock Trading App 保持一致。

### 设计 token（Token）

有名称的设计值，例如颜色、间距、圆角、描边、尺寸、字体或效果。本 Skill 使用 `tokens.json` 作为结构化来源。

### 语义 token（Semantic Token）

描述使用场景而不是裸值的产品侧 token 名称，例如 `color/text/positive`。

### 原始 token（Primitive Token）

用于构建语义 token 的原始值分组，例如 `primitive.color.neutral.900`。

### 组件（Component）

具有稳定 API 的可复用 UI 元素，例如 `Primary Button` 或 `Stock List Item`。

### 模式组件（Pattern Component）

由多个小组件构成的较大业务区块，例如 `Watchlist` 或 `Payment Method List`。

### 页面骨架（Page Shell）

可复用的页面组合结构，定义模块顺序、间距节奏和导航结构。

### 业务线覆盖规则（Product Line Overlay）

根据业务领域调整文案、模块和信息重点的规则层，但不能借此创造新的视觉语言。

## 命名术语

### 角色型字体命名（Role-Based Typography）

当前批准的文字样式命名：

- `Display`
- `Headline`
- `Title`
- `Body`
- `Label`

项目工作命名中不要使用 `H1 / H2 / body1 / body2`。

### 密度（Density）

组件内容的紧凑程度。例如 `Stock List Item` 支持 `Default` 和 `Compact`。

### 状态（State）

组件的交互或语义模式，例如：

- `Default`
- `Pressed`
- `Focus`
- `Disabled`
- `Selected`
- `Positive`
- `Negative`

### 实例替换（Instance Swap）

Figma 组件属性，允许替换嵌套的图标或股票 Logo，而不拆离父组件。

## 页面术语

### Aktivitas

投资组合和近期活动页面，重点是余额摘要、快捷操作、自选和底部导航。

### Trending

行情发现页面，重点是 Tab、趋势卡片、市场筛选和密集股票列表。

### Detail Saham

个股详情页面，重点是价格上下文、关键指标、市场变化和操作入口。

### 充值流程（Top Up Flow）

三步资金流程：

1. 输入金额
2. 选择支付方式
3. 完成或确认

## 视觉语言术语

### App 背景（App Background）

主要的深色画布颜色，通常对应 `color/bg/app`。

### 提升层（Elevated Surface）

层级更高或区隔更明显的表面，通常对应 `color/bg/elevated`。

### 玻璃表面（Glass Surface）

当前 App 语言中的半透明卡片层，通常对应 `color/bg/surface`。

### Section 卡片（Section Card）

一个分组业务模块，通常具备：

- `12px` 圆角
- `20px` 内边距
- `1px` 边框
- 深色半透明或实体表面填充

### 正向变化（Positive Movement）

价格或数据上升，使用绿色语义 token。

### 负向变化（Negative Movement）

价格或数据下降，使用红色语义 token。

## 治理术语

### 权威来源（Source Of Truth）

某一类内容应该优先信任的文件：

- 结构化数值：`tokens.json`
- CSS 变量：`design-tokens.css`
- 组件 API：`tokens.json` 加 `components.md`
- 页面组合：`page-list.md` 加 `page-shells/`

### 拆离组件债务（Detached Frame Debt）

页面只复制组件外观、没有复用真实组件实例时产生的设计债务。

### Logo 完整性（Logo Integrity）

股票列表行和市场卡片必须保留正确的本地 Logo 组件，不能回退到通用占位符。
