# 组件规范

本文件定义已批准的组件、使用方式以及稳定 API 的含义。

## 使用规则

1. 绘制新 Frame 之前先复用已有组件。
2. 保留 `tokens.json` 中的组件属性名。
3. 图标或 Logo 插槽使用本地组件实例。
4. 为导航、操作、盯盘、触发器、股票 Logo 或支付位置选择图标前，先检查 `assets/icon-index.json`。
5. 先补齐状态，再考虑新增视觉样式。
6. Section 组件是可复用模式，不是一次性布局。

## 所有组件的基础尺寸

- 屏幕宽度基准：`375px`
- 卡片圆角基准：`12px`
- 紧凑控件圆角基准：`6px`
- 主要垂直节奏：`16px`
- 页面左右边距：`20px`
- 主要操作高度：`48px` 和 `40px`

## 导航组件

### Top App Bar

- 用途：展示页面标题和顶层导航
- 组件名称：`Stock Trading / Navigation / Top App Bar`
- 必需属性：
  - `Title`
  - `Leading Icon`
  - `Trailing Icon`
  - `Leading`
  - `Trailing`
- 适用页面：
  - `Aktivitas`
  - `Trending`
  - `Detail Saham`
  - 充值流程各步骤

### Bottom Navigation

- 用途：App 级主导航
- 组件名称：`Stock Trading / Navigation / Bottom Navigation`
- 必需属性：
  - `Activity Label`
  - `Trending Label`
  - `Top Up Label`
  - `Market Label`
  - `Profile Label`
  - `Selected`
- 规则：不要拆离；选中项必须反映当前页面。

## 操作组件

### Primary Button

- 用途：主要行动入口
- 尺寸：`Large`、`Medium`
- 状态：`Default`、`Pressed`、`Focus`、`Disabled`、`Loading`
- 图标模式：`None`、`Leading`
- 适用场景：
  - 支付确认
  - 充值流程推进
  - 关键单步操作

### Icon Button

- 用途：紧凑的工具操作
- 状态：`Default`、`Pressed`、`Focus`、`Disabled`
- 规则：用于纯图标操作，不用于页面主要 CTA。
- 图标规则：图标含义必须来自 `assets/icon-index.json`，不能只因为外形相似就选择图标。

### Text Button

- 用途：次要操作和低强调导航
- 尺寸：`Medium`、`Small`
- 状态：`Default`、`Pressed`、`Disabled`
- 常用文案：
  - `Lihat Semua`
  - `Ganti`

### Quick Action Button

- 用途：快速执行投资组合操作
- 操作：`Deposit`、`Withdraw`
- 状态：`Default`、`Pressed`、`Focus`、`Disabled`

## 数据发现组件

### Segment Tab

- 用途：短分类之间的切换
- 状态：`Selected`、`Default`、`Pressed`、`Disabled`
- 规则：用于行情分组，不用于过长的筛选器。

### Filter Select

- 用途：紧凑的时间或筛选选择器
- 状态：`Default`、`Pressed`、`Focus`、`Disabled`

### Market Trend Card

- 用途：紧凑的市场重点卡片
- 状态：`Default`、`Pressed`、`Focus`
- 涨跌模式：`Positive`、`Negative`
- 必需属性：
  - `Ticker`
  - `Price`
  - `Change Label`
  - `Logo`

### Stock List Item

- 用途：密集型行情列表行
- 密度：`Default`、`Compact`
- 涨跌模式：`Positive`、`Negative`、`Neutral`
- 必需属性：
  - `Ticker`
  - `Company Name`
  - `Price`
  - `Change Label`
  - `Logo`
- 规则：Logo 必须使用本地股票 Logo 组件，不能使用占位符。

### Key Stat Row

- 用途：详情页中的紧凑指标行
- 必需属性：
  - `Metric Label`
  - `Metric Value`
  - `Divider`

## 充值和支付组件

### Payment Stepper

- 用途：展示多步骤充值进度
- 必需属性：
  - `Step One Label`
  - `Step Two Label`
  - `Current Step`

### Payment Method Item

- 用途：可选择的充值方式列表行
- 状态：`Selected`、`Default`、`Pressed`、`Disabled`
- 必需属性：
  - `Method Label`
  - `Method Icon`

### Amount Chip

- 用途：选择预设金额
- 状态：`Default`、`Selected`、`Pressed`、`Disabled`
- 必需属性：
  - `Amount`

### Amount Input

- 用途：输入自定义金额
- 状态：`Default`、`Focused`、`Filled`、`Error`、`Disabled`
- 必需属性：
  - `Value`

## Section 组件

以下是可复用的业务区块，比原子组件更大，应该用于页面组装：

- `Balance Summary`
- `Trending Carousel`
- `Watchlist`
- `Market Filter Header`
- `Payment Method List`
- `Amount Presets`
- `Top Up Destination`
- `Key Stats`

规则：

- 构建相同业务结构的页面时优先复用这些模式。
- 已有模式能够满足需求时，不要另造一个 Section 外壳。

## 命名规则

- 组件名称保留 Title Case。
- 属性名称保持可读且稳定。
- 状态名称保持简短明确。
- 不要为了匹配某个局部 Frame 的文案而重命名属性。

## 审查清单

- 是否使用了真实组件实例？
- 是否保留了正确的状态模型？
- 是否保留了正确的本地图标或 Logo？
- 语义颜色是否一致？
- 组件 API 是否同时便于产品经理、设计师和开发人员理解？
