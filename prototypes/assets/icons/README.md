# 通用 Icon 资产

本目录保存股票交易 App 原型可复用的基础功能图标。

- `icon-map.json`：图标 ID、中文含义、分类和状态。
- `common-icons/icon-sprite.svg`：实际 SVG 图标资产。
- 页面使用 `<svg><use href="...#icon-id"></use></svg>` 调用图标。

通用图标优先复用；特殊页面图标可以临时绘制，但不能替代本目录已有图标，也要在交付说明中标记为临时方案。
