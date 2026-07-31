# Implementation Plan: One-Stop Econ Research for Trae — Product Brief HTML

**Based on approved design spec:** `docs/superpowers/specs/2026-06-25-trae-partnership-brief-design.md`
**Date:** 2026-06-25
**Output:** Single-file HTML page, hosted on GitHub Pages

---

## 1. Goal & Deliverables

Build a single-file, self-contained HTML product brief (editorial style, ~15-20 min read) that:
- Establishes credibility through 11 university lecture cards (6 completed with photos, 5 upcoming)
- Defines the fragmented empirical research toolchain gap
- Proposes a concrete "One-Stop Econ Research" plugin concept for Trae
- Is fully responsive, accessible, and works offline after first load

**Deliverable:** `trae-proposal.html` (or hosted at `zhiyuanryanchen.github.io/trae-proposal`)

---

## 2. Architecture

### Single-File HTML Structure
```
trae-proposal.html
├── <head>
│   ├── Meta tags (charset, viewport, title, description)
│   ├── Inline CSS (all styles self-contained, ~15-20KB)
│   ├── Google Fonts preconnect (Inter + Noto Sans SC) with local fallback
│   └── Optional: Tailwind CDN config (if using utility classes)
├── <body>
│   ├── <nav> — Sticky navigation with smooth-scroll anchor links
│   ├── <main>
│   │   ├── Section 1: Hero — Full-width dark navy, thesis statement, CTA buttons
│   │   ├── Section 2: Lecture Footprint — 11-card responsive grid
│   │   ├── Section 3: The Problem — 3 pain cards with CSS icons
│   │   ├── Section 4: The Demo — CSS-generated workflow diagrams
│   │   ├── Section 5: The Gap — 3 strategic gap cards on dark background
│   │   ├── Section 6: The Proposal — 5 feature cards + user flow timeline
│   │   └── Section 7: Why Trae + CTA — Strategic arguments + 3 action cards
│   └── <footer> — Minimal credits + contact
└── <script> — Optional: smooth-scroll polyfill (vanilla JS, ~1KB)
```

### CSS Strategy
- **Approach A (Recommended):** Pure CSS with custom properties (variables). No external dependency. File size ~20KB.
- **Approach B (Alternative):** Tailwind CSS via CDN with custom config. Faster to write but adds external dependency. File size ~15KB + CDN.

**Decision:** Use **Approach A** (pure CSS) for maximum reliability and offline capability. All styles in a single `<style>` block.

---

## 3. Implementation Steps

### Phase 1: Foundation (30 min)
**Step 1.1 — HTML Skeleton**
- Create `trae-proposal.html` with basic structure
- Add meta tags, viewport, title, description
- Set up CSS custom properties (color system, spacing, typography)
- Define font stack: `Inter, "Noto Sans SC", "PingFang SC", "Microsoft YaHei", sans-serif`
- Add `@font-face` or `font-display: swap` for web fonts

**Step 1.2 — Base Styles**
- Reset + normalize (minimal, ~50 lines)
- Typography scale (H1-H3, body, caption, code)
- Spacing system (section padding, card gaps, content max-widths)
- Responsive breakpoints (mobile < 768px, tablet 768-1024px, desktop > 1024px)
- Dark/light section alternation (hero/gap/CTA = dark; lectures/problem/demo/proposal = light/white)

**Verification:** Open in browser, confirm base styles render correctly at 320px, 768px, 1440px widths.

### Phase 2: Navigation & Hero (30 min)
**Step 2.1 — Sticky Navigation**
- Fixed top bar, transparent → solid on scroll (backdrop-filter: blur)
- Anchor links: 讲座足迹, 问题, 演示, 差距, 提案, 合作
- Mobile: hamburger menu (optional for MVP, can skip if nav items fit)
- Smooth scroll behavior (CSS `scroll-behavior: smooth` or 2KB JS polyfill)

**Step 2.2 — Hero Section**
- Full viewport height (or generous padding), dark navy background (`#1a1a2e`)
- Top tag: "科研工作流 × AI-Native IDE" (small, all-caps, cyan, letter-spacing)
- Headline: "为实证研究者打造真正需要的 IDE" (large, bold, white)
- Subheadline: "从碎片化工具到统一 Agent 驱动科研 — 一份给 Trae 的合作提案"
- Author line: "陈志远 · 中国人民大学商学院"
- CTA buttons: "阅读提案" (primary cyan) + "查看讲座足迹" (text link)
- Background: subtle abstract network pattern (CSS-generated, very low opacity)

**Verification:** Confirm hero renders correctly at all breakpoints. CTA buttons scroll to correct sections.

### Phase 3: Lecture Footprint (45 min)
**Step 3.1 — Card Grid Layout**
- CSS Grid: 3 columns on desktop, 2 on tablet, 1 on mobile
- Gap: `1.5rem`, max-width: `1200px`, centered
- Section title: "我在哪里讲过 — 学生们在问什么"
- Subtitle: "AI-Native IDE 科研方法论受邀讲座系列，覆盖 9 所中国高校。"

**Step 3.2 — 11 Lecture Cards**
For each card (completed lectures):
- Photo thumbnail: `<img>` loading from `zhiyuanryanchen.github.io/gallary/[filename]` with `loading="lazy"`
- Fallback: if image fails, card shows text-only with institution name prominent
- Institution name (bold), audience badge, key takeaway (italic, quoted)
- For upcoming lectures: placeholder gradient background (`#00A8CC` to `#0088a8`), "即将举办" badge

**Card content mapping:**
| # | Institution | Photo | Status | Key Takeaway |
|---|-------------|-------|--------|--------------|
| 1 | 中国人民大学 | `20260604_One-StopVScode.jpeg` | 已完成 | AI平权框架... |
| 2 | 中央财经大学 | `20260609-onestopresearch-cufe1.jpg` | 已完成 | AI是放大器... |
| 3 | 南京大学 | `20260615_onestopresearch_nju.jpeg` | 已完成 | 碎片化工具链... |
| 4 | 对外经济贸易大学 | `20260617-onestopresearch-uibe.png` | 已完成 | 每个工具都是开源的... |
| 5 | 首都经济贸易大学 | `20260624CUEB_SOF.png` | 已完成 | Stata+Python+LaTeX... |
| 6 | 首都经济贸易大学 ISEM | `20260624CUEB-ISEM.png` | 已完成 | Agent模式... |
| 7-11 | 北师大/江西财经/西安交大/湘潭大学/重庆大学 | (placeholder) | 即将举办 | — |

**Step 3.3 — Summary Line**
- Bottom text: "6 场已完成讲座，5 场已确认排期。反馈高度一致：研究者需要这个，但没有 IDE 为他们的工作流而构建。"

**Verification:** Confirm all 11 cards render correctly. Images load lazily. Mobile layout stacks to 1 column. Placeholder cards render with gradient.

### Phase 4: The Problem (45 min)
**Step 4.1 — Section Layout**
- Light gray background (`#f8f9fa`), max-width 960px, centered
- Section title: "问题：科研不是普通的编程"
- Opening paragraph (as per spec)

**Step 4.2 — 3 Pain Cards**
Each card:
- CSS-generated icon (no images, no icon libraries)
- Headline, body text, VS Code reality note
- Card layout: white background, rounded corners, shadow, padding
- Icons:
  - Card 1 (Fragmented): Chain link icon = two overlapping rounded rectangles, one broken
  - Card 2 (Blindness): Eye with slash = circle + diagonal line
  - Card 3 (No Workflow): Single person vs team = two stick figures or overlapping circles

**Step 4.3 — Closing Line**
- Bold centered text: "VS Code 把科研当成普通编程。实证科研不是普通编程。"

**Verification:** Confirm CSS icons render correctly across browsers. Card grid responsive (2 columns desktop, 1 column mobile).

### Phase 5: The Demo (45 min)
**Step 5.1 — Section Layout**
- White background, max-width 1200px
- Alternating text + diagram layout (text left, diagram right; reverse for next)
- Section title: "今天能跑通的方案 — 以及为什么还不够"

**Step 5.2 — 3 Demo Steps with CSS Diagrams**

**Step 1: Unified Project**
- Text: Description of folder structure
- Diagram: CSS file tree
  - Root folder icon + "demo-project/"
  - Subfolders: `data/`, `scripts/`, `notebooks/`, `paper/`, `output/`
  - Each folder has color-coded label (blue=Stata, yellow=Python, orange=Matlab, green=LaTeX)
  - Use CSS flexbox with indentation (margin-left) for tree structure

**Step 2: AI Cross-Tool Execution**
- Text: Description of MCP workflow
- Diagram: CSS flow diagram
  - 4 boxes: Stata → MCP → AI → LaTeX
  - Arrow connectors between boxes (CSS borders or pseudo-elements with triangles)
  - Color coding: blue → gray → purple → green

**Step 3: Final Output**
- Text: Description of submission-ready PDF
- Diagram: CSS mock document
  - Rectangle with "PDF" label, internal highlighted regions (table area, figure area)
  - Use dashed borders or background colors to indicate active areas

**Step 5.3 — Transition Bridge**
- Text: "这是概念验证。但胶带已经露出来了。如果这个工作流是 IDE 原生的 — 而不是拼凑的扩展集合 — 会怎样？"

**Verification:** Confirm all diagrams render correctly. Alternating layout works on desktop (side-by-side) and stacks on mobile. No horizontal scroll.

### Phase 6: The Gap (30 min)
**Step 6.1 — Section Layout**
- Dark navy background (`#1a1a2e`), white text, max-width 960px
- Section title: "为什么 Trae 是这件事的正确归宿"

**Step 6.2 — 3 Gap Cards**
- Vertical stack, each with left cyan accent bar (`border-left: 4px solid #00A8CC`)
- Card backgrounds: slightly lighter than section background (`#22223e`)
- Headlines: "从问答到委托执行", "为最需要它的受众构建", "IDE 作为科研编排器"
- Body text: as per spec

**Step 6.3 — Closing Line**
- Bold cyan text: "Trae 不是 '带更好聊天的 VS Code'。它是一种新架构，为一个新类别的工具链。"

**Verification:** Confirm contrast ratios meet WCAG AA (cyan `#00A8CC` on dark `#1a1a2e`: ~4.5:1). Text readable.

### Phase 7: The Proposal (60 min)
**Step 7.1 — Section Layout**
- White background, max-width 1200px
- Section title: "提案：面向 Trae 的 One-Stop Econ Research 插件"
- Subtitle: "一个将整个实证研究工作流打包成一键、Agent 原生环境的插件。"

**Step 7.2 — 5 Feature Cards**
- 3-column grid (responsive)
- Each card: icon (CSS-generated), headline, body text
- Feature icons:
  - Project Template: Folder with plus sign
  - Stata/Matlab: Terminal window with code brackets
  - LaTeX: Document with "TeX" label
  - Reproducibility: Checkmark circle or refresh loop
  - Audit Log: Document with lines and checkmarks

**Step 7.3 — User Flow Timeline**
- CSS-generated vertical timeline
- 6 numbered steps, connected by line
- Each step: number circle + title + brief description
- Steps:
  1. 打开 Trae → 选择 "新建实证项目"
  2. Agent 脚手架项目 + 询问数据源
  3. 上传数据 → Agent 建议识别策略
  4. Agent 运行估计 → 生成图形/表格 → 写 LaTeX
  5. 审阅 → 编译 PDF → Git 提交
  6. 投稿前一键 "复现"

**Step 7.4 — MVP Note**
- Boxed text area with light gray background
- Text: "试点阶段，插件从项目模板 + Python/Jupyter 集成开始..."

**Verification:** Confirm feature cards responsive. Timeline renders correctly on mobile (steps stack vertically).

### Phase 8: CTA & Footer (30 min)
**Step 8.1 — Why Trae Section**
- Dark navy background, max-width 720px, centered
- 3 strategic arguments (bullet list)
- Clean, generous spacing

**Step 8.2 — 3 CTA Cards**
- 2-column grid (or 3-column on wide desktop)
- White cards on dark background
- Each card: headline, body, action button
- Buttons link to `mailto:chenzhiyuan@rmbs.ruc.edu.cn`
  - CTA 1: "一起设计规格" → mailto with subject "Trae 插件合作讨论"
  - CTA 2: "在我的下一门课试点" → mailto with subject "课程试点合作"
  - CTA 3: "开源模板" → mailto with subject "开源模板合作"

**Step 8.3 — Footer**
- Minimal: "这不是功能请求。这是一份合作提案..."
- Contact: 邮箱链接
- Copyright: © 2026 陈志远

**Verification:** Confirm mailto links work. CTA cards responsive. Footer text readable on dark background.

### Phase 9: Polish & Accessibility (30 min)
**Step 9.1 — Smooth Scroll**
- Add `scroll-behavior: smooth` to CSS
- Add JS polyfill for older browsers (optional, ~1KB inline)
- Verify nav links scroll to correct sections with offset for sticky nav height

**Step 9.2 — Accessibility**
- Add `aria-label` to nav, sections, and interactive elements
- Verify all images have `alt` text (including placeholder fallbacks)
- Add `prefers-reduced-motion` media query to disable smooth scroll and transitions
- Verify color contrast ratios (WCAG AA minimum)
- Add focus styles for keyboard navigation (visible outlines on links/buttons)

**Step 9.3 — Performance**
- Minimize CSS (remove unused rules, consolidate)
- Verify file size < 200KB (target: ~50-80KB with inlined CSS)
- Add `loading="lazy"` to all images
- Preconnect to Google Fonts CDN (if used)

**Step 9.4 — Final Review**
- Read through all copy for typos and consistency
- Verify all Chinese quotes use proper directional quotes (`"` `"` `' `'`)
- Verify English terms are consistent (Agent, MCP, IDE, Trae, VS Code, Copilot)
- Check that no placeholder text remains (e.g., "[upcoming semester]")

---

## 4. Verification Steps (Before Delivery)

### 4.1 Visual Verification
- [ ] Open in Chrome, Safari, Firefox at 320px, 768px, 1024px, 1440px
- [ ] Confirm no horizontal scroll at any width
- [ ] Confirm text never touches viewport edges (min padding 1rem)
- [ ] Confirm dark sections have sufficient contrast (WCAG AA)
- [ ] Confirm images load and have fallback if failed
- [ ] Confirm CTA buttons are prominent and clickable

### 4.2 Functional Verification
- [ ] All nav links smooth-scroll to correct sections
- [ ] Sticky nav appears after scrolling past hero
- [ ] Mobile layout stacks correctly (no overflow, readable font sizes)
- [ ] Mailto links open email client with pre-filled subject
- [ ] Page works offline after first load (no dynamic resources needed)

### 4.3 Content Verification
- [ ] All 11 lecture cards present with correct content
- [ ] All 3 pain cards present with CSS icons
- [ ] All 3 demo diagrams present with CSS styling
- [ ] All 3 gap cards present with cyan accent bars
- [ ] All 5 feature cards present with icons
- [ ] User flow timeline has 6 steps with connectors
- [ ] 3 CTA cards present with mailto links
- [ ] No typos or placeholder text

### 4.4 Performance Verification
- [ ] File size < 200KB (check with `ls -la` or browser dev tools)
- [ ] First Contentful Paint < 1.5s (Lighthouse or manual check)
- [ ] No render-blocking external resources (CSS is inline)
- [ ] All images have explicit dimensions (width/height attributes) to prevent layout shift

---

## 5. Deployment / Usage Plan

**重要：这是一次线下会议材料，不需要部署到网站或分发链接。**

### 使用方式
- 将 `trae-proposal.html` 作为单个文件通过邮件发送或拷贝到展示设备上
- 在会议现场用浏览器直接打开（双击文件即可，无需服务器）
- 所有资源完全自包含，无需网络连接
- 建议提前在展示设备上测试打开效果

### 备选方案
- 可转换为 PDF 打印版（浏览器 → 打印 → 保存为 PDF）
- 可放入 U 盘或网盘，现场拷贝到对方设备上查看

---

## 6. Estimated Timeline

| Phase | Steps | Estimated Time |
|-------|-------|--------------|
| Phase 1 | Foundation | 30 min |
| Phase 2 | Nav + Hero | 30 min |
| Phase 3 | Lecture Footprint | 45 min |
| Phase 4 | The Problem | 45 min |
| Phase 5 | The Demo | 45 min |
| Phase 6 | The Gap | 30 min |
| Phase 7 | The Proposal | 60 min |
| Phase 8 | CTA + Footer | 30 min |
| Phase 9 | Polish + Accessibility | 30 min |
| **Verification** | All checks | 30 min |
| **Total** | | **~6 hours** |

---

## 7. Risk Mitigation

| Risk | Mitigation |
|------|------------|
| Lecture photos fail to load | Cards have text-only fallback; images use `loading="lazy"` and `onerror` handler |
| Google Fonts blocked in China | Use `font-display: swap` and system font fallback stack |
| File size too large | Pure CSS approach keeps size ~50-80KB; minify if needed |
| CSS icons don't render consistently | Test in Chrome, Safari, Firefox; use simple shapes (rectangles, circles, borders) |
| Mailto links don't work for some users | Include plain email text as backup |
| Mobile layout breaks | Test at 320px; use `min-width` and `overflow-wrap` |

---

## 8. Success Criteria (Reiterated from Design Spec)

- [ ] Single file, opens in browser without server
- [ ] Mobile responsive (320px to 1440px+)
- [ ] All CSS-generated diagrams render correctly
- [ ] All 11 lecture cards present (6 with photos, 5 with placeholders)
- [ ] All mailto CTAs functional
- [ ] WCAG AA color contrast met
- [ ] File size < 200KB
- [ ] Works offline after first load
- [ ] No external dependencies required (optional CDN enhancements)

---

**Ready to proceed with implementation.**
