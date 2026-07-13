# 安装和使用指南

## 目的

这个 Skill 供产品经理、设计师和开发人员共同使用，让新需求、原型和实现提示词都遵循当前 Stock Trading 设计系统。

## 推荐目录

完整目录放在：

```text
.codex/skills/stock-trading-design-system/
```

请保留完整目录结构，不要只复制 `SKILL.md`。

## 必须同步的文件

以下文件应始终一起更新：

- `SKILL.md`
- `tokens.json`
- `design-tokens.css`
- `component-variables.css`
- `components.md`
- `page-list.md`

只复制部分文件会降低任务路由和使用质量。

## 团队使用方式

### 产品经理

以下场景使用本 Skill：

- 编写原型需求
- 描述新页面
- 审查方案是否符合当前 App 视觉语言

推荐阅读：

1. `SKILL.md`
2. `page-list.md`
3. `page-shells/` 中的一个文件
4. `product-lines/` 中的一个文件

### 设计师

以下场景使用本 Skill：

- 扩展现有 Figma 页面
- 创建新的组件状态
- 审查跨页面一致性

推荐阅读：

1. `SKILL.md`
2. `components.md`
3. `docs/layout-and-component-specs.md`
4. `case-studies/common-breakages.md`

### 开发人员

以下场景使用本 Skill：

- 构建 HTML/CSS 原型
- 根据设计实现页面
- 将组件 API 映射到代码属性

推荐阅读：

1. `SKILL.md`
2. `tokens.json`
3. `design-tokens.css`
4. `component-variables.css`
5. `components.md`

## 更新流程

当 Figma 组件库发生变化时：

1. 先更新 token
2. 再更新组件 API 说明
3. 然后更新页面规则
4. 最后在 `CHANGELOG.md` 记录变更

如果变化涉及命名，也要同步更新 `GLOSSARY.md`。

## 发布前检查

发布新的 Skill 版本前：

- 确认页面清单仍与 Figma 文件一致
- 确认核心组件仍然存在且名称不变
- 确认 token 名称仍与导出的 CSS 变量一致
- 确认产品经理和设计师无需内部背景也能读懂文档

## 分发说明

如果通过压缩包或内部知识库共享，请发布完整目录，不要只发布单个文件。本 Skill 依赖多个文件之间的路由关系。
