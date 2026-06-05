# 碳行家广告实验模拟器 / Carbon Navigator Ad Experiment Simulator

一个中英双语、纯静态、可公开部署的腾讯广告漏斗模拟器。

A bilingual, static, deployable scenario simulator for the Tencent Ads → WeChat Mini Program research funnel.

## 本地运行 / Run locally

最简单的方式：直接双击 `index.html`。

推荐用本地服务器：

```bash
cd carbon-ad-simulator-bilingual
python3 -m http.server 8000
```

然后打开：

```text
http://localhost:8000
```

## 文件结构 / Files

- `index.html` — 页面结构 / page structure
- `styles.css` — 样式 / styles
- `app.js` — 双语、模拟逻辑、导入导出 / bilingual UI, simulation logic, import/export
- `PROJECT_CONTEXT.md` — 项目背景，给新成员和 Codex 阅读
- `AGENTS.md` — Codex 项目级工作说明
- `DEPLOYMENT_GUIDE_CN.md` — GitHub Pages 公开部署教程
- `.nojekyll` — 让 GitHub Pages 按静态文件直接发布

## 数据安全 / Data safety

本网页只包含汇总后的漏斗数字，不包含参与者姓名、OpenID、CloudBase 导出、问卷原始答案或其他个人数据。模拟在浏览器本地运行。

The site contains aggregate funnel numbers only. It includes no participant names, OpenIDs, CloudBase exports, raw survey answers, or other personal data. Simulations run locally in the browser.
