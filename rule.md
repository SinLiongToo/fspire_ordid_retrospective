# 🧭 Project Rules & Coding Guidelines (ORID Mindset & Decision Compass)

This document establishes the architecture rules, coding standards, and deployment guidelines for the **ORID Mindset & Decision Compass** project.

---

## 🏛️ 1. Architecture & File Parity Rules

1. **Zero-Build Single-Page Application (SPA)**:
   - The application is a self-contained, client-side web application using pure Vanilla JavaScript, CSS3, and HTML5.
   - **No external heavy frameworks** (React/Vue/Angular) or Node build steps (Webpack/Vite) should be added unless explicitly requested.
   - Keep all dependencies zero-install and portable.

2. **Strict File Parity (`index.html` ↔ `orid_life_compass.html`)**:
   - `index.html` serves as the primary root document for **GitHub Pages**.
   - `orid_life_compass.html` serves as the local development reference.
   - **Rule**: Whenever any change is made to styling, markup, or script logic, **both files must be kept 100% identical and synchronized**.

3. **DOM Integrity & Anti-Duplicate Rule**:
   - Never insert duplicate modal elements or duplicate ID attributes (`#mindfulModal`, `#mindfulPanelStop`, `#breatheCycleCount`, etc.).
   - Modals and fixed overlays must be placed as direct children of `<body>` right before `<script>` to guarantee correct stacking context, z-index, and event bubbling.

---

## 🌐 2. Internationalization (i18n) Rules

1. **Complete Bilingual Parity (繁體中文 / English)**:
   - Every single user-facing label, prompt, placeholder, explanation, and error alert must exist in both `I18N.zh` and `I18N.en`.
   - When adding new domains, models, or synthesis panels, always provide full Chinese and English translations in the corresponding dictionaries.

2. **Language Persistence**:
   - Language preferences (`zh` / `en`) must be persisted in `localStorage` under `state.lang` and automatically restored on page reload.

---

## 🧘 3. Framework & Mental Model Guidelines

1. **0. Mindful Grounding (Pre-reflection)**:
   - Provide intentional space before deep reflection to calm the nervous system (Box Breathing 4-4-4-4 & STOP practice: Stop, Take a breath, Observe, Proceed).

2. **1. Life Balance (F-SPIRE Framework)**:
   - 6 Core Dimensions: Financial (財務), Spiritual (靈性), Physical (身體), Intellectual (智識), Relational (關係), Emotional (情緒).
   - Integrate cross-model cues: 4M (Money, Muscle, Mindset, Mood), 4F of Life (Fuel, Find, Focus, Forgive), and 6P of Life (Prove, Prayer, Push, Promise, Proud, Pick up).

3. **2. Decision Mindset (6 Themed Templates)**:
   - Problem Solving (問題解決), Retrospective (專案復盤), Career Decision (職涯決策), Book & Learning (讀書學習), Stoic Reflection (斯多葛反思), Weekly Reflection (每週回顧).

4. **3. ORID Focused Conversation Method**:
   - Objective (O) ➔ Reflective (R) ➔ Interpretive (I) ➔ Decisional (D).

5. **4. Synthesis & Execution Frameworks**:
   - **Pyramid Principle & MECE**: Conclusion First (Key Message), MECE Supporting Arguments (Mutually Exclusive, Collectively Exhaustive), and Evidence Facts.
   - **PDCA Cycle**: Plan ➔ Do ➔ Check ➔ Act.
   - **SMART Criteria**: Specific, Measurable, Achievable, Relevant, Time-bound.
   - **Decision Quality (DQ) Score**: Clarity, Evidence, Insight, Actionability (1-5 scale).

---

## 🚀 4. Deployment & Git Workflow

1. **Commit & Push Standard**:
   - Every feature update or bug fix must be staged (`git add .`), committed with conventional commit messages (`feat: ...`, `fix: ...`, `docs: ...`), and pushed directly to `origin master`.
2. **GitHub Pages URL**:
   - Live Demo: `https://sinliongtoo.github.io/fspire_ordid_retrospective/`
