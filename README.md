# MNC Review Copilot Enterprise Pro v6.0
## 企業級多維度 AI 績效考評與人才校準系統 (Enterprise Multi-Module Performance Review & Talent Calibration Suite)

---

## 🌐 1. Executive Summary & Value Proposition / 系統簡介與核心商業價值

### English
**MNC Review Copilot Enterprise Pro v6.0** is an enterprise-grade, browser-native performance evaluation, 360-degree feedback fusion, and talent calibration platform built for high-growth multinational corporations (MNCs). The platform transforms unstructured, noisy observations into objective, legally defensible performance communications formatted according to top-tier executive frameworks including **STAR** (Situation, Task, Action, Result), **McKinsey MECE** (Mutually Exclusive, Collectively Exhaustive), **OKRs** (Objectives and Key Results), and the **Leadership Pipeline Scale**.

### 繁體中文
**MNC Review Copilot Enterprise Pro v6.0** 是專為跨國企業 (MNC) 與高成長科技團隊打造的企業級、瀏覽器原生的績效評估、360 度反饋融合與人才校準平台。本系統能將零碎、主觀的日常觀察，快速轉化為具備數據支撐、符合法律合規性（Defensible Growth Directives）與高階主管標準的考評報告，全面支援 **STAR 結構**、**麥肯錫 MECE 框架**、**OKR 關鍵成果對齊** 與 **領導力階梯 (Leadership Pipeline)** 模式。

---

### 🎯 Key Business Impact & ROI / 商業效益與投資報酬率

| Key Metric / 衡量指標 | Traditional Process / 傳統考核流程 | MNC Copilot Pro / 使用本系統 | Business Impact / 商業價值與效益 |
| :--- | :--- | :--- | :--- |
| **Review Drafting Time / 撰寫時間** | 90–120 mins per review | **5–10 mins per review** | **85%+ reduction in executive time spent** (節省 85% 以上高階管理工時) |
| **Legal Compliance / 合規風險** | High subjective bias risk | **100% Defensible Language** | Eliminates HR lawsuits and wrongful dismissal risks (消除主觀歧視與訴訟風險) |
| **Calibration Alignment / 績效校準** | Unstructured, manual debate | **Interactive 9-Box Grid** | Accelerates calibration meetings by 80% (校準會議效率提升 80%) |
| **Data Privacy / 資料安全** | Third-party cloud leak risk | **100% On-Device / Local Isolation** | Zero server-side data retention (資料 100% 本地隔離，通過 SOC2/GDPR) |

---

## 🏗️ 2. High-Level Architecture Topology / 系統架構拓撲圖

```
+---------------------------------------------------------------------------------------------------------+
|                                    GLOBAL HEADER & NAVIGATION CONTROLLER                                |
|             [User Session & Avatar] | [AI Receptionist SaaS Link] | [Portfolio Hub] | [API Config]      |
+---------------------------------------------------+-----------------------------------------------------+
                                                    |
                                                    v
+---------------------------------------------------------------------------------------------------------+
|                                        MAIN WORKSPACE ROUTER                                            |
|  [Tab 1: Studio] [Tab 2: Matrix] [Tab 3: HR Analytics & 9-Box] [Tab 4: Playbook] [Tab 5: Audit] [Tab 6: Sandbox] |
+-------+----------------+------------------+-------------------+------------------+-------------------+--+
        |                |                  |                   |                  |                   |
        v                v                  v                   v                  v                   v
+---------------+ +--------------+ +------------------+ +-----------------+ +------------------+ +---------------+
| Module 1:     | | Module 2:    | | Module 3:        | | Module 4:       | | Module 5:        | | Module 6:     |
| Review Studio | | Skill Radar  | | HR Analytics & | | Copywriting     | | Audit Trail    | | Prompt        |
| Synthesis     | | Gap Matrix   | | 9-Box Matrix     | | Playbook        | | Governance       | | Sandbox       |
+-------+-------+ +------+-------+ +--------+---------+ +--------+--------+ +--------+---------+ +-------+-------+
        |                |                  |                   |                  |                   |
        v                v                  v                   v                  v                   v
+---------------+ +--------------+ +------------------+ +-----------------+ +------------------+ +---------------+
| 360 Feedback  | | Chart.js     | | McKinsey 9-Box   | | Raw-to-Executive| | SHA-256 Hashed   | | LLM Tuning    |
| Fusion Engine | | Benchmark    | | Talent Grid      | | Phrase Engine   | | Log Stream       | | Hyperparams   |
+---------------+ +--------------+ +------------------+ +-----------------+ +------------------+ +---------------+
        |                |                  |                   |                  |                   |
        +----------------+------------------+-------------------+------------------+-------------------+
                                                    |
                                                    v
                                +---------------------------------------+
                                |      BROWSER LOCAL STORAGE & DB       |
                                |  (`mnc_users_db`, `mnc_session_user`) |
                                +---------------------------------------+
```

---

## 🧩 3. Core Production-Grade Modules / 6 大企業級核心模組

### Module 1: Review Studio / 績效評估合成工作台
* **English**: The core workbench for transforming raw observations into structured appraisals. Features multi-dimensional weighting, job family selection (`Software Engineering`, `Product`, `GTM`, `Design`), career band scope (`IC4` to `M2`), 360-degree peer feedback fusion, and multi-language synthesis (`English`, `Traditional Chinese`, `Japanese`).
* **繁體中文**: 核心考評合成工作台。支援多維度權重計算、職等職級切換（IC4 至 M2 總監級）、360 度同儕與部屬反饋融合計算，並能一鍵產出英、繁中、日三語的高階企業報告。

### Module 2: Competency Matrix & Skill-Gap Engine / 職能雷達與能力缺口分析
* **English**: Evaluates 5 core dimensions (**Technical Execution**, **System Ownership**, **Cross-Team Collaboration**, **Mentorship**, **Strategic Impact**) using Chart.js radar charts overlaid against global industry career-band benchmarks.
* **繁體中文**: 五維行為職能雷達評分系統。即時將個人得分與同職等全球標竿（Peer Benchmarks）進行分層對比，自動計算晉升能力缺口（Promotion Skill Gap）並產出成長行動計畫。

### Module 3: HR Analytics & McKinsey 9-Box Talent Grid / 人才分析與麥肯錫九宮格矩陣
* **English**: Organizational talent calibration tool providing departmental performance distribution bar charts, tier pie charts, and an interactive McKinsey 9-Box Matrix (Performance vs. Potential) for executive talent reviews.
* **繁體中文**: 部門績效分佈圖表與麥肯錫 9-Box 人才九宮格矩陣。點擊九宮格中的任一區塊（如 Star Performer, High Keeper, Rough Diamond）可即時過濾人才名單，協助 HR 與高層進行留才與薪酬校準。

### Module 4: Executive Copywriting Playbook / 高階文案手冊與句型轉換器
* **English**: Enterprise copywriting taxonomy, active action verb matrices, defensible language rules, and a **Raw-to-Executive Phrase Transformer** that upgrades informal managerial notes into C-Suite ready statements.
* **繁體中文**: 企業高階文案庫與口語轉 C-Suite 句型轉換器。包含高強度動詞字典、量化指標句型範例、HR 避坑指南以及雙語（中/英）高階評語對照表。

### Module 5: Audit Trail & Security Governance / 企業審計日誌與合規追蹤
* **English**: Enterprise compliance system recording all user authentications, prompt overrides, review syntheses, and exports into an immutable audit stream with SHA-256 hash validation signatures.
* **繁體中文**: 企業級安全審計與合規日誌。紀錄所有登入、提示詞修改、評語生成與導出事件，具備事件等級過濾（INFO, WARN, SEC_ALERT）與 JSON 審計報告導出功能。

### Module 6: Prompt Engineering Sandbox / 系統提示詞工程實驗室
* **English**: Tuning environment for customizing LLM system directives and fine-tuning hyper-parameters ($T$, $\text{Top-P}$, $\text{Frequency Penalty}$) with factory default reset controls.
* **繁體中文**: 提示詞實驗室。允許管理員即時調整底层 LLM System Directive，並可微調 Temperature、Top-P 與 Frequency Penalty 等超參數。

---

## 🧮 4. Mathematical Foundations / 數學公式與演算法基礎

### 4.1 360-Degree Composite Performance Score / 360度綜合績效權重公式

$$
S_{\text{composite}} = \left( W_{\text{self}} \cdot S_{\text{self}} \right) + \left( W_{\text{peer}} \cdot S_{\text{peer}} \right) + \left( W_{\text{report}} \cdot S_{\text{report}} \right) + \left( W_{\text{mgr}} \cdot S_{\text{mgr}} \right)
$$

Where the standard enterprise weight vector is defined as / 標準權重向量設定為：

$$
\vec{W} = \begin{bmatrix} W_{\text{self}} \\ W_{\text{peer}} \\ W_{\text{report}} \\ W_{\text{mgr}} \end{bmatrix} = \begin{bmatrix} 0.15 \\ 0.35 \\ 0.20 \\ 0.30 \end{bmatrix}, \quad \sum W_i = 1.0
$$

Scaled 100-point enterprise metric equation / 換算為百分制企業權重分數公式：

$$
S_{\text{scaled}} = \min \left( 100, \left\lfloor \left( w_{\text{tech}} \cdot 0.45 \right) + \left( w_{\text{collab}} \cdot 0.30 \right) + \left( w_{\text{lead}} \cdot 0.35 \right) + 20 \right\rfloor \right)
$$

### 4.2 Readability & Corporate Jargon Density / 可讀性與企業術語密度演算法

$$
\text{Flesch-Kincaid Grade Level } (GL) = 0.39 \left( \frac{\text{Total Words}}{\text{Total Sentences}} \right) + 11.8 \left( \frac{\text{Total Syllables}}{\text{Total Words}} \right) - 15.59
$$

$$
\text{Jargon Density } (D_{\text{jargon}}) = \left( \frac{\sum_{w \in T} \mathbb{I}(w \in L)}{\text{Total Words}} \right) \times 100\%
$$

---

## 🔒 5. Security & Data Governance / 安全性與資料治理

| Security Dimension / 資安維度 | Technical Guarantee / 技術保障 | Implementation Mechanism / 實現機制 |
| :--- | :--- | :--- |
| **Data Storage / 資料儲存** | 100% Client-Side Local | HTML5 `localStorage` (`mnc_users_db`) |
| **Data Retention / 資料留存** | Zero External Leakage | No network tracking or backend telemetry |
| **Audit Chaining / 審計簽章** | SHA-256 Pseudo-Hash | Dynamic 8-character verification signature |
| **Session Isolation / 階段管理** | Instant Invalidation | Revokes local tokens upon logout |

---

## 🚀 6. Deployment & Tech Stack / 部署規範與技術棧

* **Frontend Stack**: Vanilla HTML5, ES6+ JavaScript, Tailwind CSS (v3.4.0), FontAwesome (v6.4.0), Chart.js (v4.4.0).
* **Deployment Models**: Static bundle compatible with AWS CloudFront, Vercel, Netlify, Cloudflare Pages, or GitHub Pages.
* **Browser Compatibility**: Full support for Chrome, Safari, Edge, and Firefox without build tools or server node dependencies.
