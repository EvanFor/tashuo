# TA说

TA说是一个以真人表达、内容交流和观点碰撞为核心的社区产品。用户以稳定公开身份参与日常交流，仅在明确允许匿名的指定主题中使用受保护的表达身份。

## 开发约定

- `main`：稳定版本。
- `dev`：日常开发分支。
- 产品文档位于 `docs/`。
- 技术栈：Next.js、TypeScript、PostgreSQL、Prisma。

## 项目状态

当前为项目初始化阶段。首批目标是建立可运行的 Web 骨架、数据模型和自动化检查；邮箱认证、社区互动、匿名发布及治理后台将按 MVP 计划逐步实现。

## 本地开发

```bash
npm install
cp .env.example .env
npm run dev
```

配置数据库后可执行：

```bash
npm run db:generate
npm run db:migrate
```
