<div align="center">

<img src="https://avatars.githubusercontent.com/u/275732418?v=4" width="96" height="96" alt="Utterlog" />

# Utterlog

**现代化博客平台 · Modern self-hosted blogging**

[utterlog.io](https://utterlog.io) · [dev@utterlog.com](mailto:dev@utterlog.com)

</div>

---

## 是什么

Utterlog 是一个为独立博主设计的全栈博客系统 —— 兼顾内容创作自由、阅读体验和数据自主。

- **写作** —— Markdown 编辑器、AI 辅助摘要和点评、段落级评论、图片 EXIF 自动解析
- **阅读** —— 多主题（Azure / Flux / 2026 / Chred / Westlife）、响应式、自定义页脚按钮、语义搜索
- **数据主权** —— 完全自部署，支持从 WordPress / Typecho 一键导入
- **社交** —— Utterlog Network 联盟身份（跨站评论 / 关注 / 段落点评）、Passkey / 2FA 登录
- **架构** —— Go 1.26 后端 + Next.js 16 前端 + Vite SPA 管理后台（`go:embed` 打入单个二进制）

## 快速开始

```bash
git clone https://github.com/Utterlog/utterlog.git
cd utterlog
cp .env.example .env            # 修改 DB_PASSWORD / JWT_SECRET
cd api/admin && npm install && npm run build && cd ../..
docker compose up -d --build
# 浏览器打开 http://localhost:3000 → /install 向导
```

详细说明见仓库 [INSTALL.md](https://github.com/Utterlog/utterlog/blob/main/INSTALL.md)。

## 技术栈

| 层 | 技术 |
|---|---|
| 前端博客 | Next.js 16 + React 19 + TypeScript |
| 管理后台 | Vite + React + React Router + Zustand + TanStack Query |
| 后端 API | Go 1.26 + Gin + sqlx |
| 数据库 | PostgreSQL 18（pgvector 语义搜索） |
| 缓存 | Redis 7 |
| 部署 | Docker Compose |

## 仓库

- **[utterlog](https://github.com/Utterlog/utterlog)** — 主项目（前端 + 后端 + 管理 SPA + 主题）
- **[utterlog-sync](https://github.com/Utterlog/utterlog-sync)** — WordPress 插件（导出 `.ulbk` 包或直推到 Utterlog 站点）

## 贡献

Issues / Pull Requests 欢迎。写作、翻译、主题和插件同样欢迎。

## 许可

MIT
