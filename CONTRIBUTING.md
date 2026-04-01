# 贡献指南

感谢你对 Claude Code 源码泄露资源合集的关注！欢迎提交 PR 贡献资源。

## 如何提交资源

### 1. Fork 仓库
```bash
gh repo fork claude-code-leak-resources
```

### 2. 创建分支
```bash
git checkout -b add-resource-xxx
```

### 3. 编辑 README.md
在对应分类下添加资源，格式如下：

```markdown
| 仓库 | Stars | 说明 |
|------|-------|------|
| [owner/repo](https://github.com/owner/repo) | ⭐123 | 简短描述 |
```

### 4. 提交更改
```bash
git add README.md
git commit -m "docs: 添加 xxx 资源"
git push origin add-resource-xxx
```

### 5. 创建 Pull Request
- 标题：`docs: 添加 xxx 资源`
- 描述：说明资源价值和分类理由

## 资源标准

### ✅ 接受
- 高质量原创分析文章
- 技术深度解读
- 安全研究成果
- 实用工具/插件/技能
- 社区讨论汇总

### ❌ 不接受
- 纯搬运无增值内容
- 侵权内容
- 恶意利用教程
- 低质量营销内容

## 分类说明

### 源码镜像
- 完整的 Claude Code 源码镜像
- 本地可运行版本
- 重写/重构版本

### 深度分析
- 架构分析文章
- 子系统深度解读
- 隐藏功能挖掘

### 安全审计
- 安全研究工具
- 审计报告
- 漏洞分析

### 工具/插件
- 开发工具
- 安全工具
- 插件/技能
- 专业应用

## 更新频率

- 日常更新：社区新资源
- 每周汇总：Star 数据更新
- 每月整理：分类优化

## 联系方式

- Issue: https://github.com/your-username/claude-code-leak-resources/issues
- Discussion: https://github.com/your-username/claude-code-leak-resources/discussions

## 许可证

MIT License - 原创内容
第三方内容版权归各自作者所有
