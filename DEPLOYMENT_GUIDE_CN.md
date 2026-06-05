# GitHub Pages 公开部署教程（Mac + VS Code）

这个项目是纯静态网页，不需要购买服务器，也不需要 Node.js 构建。

## 一、本地打开与检查

1. 解压项目文件夹。
2. 用 VS Code 打开整个文件夹，而不是只打开 `index.html`。
3. 在 VS Code 顶部选择 `Terminal` → `New Terminal`。
4. 确认终端位于项目文件夹：

```bash
pwd
ls
```

你应看到 `index.html`、`styles.css`、`app.js`。

5. 启动本地服务器：

```bash
python3 -m http.server 8000
```

6. 浏览器打开：

```text
http://localhost:8000
```

7. 检查：

- 双语、中文、英文模式都能切换
- 参数可以修改
- 点击模拟后有结果
- 情景对比能显示
- 手机宽度下页面没有明显溢出

结束本地服务器：回到终端，按 `Control + C`。

## 二、创建独立 GitHub 仓库

不要把完整小程序源代码、CloudBase 导出和参与者数据一起发布。建议单独创建一个仓库：

```text
carbon-ad-simulator
```

在 GitHub 网站：

1. 点击右上角 `+`。
2. 选择 `New repository`。
3. Repository name 填 `carbon-ad-simulator`。
4. 选择 `Public`。
5. 不要勾选自动创建 README、.gitignore 或 license。
6. 点击 `Create repository`。

## 三、把本地文件推送到 GitHub

在 VS Code 终端执行。把 `YOUR_GITHUB_USERNAME` 换成你的 GitHub 用户名：

```bash
git init
git add .
git commit -m "Initial bilingual Carbon Navigator ad simulator"
git branch -M main
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/carbon-ad-simulator.git
git push -u origin main
```

第一次推送时，GitHub 可能要求你在浏览器登录或授权。

## 四、开启 GitHub Pages

1. 打开 GitHub 上的 `carbon-ad-simulator` 仓库。
2. 点击 `Settings`。
3. 左侧找到 `Pages`。
4. 在 `Build and deployment` 中：
   - Source：选择 `Deploy from a branch`
   - Branch：选择 `main`
   - Folder：选择 `/(root)`
5. 点击 `Save`。
6. 等待部署完成。

网址通常是：

```text
https://YOUR_GITHUB_USERNAME.github.io/carbon-ad-simulator/
```

## 五、以后更新网页

每次修改并检查完成后，在终端运行：

```bash
git status
git add .
git commit -m "Describe the update"
git push
```

GitHub Pages 会自动重新部署。

## 六、在 VS Code 里的 Codex 继续开发

打开项目文件夹后，在 Codex 中发送：

```text
请先阅读 AGENTS.md、PROJECT_CONTEXT.md、README.md 和 DEPLOYMENT_GUIDE_CN.md。
接下来继续开发碳行家广告实验模拟器。先检查当前页面和代码，不要修改任何真实基准数据，也不要引入参与者级数据。请告诉我你理解的项目结构，然后等我给下一步任务。
```

`AGENTS.md` 会给 Codex 持续的项目级约束，`PROJECT_CONTEXT.md` 保存这个项目的背景和已确定数据。

## 七、绝对不要公开上传的文件

- CloudBase 原始导出
- live-monitor 数据
- OpenID
- 用户姓名、邮箱或联系方式
- 原始问卷答案
- API key、Secret、云环境密钥
- 含个人数据的报告或截图
