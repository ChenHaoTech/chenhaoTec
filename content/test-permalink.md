---
title: 测试自定义URL功能
permalink: custom-url-test
tags: [测试, URL, permalink]
created: 2025-12-12
description: 这是一个测试permalink功能的页面，验证自定义URL是否生效
---

# 测试自定义URL功能

## 🎯 测试目标

这个页面用于测试 Quartz 的 `permalink` 功能。

### 期望结果

- **文件名**: `test-permalink.md`
- **期望URL**: `/custom-url-test`
- **实际访问**: 应该可以通过自定义URL访问，而不是文件名URL

### 功能说明

`permalink` 字段允许我们为页面设置自定义的URL，这样即使文件名改变，URL也能保持不变，有利于SEO和链接稳定性。

## 📝 配置信息

```yaml
permalink: custom-url-test
```

## 🔗 相关链接

- [[技术笔记]]
- [[项目记录]]

---

*如果你能通过 `/custom-url-test` 访问到这个页面，说明 permalink 功能正常工作！*