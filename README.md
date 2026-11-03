# King - 个人网站

基于 Hugo 和 Stack 主题搭建的个人网站，用于记录项目、技术文章与个人经历。

线上地址：https://kinguang3.github.io/King/

## 文章

- [学习 Pi Agent 的工作流](https://kinguang3.github.io/King/p/pi-agent-workflow/) - 最小化 Agent Harness 的自我规划与任务处理
- [GBC Nina - 住在你桌面上的小猫](https://kinguang3.github.io/King/p/gbc-nina/) - 基于 Python + PySide6 的 Windows 桌面宠物

## 项目

更多项目见 [项目页](https://kinguang3.github.io/King/projects/)，主要包括：

- **TheNook** - 推理小说发现与收藏平台
- **GBC Nina / Deskpot-Pet-Cat** - Windows 桌面宠物
- **Nexus** - LangChain Agent 框架
- **Card-Forge** - 卡牌设计与实时预览工具

## 特性

- 关于、项目、归档与搜索页面
- 响应式布局与暗色模式
- 首页点阵光晕动态背景（跟随鼠标）
- 全文搜索
- 文章目录与分页
- GitHub Pages 自动部署

## 技术栈

- **Hugo** - 静态网站生成器
- **Stack Theme** - Hugo 个人博客主题
- **GitHub Pages** - 托管平台
- **GitHub Actions** - 持续集成与自动部署

## 本地开发

### 环境要求

- Hugo Extended 0.150.1 或更高版本
- Git

### 启动

```bash
# 克隆仓库
git clone https://github.com/kinguang3/King.git
cd King

# 本地预览
hugo server

# 生产构建
hugo --minify
```

### 预览地址

- 本地开发：http://localhost:1313/King/
- 线上站点：https://kinguang3.github.io/King/

## 目录结构

```
.
├── archetypes/               # 内容模板
├── assets/                   # 头像、编辑器配置等资源
├── content/                  # 页面与文章
│   ├── _index.zh-cn.md       # 首页配置
│   ├── page/                 # 关于、项目、归档、搜索
│   └── post/                 # 博客文章
├── layouts/partials/         # 首页背景等自定义模板
├── static/                   # 静态文件（favicon）
├── themes/hugo-theme-stack/  # Hugo 主题
├── .github/workflows/        # GitHub Actions 工作流
├── hugo.yaml                 # Hugo 站点配置
└── .gitignore                # Git 忽略规则
```

## 部署

推送代码到 `main` 分支后，GitHub Actions 会自动构建并部署到 GitHub Pages。

手动构建：

```bash
hugo --minify
```

构建产物位于 `public/` 目录。

## 配置说明

站点配置位于 `hugo.yaml`：

```yaml
baseurl: https://kinguang3.github.io/King
theme: hugo-theme-stack
DefaultContentLanguage: zh-cn
```

- 站点语言为简体中文，未启用其他语言
- 评论功能默认关闭，可在 `params.comments` 中开启
- 首页背景效果位于 `layouts/partials/head/custom.html` 与 `layouts/partials/footer/custom.html`，仅作用于首页

## 许可

本项目仅供个人使用。

## 致谢

- [Hugo](https://gohugo.io/)
- [Stack Theme](https://github.com/CaiJimmy/hugo-theme-stack)
