# 行情发现页骨架

## 适用场景

- `Trending`
- 按分类浏览行情
- 包含多个数据分组的密集扫描页面

## 结构

1. 顶部 App Bar
2. 短分类或 Tab 控件
3. 紧凑趋势卡片或重点摘要
4. 筛选标题区
5. 密集股票列表
6. 底部导航

## 布局规则

- 优先保证扫描节奏，不追求装饰性布局。
- 卡片保持紧凑。
- 列表行保持一致。
- 筛选项尽量短，并尽可能保持单行。

## 内容规则

- Tab 用于行情分组，不用于长句子。
- 趋势卡片要短，先展示 Logo，再展示数字。
- 列表行必须保留 ticker、公司名、价格和涨跌。

## 常用组件

- `Top App Bar`
- `Segment Tab`
- `Market Trend Card`
- `Filter Select`
- `Market Filter Header`
- `Stock List Item`
- `Bottom Navigation`
