# 🚀 GitHub 仓库推送指南

## 方式一：使用 GitHub CLI（推荐）

### 1. 登录 GitHub
```bash
gh auth login
```
按提示完成认证（选择 GitHub.com → HTTPS → Login with a web browser）

### 2. 创建并推送仓库
```bash
cd /Users/zbj/Documents/OpenClaw/claude-code-leak-resources

# 创建仓库并推送
gh repo create claude-code-leak-resources --public --source=. --branch=main --push
```

### 3. 添加 Topics
```bash
gh repo edit claude-code-leak-resources \
  --add-topic claude-code \
  --add-topic ai-security \
  --add-topic source-code-leak \
  --add-topic awesome-list \
  --add-topic curated-resources
```

---

## 方式二：手动创建

### 1. 在 GitHub 创建空仓库
访问：https://github.com/new

- **仓库名：** claude-code-leak-resources
- **描述：** Claude Code 源码泄露资源合集 - 150+ 高质量资源 curated list
- **可见性：** Public ✅
- **⚠️ 不要勾选** "Add a README file"
- **⚠️ 不要勾选** "Add .gitignore"
- **⚠️ 不要勾选** "Choose a license"

点击 **Create repository**

### 2. 关联远程仓库并推送
```bash
cd /Users/zbj/Documents/OpenClaw/claude-code-leak-resources

# 重命名分支为 main
git branch -M main

# 添加远程仓库（替换 YOUR_USERNAME 为你的 GitHub 用户名）
git remote add origin https://github.com/YOUR_USERNAME/claude-code-leak-resources.git

# 推送
git push -u origin main
```

### 3. 添加 Topics
进入仓库页面 → Settings → Topics → 添加：
- claude-code
- ai-security
- source-code-leak
- awesome-list
- curated-resources

---

## 启用 GitHub Pages（可选）

### 1. 启用 Pages
进入仓库 → Settings → Pages

- **Source:** Deploy from a branch
- **Branch:** main / (root)
- 点击 **Save**

### 2. 访问网站
等待 1-2 分钟后访问：
```
https://YOUR_USERNAME.github.io/claude-code-leak-resources/
```

---

## 验证推送

### 检查仓库
```bash
gh repo view claude-code-leak-resources
```

或访问：
```
https://github.com/YOUR_USERNAME/claude-code-leak-resources
```

---

## 后续维护

### 更新内容
```bash
# 编辑 README.md
vim README.md

# 提交推送
git add README.md
git commit -m "docs: 更新资源列表"
git push
```

### 查看 Star 增长
```bash
gh repo view claude-code-leak-resources --json stargazerCount
```

---

## 快速命令汇总

```bash
# 进入仓库目录
cd /Users/zbj/Documents/OpenClaw/claude-code-leak-resources

# 查看状态
git status

# 查看远程
git remote -v

# 推送更新
git push

# 查看 GitHub 状态
gh repo view
```

---

**需要帮助？** 运行 `gh help` 或访问 https://cli.github.com/manual
