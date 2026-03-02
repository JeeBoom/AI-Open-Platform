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
