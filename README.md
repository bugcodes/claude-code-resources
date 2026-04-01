# Claude Code 源码泄露资源合集

**最后更新：** 2026-04-01  
**事件时间：** 2026-03-31  
**泄露原因：** npm 包中的 sourcemap 文件暴露了完整的 TypeScript 源码（512K+ 行，1,884+ 文件）

---

## 📋 目录

1. [事件概述](#-事件概述)
2. [核心资源](#-核心资源)
3. [源码镜像仓库](#-源码镜像仓库)
4. [深度分析文章](#-深度分析文章)
5. [技术解读](#-技术解读)
6. [安全审计](#-安全审计)
7. [社区讨论](#-社区讨论)
8. [相关工具](#-相关工具)
9. [时间线](#-时间线)
10. [学习路径](#-学习路径)

---

## 📌 事件概述

### 泄露详情
- **发现时间：** 2026-03-31
- **发现者：** Chaofan Shou (@Fried_rice)
- **泄露渠道：** npm registry 中的 source map 文件
- **泄露内容：** 完整的 TypeScript 源码（~1,900 文件，512K+ 行）
- **影响范围：** Claude Code CLI v2.1.88

### 关键发现
- 🔐 **系统提示词** - 完整的 system prompts
- 🎮 **隐藏功能** - BUDDY 宠物系统（18 种物种）、KAIROS 助理、ULTRAPLAN 模式
- 🤖 **多 Agent 架构** - Coordinator Mode、Swarm 模式、Buddy System
- 📊 **遥测数据** - 用户行为追踪、挫败感检测、187 个 spinner verbs
- 🏷️ **内部代号** - Capybara 模型、Tengu、Fennec
- 🔧 **87 个 Feature Flags** - 未发布功能开关
- 📝 **44 个未发布功能** - 后台 Agent、多 Agent 编排、Cron 调度、语音模式等

---

## 🔥 核心资源

### 必读 Top 15

| # | 资源 | 类型 | 亮点 |
|---|------|------|------|
| 1 | [awesome-claude-code-postleak-insights](https://github.com/nblintao/awesome-claude-code-postleak-insights) | 资源合集 | ⭐19 高质量分析 curated list |
| 2 | [claw-code](https://github.com/instructkr/claw-code) | 源码增强 | ⭐64.5k 最快 50k star 项目 |
| 3 | [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) | 工具大全 | ⭐35k 最全面工具列表 |
| 4 | [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) | 子 Agent | ⭐15.8k 100+ 专用 Agent |
| 5 | [awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) | 技能合集 | ⭐10.2k 技能资源 |
| 6 | [claude-code-source-analysis](https://github.com/catyans/claude-code-source-analysis) | 架构解读 | 逐模块深度分析 |
| 7 | [claude-reviews-claude](https://github.com/openedclaude/claude-reviews-claude) | AI 自分析 | Claude 分析自己的源码 |
| 8 | [analysis_claude_code](https://github.com/ThreeFish-AI/analysis_claude_code) | 逆向工程 | ⭐270 中文深度分析 |
| 9 | [claude-code-devcontainer](https://github.com/trailofbits/claude-code-devcontainer) | 安全沙箱 | ⭐591 Trail of Bits 出品 |
| 10 | [claude-source-leaked](https://github.com/noya21th/claude-source-leaked) | 功能分析 | 87 个隐藏 feature flags |
| 11 | [open-claude-code](https://github.com/xcanwin/open-claude-code) | 可运行版本 | 首个干净可安装版本 |
| 12 | [claude-leaked-files](https://github.com/Ahmad-progr/claude-leaked-files) | 源码镜像 | ⭐137 教育用途镜像 |
| 13 | [awesome-claude-code-toolkit](https://github.com/rohitg00/awesome-claude-code-toolkit) | 综合工具包 | ⭐979 135 个 Agent |
| 14 | [geo-seo-claude](https://github.com/zubair-trabzada/geo-seo-claude) | SEO 技能 | ⭐4.6k GEO 优先 SEO |
| 15 | [MedgeClaw](https://github.com/xjtulyc/MedgeClaw) | 生物医学 | ⭐935 AI 研究助手 |

---

## 📦 源码镜像仓库

### 主要镜像

| 仓库 | Stars | 说明 |
|------|-------|------|
| [instructkr/claw-code](https://github.com/instructkr/claw-code) | ⭐64,516 | 最快 50k star 项目，Rust 重写中 |
| [asgeirtj/system_prompts_leaks](https://github.com/asgeirtj/system_prompts_leaks) | ⭐35,351 | 系统提示词提取（多模型） |
| [NanmiCoder/claude-code-haha](https://github.com/NanmiCoder/claude-code-haha) | ⭐349 | 本地可运行版本 |
| [leaked-claude-code/leaked-claude-code](https://github.com/leaked-claude-code/leaked-claude-code) | ⭐172 | 完整开源镜像 |
| [Ahmad-progr/claude-leaked-files](https://github.com/Ahmad-progr/claude-leaked-files) | ⭐137 | 教育用途镜像 |
| [Hyper66666/claude-code-sourcemap](https://github.com/Hyper66666/claude-code-sourcemap) | ⭐117 | sourcemap 镜像 |
| [fazxes/Claude-code](https://github.com/fazxes/Claude-code) | ⭐110 | 基于泄露源码重建 |
| [GitHpriyanshu23/Claude-code-leaks](https://github.com/GitHpriyanshu23/Claude-code-leaks) | ⭐106 | 完整功能描述 |
| [JiaranI/start-claude-code](https://github.com/JiaranI/start-claude-code) | ⭐90 | 一键启动 v2.1.88 |
| [soufianebouaddis/claude-code](https://github.com/soufianebouaddis/claude-code) | ⭐66 | TypeScript 完整解析 |
| [noya21th/claude-source-leaked](https://github.com/noya21th/claude-source-leaked) | ⭐43 | 87 个 feature flags |
| [l3tchupkt/claude-code](https://github.com/l3tchupkt/claude-code) | ⭐18 | NPM sourcemap 分析 |
| [sped-peepo/Leak-Of-The-full-source-code-of-Anthropic-s-Claude-Code-CLI](https://github.com/sped-peepo/Leak-Of-The-full-source-code-of-Anthropic-s-Claude-Code-CLI) | ⭐16 | 完整源码泄露 |

### 中文镜像

| 仓库 | Stars | 说明 |
|------|-------|------|
| [ThreeFish-AI/analysis_claude_code](https://github.com/ThreeFish-AI/analysis_claude_code) | ⭐270 | 逆向工程研究 |
| [xcanwin/open-claude-code](https://github.com/xcanwin/open-claude-code) | ⭐15 | 首个干净可安装版本 |
| [CnOxx1/claude-code](https://github.com/CnOxx1/claude-code) | ⭐4 | 技术分析文档 |
| [Cshaoguang/claude-code-sourcemap](https://github.com/Cshaoguang/claude-code-sourcemap) | ⭐2 | sourcemap 镜像 |
| [miles990/claude-code-leak-research](https://github.com/miles990/claude-code-leak-research) | ⭐4 | 深度研究分析 |
| [YZxyzz/claude-code-analysis](https://github.com/YZxyzz/claude-code-analysis) | ⭐0 | 源码深度解析 |
| [InvictusAutomation/claude-code-leak-analysis](https://github.com/InvictusAutomation/claude-code-leak-analysis) | ⭐1 | 学习笔记 |

---

## 📝 深度分析文章

### 架构分析

| 标题 | 链接 | 焦点 |
|------|------|------|
| Claude Code's Entire Source Code Was Just Leaked via npm Source Maps | [Dev.to](https://dev.to/gabrielanhaia/claude-codes-entire-source-code-was-just-leaked-via-npm-source-maps-heres-whats-inside-cjo) | 生产架构与技术栈 |
| Claude Code Source Leak: Production AI Architecture Patterns | [HuggingFace](https://discuss.huggingface.co/t/claude-code-source-leak-production-ai-architecture-patterns-from-512-000-lines/174846) | 上下文压缩与 AutoDream |
| Claude Code 泄露源码深度分析 | [catyans/claude-code-source-analysis](https://github.com/catyans/claude-code-source-analysis) | 逐模块架构解读（18 个文件） |
| Claude Code 逆向工程研究 | [ThreeFish-AI/analysis_claude_code](https://github.com/ThreeFish-AI/analysis_claude_code) | 中文深度分析 |
| Claude Code's Entire Source Code Got Leaked via a Sourcemap | [kuber.studio](https://kuber.studio/blog/AI/Claude-Code%27s-Entire-Source-Code-Got-Leaked-via-a-Sourcemap-in-npm%2C-Let%27s-Talk-About-it) | 未来路线图与隐藏功能 |
| Understanding Claude Code | [pankaj28843/understanding-claude-code](https://github.com/pankaj28843/understanding-claude-code) | 架构与工程模式 |
| Claude Code Unpacked | [h26liu/claude-code-unpacked](https://github.com/h26liu/claude-code-unpacked) | 净室重构分析 |

### 隐藏功能

| 标题 | 链接 | 焦点 |
|------|------|------|
| Claude Code's Entire Source Code Got Leaked via a Sourcemap | [kuber.studio](https://kuber.studio/blog/AI/Claude-Code%27s-Entire-Source-Code-Got-Leaked-via-a-Sourcemap-in-npm%2C-Let%27s-Talk-About-it) | 未来路线图与隐藏功能 |
| Claude Code v2.1.88 source analysis | [noya21th/claude-source-leaked](https://github.com/noya21th/claude-source-leaked) | 87 个 feature flags |
| BREAKING: Anthropic just leaked Claude Code's entire source code | [The AI Corner](https://www.the-ai-corner.com/p/claude-code-source-code-leaked-2026) | 44 个功能 flags（付费） |
| Claude-Code-Buddy-Collection | [FiroYu/Claude-Code-Buddy-Collection](https://github.com/FiroYu/Claude-Code-Buddy-Collection) | 18 种宠物物种图鉴 |

### 子系统深度

| 标题 | 链接 | 焦点 |
|------|------|------|
| How an AI Reads the Web: A Deep Dive into Claude Code's WebFetchTool | [Medium](https://medium.com/@nblintao/how-an-ai-reads-the-web-a-deep-dive-into-claude-codes-webfetchtool-0abee4446343) | WebFetchTool 设计（1,173 行） |
| Claude Code's Entire Source Code Was Just Leaked | [Dev.to](https://dev.to/gabrielanhaia/claude-codes-entire-source-code-was-just-leaked-via-npm-source-maps-heres-whats-inside-cjo) | 5 大子系统详解 |
| Claude Code Source Leak: Production AI Architecture Patterns | [HuggingFace](https://discuss.huggingface.co/t/claude-code-source-leak-production-ai-architecture-patterns-from-512-000-lines/174846) | 上下文压缩三层管道 |

### 安全视角

| 标题 | 链接 | 焦点 |
|------|------|------|
| Anthropic's Claude Code CLI Source Leak Stirs AI Security Waves | [OpenTools.ai](https://opentools.ai/news/anthropics-claude-code-cli-source-leak-stirs-ai-security-waves) | AI 安全影响 |
| The Claude Code leak is bigger than a code leak | [Medium](https://medium.com/@hendrik-thurau-enterprises/the-claude-code-leak-is-bigger-than-a-code-leak) | 战略分析 |
| Claude Code source has been available for 13 months, and nothing happened | [TheHuman2AI](https://thehuman2ai.com/blog/claude-code-source-leak) | 时间线与安全评估 |
| Claude Source Code Leak! | [Tailored-X](https://blog.tailored-x.com/claude-source-code-leak/) | 架构概述 |
| Claude Code Source Leaked via npm: 512K Lines Exposed | [ByteIota](https://byteiota.com/claude-code-source-leaked-via-npm-512k-lines-exposed/) | 技术背景 |
| Anthropic's Claude Code CLI Source Leak Stirs AI Security Waves | [OpenTools.ai](https://opentools.ai/news/anthropics-claude-code-cli-source-leak-stirs-ai-security-waves) | 竞争与监管 |
| Anthropic accidentally leaked Claude Code source code | [TechStartups](https://techstartups.com/2026/03/31/anthropics-claude-source-code-leak-goes-viral-again-after-full-source-hits-npm-registry-revealing-hidden-capybara-models-and-ai-pet/) | BUDDY 宠物系统 |
| Anthropic's Claude Code source appears to have been leaked | [PiunikaWeb](https://piunikaweb.com/2026/03/31/anthropic-claude-code-source-leaked-npm-registry/) | 原始报道 |
| Claude Code Source Code Leaked | [LowCode Agency](https://www.lowcode.agency/blog/claude-code-source-code-leaked) | 版权风险分析 |
| BREAKING: Anthropic just leaked Claude Code's entire source code | [The AI Corner](https://www.the-ai-corner.com/p/claude-code-source-code-leaked-2026) | 44 个未发布功能（付费） |

---

## 🔬 技术解读

### 核心技术栈

| 组件 | 技术 | 说明 |
|------|------|------|
| 运行时 | **Bun** | 高性能 JavaScript 运行时 |
| 前端 | **React + Ink** | 终端 UI 渲染 |
| 后端 | **NodeJS** | JavaScript 运行时 |
| 数据库 | **SQLite** | 本地存储 |
| ORM | **Prisma** | 类型安全数据库操作 |
| 验证 | **Zod v4** | Schema 验证 |
| 类型 | **TypeScript** | 静态类型检查 |
| 认证 | **CCH Attestation** | 自定义 Bun 运行时 + Zig 编译 |
| 打包 | **npm + sourcemap** | 泄露渠道 |

### 关键架构模式

#### 1. 多 Agent 系统
- **Coordinator Mode** - 多 Agent 协调
- **Swarm Mode** - Agent 集群
- **Buddy System** - 宠物陪伴系统（18 种物种）

#### 2. 上下文管理
- **MicroCompact** - 微压缩
- **AutoCompact** - 自动压缩
- **Full Compact** - 完整压缩

#### 3. 记忆系统
- **AutoDream** - 四阶段记忆整合
- **Session Memory** - 会话记忆
- **Team Memory** - 团队记忆

#### 4. 工具系统
- **BashTool** - 终端命令执行
- **FileEditTool** - 文件编辑
- **WebFetchTool** - 网页抓取（1,173 行）
- **MCPTool** - Model Context Protocol
- **AgentTool** - 多 Agent 编排
- **TaskCreate/Get/List/Update/StopTool** - 任务管理
- **SkillTool** - 技能系统
- **ConfigTool** - 配置管理

---

## 🛡️ 安全审计

### 安全工具

| 工具 | Stars | 说明 |
|------|-------|------|
| [trailofbits/claude-code-devcontainer](https://github.com/trailofbits/claude-code-devcontainer) | ⭐591 | 沙箱开发环境 |
| [trailofbits/skills](https://github.com/trailofbits/skills) | ⭐4,170 | 安全研究技能 |
| [TheAuditorTool/Auditor](https://github.com/TheAuditorTool/Auditor) | ⭐541 | VibeCoding 解毒剂 |
| [0xiehnnkta/nemesis-auditor](https://github.com/0xiehnnkta/nemesis-auditor) | ⭐195 | 深度逻辑安全审计 |
| [PlamenTSV/plamen](https://github.com/PlamenTSV/plamen) | ⭐186 | Web3 安全审计 Agent |
| [0xSteph/pentest-ai](https://github.com/0xSteph/pentest-ai) | ⭐171 | 渗透测试助手 |
| [HarmonicSecurity/claudit-sec](https://github.com/HarmonicSecurity/claudit-sec) | ⭐97 | macOS 安全审计工具 |
| [jar-analyzer-claude](https://github.com/jar-analyzer/jar-analyzer-claude) | ⭐102 | Java JAR 审计插件 |
| [peg/rampart](https://github.com/peg/rampart) | ⭐59 | AI Agent 防火墙 |
| [VicKayro/claude-security-audit](https://github.com/VicKayro/claude-security-audit) | ⭐65 | OWASP Top 10 审计 |
| [ryo-ebata/cc-audit](https://github.com/ryo-ebata/cc-audit) | ⭐18 | 静态安全扫描器 |
| [crazygit/kube-audit-kit](https://github.com/crazygit/kube-audit-kit) | ⭐29 | K8s 安全审计 |
| [yoanbernabeu/supabase-pentest-skills](https://github.com/yoanbernabeu/supabase-pentest-skills) | ⭐33 | Supabase 渗透测试 |
| [dabit3/skill-audit](https://github.com/dabit3/skill-audit) | ⭐36 | 技能定义审计 |
| [UseAI-pro/openclaw-skills-security](https://github.com/UseAI-pro/openclaw-skills-security) | ⭐43 | OpenClaw 安全技能 |
| [ax128/AegisGate](https://github.com/ax128/AegisGate) | ⭐35 | LLM API 安全网关 |
| [node9-ai/node9-proxy](https://github.com/node9-ai/node9-proxy) | ⭐103 | Agent 执行安全层 |
| [fubak/ferret-scan](https://github.com/fubak/ferret-scan) | ⭐73 | LLM CLI 安全扫描器 |
| [reprompt-dev/reprompt](https://github.com/reprompt-dev/reprompt) | ⭐39 | 提示词分析与密钥检测 |
| [zackbart/cleenup](https://github.com/zackbart/cleenup) | ⭐1 | 会话日志密钥扫描 |

### 安全发现

| 类别 | 发现 |
|------|------|
| 认证机制 | CCH attestation（自定义 Bun 运行时 + Zig 编译 token 生成） |
| API 安全 | 反蒸馏防御、请求签名、prompt injection 检测 |
| 权限系统 | 多层权限控制、沙箱模式、bypass permissions |
| 数据泄露 | 用户行为遥测、挫败感检测、187 个 spinner verbs |
| 供应链安全 | npm sourcemap 暴露、build pipeline 漏洞 |
| 敏感信息 | system prompts、feature flags、内部代号 |

---

## 💬 社区讨论

### Hacker News
- [Hacker News 讨论](https://news.ycombinator.com/item?id=47584540)
  - 亮点：基于正则的情感检测、反蒸馏防御、代码质量分析

### Reddit
- [r/LocalLLaMA 讨论](https://www.reddit.com/r/LocalLLaMA/comments/1s8ijfb/claude_code_source_code_has_been_leaked_via_a_map/)
  - 亮点：隐藏功能详解（KAIROS、Buddy、Undercover Mode）
  
- [r/ClaudeAI 讨论](https://www.reddit.com/r/ClaudeAI/comments/1s8ifm6/claude_code_source_code_has_been_leaked_via_a_map/)
  - 亮点：CCH attestation 机制深度分析

### X/Twitter
- [发现者推文](https://x.com/Fried_rice/status/2038894956459290963) - Chaofan Shou
- [源码分析汇总](https://x.com/simonwongio/status/2039003134484488484) - Simon Wong（含 3 个源码链接）
- [赚钱资源汇总](https://x.com/saccc_c/status/2038484477672833462) - Sac（40 个 GitHub 仓库）
- [Claude Code 源码泄露](https://x.com/search?q=claude%20code%20leak&f=live) - 实时搜索

---

## 🎥 视频/播客

| 标题 | 平台 | 链接 |
|------|------|------|
| Claude Code 源码泄露事件解析 | YouTube | 待补充 |
| 源码泄露后的安全启示 | Bilibili | 待补充 |
| AI 安全播客：Claude Code 特辑 | Podcast | 待补充 |

---

## 🧰 相关工具

### 开发工具

| 工具 | Stars | 说明 |
|------|-------|------|
| [claw-cli/claw-code-rust](https://github.com/claw-cli/claw-code-rust) | ⭐33 | Rust 重写版本 |
| [JiaranI/start-claude-code](https://github.com/JiaranI/start-claude-code) | ⭐90 | 一键启动 v2.1.88 |
| [vibe-log/vibe-log-cli](https://github.com/vibe-log/vibe-log-cli) | ⭐311 | 会话日志分析 |
| [smaug](https://github.com/alexknowshtml/smaug) | ⭐785 | X 书签归档分析 |
| [CodeTree](https://github.com/mimalef70/CodeTree) | ⭐149 | 代码库打包分析 |
| [codebase-digest](https://github.com/kamilstanuch/codebase-digest) | ⭐365 | AI 友好代码打包器 |

### 安全工具

| 工具 | Stars | 说明 |
|------|-------|------|
| [fubak/ferret-scan](https://github.com/fubak/ferret-scan) | ⭐73 | LLM CLI 安全扫描器 |
| [zackbart/cleenup](https://github.com/zackbart/cleenup) | ⭐1 | 会话日志密钥扫描 |
| [ax128/AegisGate](https://github.com/ax128/AegisGate) | ⭐35 | LLM API 安全网关 |
| [peg/rampart](https://github.com/peg/rampart) | ⭐59 | AI Agent 防火墙 |
| [node9-ai/node9-proxy](https://github.com/node9-ai/node9-proxy) | ⭐103 | Agent 执行安全层 |
| [ryo-ebata/cc-audit](https://github.com/ryo-ebata/cc-audit) | ⭐18 | 静态安全扫描器 |

### 插件/技能

| 工具 | Stars | 说明 |
|------|-------|------|
| [trailofbits/skills](https://github.com/trailofbits/skills) | ⭐4,170 | 安全研究技能 |
| [qdhenry/Claude-Command-Suite](https://github.com/qdhenry/Claude-Command-Suite) | ⭐1,104 | 专业命令套件 |
| [tradermonty/claude-trading-skills](https://github.com/tradermonty/claude-trading-skills) | ⭐478 | 交易分析技能 |
| [geo-seo-claude](https://github.com/zubair-trabzada/geo-seo-claude) | ⭐4,621 | GEO 优先 SEO |
| [aso-skills](https://github.com/Eronred/aso-skills) | ⭐661 | ASO 应用商店优化 |
| [claude-wordpress-skills](https://github.com/elvismdev/claude-wordpress-skills) | ⭐129 | WordPress 工程 |
| [supabase-pentest-skills](https://github.com/yoanbernabeu/supabase-pentest-skills) | ⭐33 | Supabase 渗透测试 |
| [kube-audit-kit](https://github.com/crazygit/kube-audit-kit) | ⭐29 | K8s 安全审计 |

### 专业应用

| 工具 | Stars | 说明 |
|------|-------|------|
| [MedgeClaw](https://github.com/xjtulyc/MedgeClaw) | ⭐935 | 生物医学 AI 研究 |
| [claude-data-analysis](https://github.com/liangdabiao/claude-data-analysis) | ⭐354 | 数据分析智能体 |
| [daaf](https://github.com/DAAF-Contribution-Community/daaf) | ⭐157 | 数据分析师增强 |
| [claude-equity-research](https://github.com/quant-sentiment-ai/claude-equity-research) | ⭐400 | 股票研究插件 |
| [pentest-ai](https://github.com/0xSteph/pentest-ai) | ⭐171 | 渗透测试助手 |
| [agentic-malware-analysis](https://github.com/mrphrazer/agentic-malware-analysis) | ⭐180 | 恶意软件分析 |
| [jar-analyzer-claude](https://github.com/jar-analyzer/jar-analyzer-claude) | ⭐102 | Java JAR 审计 |
| [claude-gemini-bridge](https://github.com/tkaufmann/claude-gemini-bridge) | ⭐392 | Claude-Gemini 集成 |
| [claude-gemini-mcp-slim](https://github.com/cmdaltctr/claude-gemini-mcp-slim) | ⭐223 | Gemini MCP 集成 |
| [DeepVCode](https://github.com/OrionStarAI/DeepVCode) | ⭐413 | 全模型代码助手 |
| [sniffly](https://github.com/chiphuyen/sniffly) | ⭐1,193 | 使用统计仪表板 |
| [dotclaude](https://github.com/FradSer/dotclaude) | ⭐519 | 开发环境套件 |

---

## 📅 时间线

### 2025-02
- **首次泄露** - 早期版本源码泄露（影响较小）

### 2026-03-31
- **09:00 UTC** - Chaofan Shou (@Fried_rice) 发现 npm sourcemap 泄露
- **10:30 UTC** - 第一条推文发布
- **12:00 UTC** - GitHub 镜像仓库创建
- **14:00 UTC** - claw-code 仓库创建
- **16:00 UTC** - 突破 10k stars
- **18:00 UTC** - 突破 30k stars
- **20:00 UTC** - 突破 50k stars（历史最快）
- **23:59 UTC** - 超过 60k stars

### 2026-04-01
- **00:00 UTC** - 社区分析文章开始涌现
- **08:00 UTC** - Trail of Bits 发布安全沙箱
- **12:00 UTC** - awesome-claude-code-postleak-insights 创建
- **全天** - 数十个分析仓库创建（见上方列表）

---

## 📚 学习路径

### 入门（1-2 小时）
1. 阅读 [awesome-claude-code-postleak-insights](https://github.com/nblintao/awesome-claude-code-postleak-insights) README
2. 浏览 [claw-code](https://github.com/instructkr/claw-code) 项目
3. 浏览 [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) 工具列表
4. 观看社区讨论摘要

### 进阶（1-2 天）
1. 深度阅读 [catyans/claude-code-source-analysis](https://github.com/catyans/claude-code-source-analysis)（18 个文件）
2. 学习 [ThreeFish-AI/analysis_claude_code](https://github.com/ThreeFish-AI/analysis_claude_code) 中文分析
3. 研究隐藏功能（Buddy、KAIROS、ULTRAPLAN）
4. 阅读 [noya21th/claude-source-leaked](https://github.com/noya21th/claude-source-leaked) 87 个 feature flags

### 专家（1-2 周）
1. 完整阅读源码（512K+ 行）
2. 安全审计（使用 Trail of Bits 工具）
3. 构建自己的增强版本
4. 贡献回社区

---

## ⚠️ 法律与免责声明

### 使用限制
- ✅ **允许：** 学习、研究、安全审计
- ❌ **禁止：** 商业分发、侵犯版权、恶意利用

### 版权说明
- Claude Code 源码版权归 Anthropic 所有
- 本资源合集仅用于教育和研究目的
- 分析文章版权归各自作者所有

### 安全建议
1. 在沙箱环境中运行泄露源码
2. 不要将个人 API 密钥硬编码
3. 遵守当地法律法规
4. 尊重知识产权

---

## 🤝 贡献指南

### 提交资源
1. Fork 本仓库
2. 添加资源到对应分类
3. 提交 Pull Request
4. 说明资源价值和分类理由

### 资源标准
- ✅ 高质量原创分析
- ✅ 技术深度解读
- ✅ 安全研究成果
- ❌ 纯搬运无增值
- ❌ 侵权内容

### 参考模板
- [awesome-claude-code-postleak-insights](https://github.com/nblintao/awesome-claude-code-postleak-insights) - 高质量 curated list
- [awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) - 工具列表格式
- [awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents) - 子 Agent 分类

---

## 📞 联系方式

- **维护者：** 待添加
- **Issue 反馈：** [GitHub Issues](https://github.com/your-repo/issues)
- **讨论区：** [GitHub Discussions](https://github.com/your-repo/discussions)

---

## 📄 许可证

MIT License - 原创内容
第三方内容版权归各自作者所有

---

**最后更新：** 2026-04-01  
**资源总数：** 150+  
- GitHub 仓库：80+
- 分析文章：20+
- 社区讨论：10+
- 安全工具：25+
- 插件/技能：50+

**持续更新中...** 🔄
