# Chong Reading Method
# Chong 阅读方法

> Complete academic paper workflow using Phillip Chong Ho Shon's functional coding method
> 使用 Phillip Chong Ho Shon 功能编码法的完整学术论文工作流程

[English](#english) | [中文](#中文)

---

## English

### Overview

**Chong Reading Method** is a systematic approach for reading, analyzing, and synthesizing academic papers. It transforms passive reading into active academic production through a three-phase workflow using 16 functional codes.

### Features

- **Three-Phase Workflow**: Reading → Synthesis → Writing
- **16 Functional Codes**: WTD, SPL, CPL, GAP, RAT, ROF, WTDD, RCL, RTC, RFW, POC, MOP, RPP, WIL + Theme Codes
- **Language Support**: Output in paper's original language, English, Simplified Chinese, or Traditional Chinese
- **Automated Output**: Generates Annotated.md, RCOS_Master.md, Synthesis.md, and WritingScaffold.md

### What's New (v1.2.0)

- **Language Selection**: Choose output language (follow paper / English / Simplified Chinese / Traditional Chinese)
- **Improved Formatting**: Content, Theme, and Location fields now display on separate lines
- **Prerequisite Check**: Warns before synthesis/writing if no Annotated Documents exist

### The Three-Phase Workflow

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│    READING      │────▶│    SYNTHESIS    │────▶│    WRITING      │
│                 │     │                 │     │                 │
│ Analyze papers  │     │ Find patterns   │     │ Transform to    │
│ one at a time   │     │ across papers   │     │ academic output │
│                 │     │                 │     │                 │
│ Output:         │     │ Output:         │     │ Output:         │
│ • Annotated.md  │     │ Synthesis.md    │     │ WritingScaffold│
│ • RCOS row      │     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘

         ▲                                                │
         │                                                │
         └────────────────────────────────────────────────┘
                    (Read more papers as needed)
```

### Installation

#### Option 1: Direct Skill Import
Copy the `chong-reading-method.skill` file to your Claude Code skills directory:
```
~/.claude/skills/chong-reading-method/
```

Then import in Claude Code:
```
/chong-reading-method
```

#### Option 2: Manual Installation
1. Download the `chong-reading-method.skill` file
2. Extract its contents (it's a ZIP file)
3. Place the `SKILL.md` file in your skills directory: `~/.claude/skills/chong-reading-method/SKILL.md`
4. (Optional) Place the `README.md` in the same directory for documentation
5. Restart Claude Code or the skill will be available

### How It Works

The skill automatically detects which phase you need based on your request:

| You say... | Phase | What happens |
|------------|-------|--------------|
| "paper-reader", "read this paper", "analyze this" | READING | Analyze a single paper with functional codes |
| "paper-synthesis", "compare papers", "synthesize" | SYNTHESIS | Find patterns across papers |
| "paper-writer", "help me write", "right-angle turn" | WRITING | Generate writing scaffold |

**Note**: The synthesis and writing phases require Annotated Documents from the reading phase. If none exist, the skill will remind you to run paper-reader first.

### The 16 Reading Codes

| Code | Full Name | What It Identifies |
|------|-----------|-------------------|
| **WTD** | What They Do | Research question or objective |
| **SPL** | Summary of Previous Literature | What others have found |
| **CPL** | Critique of Previous Literature | Limitations of existing studies |
| **GAP** | Gap | Missing element in current knowledge |
| **RAT** | Rationale | Why this study is necessary |
| **ROF** | Results of Findings | Primary findings/claims |
| **WTDD** | What They Did | Summary of what was accomplished |
| **RCL** | Results Consistent with Literature | Findings supporting existing research |
| **RTC** | Results to The Contrary | Findings contradicting previous research |
| **RFW** | Recommendations for Future Works | What still needs study |
| **POC** | Point of Critique | Flaw/limitation YOU identify |
| **MOP** | Missed Obvious Point | Overlooked connection or literature |
| **RPP** | Relevant Point to Pursue | Basis for your own paper |
| **WIL** | Will | Logical prompt: can X resolve Y? |

### Storage

All outputs are saved to:
```
~/Documents/Papers/{ProjectName}/
```

Files generated:
- `{Author}_{Year}_Annotated.md` — Individual paper analysis
- `RCOS_Master.md` — Cumulative table of all papers (auto-maintained)
- `Synthesis_{date}.md` — Cross-paper synthesis (when you run synthesis)
- `WritingScaffold_{date}.md` — Writing scaffold (when you run writing phase)

### Requirements

- Claude Code with access to Read tool
- WebFetch or similar capabilities for reading papers from URLs
- (Optional) Zotero integration for reading papers from your library

### Credits

Based on Phillip Chong Ho Shon's functional coding method for academic reading.

---

## 中文

### 概述

**Chong 阅读方法**是一种系统化的学术论文阅读、分析和综合方法。它通过三阶段工作流程和16个功能编码，将被动阅读转变为主动学术产出。

### 功能特点

- **三阶段工作流程**：阅读 → 综合 → 写作
- **16个功能编码**：WTD、SPL、CPL、GAP、RAT、ROF、WTDD、RCL、RTC、RFW、POC、MOP、RPP、WIL + 主题编码
- **语言支持**：输出语言可选择跟随论文原文、英语、简体中文或繁体中文
- **自动生成输出**：生成 Annotated.md、RCOS_Master.md、Synthesis.md 和 WritingScaffold.md

### 最新更新 (v1.2.0)

- **语言选择**：可选择输出语言（跟随论文原文/英语/简体中文/繁体中文）
- **格式优化**：内容、主题、位置字段现在分行显示
- **前置检查**：在综合/写作阶段前检查是否存在标注文档

### 三阶段工作流程

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│    阅读阶段      │────▶│    综合阶段      │────▶│    写作阶段      │
│                 │     │                 │     │                 │
│ 逐篇分析论文    │     │ 发现跨论文模式   │     │ 转化为学术输出  │
│                 │     │                 │     │                 │
│ 输出:           │     │ 输出:           │     │ 输出:           │
│ • Annotated.md │     │ Synthesis.md   │     │ WritingScaffold│
│ • RCOS 行      │     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘

         ▲                                                │
         │                                                │
         └────────────────────────────────────────────────┘
                    (根据需要阅读更多论文)
```

### 安装方法

#### 方法一：直接导入技能
将 `chong-reading-method.skill` 文件复制到您的 Claude Code 技能目录：
```
~/.claude/skills/chong-reading-method/
```

然后在 Claude Code 中导入：
```
/chong-reading-method
```

#### 方法二：手动安装
1. 下载 `chong-reading-method.skill` 文件
2. 解压文件内容（这是 ZIP 文件）
3. 将 `SKILL.md` 放到技能目录：`~/.claude/skills/chong-reading-method/SKILL.md`
4. （可选）将 `README.md` 放到同一目录作为文档
5. 重启 Claude Code 或技能将可用

### 使用方法

技能会根据您的请求自动检测需要哪个阶段：

| 您说... | 阶段 | 发生什么 |
|---------|------|----------|
| "paper-reader"、"read this paper"、"analyze this" | 阅读 | 使用功能编码分析单篇论文 |
| "paper-synthesis"、"compare my papers"、"synthesize" | 综合 | 发现跨论文模式 |
| "paper-writer"、"help me write"、"right-angle turn" | 写作 | 生成写作脚手架 |

**注意**：综合和写作阶段需要阅读阶段生成的标注文档。如果不存在，技能会提醒您先运行 paper-reader。

### 16个阅读编码

| 编码 | 全称 | 识别内容 |
|------|------|----------|
| **WTD** | 他们做什么 | 研究问题或目标 |
| **SPL** | 文献综述总结 | 他人发现 |
| **CPL** | 文献综述批评 | 现有研究的局限性 |
| **GAP** | 研究空白 | 当前知识的缺失 |
| **RAT** | 研究理由 | 为什么这项研究是必要的 |
| **ROF** | 研究发现结果 | 主要发现/主张 |
| **WTDD** | 他们做了什么 | 完成内容的总结 |
| **RCL** | 与文献一致的结果 | 支持现有研究的结果 |
| **RTC** | 与文献相反的结果 | 与先前研究相矛盾的发现 |
| **RFW** | 未来工作建议 | 仍需研究的内容 |
| **POC** | 批评观点 | 您识别的缺陷/局限性 |
| **MOP** | 遗漏的明显观点 | 忽略的关联或文献 |
| **RPP** | 可追求的相关观点 | 您自己论文的基础 |
| **WIL** | 延伸思考 | 逻辑提示：X能解决Y吗？ |

### 存储位置

所有输出保存至：
```
~/Documents/Papers/{项目名称}/
```

生成的文件：
- `{作者}_{年份}_Annotated.md` — 单篇论文分析
- `RCOS_Master.md` — 所有论文的累积表（自动维护）
- `Synthesis_{日期}.md` — 跨论文综合（运行综合时生成）
- `WritingScaffold_{日期}.md` — 写作脚手架（运行写作阶段时生成）

### 需求

- 可使用 Read 工具的 Claude Code
- 用于从 URL 读取论文的 WebFetch 或类似功能
- （可选）Zotero 集成，用于从您的文献库读取论文

### 致谢

基于 Phillip Chong Ho Shon 的学术阅读功能编码方法。

---

## License | 许可证

MIT License
