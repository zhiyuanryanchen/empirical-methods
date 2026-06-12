# 经济与商务实证研究方法课程大纲

2026 春季学期  
版本：2026-04-24

## 课程基本信息

- **任课教师**：陈志远
- **邮箱**：[chenzhiyuan@rmbs.ruc.edu.cn](mailto:chenzhiyuan@rmbs.ruc.edu.cn)
- **办公地点**：商学楼316（通州校区）
- **上课时间**：周五 14:00-17:30
- **上课地点**：商学楼103（通州校区）
- **答疑方式**：预约制

说明：本课程按 9 周组织。目前已发布第 1 至第 4 周讲义与详稿，第 5 至第 9 周材料将按授课进度陆续更新。

## 课程定位

本课程面向经济学、管理学与金融学方向的研究生，训练学生在 AI 时代开展高水平实证研究。课程围绕五条主线展开：

1. 简约形式因果推断
2. 因果机器学习
3. 结构估计
4. LLM 文本分析
5. AI 研究自动化

课程的核心教学主张是：AI 改变了研究的速度、边界与协作方式，但不会替代识别判断、验证过程与研究者责任。学生需要学会高强度使用 AI 工具，同时保留清晰的审计轨迹、纠错记录与复现能力。

## 先修要求

学生应具备研究生层面的计量经济学基础，并熟悉基本微观经济学逻辑。此前接触过 Stata 或 Python 会有帮助，但不是硬性要求。

课程默认学生愿意学习并逐步熟悉以下工作流：

- VS Code
- Python
- Stata 或 R
- Jupyter notebooks
- 基本版本控制习惯

## 学习目标

课程结束后，学生应能够：

1. 将经验问题明确表述为描述性、因果性或反事实问题
2. 实现并解释现代简约形式工具，尤其是 DiD 及其拓展形式
3. 理解 DML、因果森林等因果机器学习工具的逻辑与适用边界
4. 解释何时需要结构估计，并能够阅读和讨论基本反事实分析
5. 构造并验证一个可进入经验研究的 LLM 文本指标
6. 在使用 AI 工具时记录验证过程、不确定性与失败模式

## AI 使用规范

课程允许并鼓励使用 Copilot、ChatGPT、Claude、Gemini 等工具辅助编码、调试、文献筛选、提示标注和研究写作，但任何 AI 输出都不能绕过人工验证。

学生可以在以下任务中使用 AI：

- 代码起草
- debugging 辅助
- 文献初筛
- 提示式文本标注
- notebook 文档整理
- 复现流程支持

学生不得将未经验证的 AI 输出直接作为原创成果提交。

凡使用 AI 的作业、实验或项目，必须附上一段简短的工作流附录，至少说明：

- 使用了哪些工具
- 分别用于哪些任务
- 至少一个被采纳的输出示例
- 至少一个被拒绝或修正的输出示例
- 最终结果如何被验证

未披露的 AI 使用将被视为工作流规范违例。

## 成绩构成

- 课堂参与与讨论：20%
- Problem sets 与实验室练习：30%
- AI 工作流备忘录与审计附录：10%
- 期末项目与展示：40%

### 参与和讨论

本课程重视课堂参与，因为很多讨论围绕研究设计、编码决策、工具使用与验证逻辑展开。学生应准备好同时讨论经验研究内容和工作流选择。

### 实验与作业

作业更强调实现、解释与验证，而不是机械推导。部分作业将以 notebook 为载体，部分作业会要求学生比较传统工作流与 AI 辅助工作流。

### 期末项目

学生可以个人完成，也可以最多三人组队。期末项目可以采用以下四种形式之一：

1. 一个简约形式复制并扩展项目，并加入 AI 辅助稳健性检查
2. 一个因果机器学习应用，并清楚解释识别与异质性结论
3. 一个结构估计演示，并至少完成一个反事实练习
4. 一个 LLM 文本分析项目，并对文本指标进行人工校验与下游应用

所有期末项目都必须提交 AI 工作流附录。

## 9 周课程安排

### 第 1 周：AI 时代的实证研究

**核心主题**

- 潜在结果框架与研究设计
- 描述性、因果性与反事实问题的区别
- AI 如何改变研究前沿

**讲义入口**

- [第 1 周讲义](../LectureNotes/W1_AI_Era_Empirical_Research.qmd)
- [第 1 周详细讲义](../LectureNotes/W1_AI_Era_Empirical_Research_notes.qmd)

**建议阅读**

- Abadie & Cattaneo (2018)
- *Good and Bad Controls*
- [Applied Causal Inference Powered by ML and AI](https://arxiv.org/abs/2403.02467)

### 第 2 周：计算基础与工作流

**核心主题**

- VS Code、Python、Stata、Jupyter 的协同使用
- 仿真、debugging 与数值直觉
- 带审计轨迹的 vibe coding

**讲义入口**

- [第 2 周讲义](../LectureNotes/W2_Computational_Foundations.qmd)
- [第 2 周详细讲义](../LectureNotes/W2_Computational_Foundations_notes.qmd)

**实验入口**

- [L2_Python_Basics.ipynb](../Labs/L2_Python_Basics.ipynb)
- [L2_Stata_Basics.ipynb](../Labs/L2_Stata_Basics.ipynb)
- [L2_R_Basics.ipynb](../Labs/L2_R_Basics.ipynb)

### 第 3 周：面板数据与经典 DiD

**核心主题**

- 面板结构与固定效应
- 经典 2x2 DiD 与 two-way fixed effects
- 平行趋势、事件研究与 placebo 检验
- 聚类标准误 Monte Carlo

**讲义入口**

- [第 3 周讲义](../LectureNotes/W3_Panel_and_Classical_DID.qmd)
- [第 3 周详细讲义](../LectureNotes/W3_Panel_and_Classical_DID_notes.qmd)

**实验入口**

- [L3_Clustering_MonteCarlo.ipynb](../Labs/L3_Clustering_MonteCarlo.ipynb)

### 第 4 周：现代 DiD 与合成控制

**核心主题**

- Goodman-Bacon 分解与 staggered adoption
- Callaway-Sant'Anna、Sun-Abraham、dCdH、BJS
- synthetic control 与 synthetic DiD

**讲义入口**

- [第 4 周讲义](../LectureNotes/W4_Modern_DID_and_Synthetic_Control.qmd)
- [第 4 周详细讲义](../LectureNotes/W4_Modern_DID_and_Synthetic_Control_notes.qmd)

**实验入口**

- [L4-Diff-in-Diffs-More.ipynb](../Labs/L4-Diff-in-Diffs-More.ipynb)

### 第 5 周：因果机器学习

**核心主题**

- prediction versus causation
- LASSO、Double / Debiased ML、orthogonalization
- causal forests 与异质性处理效应

**材料状态**

- 即将发布

### 第 6 周：结构估计基础

**核心主题**

- 原语、矩条件、似然、仿真与识别
- 反事实逻辑与机制分析

**材料状态**

- 即将发布

### 第 7 周：结构估计应用

**核心主题**

- 需求估计
- 引力模型
- 定价、并购、关税与平台反事实

**材料状态**

- 即将发布

### 第 8 周：LLM 文本分析

**核心主题**

- prompt-based classification
- construct validity 与 annotation reliability
- 文本指标进入下游经验模型

**材料状态**

- 即将发布

### 第 9 周：AI 研究自动化与期末展示

**核心主题**

- 文献综述自动化
- 规格搜索与 guardrails
- agentic research workflows
- 复现检查与工作流治理

**材料状态**

- 即将发布

## 推荐阅读主线

### 方法基础

- Abadie & Cattaneo (2018)
- Bertrand, Duflo & Mullainathan (2004)
- Cameron & Miller (2015)
- Wooldridge DID lecture notes

### 文本与 AI

- [Applied Causal Inference Powered by ML and AI](https://arxiv.org/abs/2403.02467)
- [Automated Social Science](https://arxiv.org/abs/2404.11794)
- [AI-Powered (Finance) Scholarship](https://www.nber.org/papers/w33363)

## 提交规范

所有 notebook 或代码型作业都应当可复现。学生需要清楚说明运行环境，并保持脚本、notebook 与输出结果组织有序。凡使用 AI，应保留足够证据，使其他研究者能够理解工具做了什么，以及学生在何处进行了判断和修正。

本课程最重要的工作流原则很简单：积极使用现代工具，但绝不让工具掩盖你的推理过程。
