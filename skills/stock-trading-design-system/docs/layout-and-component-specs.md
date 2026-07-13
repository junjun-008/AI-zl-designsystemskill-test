# 布局和组件尺寸规范

本文件记录 Stock Trading App 页面和设计系统所需的具体尺寸。与 `tokens.json` 和 `component-variables.css` 一起使用。

## 页面网格

| 项目 | 数值 | Token / 说明 |
|---|---:|---|
| 移动端屏幕宽度 | 375px | `size/screen/mobile-width` |
| 默认页面左右边距 | 20px | 左右两侧使用 |
| 默认内容宽度 | 343px | 375px - 40px |
| 宽内容宽度 | 360px | 只用于需要贴边的模块 |
| 顶部安全区 | 24px+ | 取决于设备 |
| 主要模块垂直间距 | 16px | 堆叠模块之间使用 |
| 页面背景 | `#12121C` | `color/bg/app` |

## 卡片和 Section 结构

| 项目 | 数值 | Token / 说明 |
|---|---:|---|
| 卡片填充 | `rgba(37, 36, 50, 0.4)` | `color/bg/surface` |
| 不透明回退填充 | `#252432` | 透明度无法表达时用于文档或导出 |
| 卡片边框 | 1px | `stroke/hairline` |
| 卡片边框颜色 | `#3A3A47` | `color/border/default` |
| 强调边框 | `#7FDF9A` | `color/border/accent` |
| 卡片圆角 | 12px | `radius/xl` |
| 默认卡片内边距 | 20px | 业务模块使用 |
| 紧凑卡片内边距 | 16px | 密集组件演示使用 |
| 卡片内部间距 | 16px | 主要垂直节奏 |
| 标题到辅助文字间距 | 6-8px | Section 标题保持紧凑 |
| 卡片之间垂直间距 | 16px | 默认页面节奏 |

## 控件

| 组件 | 数值 | 说明 |
|---|---:|---|
| 大号 Primary Button 高度 | 48px | 主要 CTA |
| 中号 Primary Button 高度 | 40px | 紧凑操作 |
| Button 左右内边距 | 16px | 默认值 |
| Button 图标与文字间距 | 8px | 默认值 |
| Button 圆角 | 6px | `radius/md` |
| Icon Button 尺寸 | 40px | 内部使用 24px 图标 |
| Segment Tab 高度 | 28px | 筛选 Tab |
| Amount Chip 高度 | 40px | 两列预设金额网格 |
| 输入框高度 | 44-56px | 取决于状态和上下文 |
| Payment Method 行高 | 56px | 可选择行 |
| Payment Method 圆角 | 6px | `radius/md` |
| Bottom Navigation 高度 | 68px | 固定底部区域 |
| 最小触控目标 | 40px | 原型中不要低于此尺寸 |

## 行情列表和数据卡片

| 组件部分 | 数值 | 说明 |
|---|---:|---|
| 默认股票行高度 | 56px | `Stock List Item / Density=Default` |
| 紧凑股票行高度 | 44px | `Stock List Item / Density=Compact` |
| 股票 Logo 尺寸 | 24px | 使用本地 Logo 组件 |
| Logo 到文字间距 | 12px | 默认行间距 |
| Ticker 文字 | 16px / 19px | 大号 Body，半粗 |
| 公司文字 | 12px / 14px | 小号 Body |
| 价格文字 | 16px / 19px | 右对齐 |
| 涨跌文字 | 12px / 14px | 使用正向或负向颜色 |
| 行情卡片宽度 | 100px | 紧凑横向 Carousel 卡片 |
| 行情卡片高度 | 98px | 紧凑横向 Carousel 卡片 |
| 行情卡片圆角 | 6px | `radius/md` |

## 字体角色

使用 Material 风格的角色名称，不要用 H1/H2 标签。根据产品角色选择字体。

| 角色 | 字号 / 行高 / 字重 | 用途 |
|---|---|---|
| Display Medium | 36px / 42px / 600 | 投资组合余额和主要数字焦点 |
| Headline Small | 24px / 28px / 600 | 页面标题或主要模块标题 |
| Title Large | 22px / 26px / 600 | App Bar 标题和 Section 标题 |
| Body Large | 16px / 19px / 400-600 | Ticker、关键值和强调行内容 |
| Body Medium | 14px / 16px / 400 | 表单、按钮和普通行内容 |
| Body Small | 12px / 14px / 400 | 次要信息和公司名称 |
| Label Medium | 11px / 12px / 500 | 紧凑标签 |
| Label Small | 10px / 12px / 500 | 导航标签和密集元数据 |

规则：

- 字距始终为 `0`。
- 不要根据视口宽度缩放字号。
- 正负颜色只用于行情变化、激活状态、成功、错误或下跌数据。
- 标签长度必须适合 375px 移动端宽度。

## 页面组合规则

1. 所有移动页面从 375px 宽度和 20px 左右边距开始。
2. 主要模块使用 343px 内容宽度。
3. 分组内容使用 20px 内边距和 12px 圆角的 Section 卡片。
4. 主要模块之间使用 16px 垂直节奏。
5. 使用可复用组件状态，不要复制脱离组件体系的 Frame。
6. 行情行和自选列表使用 `Stock List Item`。
7. 紧凑横向行情卡片使用 `Market Trend Card`。
8. 可选择的资金方式使用 `Payment Method Item`。
9. 预设金额选择使用 `Amount Chip`。
10. 每个页面或任务区只保留一个主要 CTA。
11. App 页面中不要引入营销 Hero 布局。
12. 未经设计系统批准，不要新增按钮样式。
