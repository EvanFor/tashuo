# TA说

TA说是一个以真人表达、内容交流和观点碰撞为核心的社区产品。用户以稳定公开身份参与日常交流，仅在明确允许匿名的指定主题中使用受保护的表达身份。

## 开发约定

- `main`：稳定版本。
- `dev`：日常开发分支，当前所有开发变更进入该分支。
- `src/`：Vue 3 前端源码。
- `docs/`：产品、数据模型、API、隐私与治理文档。
- 技术栈：Vue 3、Vite、TypeScript、PostgreSQL、Prisma。

## 本地开发

需要 Node.js 20 或更高版本。

```bash
npm install
cp .env.example .env
npm run dev
```

Vite 默认在终端显示本地访问地址。

## 数据库

配置 `.env` 中的 `DATABASE_URL` 后执行：

```bash
npm run db:generate
npm run db:migrate
```

## 当前阶段

当前为项目初始化阶段。已有基础首页、前端工程配置和初始数据模型；邮箱认证、社区业务 API、匿名发布权限和治理后台仍需后续实现。不要将当前工程骨架视为完整 MVP。
