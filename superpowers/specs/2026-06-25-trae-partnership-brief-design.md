# Design Spec: Trae Partnership Brief — "One-Stop Econ Research"

**Date:** 2026-06-25
**Author:** 陈志远 (Zhiyuan Chen), 中国人民大学商学院
**Target Audience:** 字节跳动 Trae 产品 & 工程团队
**Format:** Single-file HTML product brief (editorial style)
**Language:** 中文为主 (Chinese primary)
**Estimated Read Time:** 15–20 minutes
**Goal:** 展示高校讲座足迹与需求，指出当前科研工具链碎片化痛点，提出基于 Trae Agent 架构的「One-Stop Econ Research」插件概念，推进产学研合作落地。

---

## 1. Narrative Arc

| Section | Purpose | Read Time | Emotional Beat |
|---------|---------|-----------|----------------|
| **Hero** | 建立 credibility + 核心论点 | 30 sec | 自信、好奇 |
| **Lecture Footprint** | 证明需求：在哪讲过、谁听过、他们带走了什么 | 2 min | 权威、规模 |
| **The Problem** | 痛点：科研工具链碎片化 | 2 min | 共鸣、焦虑 |
| **The Demo** | 今天可行的方案 (VS Code + AI workflow) | 3 min | "这能跑通" |
| **The Gap** | VS Code + Copilot 做不到的事 — Trae 的机会 | 2 min | 期待、清晰 |
| **The Proposal** | 具体插件概念：「One-Stop Econ Research」 | 4 min | 兴奋、可行 |
| **Why Trae + CTA** | 战略契合与下一步 | 2 min | 紧迫、合作 |

**Core Narrative:**
> *"我在中国顶尖高校讲授了 AI-Native IDE 科研方法论，听众超过 300 人。反馈高度一致：他们需要这个，但 VS Code + Copilot 不是为他们建的。Trae 可以是。"*

---

## 2. Section-by-Section Content & Copy

### 2.1 Hero Section

**Layout:** Full-width, deep navy background (`#1a1a2e`), centered text, generous padding (`clamp(6rem, 8vw, 12rem)` vertical).

**Elements:**
- **Top tag:** "科研工作流 × AI-Native IDE" — small, all-caps, cyan (`#00A8CC`), letter-spacing 0.1em
- **Headline (H1):** "为实证研究者打造真正需要的 IDE"
- **Subheadline:** "从碎片化工具到统一 Agent 驱动科研 — 一份给 Trae 的合作提案"
- **Author line:** "陈志远 · 中国人民大学商学院 · 经济实证研究方法课程负责人"
- **CTA Button:** "阅读提案" — primary cyan button, smooth-scroll to Section 3 (The Problem)
- **Secondary link:** "查看讲座足迹" — text link, smooth-scroll to Section 2

**Visual:** Optional subtle background pattern — abstract network/graph lines (echoing DAG diagrams from econometrics) in very low opacity (`rgba(0, 168, 204, 0.05)`).

---

### 2.2 Lecture Footprint Section

**Layout:** White background, max-width 1200px, responsive card grid (3 columns on desktop, 2 on tablet, 1 on mobile).

**Section Title:** "我在哪里讲过 — 学生们在问什么"

**Subtitle:** "AI-Native IDE 科研方法论受邀讲座系列，覆盖 9 所中国高校。"

**Card Content (11 cards, 6 已完成带照片, 5  upcoming 带占位):**

| Card | Institution | Status | Audience | Key Takeaway | Photo |
|------|-------------|--------|----------|--------------|-------|
| 1 | **中国人民大学** | 已完成 | ~100 研究生与教师 | *"AI平权框架：AI 素养正在成为新的不平等来源。"* | `gallary/20260604_One-StopVScode.jpeg` |
| 2 | **中央财经大学** | 已完成 | ~80 研究生与教师 | *"AI 是放大器 — 既放大能力，也放大无知。"* | `gallary/20260609-onestopresearch-cufe1.jpg` |
| 3 | **南京大学** | 已完成 | ~60 研究生与教师 | *"碎片化的工具链才是瓶颈，不是模型。"* | `gallary/20260615_onestopresearch_nju.jpeg` |
| 4 | **对外经济贸易大学** | 已完成 | ~50 研究生与教师 | *"每个工具都是开源的，但整合是缺失的。"* | `gallary/20260617-onestopresearch-uibe.png` |
| 5 | **首都经济贸易大学** | 已完成 | ~40 研究生与教师 | *"Stata + Python + LaTeX 在一个项目里 — 学生非常喜欢。"* | `gallary/20260624CUEB_SOF.png` |
| 6 | **首都经济贸易大学 ISEM** | 已完成 | ~30 教师与研究者 | *"Agent 模式是处理多文件科研工作流的唯一方式。"* | `gallary/20260624CUEB-ISEM.png` |
| 7 | **北京师范大学** | 即将举办 | — | — | 占位符 |
| 8 | **江西财经大学** | 即将举办 | — | — | 占位符 |
| 9 | **西安交通大学** | 即将举办 | — | — | 占位符 |
| 10 | **湘潭大学** | 即将举办 | — | — | 占位符 |
| 11 | **重庆大学** | 即将举办 | — | — | 占位符 |

**Photo Handling:**
- 已完成讲座：使用 `zhiyuanryanchen.github.io/gallary/` 中的真实照片。每张卡片显示小照片缩略图（圆角，16:9 比例，~200px 宽），展示大学建筑或讲堂场景。
- 即将举办讲座：使用 subtle 占位符，Trae 青色 (`#00A8CC`) 渐变背景，带 "即将举办" 徽章。
- **注意：** 湘潭大学 (XTU) 尚未在网站图库中 — 标记为即将举办。

**Card Design:**
- 每张卡片：白色背景，圆角 (`12px`)，轻微阴影 (`0 4px 24px rgba(0,0,0,0.06)`)，内边距 `1.5rem`。
- 顶部：照片徽章（如有）或占位符渐变。
- 学校名称：粗体，`1.1rem`，`--text-primary`。
- 听众：小徽章（如 "~100 研究生与教师"）。
- 关键收获：斜体，引号，`--text-secondary`，略小字体。
- 即将举办卡片：右上角添加青色 "UPCOMING" 徽章。

**底部总结语：**
> "6 场已完成讲座，5 场已确认排期。反馈高度一致：研究者需要这个，但没有 IDE 为他们的工作流而构建。"

**视觉要点：** 照片创造情感、人性化的连接 — Trae 看到真实的讲堂、真实的学生、真实的需求。不是一份泛泛而谈的提案。

---

### 2.3 The Problem Section

**Layout:** Light gray background (`#f8f9fa`), max-width 960px, centered.

**Section Title:** "问题：科研不是普通的编程"

**Opening paragraph:**
> "VS Code + Copilot 是出色的通用编程环境。但经济与管理学科的实证研究不是普通的编程。它是一个跨数据、估计、可视化、写作的结构性多步骤工作流 — 带有严格的可复现性要求和领域特定惯例，而通用 AI 并不理解这些。"

**Three Pain Cards (2-column grid on desktop, stacked on mobile):**

**Card 1: Fragmented Toolchain**
- **Icon:** Broken chain or scattered windows icon (CSS-generated)
- **Headline:** "五个窗口，一个项目"
- **Body:** "Stata 做 DID 估计。Python 做数据清洗。Matlab 做结构校准。LaTeX 写论文。浏览器标签页开 ChatGPT。结果在工具之间手动复制粘贴。表格里一个系数 typo 就能毁掉整篇论文 — 而且没人发现，直到审稿。"
- **VS Code reality:** "每个工具都有扩展，但它们互不通信。Copilot 能补全 `reghdfe` 的一行，但不知道这行输出对论文下一节意味着什么。"

**Card 2: Domain Blindness**
- **Icon:** Eye with slash or puzzle piece (CSS-generated)
- **Headline:** "AI 不懂计量经济学"
- **Body:** "让 Copilot '跑一个带聚类标准误的 DID'。它会写一段看起来合理的代码。但它不会问：平行趋势假设可信吗？事件研究的 lead 检查了吗？你在正确的层级聚类吗？这些不是编程问题 — 是研究设计问题。"
- **VS Code reality:** "聊天就是聊天。没有系统性验证。没有对标准误聚类层级为什么影响因果推断的理解。"

**Card 3: No Native Agent Workflow**
- **Icon:** Single person vs. team (CSS-generated)
- **Headline:** "聊天不是工作流"
- **Body:** "学生把 AI 输出复制粘贴进脚本。他们不知道什么改了。六个月后再跑论文，已经复现不了。导师问 '这个表怎么生成的？' 答案是：'我问了 AI，它给了我一个看起来对的。'"
- **VS Code reality:** "Copilot Chat 回答问题。它不会规划一个多步骤研究管线，跨工具执行，验证输出，并记录一切以保证可复现。"

**Closing line (bold, centered):**
> **"VS Code 把科研当成普通编程。实证科研不是普通编程。"**

---

### 2.4 The Demo Section

**Layout:** White background, max-width 1200px, alternating text + CSS diagram layout (text left, diagram right; then reverse).

**Section Title:** "今天能跑通的方案 — 以及为什么还不够"

**Intro:**
> "我构建了一个概念验证工作流，证明这个愿景是可行的。它能跑。但它需要 4 个独立扩展、3 个 MCP 服务器、手动 Git 纪律，而且 AI 在 Stata 和 LaTeX 之间切换时经常丢失上下文。研究者们在拼凑这个，因为没有 IDE 为他们的工作流而构建。"

**Demo Step 1: The Unified Project**
- **Text:** "所有工具在一个文件夹：`data/`、`scripts/`、`notebooks/`、`paper/`、`output/`。Python 生成合成数据。Stata 做 DID 估计。Matlab 做结构校准。LaTeX 写最终论文。"
- **Diagram:** CSS-generated project tree diagram showing the folder structure with file icons and labels

**Demo Step 2: AI Cross-Tool Execution**
- **Text:** "Claude Code 通过 MCP 运行 Stata DID 分析，读取回归输出，然后写 LaTeX 表格到 `paper/main.tex`。AI 理解完整上下文：不只是代码，而是研究流程。"
- **Diagram:** CSS-generated flow diagram showing: Stata → MCP → AI → LaTeX with arrow connections

**Demo Step 3: The Final Output**
- **Text:** "一个提交就绪的 PDF，带表格、图形和可追溯的出处。每个数字都能链接回生成它的脚本。"
- **Diagram:** CSS-generated document preview with highlighted table and figure areas

**Transition bridge:**
> "这是概念验证。但胶带已经露出来了。如果这个工作流是 IDE 原生的 — 而不是拼凑的扩展集合 — 会怎样？"

**Visual Note:** All diagrams are CSS-generated (no screenshots needed). Use:
- Simple CSS box diagrams with borders and shadows for file trees
- Arrow connectors using CSS borders or pseudo-elements
- Color coding: blue for Stata, yellow for Python, orange for Matlab, green for LaTeX

---

### 2.5 The Gap Section

**Layout:** Deep navy background (`#1a1a2e`), white text, max-width 960px.

**Section Title:** "为什么 Trae 是这件事的正确归宿"

**Opening:**
> "当前的工具栈是权宜之计。Trae 的 Agent 架构是解决方案。以下是三个具体缝隙，Trae 能关闭 — 而且其他 IDE 没这个条件。"

**Three Gap Cards (vertical stack, each with a left accent bar in cyan):**

**Gap 1: Agent Mode vs. Chat Mode**
- **Accent:** Cyan left border
- **Headline:** "从问答到委托执行"
- **Body:** "VS Code Copilot Chat 回答问题。Trae Builder 规划、执行、验证。对一个研究项目，这意味着：'跑 Stata DID → 生成事件研究图 → 写 LaTeX 结果节 → 编译 PDF → 检查表数字是否匹配 Stata 输出。' 全部在一个 Agent 会话里。研究者审阅，而不是复制粘贴。"

**Gap 2: Chinese-First, Research-Vertical**
- **Accent:** Cyan left border
- **Headline:** "为最需要它的受众构建"
- **Body:** "中国经济学研究生主要使用中文界面，面对中国特定的约束（海外模型访问、机构 Stata 许可），需要本地模型集成（DeepSeek、Doubao）。Trae 的原生中文支持 + 本地 AI 骨干消除了让 VS Code + Copilot 在这个受众中不可靠的语言和 API 障碍。"

**Gap 3: Multi-Tool Orchestration**
- **Accent:** Cyan left border
- **Headline:** "IDE 作为科研编排器"
- **Body:** "我工作流中的每个工具（Stata、Python、Matlab、LaTeX、Git）都可通过 CLI 或 MCP 获得。Trae 的 Agent 能原生编排这些 CLI 工具 — 规划一步，在 Stata 执行，读取结果，传给 Python 可视化，然后写进 LaTeX。这不是 '更好的代码补全'。这是一个根本不同的范式：跨工具的委托执行。实证研究正是 Agent 模式为之设计的——多工具、多文件、重度验证——工作流。"

**Closing line (bold, cyan):**
> **"Trae 不是 '带更好聊天的 VS Code'。它是一种新架构，为一个新类别的工具链。"**

---

### 2.6 The Proposal Section

**Layout:** White background, max-width 1200px, feature card grid.

**Section Title:** "提案：面向 Trae 的 One-Stop Econ Research 插件"

**Subtitle:** "一个将整个实证研究工作流打包成一键、Agent 原生环境的插件。"

**Feature Cards (3-column grid, responsive):**

| Feature | Headline | Body |
|---------|----------|------|
| **Project Template** | `新建 → 社会科学研究项目` | 脚手架 `data/`、`scripts/`、`notebooks/`、`paper/`、`output/`、`.gitignore` 和 `audit-log.md`。研究者不再手动组织；每个项目从第一天起就可复现。 |
| **Stata/Matlab Integration** | 原生内核，Agent 就绪 | 内置终端中的 Stata 和 Matlab 内核，带 MCP 桥接供 Agent 模式。Agent 执行 Stata DID，读取结果，写 Python 可视化或 LaTeX 表格 — 跨语言工作流。 |
| **LaTeX Paper Pipeline** | 从估计到投稿 | `paper/main.tex` 模板，带 AER/《经济研究》格式。Agent 从脚本输出生成表格和图形。学生从估计走到提交就绪论文，不离开 IDE。 |
| **Reproducibility Check** | 一键验证 | "验证可复现性" 按顺序运行所有脚本，检查输出哈希，标记漂移。防止 '我昨天跑过，结果不一样' 的问题。 |
| **AI Audit Log** | 通过透明建立信任 | 自动生成的 `audit-log.md`，跟踪每个 Agent 动作：请求了什么、改了哪些文件、验证了什么。满足导师和审稿人对 AI 参与的疑问。 |

**User Flow Diagram (CSS-generated):**
1. 研究者打开 Trae → 选择 "新建实证项目"
2. Agent 脚手架项目 + 询问数据源
3. 研究者上传数据 → Agent 建议识别策略（基于数据结构的 DID/IV/RD）
4. Agent 运行估计（Stata/Python） → 生成图形/表格 → 写 LaTeX
5. 研究者审阅 → Agent 编译 PDF → Git 提交描述性消息
6. 投稿前一键 "复现"

**MVP Scope Note:**
> "试点阶段，插件从项目模板 + Python/Jupyter 集成开始。Stata/Matlab 内核是扩展目标，需要许可合作，但 Trae 的 Agent 架构已准备好接纳它们。"

---

### 2.7 Why Trae + CTA Section

**Layout:** Deep navy background, max-width 720px, centered.

**Section Title:** "为什么 Trae 应该构建这个"

**Three strategic arguments (bullet list, clean):**
1. **分发与基础设施：** 字节跳动有规模（抖音/TikTok）和 AI 骨干（Doubao/DeepSeek 集成），能把这个变成大众市场学术工具。没有西方 IDE 在中国有这种组合。
2. **架构契合：** Trae 的 Agent 优先设计在 Copilot 面前领先一步，适合多步骤、多工具工作流。实证研究是展示这一优势的理想用例。
3. **蓝海：** 中国学术界服务不足。没有 IDE 为中国社会科学研究工作流优化。先发优势唾手可得。

**CTA Cards (2-column, white cards on navy background):**

| CTA | Headline | Body | Action |
|-----|----------|------|--------|
| **Deep Dive** | "一起设计规格" | 与 Trae 工程师 30 分钟技术会议，回顾插件架构、MCP 集成和 Agent 工作流设计。 | "邮件联系" |
| **Pilot** | "在我的下一门课试点" | 我在 [即将到来学期] 有 50+ 学生。提议在真实学术环境中插件 beta 测试。 | "提议试点时间线" |
| **Open Source** | "开源模板" | 把我的 `demo-project/` 作为 Trae 兼容模板发布，驱动有机采纳。 | "查看模板" |

**CTA Action:** All CTAs link to email: `chenzhiyuan@rmbs.ruc.edu.cn` (mailto link)

**Footer line:**
> "这不是功能请求。这是一份合作提案 — 一个理解工作流的研究者，和一个能构建平台的团队。"

---

## 3. Visual Specifications

### 3.1 Color System

```css
:root {
  --bg-primary: #ffffff;
  --bg-secondary: #f8f9fa;
  --bg-dark: #1a1a2e;
  --text-primary: #1a1a2e;
  --text-secondary: #5a5a7a;
  --text-on-dark: #ffffff;
  --accent: #00A8CC;
  --accent-hover: #0088a8;
  --accent-muted: rgba(0, 168, 204, 0.1);
  --border: #e5e7eb;
  --shadow: 0 4px 24px rgba(0, 0, 0, 0.06);
}
```

### 3.2 Typography

| Element | Font | Size | Weight | Line Height | Color |
|---------|------|------|--------|-------------|-------|
| H1 (Hero) | Inter / system-ui | `clamp(2.5rem, 5vw, 4rem)` | 800 | 1.1 | white (on dark) |
| H2 (Section) | Inter / system-ui | `clamp(1.75rem, 3vw, 2.5rem)` | 700 | 1.2 | text-primary |
| H3 (Card) | Inter / system-ui | `1.25rem` | 600 | 1.3 | text-primary |
| Body | Inter / system-ui | `1.125rem` | 400 | 1.6 | text-primary |
| Caption | Inter / system-ui | `0.875rem` | 400 | 1.5 | text-secondary |
| Code | JetBrains Mono / SF Mono | `0.875rem` | 400 | 1.6 | accent (inline) or text-primary (blocks) |
| Chinese | Noto Sans SC | (fallback) | (matching weight) | 1.6 | (matching) |

### 3.3 Spacing & Layout

| Token | Value |
|-------|-------|
| Section padding | `clamp(4rem, 5vw, 8rem)` top/bottom |
| Content max-width | `720px` for text, `1200px` for cards/galleries |
| Card gap | `1.5rem` |
| Card padding | `2rem` |
| Card border-radius | `12px` |
| Card shadow | `0 4px 24px rgba(0,0,0,0.06)` |
| Button border-radius | `8px` |
| Button padding | `0.75rem 1.5rem` |

### 3.4 Responsive Breakpoints

| Breakpoint | Behavior |
|------------|----------|
| `>= 1024px` | 3-column feature grids, 2-column pain cards, side-by-side demo |
| `>= 768px` | 2-column grids, stacked demo |
| `< 768px` | Single column, stacked everything, reduced section padding |

---

## 4. Asset Inventory

### 4.1 Lecture Photos (from zhiyuanryanchen.github.io/gallary/)

| ID | University | Filename | Status |
|----|------------|----------|--------|
| `ruc-20260604` | 中国人民大学 | `20260604_One-StopVScode.jpeg` | Completed |
| `cufe-20260609` | 中央财经大学 | `20260609-onestopresearch-cufe1.jpg` | Completed |
| `nju-20260615` | 南京大学 | `20260615_onestopresearch_nju.jpeg` | Completed |
| `uibe-20260617` | 对外经济贸易大学 | `20260617-onestopresearch-uibe.png` | Completed |
| `cueb-sof-20260624` | 首都经济贸易大学 | `20260624CUEB_SOF.png` | Completed |
| `cueb-isem-20260624` | 首都经济贸易大学 ISEM | `20260624CUEB-ISEM.png` | Completed |

### 4.2 CSS-Generated Diagrams (No Screenshots Needed)

| Diagram | Description | Implementation |
|---------|-------------|--------------|
| **Project Tree** | File structure: `data/`, `scripts/`, `notebooks/`, `paper/`, `output/` | CSS flex tree with folder icons and file labels |
| **Tool Flow** | Stata → MCP → AI → LaTeX | CSS boxes with arrow connectors |
| **Document Preview** | PDF with highlighted table and figure | CSS mock document with colored regions |
| **User Flow** | 6-step vertical timeline | CSS timeline with numbered steps and connectors |
| **Pain Cards** | Three cards with icons | CSS icons (font icons or SVG data URIs) |
| **Feature Cards** | Five cards with icons | CSS icons + text descriptions |

**CSS Icon Strategy:** Use inline SVG or simple CSS shapes (circles, squares, borders) for all icons. No external icon library dependency. Example: chain link icon = two overlapping rectangles with rounded corners; broken chain = same with a gap in the middle.

### 4.3 Fallback for Missing Images

All visual elements are CSS-generated. No image dependencies. Lecture photos are loaded from external URLs (`zhiyuanryanchen.github.io/gallary/`) with `loading="lazy"` and `alt` text. If photos fail to load, the card layout remains intact with text-only fallback.

---

## 5. Technical Implementation

### 5.1 Stack: Single-File HTML

**Output:** One self-contained `.html` file (no build step, no external dependencies except CDN).

**Why single-file:**
- Easy to email (attach and open locally)
- Easy to host (GitHub Pages, Netlify Drop, or any static server)
- Zero maintenance (no build pipeline, no dependency updates)
- Reliable in China (no blocked CDNs; can be self-hosted)

**CDN Dependencies (optional but recommended):**
- Tailwind CSS: `https://cdn.tailwindcss.com` (with custom config for colors)
- Google Fonts (Inter, Noto Sans SC): `https://fonts.googleapis.com` (with fallback if blocked)
- Smooth-scroll: `https://cdn.jsdelivr.net/npm/smooth-scroll@16.1.3` (optional, 2KB)

**Fallback if CDNs blocked:** Inline all CSS and fonts. File size increases to ~50KB (still tiny).

### 5.2 HTML Structure

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>为实证研究者打造真正需要的 IDE — 给 Trae 的合作提案</title>
  <!-- Inline CSS or Tailwind CDN -->
  <!-- Fonts: Inter + Noto Sans SC -->
</head>
<body>
  <nav class="sticky-nav">...</nav>
  
  <section id="hero" class="bg-dark">...</section>
  <section id="lectures" class="bg-white">...</section>
  <section id="problem" class="bg-secondary">...</section>
  <section id="demo" class="bg-white">...</section>
  <section id="gap" class="bg-dark">...</section>
  <section id="proposal" class="bg-white">...</section>
  <section id="cta" class="bg-dark">...</section>
  
  <footer>...</footer>
  
  <!-- Optional: smooth-scroll JS -->
</body>
</html>
```

### 5.3 Interactions

| Interaction | Behavior | Tech |
|-------------|----------|------|
| Smooth scroll | Click nav link → smooth scroll to section | `smooth-scroll` library or `scroll-behavior: smooth` CSS |
| Sticky nav | Nav fixed at top after scrolling past hero | `position: fixed` with `backdrop-filter: blur()` |
| Card hover | Subtle lift (`transform: translateY(-2px)`, shadow increase) | CSS `transition` |
| Button hover | Background darken, slight scale | CSS `transition` |
| Mobile nav | Hamburger menu → overlay | Optional JS (if nav has many items) |

**No JavaScript required for core reading experience.** JS only enhances navigation and aesthetics.

### 5.4 Hosting Recommendations

| Option | Steps | URL |
|--------|-------|-----|
| **GitHub Pages** | Push to `zhiyuanryanchen.github.io` repo, enable Pages | `https://zhiyuanryanchen.github.io/trae-proposal` |
| **Netlify Drop** | Drag and drop HTML file to Netlify | `https://[random].netlify.app` (customizable) |
| **Local File** | Email the `.html` file directly | `file://...` (opens in browser) |

**Recommendation:** GitHub Pages — consistent with your existing course site, free, version-controlled, and professional.

---

## 6. Success Criteria

### 6.1 Content Criteria

- [ ] Trae 在每个 Hero 之后的 section 中都被提及（不只是结尾）
- [ ] 问题被框定为 Trae 独特关闭的缝隙（不是泛泛的 "IDE 都很烂" 抱怨）
- [ ] 讲座可信度具体（学校、听众规模、引用语录）
- [ ] 插件提案有 5 个具体功能卡片，每个有清晰用户价值
- [ ] 用户流用 6 步描述，从项目创建到投稿
- [ ] MVP 范围明确限制（不过度承诺）
- [ ] CTA 包含 3 个具体下一步（不只是 "联系我"）
- [ ] 所有 CTA 链接到邮件: `chenzhiyuan@rmbs.ruc.edu.cn`
- [ ] 语言以中文为主，英文术语保留（如 Agent, MCP, IDE）

### 6.2 Visual Criteria

- [ ] 单文件，无需服务器即可在 Chrome/Safari/Firefox 中正确打开
- [ ] 移动端响应式：在 iPhone 13 Pro (390px 宽) 上可读，无横向滚动
- [ ] 深色/浅色 section 交替，创造视觉节奏
- [ ] 青色强调色 (`#00A8CC`) 一致用于链接、CTA 和高亮
- [ ] 字体层次清晰：H1 > H2 > H3 > body > caption
- [ ] Section 内边距充裕（从不感到拥挤）
- [ ] 图片有 `alt` 文本，加载失败时有优雅降级
- [ ] 所有图表用 CSS 生成，无外部图片依赖

### 6.3 Performance Criteria

- [ ] First Contentful Paint < 1.5s (单文件，最少外部请求)
- [ ] 总文件大小 < 200KB (内联 CSS) 或 < 100KB (CDN)
- [ ] 无阻塞渲染的资源 (CSS 内联或异步)
- [ ] 首次加载后离线可用 (无动态内容)

### 6.4 Accessibility Criteria

- [ ] 语义化 HTML (`<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- [ ] 所有图片有描述性 `alt` 属性
- [ ] 颜色对比度符合 WCAG AA (青色在深色海军上：需用对比度工具检查)
- [ ] 键盘可导航 (平滑滚动链接可用键盘操作)
- [ ] 减少动画支持：`@media (prefers-reduced-motion: reduce)` 禁用平滑滚动和悬停过渡

---

## 7. Implementation Notes

### 7.1 From This Spec to HTML

The implementation is straightforward: one HTML file with inline CSS (or Tailwind CDN). No JavaScript framework needed. Estimated implementation time: 2–3 hours.

### 7.2 Content Sources

- **Lecture data:** From `zhiyuanryanchen.github.io/index.html` (Recent Updates section)
- **Workflow descriptions:** From `slides.qmd` and `handout.qmd`
- **Stata/Matlab specifics:** From `stata-code-conventions.md` and `.claude/skills/`
- **Teaching insights:** From `teaching-memory.md`

### 7.3 Open Questions (Resolved)

1. **Screenshots:** 不需要 — 使用 CSS 生成图表 ✅
2. **CTA links:** 所有 CTA 链接到邮件 `chenzhiyuan@rmbs.ruc.edu.cn` ✅
3. **Language:** 中文为主 ✅
4. **Lecture dates:** 已完成讲座不显示具体日期，只显示状态；即将举办显示 "即将举办" 徽章 ✅
5. **Plugin name:** "One-Stop Econ Research" ✅

---

## 8. Self-Review Checklist

| Check | Status | Notes |
|-------|--------|-------|
| Trae-specific focus maintained? | ✅ | Problem, Gap, Proposal all center on Trae |
| Concrete plugin concept with 5 feature cards? | ✅ | Project Template, Stata/Matlab Integration, LaTeX Pipeline, Reproducibility Check, AI Audit Log |
| Lecture credibility as opening proof? | ✅ | 11 cards (6 completed with photos, 5 upcoming with placeholders) |
| Self-contained HTML, no build dependencies? | ✅ | Single file, CDN optional |
| 15–20 min read time? | ✅ | ~18 min across 7 sections |
| Matches narrative arc (credibility → problem → Trae solution)? | ✅ | Arc is explicit in Section 1 |
| VS Code framed as current reality, not competing alternative? | ✅ | "VS Code 是优秀但非为科研构建的通用环境" |
| No mention of other AI IDEs (Cursor, etc.)? | ✅ | Trae is the only alternative discussed |
| Success criteria are measurable? | ✅ | Content, visual, performance, accessibility criteria defined |
| All open questions resolved? | ✅ | Screenshots, CTA, language, dates, plugin name all confirmed |

---

**End of Design Spec.**

Next step: Invoke `writing-plans` skill to create the implementation plan for building the HTML page.
