# 变更记录

## 2026.07.13

### 新增

- 新增包含 24 个可复用 App 图标的 `assets/icons/common-icons/icon-sprite.svg`
- 新增机器可读的图标注册表 `assets/icons/icon-map.json`
- 当前 HTML 原型改为使用内联 Sprite 引用，不再使用页面专属的通用 SVG 路径

### 说明

- CSS 控制图标尺寸、颜色和状态；SVG 保存图标几何；JSON 将 ID 映射到资源
- 特殊页面图标可以是临时方案，但已批准的通用图标必须复用

## 2026.07.10

### 新增

- 新增第一版语义图标/Logo 使用索引 `assets/icon-index.json`
- 覆盖导航、操作、自选、持仓、盯盘、触发器、行情、支付和股票 Logo 场景
- 为图标审核增加中文名称和含义

### 调整

- 更新 `SKILL.md` 路由，使图标/Logo 相关任务读取 `assets/icon-index.json`
- 加强对通用图标，以及“外形相似但语义错误”图标的限制

## 2026.05.18

### 新增

- 将 Skill 从轻量 token 包扩展为可用于团队协作的设计系统 Skill
- 重写 `SKILL.md`，增加任务路由、强制规则和最终自检
- 新增 `GLOSSARY.md`、`INSTALL.md`、`components.md` 和 `page-list.md`
- 新增面向代码使用的 token 入口文件 `design-tokens.css`
- 新增可复用页面组合模式目录 `page-shells/`
- 新增业务领域规则目录 `product-lines/`
- 新增常见问题和修复规则目录 `case-studies/`

### 说明

- 根据 Figma 源文件正式确定核心页面清单
- 确定角色型字体命名体系
- 明确这个 Skill 同时服务产品经理、设计和开发协作

### 备注

- `tokens.json` 仍是结构化 token 的权威来源
- `component-variables.css` 仍然有效，并为向后兼容保留
