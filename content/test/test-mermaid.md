---
title: 测试Mermaid图表功能
permalink: mermaid-test
tags: [测试, mermaid, 图表, 流程图]
created: 2025-12-12
description: 这是一个测试Mermaid图表功能的页面，包含多种类型的图表示例
---

# 测试Mermaid图表功能

## 🎯 测试目标

这个页面用于测试 Quartz 的 Mermaid 图表渲染功能。

## 📊 图表类型测试

### 1. 流程图 (Flowchart)

```mermaid
flowchart TD
    A[开始] --> B{是否支持Mermaid?}
    B -->|是| C[渲染图表]
    B -->|否| D[显示代码块]
    C --> E[测试成功]
    D --> F[需要配置插件]
    F --> G[检查配置文件]
    G --> B
```

### 2. 序列图 (Sequence Diagram)

```mermaid
sequenceDiagram
    participant U as 用户
    participant B as 浏览器
    participant S as 服务器
    participant Q as Quartz

    U->>B: 访问页面
    B->>S: 请求HTML
    S->>Q: 处理Markdown
    Q->>Q: 渲染Mermaid图表
    Q->>S: 返回处理结果
    S->>B: 返回完整页面
    B->>U: 显示页面和图表
```

### 3. Git图 (Git Graph)

```mermaid
flowchart LR
    A[初始提交] --> B[更新文档]
    A --> C[创建feature分支]
    C --> D[添加功能]
    D --> E[修复bug]
    E --> F[合并到main]
    B --> F
    F --> G[发布版本]
```

### 4. 饼图 (Pie Chart)

```mermaid
pie title 数字花园内容分布
    "技术笔记" : 40
    "学习资源" : 25
    "项目记录" : 20
    "今日想法" : 10
    "测试文件" : 5
```

### 5. 甘特图 (Gantt Chart)

```mermaid
gantt
    title 数字花园开发计划
    dateFormat  YYYY-MM-DD
    section 基础设置
    环境配置           :done,    setup, 2025-12-01, 2025-12-02
    GitHub Pages部署   :done,    deploy, 2025-12-02, 2025-12-03
    section 功能测试
    Frontmatter测试    :done,    frontmatter, 2025-12-03, 2025-12-04
    Mermaid测试        :active,  mermaid, 2025-12-04, 2025-12-05
    section 内容创作
    技术笔记           :         content, 2025-12-05, 2025-12-10
    学习资源整理       :         resources, 2025-12-08, 2025-12-15
```

### 6. 时间线 (Timeline)

```mermaid
timeline
    title 数字花园发展历程

    2025-12-01 : 项目启动
               : 环境配置

    2025-12-02 : GitHub Pages部署
               : 基础配置完成

    2025-12-03 : Frontmatter功能测试
               : URL、别名、描述测试

    2025-12-04 : Mermaid图表测试
               : 多种图表类型验证
```

### 7. 类图 (Class Diagram)

```mermaid
classDiagram
    class DigitalGarden {
        +String title
        +String description
        +Array content
        +render()
        +deploy()
    }

    class Page {
        +String title
        +String permalink
        +Array tags
        +String content
        +render()
    }

    class MermaidChart {
        +String type
        +String syntax
        +render()
        +validate()
    }

    DigitalGarden *-- Page : contains
    Page *-- MermaidChart : includes
```

## 🔍 验证方法

### 预期结果
- ✅ 所有图表应该正确渲染为可视化图形
- ✅ 图表应该适配网站主题色彩
- ✅ 图表应该具有交互性（如果支持）

### 如果图表未显示
1. 检查是否显示为普通代码块
2. 确认 `ObsidianFlavoredMarkdown` 插件已启用
3. 确认插件顺序：`SyntaxHighlighting` 在 `ObsidianFlavoredMarkdown` 之前

## 🔗 相关链接

- [[技术笔记]]
- [Mermaid官方文档](https://mermaid.js.org/)
- [Quartz Mermaid支持说明](_docs/features/Mermaid diagrams.md)

---

*如果上面的图表都能正确显示，说明 Mermaid 功能正常工作！*