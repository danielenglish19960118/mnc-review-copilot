=========================================
LINE 115: UPDATE SECTION 4 WITH EXTENDED MATHEMATICAL FORMULATION AND DETAILED EXPLANATION
=========================================
## 🧮 4. Mathematical Foundations & Algorithm Specs / 數學公式與演算法詳細說明

### 4.1 360-Degree Multi-Rater Composite Performance Engine / 360度多方評估綜合分數演算法與變數說明

#### English
The 360-Degree Composite Performance Rating system merges multi-rater input vectors with core organizational competency weights. Let $S_i$ represent the raw rating score provided by evaluator source $i$, where $i \in \{\text{self}, \text{peer}, \text{report}, \text{mgr}\}$. Each source is governed by a normalized weight $W_i$.

#### 繁體中文
360 度多方評估綜合分數系統將多元評估來源輸入向量與企業核心職能權重進行融合計算。設 $S_i$ 表示評估來源 $i$ 所提供之原始評分，其中 $i \in \{\text{self (自評)}, \text{peer (同儕)}, \text{report (部屬)}, \text{mgr (主管)}\}$。各評估來源受歸一化權重 $W_i$ 所約束。

#### Equation 1: Normalized Rater Weight Composite / 多評估者權重綜合公式
$$
S_{\text{composite}} = \sum_{i \in \{\text{self}, \text{peer}, \text{report}, \text{mgr}\}} W_i \cdot S_i = \left( W_{\text{self}} \cdot S_{\text{self}} \right) + \left( W_{\text{peer}} \cdot S_{\text{peer}} \right) + \left( W_{\text{report}} \cdot S_{\text{report}} \right) + \left( W_{\text{mgr}} \cdot S_{\text{mgr}} \right)
$$

**Variable & Constraint Definitions / 變數與約束條件說明：**
* $S_{\text{self}} \in [1.0, 5.0]$: Self-evaluation rating score (自評分數).
* $S_{\text{peer}} \in [1.0, 5.0]$: Aggregated mean peer evaluation score (同儕平均評分).
* $S_{\text{report}} \in [1.0, 5.0]$: Direct reports upward evaluation score (部屬向上反饋平均分).
* $S_{\text{mgr}} \in [1.0, 5.0]$: Direct manager official appraisal score (直屬主管官方評分).
* **Weight Normalization Constraint (權重歸一化約束)**: 
  $$\sum_{i} W_i = W_{\text{self}} + W_{\text{peer}} + W_{\text{report}} + W_{\text{mgr}} = 1.0, \quad W_i \ge 0$$
* Standard Enterprise Weight Matrix / 標準企業預設權重矩陣:
  $$\vec{W} = \begin{bmatrix} W_{\text{self}} \\ W_{\text{peer}} \\ W_{\text{report}} \\ W_{\text{mgr}} \end{bmatrix} = \begin{bmatrix} 0.15 \\ 0.35 \\ 0.20 \\ 0.30 \end{bmatrix}$$

#### Equation 2: Scaled 100-Point Enterprise Score Transformation / 百分制企業分數轉換公式
$$
S_{\text{scaled}} = \min \left( 100, \left\lfloor \left( w_{\text{tech}} \cdot 0.45 \right) + \left( w_{\text{collab}} \cdot 0.30 \right) + \left( w_{\text{lead}} \cdot 0.35 \right) + 20 \right\rfloor \right)
$$
* $w_{\text{tech}} \in [0, 100]$: User-adjusted Technical Execution weight slider value (技術交付權重 slider 設定值).
* $w_{\text{collab}} \in [0, 100]$: Cross-Team Collaboration weight slider value (跨團隊協作權重 slider 設定值).
* $w_{\text{lead}} \in [0, 100]$: Strategic Leadership weight slider value (戰略領導力權重 slider 設定值).
* $20$: Enterprise baseline offset constant ensuring minimum calibrated floor (企業基礎校準常數偏移量).

---

### 4.2 Readability & Corporate Jargon Density / 可讀性與企業術語密度演算法說明

#### Equation 3: Flesch-Kincaid Grade Level (FKGL) / 可讀性年級指標公式
$$
\text{FKGL} = 0.39 \left( \frac{N_{\text{words}}}{N_{\text{sentences}}} \right) + 11.8 \left( \frac{N_{\text{syllables}}}{N_{\text{words}}} \right) - 15.59
$$

**Parameter Explanation / 參數與意義解讀：**
* $N_{\text{words}}$: Total word count in synthesized output review text (生成的評語文字總詞數).
* $N_{\text{sentences}}$: Total sentence count bounded by punctuation terminators (`.`, `!`, `?`) (總句數).
* $N_{\text{syllables}}$: Total acoustic syllable count determined via vowel group regex parsing (總音節數).
* **Target Value (目標區間)**: $\text{FKGL} \in [10.0, 14.0]$ represents optimal C-suite professional readability without excessive verbal complexity (代表具備最佳高階主管專業可讀性，既不口語化亦無冗長病句).

#### Equation 4: Corporate Jargon Density Metric / 企業術語密度指標
$$
D_{\text{jargon}} = \left( \frac{\sum_{w \in T} \mathbb{I}(w \in \mathcal{L}_{\text{corporate}})}{N_{\text{words}}} \right) \times 100\%
$$

**Indicator Components / 函數元件解讀：**
* $T$: Set of all tokens in the generated performance review (生成評語中所有詞彙之集合).
* $\mathcal{L}_{\text{corporate}}$: Standard Enterprise MNC Business Taxonomy dictionary comprising high-impact corporate terms (such as *synergy*, *spearheaded*, *KPI*, *blue-green*, *ROI*, *SLA*) (高階企業術語詞典).
* $\mathbb{I}(\cdot)$: Indicator function returning $1$ if token $w \in \mathcal{L}_{\text{corporate}}$, else $0$ (示性函數，當詞彙屬於企業術語時傳回 1，反之傳回 0).

---

### 4.3 Skill-Gap & Promotion Vector Diagnostics / 職能缺口與晉升向量診斷演算法

#### Equation 5: Euclidean Competency Vector Distance / 歐幾里得職能向量距離公式
Let $\vec{V}_{\text{emp}} = [d_1, d_2, d_3, d_4, d_5]^T$ be the employee's score vector across 5 dimensions (Delivery, Ownership, Collaboration, Mentorship, Impact). Let $\vec{V}_{\text{target}}$ be the benchmark score vector for the target career band (e.g., IC6 Staff Engineer).

$$
\Delta_{\text{gap}} = \|\vec{V}_{\text{target}} - \vec{V}_{\text{emp}}\|_2 = \sqrt{\sum_{k=1}^{5} \left( V_{\text{target}, k} - V_{\text{emp}, k} \right)^2}
$$

$$
\text{Promotion Readiness Index } (PRI) = \max \left( 0, 1.0 - \frac{\Delta_{\text{gap}}}{\sqrt{5 \times (5.0)^2}} \right) \times 100\%
$$

**Diagnostic Thresholds / 診斷門檻數值：**
* $PRI \ge 85\%$: Ready for Immediate Promotion Calibration (具備立即晉升校準資格).
* $70\% \le PRI < 85\%$: Targeted 6-Month Skill-Gap Action Plan Required (需執行 6 個月定向缺口補強計畫).
* $PRI < 70\%$: Core Role Stabilization Phase (處於目前職等能力穩定打底階段).

---

### 4.4 McKinsey 9-Box Spatial Cell Mapping / 麥肯錫九宮格空間矩陣映射演算

Let $P_{\text{perf}} \in [1.0, 5.0]$ represent the quantitative Performance axis score and $P_{\text{pot}} \in [1.0, 5.0]$ represent the Qualitative Potential axis rating.

$$
\text{GridX}(P_{\text{perf}}) = \begin{cases} 
1 & \text{if } 1.0 \le P_{\text{perf}} < 3.0 \text{ (Low)} \\ 
2 & \text{if } 3.0 \le P_{\text{perf}} < 4.2 \text{ (Moderate)} \\ 
3 & \text{if } 4.2 \le P_{\text{perf}} \le 5.0 \text{ (High)} 
\end{cases}
$$

$$
\text{GridY}(P_{\text{pot}}) = \begin{cases} 
1 & \text{if } 1.0 \le P_{\text{pot}} < 3.0 \text{ (Low)} \\ 
2 & \text{if } 3.0 \le P_{\text{pot}} < 4.2 \text{ (Moderate)} \\ 
3 & \text{if } 4.2 \le P_{\text{pot}} \le 5.0 \text{ (High)} 
\end{cases}
$$

$$
\text{CellIndex}(\text{GridX}, \text{GridY}) = 3 \cdot (\text{GridY} - 1) + \text{GridX}, \quad \text{CellIndex} \in \{1, 2, \dots, 9\}
$$

When $\text{CellIndex} = 9$ ($\text{GridX}=3, \text{GridY}=3$), the employee is mapped into the **★ STAR PERFORMER** quadrant, triggering high-retention equity grant recommendations and fast-track executive promotion pathways.