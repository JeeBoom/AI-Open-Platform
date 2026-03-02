# AI Open Platform 导航

一个基于 Vue 3 + Vite 的 AI 官网 / 开放平台 / 工具 / 企业软件导航页。

## 启动

```bash
npm install
npm run dev
```

## 构成

- `src/data/platforms.js`：所有平台链接数据（维护时优先改这里）
- `src/components/PlatformColumn.vue`：单列复用组件
- `src/App.vue`：页面结构与标题区
- `src/style.css`：整体深色科技风样式

## 打包

```bash
npm run build
npm run preview
```

## GitHub Pages 部署

- 本项目已内置 `GitHub Actions` 工作流：`.github/workflows/deploy-pages.yml`
- 推送到 `main` 分支后会自动构建并发布 `dist`
- 在仓库设置中进入 `Settings -> Pages`，`Source` 选择 `GitHub Actions`
- 发布地址：`https://JeeBoom.github.io/AI-Open-Platform/`
