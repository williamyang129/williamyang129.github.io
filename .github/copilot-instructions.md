# Copilot 指南

本文档为 AI 编码助手提供关于此 Jekyll 博客项目的重要指导。

## 项目概述

这是一个使用 Jekyll 和 GitHub Pages 搭建的个人博客网站。该项目基于 `minima` 主题，并支持数学公式渲染。

## 关键文件结构

- `_config.yml`: 站点配置文件，包含博客标题、描述、主题设置等
- `_posts/`: 博客文章目录，文章必须使用 `YYYY-MM-DD-title.md` 格式命名
- `_includes/`: 可重用的页面组件，如页眉、页脚等
- `assets/`: 样式表和其他静态资源
- `images/`: 图片资源目录
- `index.md`: 首页内容
- `about.md`: "关于"页面内容

## 工作流程

### 添加新博文

1. 在 `_posts/` 目录下创建新的 Markdown 文件
2. 文件名格式: `YYYY-MM-DD-title.md`
3. 文件开头需要包含 YAML front matter:
   ```yaml
   ---
   layout: post
   title: "文章标题"
   categories: [分类1, 分类2]
   ---
   ```

### 数学公式支持

本博客启用了 KaTeX 支持，可以渲染 LaTeX 数学公式：
- 行内公式使用单个 `$` 符号包裹
- 块级公式使用两个 `$` 符号包裹

### 主题定制

样式表位于 `assets/main.scss`，可以通过修改此文件来自定义主题样式。

## 依赖说明

主要 Jekyll 插件：
- jekyll-feed: RSS 订阅支持
- jekyll-gist: GitHub Gist 嵌入支持
- jekyll-octicons: GitHub 图标支持
- jekyll-github-metadata: GitHub 元数据支持

Markdown 引擎配置：
- 使用 kramdown 作为 Markdown 处理器
- 启用 GFM (GitHub Flavored Markdown)
- 使用 Rouge 作为代码高亮器
- 使用 KaTeX 作为数学公式渲染引擎

## 特殊约定

1. 所有图片应存放在 `images/` 目录下
2. 通过 `_includes/` 下的模板组件复用页面元素
3. 使用 `{: .class-name}` 语法添加 CSS 类