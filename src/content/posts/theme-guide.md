---
title: '主题指南'
pubDate: '2025-07-10'
---

Chiri 是一个使用 [Astro](https://astro.build) 构建的极简博客主题，它在保持清爽美感的同时提供了丰富的自定义选项。

---

## 基本命令

- `pnpm new <title>` - 创建新文章（草稿请使用 `_title`）
- `pnpm update-theme` - 更新主题到最新版本

## 主要文件与目录

- `src/content/about/about.md` - 编辑首页“关于”部分内容。如果不想显示内容，可以留空。
- `src/content/posts/` - 博客文章存放目录
- `src/config.ts` - 配置站点信息和设置

```ts
// 站点信息
site: {
  website: 'https://chiri.the3ash.com/', // 站点域名
  title: 'CHIRI', // 站点标题
  author: '3ASH', // 作者名称
  description: 'Minimal blog built by Astro', // 站点描述
  language: 'en-US' // 默认语言
},
```

```ts
// 通用设置
general: {
  contentWidth: '35rem', // 内容区宽度
  centeredLayout: true, // 中央布局（false 为左对齐）
  themeToggle: false, // 显示主题切换按钮（默认使用系统主题）
  postListDottedDivider: false, // 文章列表是否显示点状分隔线
  footer: true, // 显示页脚
  fadeAnimation: true // 启用淡入淡出动画
},
```

```ts
// 日期设置
date: {
  dateFormat: 'YYYY-MM-DD', // 日期格式：YYYY-MM-DD、MM-DD-YYYY、DD-MM-YYYY、MONTH DAY YYYY、DAY MONTH YYYY
  dateSeparator: '.', // 日期分隔符：. - /（MONTH DAY YYYY 和 DAY MONTH YYYY 除外）
  dateOnRight: true // 文章列表中日期位置（true 为右侧，false 为左侧）
},
```

```ts
// 文章设置
post: {
  readingTime: false, // 是否显示阅读时间
  toc: true, // 是否显示目录（当页面宽度足够时）
  imageViewer: true, // 启用图片查看器
  copyCode: true, // 启用代码块复制按钮
  linkCard: true, // 启用链接卡片
  katex: true // 启用 KaTeX 公式渲染
}
```

## 文章 Frontmatter

仅需 `title` 和 `pubDate` 两个必填字段

```ts
---
title: '文章标题'
pubDate: '2025-07-10'
---
```

## 语法高亮

你可以在 `astro.config.ts` 中通过 `shikiConfig` 配置主题。

更多详情： [Syntax Highlighting | Astro Docs](https://docs.astro.build/en/guides/syntax-highlighting/)

```ts
import { defineConfig } from 'astro/config'

export default defineConfig({
  markdown: {
    shikiConfig: {
      light: 'github-light',
      dark: 'github-dark',
      wrap: false
    }
  }
})
```

---

## 功能预览

![Theme Toggle](./_assets/theme-toggle.webp)

![Dotted Divider](./_assets/dotted-divider.webp)

![Date on Left Side](./_assets/date-on-left.webp)

![Table of Contents](./_assets/toc.webp)

![Reading Time](./_assets/reading-time.webp)

![Copy Code](./_assets/copy-code.webp)
