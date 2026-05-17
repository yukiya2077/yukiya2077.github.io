---
title: 'Markdown 样式指南'
pubDate: '2025-06-28'
---

本主题未定义更多标题级别。如有需要，可在 `src/styles/post.css` 中自行添加。

---

## 段落

下面是一个 Markdown 段落的示例，展示了博客文章中文本自然流动的样式。

你可以在段落中使用各种格式，比如 **加粗**、_斜体_、~~删除线~~ 和 `代码`。

## 引用

> 不要通过共享记忆来进行沟通，要通过沟通来共享记忆。<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: 上述引用摘自 Rob Pike 在 2015 年 11 月 18 日 Gopherfest 的[演讲](https://www.youtube.com/watch?v=PAAkCSZUG1c)。

### 有序列表

1. 第一项
2. 第二项
3. 第三项

### 无序列表

- 项目
  - 子项目
  - 子项目

## 任务列表

- [ ] 第一项
- [ ] 第二项
- [x] 第三项

## 图片

要隐藏标题，请在标题前加下划线 `_`，或将 alt 文本留空。

![HIKARI](./_assets/hikari.webp)

## 表格

| 样式     | 权重     | 其他    |
| -------- | -------- | ------- |
| 普通     | 常规     | 文本    |
| _斜体_   | **加粗** | `代码`  |

## 代码块

```jsx
// Button.jsx

const Button = ({ text, onClick }) => {
  const [count, setCount] = useState(0)

  const handleClick = () => {
    setCount(count + 1)
    onClick?.()
  }

  return (
    <button className="btn" onClick={handleClick}>
      {text} ({count})
    </button>
  )
}
```

## 其它元素 — sub、sup、abbr、kbd、mark

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

<abbr title="Graphics Interchange Format">GIF</abbr> 是一种位图图像格式。

按 <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> 结束会话。

大多数 <mark>蝾螈</mark> 是夜行性动物，会捕食昆虫、蠕虫和其它小型生物。

---
