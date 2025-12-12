---
title: 测试别名重定向功能
permalink: aliases-test
aliases:
  - alias-test-1
  - alias-test-2
  - 别名测试
  - redirect-test
tags: [测试, 别名, aliases, 重定向]
created: 2025-12-12
description: 这是一个测试aliases别名重定向功能的页面，验证多个URL是否都能正确重定向到同一个页面
---

# 测试别名重定向功能

## 🔄 测试目标

这个页面用于测试 Quartz 的 `aliases` 别名重定向功能。

### 期望结果

以下所有URL都应该重定向到这个页面：
- `/aliases-test` (permalink)
- `/alias-test-1` (alias 1)
- `/alias-test-2` (alias 2)
- `/别名测试` (中文别名)
- `/redirect-test` (alias 4)
- `/test-aliases` (原始文件名)

### 功能说明

`aliases` 字段允许我们为页面设置多个别名URL，当用户访问任何一个别名URL时，都会自动重定向到主页面。这对以下场景很有用：

1. **URL重构**: 改变页面URL时保持旧链接有效
2. **多语言支持**: 同一内容提供不同语言的URL
3. **用户友好**: 提供更容易记忆的短链接
4. **SEO优化**: 整合多个相关URL的权重

## 📝 配置信息

```yaml
aliases:
  - alias-test-1
  - alias-test-2
  - 别名测试
  - redirect-test
```

## 🧪 测试方法

### 自动测试
系统会为每个别名创建重定向页面，访问时自动跳转。

### 手动验证
尝试访问以下URL，都应该跳转到当前页面：

1. `https://your-site.com/alias-test-1`
2. `https://your-site.com/alias-test-2`
3. `https://your-site.com/别名测试`
4. `https://your-site.com/redirect-test`

## ⚠️ 注意事项

- 别名必须是唯一的，不能与现有页面冲突
- 重定向是永久重定向（301）
- 中文别名会被URL编码
- 别名不支持路径分隔符（/）

## 📊 重定向类型

根据文档，Quartz 使用**永久重定向**：
- HTTP状态码: 301 Moved Permanently
- 搜索引擎会将权重转移到目标页面
- 浏览器会缓存重定向规则

## 🔗 相关链接

- [[技术笔记]]
- [[项目记录]]

---

*如果你能通过任何一个别名URL访问到这个页面，说明 aliases 功能正常工作！*