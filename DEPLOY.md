# 部署到 GitHub Pages 完整指南

## 📋 前置准备

- 一个 GitHub 账号（已有的）
- 基本的命令行操作知识
- 项目文件已准备好（在 wechat-recharge-optimization 文件夹中）

---

## 🚀 方法一：最简单 - 通过 GitHub 网页界面（推荐新手）

### 步骤 1：在 GitHub 上创建新仓库

1. 访问 https://github.com/new
2. 填写仓库信息：
   - **Repository name（仓库名称）**: `wechat-recharge-optimization` （或您喜欢的名称）
   - **Description（描述）**: 微信话费充值体验优化项目方案
   - 选择 **Public**（公开仓库，免费使用 GitHub Pages）
   - **不要**勾选 "Initialize this repository with..."（我们会自己上传文件）
3. 点击 **Create repository**

### 步骤 2：上传项目文件

在创建好的仓库页面：

1. 点击 **uploading an existing file** 链接
2. 将 `wechat-recharge-optimization` 文件夹中的以下文件拖拽到上传区域：
   - `index.html`
   - `README.md`
   - `DEPLOY.md`
3. 在底部的 "Commit changes" 区域填写：
   - 第一行：`Initial commit`
4. 点击 **Commit changes**

### 步骤 3：启用 GitHub Pages

1. 在仓库页面，点击顶部的 **Settings** 标签
2. 在左侧菜单中找到并点击 **Pages**（在 "Code and automation" 部分）
3. 在 "Build and deployment" 部分：
   - **Source（源）**: 选择 `Deploy from a branch`
   - **Branch（分支）**: 选择 `main` 或 `master` 分支，右侧文件夹选择 `/ (root)`
4. 点击 **Save**
5. 等待 1-5 分钟，刷新页面

### 步骤 4：访问您的网站！

完成后，您会在 Pages 设置页面看到：
```
Your site is live at https://您的用户名.github.io/仓库名/
```

---

## 🖥️ 方法二：通过 Git 命令行（适合有经验用户）

### 第一步：配置 Git（如果还没配置过）

```bash
# 配置您的用户名和邮箱
git config --global user.name "您的名字"
git config --global user.email "您的邮箱@example.com"
```

### 第二步：初始化仓库并提交

```bash
# 进入项目文件夹
cd /Users/bytedance/Downloads/wechat-recharge-optimization

# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 创建提交
git commit -m "Initial commit: WeChat Recharge Optimization Project"
```

### 第三步：在 GitHub 创建仓库并关联

1. 访问 https://github.com/new 创建新仓库
2. 按照页面上的提示，关联远程仓库：

```bash
# 关联远程仓库（替换为您的实际用户名和仓库名）
git remote add origin https://github.com/您的用户名/wechat-recharge-optimization.git

# 重命名分支为 main（如果需要）
git branch -M main

# 推送到 GitHub
git push -u origin main
```

### 第四步：启用 GitHub Pages

按照方法一的步骤3-4操作。

---

## ✨ 验证部署成功

部署成功后，您可以通过以下方式访问：

- **网址格式**: `https://您的GitHub用户名.github.io/仓库名称/`
- **示例**: `https://zhangsan.github.io/wechat-recharge-optimization/`

首次部署可能需要 1-10 分钟才能生效，请耐心等待！

---

## 🔄 更新网站内容

以后如果需要更新网站内容：

### 通过网页界面：
1. 直接在 GitHub 仓库中编辑文件
2. 提交更改后，GitHub Pages 会自动重新部署

### 通过命令行：
```bash
# 修改文件后
git add .
git commit -m "描述您的更改"
git push origin main
```

几分钟后，更改就会自动反映在网站上！

---

## 💡 常见问题

### Q: 我的网站怎么一直显示 404？
A: 首次部署需要等待几分钟，请耐心等待。如果超过10分钟还是404，检查：
- 文件名是否是 `index.html`（小写）
- Pages 设置是否正确保存
- 分支是否选择正确

### Q: 可以使用自定义域名吗？
A: 可以！在 Pages 设置页面有 "Custom domain" 选项可以配置。

### Q: 仓库必须是公开的吗？
A: GitHub Free 账号需要公开仓库才能使用 Pages。GitHub Pro 账号可以用私有仓库。

---

## 📚 更多资源

- GitHub Pages 官方文档: https://pages.github.com/
- Git 入门指南: https://git-scm.com/doc
