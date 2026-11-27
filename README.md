# paper-reading-zh

用中文深度阅读研究论文的Claude Code skill，适用于大部分理工科论文。Claude会先获取论文全文和论文之外的信息（作者、venue、审稿记录、后续工作），再按定位、理解、证据、批判、延展五个部分输出16个环节的精读报告。

## 报告结构

| 部分 | 环节 |
|---|---|
| 定位 | 1 论文坐标：作者、venue与学术脉络 |
| 理解 | 2 研究问题与重要性 · 3 前人工作与不足 · 4 重建作者的思考路径 · 5 核心Intuition · 6 具体方法与完整Pipeline · 7 核心数学推导 |
| 证据 | 8 实验设计与结论 · 9 关键证据精读 · 10 Take-aways |
| 批判 | 11 审稿人视角 · 12 最脆弱的假设 · 13 最小复现实验 · 14 最强反例设计 |
| 延展 | 15 后续研究、学界反响与落地距离 · 16 Follow-up Research Idea |

两种按需行为：

- **速评模式**：只想快速判断时，输出论文坐标、三句话总结、核心intuition、最关键的证据、三个优点三个缺点、是否值得精读。
- **模拟导师追问**：准备组会、journal club或PhD面试时，在报告末尾追加5到8个最可能被追问的问题和回答要点。

## 安装

Windows（PowerShell）：

```powershell
git clone https://github.com/HongHua0/paper-reading-zh "$env:USERPROFILE\.claude\skills\paper-reading-zh"
```

macOS / Linux：

```bash
git clone https://github.com/HongHua0/paper-reading-zh ~/.claude/skills/paper-reading-zh
```

之后更新只需要在这个目录里执行`git pull`。

## 使用

在Claude Code里直接说：

- 帮我精读这篇论文 https://arxiv.org/abs/xxxx.xxxxx
- 快速看一下这篇paper值不值得读
- 下周PhD面试要和教授讨论这篇论文，帮我读一下

也可以输入`/paper-reading-zh`加上论文链接。

## 更新记录

### v2.1（2026-11）

- 删除领域适配表和针对特定学科的类比，第1、9、15节改为通用的理工科表述
- 核心证据是定理和证明的论文，第9节改为精读核心定理

### v2（2026-11）

这一版吸收了导师训练文献汇报时的提问方式和PhD面试中讨论论文的经验，把读论文从只看论文本身扩展到把论文放回作者、venue和领域脉络中审视。

- 新增第1节论文坐标：作者与lab研究线、研究类型与资源、venue与审稿记录、学术对话、验证环境、作者立场
- 新增第9节关键证据精读：对照与缺失对照，direction、significance、magnitude三步，实际意义与参照系，期望与兑现，作用发生在哪里
- 新增第11节审稿人视角：三句话总结、三个优点三个缺点、baseline比较是否公平、录用建议
- 新增第15节后续研究、学界反响与落地距离
- 加强第3、4、6、7、12、16节：领域默认选择与替代方案的内在困难、用作者前作重建思考路径、关键设计选择的取舍、核心公式的多角度解读、核心假设与backbone的一致性检查、预测作者团队的下一步
- 新增速评模式、模拟导师追问和领域适配表
- 要求作者背景、审稿意见、引用和后续研究必须来自实际检索，查不到就写查不到

### v1

12个环节的中文精读结构：研究问题、前人工作、作者思考路径、核心intuition、方法pipeline、数学推导、实验设计、take-aways、最脆弱的假设、最小复现实验、最强反例、follow-up idea。
