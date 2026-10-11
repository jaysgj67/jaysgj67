# 我的角落 · 个人主页（路线 D：有机流体 The Living Canvas）

无框架静态站点，可直接部署到 GitHub Pages。

## 本地预览

```bash
python3 -m http.server 8000
# 打开 http://localhost:8000
```

## 替换成你的内容

打开 `index.html`，全文搜索 `TODO` 注释，逐条替换：

| 位置 | 说明 |
| --- | --- |
| 顶部栏 / Hero | 你的名字、角色、一句话介绍、现居、方向、状态 |
| Now 板块 | 当前在做的事（2–4 条） |
| 手记 Journal | 便签条目（日常 / 周报 / 年报），带「示例」标签的均为占位 |
| 项目 Projects | 项目卡片（复制 `article.pcard` 即可增加，换封面色 `cover--pink/sage/mustard/lilac`） |
| 书单 Publications | 文章 / 论文 / 图书，替换标题、出处、DOI/ISBN/链接 |
| 联系 Contact | 社交账号、邮箱；将 `cv.pdf` 放到站点根目录后 CV 按钮即可下载 |
| `feed.xml` | 更新 RSS 标题、链接、条目 |

替换完成后删除各处的「示例」标签与 `sample-note` 提示。

## 部署（GitHub Pages · 已完成）

本站已部署：<https://jaysgj67.github.io/jaysgj67/>

- 仓库：`jaysgj67/jaysgj67`（公开）
- 方式：**Settings → Pages → Source: Deploy from a branch（main / root）**
- 更新：本地改完内容后 `git push origin main`，Pages 会自动重新构建，约 1 分钟内生效。

> 当前站点内文字均为「示例」占位（带 `sample-note` 提示），替换内容见上表。

## 技术说明

- 字体：Libre Caslon Text（正文衬线）+ Noto Serif SC（中文）+ Caveat（手写标注），Google Fonts 加载。
- 有机流体背景：CSS 模糊渐变光斑（`blob` 元素），纯 CSS 漂移动画，无 WebGL、无图片资源；`prefers-reduced-motion` 下自动关闭。
- 纸张噪点：CSS `feTurbulence` 内联 SVG 全屏覆盖，不依赖图片。
- 无构建步骤、无框架。
