<div align="center">

<img src="https://utterlog.com/icon.svg" width="96" height="96" alt="Utterlog" />

# Utterlog

**为独立作者打造的一体化内容平台**

</div>

<p align="center">
  <a href="https://demo.utterlog.io"><img src="https://img.shields.io/badge/Live%20Demo-demo.utterlog.io-22c55e?style=for-the-badge&logo=safari&logoColor=white" alt="Live Demo"></a>
  <a href="https://utterlog.io"><img src="https://img.shields.io/badge/Project-utterlog.io-3b82f6?style=for-the-badge&logo=hugo&logoColor=white" alt="Project Site"></a>
  <a href="https://utterlog.com"><img src="https://img.shields.io/badge/Network-utterlog.com-8b5cf6?style=for-the-badge&logo=mastodon&logoColor=white" alt="Federation Hub"></a>
</p>

<p align="center">
  <a href="https://github.com/utterlog/utterlog/actions/workflows/ci.yml"><img src="https://img.shields.io/github/actions/workflow/status/utterlog/utterlog/ci.yml?branch=main&style=flat-square&label=CI" alt="CI"></a>
  <a href="https://github.com/utterlog/utterlog/actions/workflows/docker-publish.yml"><img src="https://img.shields.io/github/actions/workflow/status/utterlog/utterlog/docker-publish.yml?branch=main&style=flat-square&label=docker%20images&logo=docker&logoColor=white" alt="Docker images"></a>
  <a href="https://github.com/utterlog/utterlog/blob/main/LICENSE"><img src="https://img.shields.io/github/license/utterlog/utterlog?style=flat-square" alt="License"></a>
  <img src="https://img.shields.io/github/go-mod/go-version/utterlog/utterlog?filename=api/go.mod&style=flat-square&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs" alt="Next.js">
  <img src="https://img.shields.io/badge/PostgreSQL-18-336791?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
</p>

---

## 是什么

为独立博主设计的全栈博客系统：兼顾内容创作自由、阅读体验和数据自主。

- **写作** — Markdown 编辑器、AI 辅助摘要 / 段落点评、图片 EXIF 自动解析、说说卡片流
- **阅读** — 5 套内置主题、自定义页脚按钮、pgvector 语义搜索、多主题切换
- **数据主权** — 完全自部署，从 WordPress / Typecho 一键导入
- **联盟身份** — Utterlog Network OAuth 跨站登录 / 评论 / 关注 / 段落点评，Passkey + 2FA
- **极简部署** — 一行命令，单端口对外，~600MB 内存可跑

## 一行部署

```bash
curl -fsSL https://raw.githubusercontent.com/utterlog/utterlog/main/install.sh | bash
```

带自动 HTTPS（无现成反代）：

```bash
curl -fsSL https://raw.githubusercontent.com/utterlog/utterlog/main/install.sh | DOMAIN=blog.yoursite.com bash
```

详细说明：[INSTALL.md](https://github.com/utterlog/utterlog/blob/main/INSTALL.md)

## 仓库

| 仓库 | 用途 |
|------|------|
| **[utterlog](https://github.com/utterlog/utterlog)** | 主项目 — 后端 (Go) + 博客前端 (Next.js) + 内嵌管理后台 (Vite SPA) |
| **[utterlog-sync](https://github.com/utterlog/utterlog-sync)** | WordPress 插件 — 导出 `.ulbk` 包或直推到 Utterlog 站点 |
| **[.github](https://github.com/utterlog/.github)** | 组织元数据（本 README + Issue 模板） |

## 三个官方站点

| 域名 | 角色 |
|------|------|
| [utterlog.io](https://utterlog.io) | 项目主站（文档、下载、博客） |
| [demo.utterlog.io](https://demo.utterlog.io) | 在线 Demo —— 体验完整功能 |
| [utterlog.com](https://utterlog.com) | 联盟中心 —— 自托管站点的内容聚合 + 跨站身份 |

## 技术栈

| 层 | 技术 |
|---|---|
| 博客前端 | Next.js 16 + React 19 + TypeScript 6 |
| 管理后台 | Vite + React + Zustand + TanStack Query（go:embed 内嵌） |
| 后端 | Go 1.26 + Gin + sqlx |
| 数据 | PostgreSQL 18 (pgvector) + Redis 7 |
| 部署 | Docker Compose + 可选内置 Caddy |

## 贡献

Issues / Pull Requests 欢迎。写作、翻译、主题、插件同样欢迎。

## 许可

MIT — 详见各仓库 LICENSE
