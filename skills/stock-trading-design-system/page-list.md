# 页面清单

本文件定义已批准的页面，以及每类页面应包含的内容。

## 核心产品页面

### Aktivitas

- 定位：首页投资组合和近期活动入口
- 必需模块：
  - `Top App Bar`
  - `Balance Summary`
  - `Quick Action Button`
  - `Watchlist`
  - `Bottom Navigation`
- 可选模块：
  - 次级摘要 Chip
  - 最近交易预览
- 组合规则：先放一个明确的余额焦点，再放操作行，最后放行情或活动模块。

### Trending

- 定位：行情发现和市场扫描
- 必需模块：
  - `Top App Bar`
  - `Segment Tab`
  - `Trending Carousel`
  - `Market Filter Header`
  - `Stock List Item`
  - `Bottom Navigation`
- 可选模块：
  - 使用 `Filter Select` 的时间筛选
  - 次级分类 Tab
- 组合规则：内容要紧凑、便于扫描，避免过大的 Hero 内容。

### Detail Saham

- 定位：个股详情和决策辅助
- 必需模块：
  - `Top App Bar`
  - 价格标题区
  - `Key Stats`
  - 图表或涨跌区
  - 主要操作区
- 可选模块：
  - 相关行情条目
  - 市场资讯摘要
- 组合规则：先展示价格上下文，再展示支持指标，最后展示操作入口。

### Topup Buying Power 1

- 定位：输入充值金额
- 必需模块：
  - `Top App Bar`
  - `Payment Stepper`
  - `Amount Input`
  - `Amount Presets`
  - 主要 CTA
- 组合规则：先做金额决策，支付方式后置。

### Topup Buying Power 2

- 定位：选择充值方式
- 必需模块：
  - `Top App Bar`
  - `Payment Stepper`
  - `Payment Method List`
  - `Top Up Destination`
  - 主要 CTA
- 组合规则：选择行要容易阅读，选中状态要清晰。

### Topup Buying Power 3

- 定位：确认或完成支付
- 必需模块：
  - `Top App Bar`
  - `Payment Stepper`
  - 确认摘要
  - 支付方式回顾
  - 主要 CTA 或完成状态
- 组合规则：提交前先总结确认，不要重新引入探索型内容。

## 设计系统页面

这些是文档页面，不是产品页面。

### Design System / Components

- 定位：原子组件和可复用组件库
- 应包含：
  - 可投入生产的组件
  - 变体集合
  - 图标和 Logo 清单
- 不应包含：
  - 与组件库混在同一区域的随机 Section 演示

### Design System / Examples

- 定位：用法示例和页面组装演示
- 规则：示例可以扩展原页面结构，但仍必须使用真实组件体系。

### Design System / Sections

- 定位：可复用业务模块模式
- 规则：这里的 Section 组件必须对应真实页面用例。

### Design System / Handbook

- 定位：基础规范和使用方式的视觉手册
- 规则：即使读者英文能力较弱，手册内容也必须清晰可读。

### Design System / Color Palette

- 定位：颜色阶梯和调色板参考
- 规则：这里是参考资料，不是随意发明新语义色的地方。

## 跨页面通用规则

1. 所有主要 App 页面使用 `375px` 宽度。
2. 主内容宽度保持 `343px`，只有明确需要贴边的区块才使用 `360px`。
3. 每个任务区只保留一个主要 CTA。
4. Bottom Navigation 只固定在 App 级页面，不固定在临时弹窗或文档页面。
5. 各页面复用同一套行情行和充值模式。

## 页面扩展规则

新需求如果不能完全对应现有页面，先映射到最接近的页面骨架：

- 投资组合或活动 = `Aktivitas`
- 行情扫描 = `Trending`
- 资产深度查看 = `Detail Saham`
- 多步骤资金操作 = `Topup Buying Power`
