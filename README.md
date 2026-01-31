# No Ego

个人博客，基于 Jekyll，托管在 GitHub Pages。

## 域名

no-ego.com

## 如何发布新文章

### 1. 创建文件

在 `_posts` 文件夹里新建一个 `.md` 文件。

文件名格式：`年-月-日-标题.md`

例如：
```
2026-02-01-新的一天.md
2026-02-05-some-thoughts.md
```

### 2. 写文章

文件开头必须有这几行（叫 front matter）：

```markdown
---
layout: post
title: 你的文章标题
date: 2026-02-01
---

正文从这里开始写...
```

### 3. 正文格式

用 Markdown 语法：

```markdown
普通段落直接写。

**加粗** 用两个星号。

*斜体* 用一个星号。

> 引用用大于号

- 列表用横杠
- 第二项
- 第三项

[链接文字](https://example.com)
```

### 4. 发布

保存文件后：

```bash
git add .
git commit -m "新文章：文章标题"
git push
```

等1-2分钟，GitHub 会自动构建，文章就上线了。

## 本地预览（可选）

如果想在发布前看效果：

```bash
# 安装依赖（只需要做一次）
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 打开浏览器访问 http://localhost:4000
```

## 文件结构

```
no-ego/
├── _config.yml      # 网站配置（一般不用改）
├── _posts/          # 所有文章放这里
├── _layouts/        # 页面模板（不用动）
├── _includes/       # 组件（不用动）
├── _pages/          # 固定页面（归档页等）
├── assets/css/      # 样式文件
├── index.html       # 首页
└── README.md        # 本文件
```

## 修改个人信息

编辑 `_config.yml`：

```yaml
author:
  name: "你的名字"
  email: "your@email.com"
  bio_en: "英文简介"
  bio_cn: "中文简介"
```

## 绑定域名

1. 在仓库根目录创建 `CNAME` 文件，内容只写一行：
   ```
   no-ego.com
   ```

2. 在域名服务商那里，添加 DNS 记录：
   - 类型：CNAME
   - 名称：@（或 www）
   - 值：你的github用户名.github.io

3. 在 GitHub 仓库的 Settings → Pages 里确认域名设置。

## 注意事项

- 文件名不要用中文，用拼音或英文
- 日期格式必须是 `YYYY-MM-DD`
- 图片尽量少用，如果用，放在 `assets/images/` 里

---

No Ego, No Enemy.
