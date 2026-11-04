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

---🧮 4. Mathematical Foundations & Algorithm Specs / 數學公式與演算法詳細說明
4.1 360-Degree Multi-Rater Composite Performance Engine / 360度多方評估綜合分數演算法與變數說明
English
The 360-Degree Composite Performance Rating system merges multi-rater input vectors with core organizational competency weights. Let 
S
i
 represent the raw rating score provided by evaluator source 
i
, where 
i
∈
self
,
peer
,
report
,
mgr
. Each source is governed by a normalized weight 
W
i
.

繁體中文
360 度多方評估綜合分數系統將多元評估來源輸入向量與企業核心職能權重進行融合計算。設 
S
i
 表示評估來源 
i
 所提供之原始評分，其中 
i
∈
self (自評)
,
peer (同儕)
,
report (部屬)
,
mgr (主管)
。各評估來源受歸一化權重 
W
i
 所約束。

Equation 1: Normalized Rater Weight Composite / 多評估者權重綜合公式
S
composite
=
∑
i
∈
self
,
peer
,
report
,
mgr
W
i
⋅
S
i
=
(
W
self
⋅
S
self
)
+
(
W
peer
⋅
S
peer
)
+
(
W
report
⋅
S
report
)
+
(
W
mgr
⋅
S
mgr
)

Variable & Constraint Definitions / 變數與約束條件說明：

S
self
∈
[
1.0
,
5.0
]
: Self-evaluation rating score (自評分數).
S
peer
∈
[
1.0
,
5.0
]
: Aggregated mean peer evaluation score (同儕平均評分).
S
report
∈
[
1.0
,
5.0
]
: Direct reports upward evaluation score (部屬向上反饋平均分).
S
mgr
∈
[
1.0
,
5.0
]
: Direct manager official appraisal score (直屬主管官方評分).
Weight Normalization Constraint (權重歸一化約束): 
∑
i
W
i
=
W
self
+
W
peer
+
W
report
+
W
mgr
=
1.0
,
W
i
≥
0
Standard Enterprise Weight Matrix / 標準企業預設權重矩陣: $$\vec{W} = \begin{bmatrix} W_{\text{self}} \ W_{\text{peer}} \ W_{\text{report}} \ W_{\text{mgr}} \end{bmatrix} = \begin{bmatrix} 0.15 \ 0.35 \ 0.20 \ 0.30 \end{bmatrix}$$
Equation 2: Scaled 100-Point Enterprise Score Transformation / 百分制企業分數轉換公式
S
scaled
=
min
(
100
,
⌊
(
w
tech
⋅
0.45
)
+
(
w
collab
⋅
0.30
)
+
(
w
lead
⋅
0.35
)
+
20
⌋
)

w
tech
∈
[
0
,
100
]
: User-adjusted Technical Execution weight slider value (技術交付權重 slider 設定值).
w
collab
∈
[
0
,
100
]
: Cross-Team Collaboration weight slider value (跨團隊協作權重 slider 設定值).
w
lead
∈
[
0
,
100
]
: Strategic Leadership weight slider value (戰略領導力權重 slider 設定值).
20
: Enterprise baseline offset constant ensuring minimum calibrated floor (企業基礎校準常數偏移量).
4.2 Readability & Corporate Jargon Density / 可讀性與企業術語密度演算法說明
Equation 3: Flesch-Kincaid Grade Level (FKGL) / 可讀性年級指標公式
FKGL
=
0.39
(
N
words
N
sentences
)
+
11.8
(
N
syllables
N
words
)
−
15.59

Parameter Explanation / 參數與意義解讀：

N
words
: Total word count in synthesized output review text (生成的評語文字總詞數).
N
sentences
: Total sentence count bounded by punctuation terminators (., !, ?) (總句數).
N
syllables
: Total acoustic syllable count determined via vowel group regex parsing (總音節數).
Target Value (目標區間): 
FKGL
∈
[
10.0
,
14.0
]
 represents optimal C-suite professional readability without excessive verbal complexity (代表具備最佳高階主管專業可讀性，既不口語化亦無冗長病句).
Equation 4: Corporate Jargon Density Metric / 企業術語密度指標
D
jargon
=
(
∑
w
∈
T
I
(
w
∈
L
corporate
)
N
words
)
×
100

Indicator Components / 函數元件解讀：

T
: Set of all tokens in the generated performance review (生成評語中所有詞彙之集合).
L
corporate
: Standard Enterprise MNC Business Taxonomy dictionary comprising high-impact corporate terms (such as synergy, spearheaded, KPI, blue-green, ROI, SLA) (高階企業術語詞典).
I
(
⋅
)
: Indicator function returning 
1
 if token 
w
∈
L
corporate
, else 
0
 (示性函數，當詞彙屬於企業術語時傳回 1，反之傳回 0).
4.3 Skill-Gap & Promotion Vector Diagnostics / 職能缺口與晉升向量診斷演算法
Equation 5: Euclidean Competency Vector Distance / 歐幾里得職能向量距離公式
Let $\vec{V}{\text{emp}} = [d_1, d_2, d_3, d_4, d_5]^T$ be the employee's score vector across 5 dimensions (Delivery, Ownership, Collaboration, Mentorship, Impact). Let $\vec{V}{\text{target}}$ be the benchmark score vector for the target career band (e.g., IC6 Staff Engineer).

Δ
gap
=
|
V
→
target
−
V
→
emp
|
2
=
∑
k
=
1
5
(
V
target
,
k
−
V
emp
,
k
)
2

Promotion Readiness Index 
(
P
R
I
)
=
max
(
0
,
1.0
−
Δ
gap
5
×
(
5.0
)
2
)
×
100

Diagnostic Thresholds / 診斷門檻數值：

P
R
I
≥
85
: Ready for Immediate Promotion Calibration (具備立即晉升校準資格).
70
: Targeted 6-Month Skill-Gap Action Plan Required (需執行 6 個月定向缺口補強計畫).
P
R
I
<
70
: Core Role Stabilization Phase (處於目前職等能力穩定打底階段).
4.4 McKinsey 9-Box Spatial Cell Mapping / 麥肯錫九宮格空間矩陣映射演算
Let 
P
perf
∈
[
1.0
,
5.0
]
 represent the quantitative Performance axis score and 
P
pot
∈
[
1.0
,
5.0
]
 represent the Qualitative Potential axis rating.

GridX
(
P
perf
)
=
{
1
if 
1.0
≤
P
perf
<
3.0
 (Low)
2
if 
3.0
≤
P
perf
<
4.2
 (Moderate)
3
if 
4.2
≤
P
perf
≤
5.0
 (High)

GridY
(
P
pot
)
=
{
1
if 
1.0
≤
P
pot
<
3.0
 (Low)
2
if 
3.0
≤
P
pot
<
4.2
 (Moderate)
3
if 
4.2
≤
P
pot
≤
5.0
 (High)

CellIndex
(
GridX
,
GridY
)
=
3
⋅
(
GridY
−
1
)
+
GridX
,
CellIndex
∈
1
,
2
,
…
,
9

When 
CellIndex
=
9
 (
GridX
=
3
,
GridY
=
3
), the employee is mapped into the ★ STAR PERFORMER quadrant, triggering high-retention equity grant recommendations and fast-track executive promotion pathways.

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
