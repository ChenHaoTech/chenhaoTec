---
title: 测试头图功能
permalink: cover-image-test
cover: images/test-cover.svg
tags: [测试, 头图, cover]
created: 2025-12-12
description: 这是一个测试cover头图功能的页面，验证图片是否正确显示
---

# 测试头图功能

## 🖼️ 测试目标

这个页面用于测试 Quartz 的 `cover` 头图功能。

### 期望结果

- **头图路径**: `./images/test-cover.svg`
- **期望效果**: 页面顶部应该显示紫色渐变背景的测试图片
- **图片内容**: 包含"测试头图"和"Test Cover Image"文字

### 功能说明

`cover` 字段允许我们为页面设置头图，这个图片会显示在页面顶部，同时也会用作社交分享时的预览图。

## 📝 配置信息

```yaml
cover: images/test-cover.svg
```

### 支持的图片格式

根据文档，Quartz 支持多种头图字段：
- `cover`
- `image`
- `socialImage`

## 🎨 图片描述

测试图片特征：
- **尺寸**: 400x200 像素
- **背景**: 紫色渐变（从 #667eea 到 #764ba2）
- **文字**: 白色"测试头图"和"Test Cover Image"
- **装饰**: 几个半透明的圆形和矩形元素

## 🔗 相关链接

- [[技术笔记]]
- [[项目记录]]

---

*如果页面顶部显示了紫色渐变的测试图片，说明 cover 功能正常工作！*