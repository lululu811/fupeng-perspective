# 付鹏视角 · Skill 蒸馏

> 「写不进去的那部分，才是你真正的护城河。」——但写得进去的部分，已经足够强大。

<div align="center">

**基于 [女娲 v2.0](https://github.com/alchaincyf/nuwa-skill) 流程的人物 Skill 蒸馏实践**

[![Python 3.10+](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Claude Code Skill](https://img.shields.io/badge/Claude%20Code-Skill-orange?logo=anthropic)](https://claude.ai/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/lululu811/fupeng-perspective/blob/main/LICENSE)

[特性](#-特性) · [快速开始](#-快速开始) · [项目结构](#-项目结构) · [方法论](#-方法论) · [核心心智模型](#-核心心智模型) · [贡献](#-贡献) · [致谢](#-致谢)

</div>

---

## 📖 项目简介

本项目是一个**人物思维框架蒸馏实验**——以著名经济学家付鹏为对象，实践「女娲 v2.0」Skill 造人术的完整流程。

**目标**：不是复制一个人，而是提炼他的**思维操作系统**——
- 🧠 他用什么**心智模型**看世界？（镜片）
- ⚡ 他用什么**决策启发式**做判断？（直觉规则）
- 🎨 他怎么**表达**？（DNA）
- 🚫 他**绝对不会**做什么？（反模式）
- 🤔 什么是这个 Skill **做不到**的？（诚实边界）

**关键区分**：捕捉的是 **HOW they think**，不是 **WHAT they said**。

最终产物是一个可运行的 [Claude Code Skill](https://docs.anthropic.com/en/docs/claude-code)，可以在分析问题时「切换到付鹏视角」。

## ✨ 特性

### 🎯 完整的蒸馏流程
从零到一的人物 Skill 蒸馏，包含 6 个阶段：
- **Phase 0**: 入口确认与需求澄清
- **Phase 1**: 6 维度 Agent 并行调研
- **Phase 1.5**: 预提炼质量门禁（自动化工具）
- **Phase 2**: 思维框架提炼（心智模型 + 决策启发式 + 表达 DNA）
- **Phase 3**: Skill 构建（基于模板）
- **Phase 4**: 质量验证与双 Agent 精炼

### 📊 丰富的素材基础
| 素材类型 | 数量 | 说明 |
|---------|------|------|
| 📚 书籍章节 | 164 篇 | 《见证逆潮》等著作 |
| 📰 文章 | 245 篇 | V 专栏、研究报告 |
| 🎙️ 访谈/演讲 | 442 份 | 长白山论坛、Bloomberg、播客 |
| 🔬 调研文档 | 10 份 | 6 维度 Agent 调研 + 验证 + 精炼 |

### 🧩 12 个核心心智模型
提炼出付鹏思维体系的 12 个核心框架：

1. **三齿轮模型** — 生产力 / 生产关系 / 秩序
2. **分子 × 分母 × g 因子** — 资产定价框架
3. **吃鸡缩圈** — 风险偏好动态收缩
4. **产业生命周期路径** — 修路 vs 通车
5. **VIX 期限结构信号** — 波动率曲线解读
6. **全球套息传导链** — 跨市场联动机制
7. **黄金三因子定价** — 实际利率 / 信用 / 避险
8. **哑铃型配置结构** — 极端分化下的资产配置
9. **分工决定分配** — 来自《见证逆潮》
10. **债务与杠杆宿命循环** — 来自《见证逆潮》
11. **K 型社会** — 来自《见证逆潮》
12. **FICC 联动框架** — 来自《见证逆潮》

### 🏷️ 置信度标注体系
每个模型、每条启发式都标注了可信度等级：
- 🟢 **一手** — 付鹏直接表述，可信度最高
- 🟡 **推断** — 基于行为/立场推断，非直接表述
- 🔴 **推测** — 基于二手信息，可信度最低

### 🔍 矛盾保留原则
矛盾是人格的核心特征，不是需要修复的 Bug：
- **时间性矛盾** — 观点演化，标注「早期」「近期」
- **领域性矛盾** — 不同场景不同规则，不强求统一
- **本质性张力** — 价值观内在冲突，明确记录

## 🚀 快速开始

### 前置要求

- Python 3.10+
- Claude Code（用于运行 Skill）

### 安装与使用

```bash
# 1. 克隆仓库
git clone https://github.com/lululu811/fupeng-perspective.git
cd fupeng-perspective

# 2. 运行预提炼工具（可选，用于质量检查）
python scripts/pre_extract.py .

# 3. 将 SKILL.md 复制到你的 Claude Code skills 目录
cp SKILL.md ~/.claude/skills/fupeng-perspective.md

# 4. 在 Claude Code 中激活
# 对话中说「用付鹏的视角」或「付鹏模式」即可触发
```

### 触发词

以下表达会激活付鹏视角 Skill：
- 「用付鹏的视角看看...」
- 「付鹏会怎么分析...」
- 「切换到付鹏模式」
- 「付鹏 perspective」
- 「帮我用付鹏的角度想想」

## 📁 项目结构

```
fupeng-perspective/
├── SKILL.md                          # 最终产物：可运行的 Claude Code Skill
├── README.md                         # 本文件
├── scripts/
│   └── pre_extract.py                # Phase 1.5 预提炼工具
├── references/
│   ├── research/                     # 6 维度 Agent 调研结果
│   │   ├── 01-writings.md            # 著作与系统思考
│   │   ├── 02-conversations.md       # 对话与访谈素材 ⭐
│   │   ├── 03-expression-dna.md      # 表达 DNA
│   │   ├── 04-external-views.md      # 他者视角
│   │   ├── 05-decisions.md           # 决策记录 ⭐
│   │   ├── 06-timeline.md            # 人物时间线
│   │   ├── 07-verification-results.md
│   │   ├── 08-refinement-suggestions.md
│   │   ├── 09-incremental-update-2025H2.md
│   │   └── 10-model-revalidation-2025H2.md
│   ├── sources/                      # 一手素材（需单独下载）
│   │   ├── books/                    # 书籍章节
│   │   ├── transcripts/              # 演讲/访谈文字稿
│   │   └── articles/                 # 专栏文章
│   ├── extraction-framework.md       # 思维框架提炼方法论
│   └── skill-template.md             # SKILL.md 构建模板
└── templates/
    └── result-card.html              # 成果展示卡片模板
```

> 📌 **关于素材**：`references/sources/` 目录包含大量受版权保护的原始素材，**不包含在本开源仓库中**。如需用于研究，请自行收集或联系作者。

## 🧪 方法论

### 心智模型识别的三重验证

一个论点要被认定为「心智模型」，必须通过：

| 验证 | 标准 | 例子 |
|------|------|------|
| **跨域复现** | 同一框架出现在 ≥2 个不同领域 | 纳瓦尔的「杠杆」在财富/成长/职业中都出现 |
| **有生成力** | 能推断此人对新问题的立场 | 芒格的「逆向思维」可以推广到任何领域 |
| **有排他性** | 不是所有聪明人都这样想 | 塔勒布的「反脆弱」是他的独特视角 |

### 表达 DNA 量化

从 20 个随机段落统计：
- 平均句长、疑问句比例、类比密度
- 第一人称使用率、确定性语气比例、转折频率

### 质量自检

- ✅ 每个模型有至少 2 个不同领域的证据
- ✅ 模型数量在 3-7 个之间（宁少勿多）
- ✅ 读起来有辨识度，不像通用 AI
- ✅ 明确写了做不到什么
- ✅ 删掉名字后，还能认出这是谁的思维方式

## 🎯 核心心智模型详解

### 1. 三齿轮模型

**置信度**: 🟢 高 | **状态**: ✅ 持续

付鹏分析宏观经济的底层框架：
- **齿轮 1**：生产力（技术、效率）
- **齿轮 2**：生产关系（制度、分配）
- **齿轮 3**：秩序（地缘、规则）

三个齿轮相互咬合，驱动历史演进。当齿轮间出现摩擦，就是变革的信号。

### 2. 分子 × 分母 × g 因子

**置信度**: 🟢 高 | **状态**: ✅ 持续

资产定价的核心公式：
- **分子**：企业盈利/现金流
- **分母**：贴现率（利率 + 风险溢价）
- **g 因子**：增长率预期

不同时期，主导因子不同。识别当前主导因子，是判断资产价格的关键。

### 3. 吃鸡缩圈

**置信度**: 🟢 高 | **状态**: ✅ 持续

风险偏好的动态模型：
- 经济扩张期 = 吃鸡游戏的「大圈」，风险偏好高，什么都涨
- 经济收缩期 = 「缩圈」，风险偏好收缩，只有核心资产存活
- 识别当前处于「圈」的哪个位置，决定配置策略

### 4. 产业生命周期：修路 vs 通车

**置信度**: 🟢 高 | **状态**: ✅ 持续

产业投资的两个阶段：
- **修路期**：基础设施投入，赢家不确定，赌的是方向
- **通车期**：格局已定，赢家通吃，赌的是执行

很多人混淆这两个阶段，用修路的逻辑投通车期的公司，或反之。

> 💡 更多模型详见 [SKILL.md](./SKILL.md)

## 🤝 贡献

欢迎贡献！你可以：

1. **补充素材**：如果你有一手素材（演讲视频、访谈文字稿等），欢迎提交 PR
2. **改进调研**：完善 `references/research/` 中的调研文档
3. **优化 Skill**：改进 SKILL.md 的表达、补充心智模型
4. **报告问题**：发现 Skill 输出不符合付鹏实际观点时，请开 Issue

### 贡献流程

```bash
# 1. Fork 本仓库
# 2. 创建分支
git checkout -b feature/your-feature

# 3. 提交更改
git commit -m "feat: 添加某某心智模型的证据"

# 4. 推送并创建 Pull Request
git push origin feature/your-feature
```

## 📚 致谢

- **付鹏** — 东北证券首席经济学家，著有《见证逆潮》，其宏观分析框架是本项目的核心素材来源
- **[女娲 · Skill 造人术](https://github.com/alchaincyf/nuwa-skill)** — 花叔创建的人物 Skill 蒸馏方法论，本项目基于其 v2.0 流程
- **Claude Code** — Anthropic 的 AI 编程助手，提供了 Skill 的运行环境

## ⚠️ 免责声明

本项目是基于公开信息的**思维框架提炼实验**，不代表付鹏本人的立场。

- 所有模型和观点均来自公开素材，经过提炼和结构化
- Skill 的输出是**推断性**的，不是付鹏本人的真实想法
- 投资相关内容仅供参考，不构成投资建议
- 调研截止：2024-2025 年初

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源。

---

<div align="center">

**如果这个项目对你有帮助，欢迎给它一个 ⭐ Star！**

[Issues](https://github.com/lululu811/fupeng-perspective/issues) · [Pull Requests](https://github.com/lululu811/fupeng-perspective/pulls) · [Discussions](https://github.com/lululu811/fupeng-perspective/discussions)

</div>
