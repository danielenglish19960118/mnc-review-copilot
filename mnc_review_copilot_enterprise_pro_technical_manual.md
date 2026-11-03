# MNC Review Copilot Enterprise Pro v6.0 — Technical Specification & Architecture Manual

## 1. Executive Summary & Architectural Philosophy

**MNC Review Copilot Enterprise Pro v6.0** is an enterprise-grade, browser-native performance evaluation and talent calibration suite built for multinational corporate leadership. It transforms unstructured managerial observations into objective, defensible, and STAR/McKinsey-compliant appraisal communications in seconds.

### Core Architectural Pillars
* **Zero-Friction Single-File Architecture**: Single-page static bundle requiring zero server-side compilation, Node.js dependencies, or backend databases. Can be served via edge CDN (Vercel, GitHub Pages, S3).
* **Privacy-First Data Sovereignty**: All employee ratings, managerial notes, and session state remain localized within browser memory (`localStorage` / `sessionStorage`). No candidate data is retained on external application servers.
* **Polyglot Executive Copy Engine**: Native support for C-Suite English, Traditional Chinese (繁體中文), and Business Japanese (日本語) evaluation framing.

---

## 2. High-Level System Architecture

```
                                  +---------------------------------------+
                                  |         Global Header & Nav           |
                                  |  (Session Badge | SaaS Links | Config)|
                                  +-------------------+-------------------+
                                                      |
                                                      v
  +-------------------------------------------------------------------------------------------------------+
  |                                        MAIN WORKSPACE ROUTER                                          |
  +------------------+------------------+------------------+------------------+------------------+--------+
  |                  |                  |                  |                  |                  |
  v                  v                  v                  v                  v                  v
+--------------+   +--------------+   +--------------+   +--------------+   +--------------+   +--------------+
| Module 1:    |   | Module 2:    |   | Module 3:    |   | Module 4:    |   | Module 5:    |   | Module 6:    |
| Review       |   | Competency   |   | HR Analytics |   | Copywriting  |   | Audit &      |   | Prompt       |
| Studio       |   | Matrix       |   | & 9-Box Grid |   | Playbook     |   | Governance   |   | Sandbox      |
+------+-------+   +------+-------+   +------+-------+   +------+-------+   +------+-------+   +------+-------+
       |                  |                  |                  |                  |                  |
       v                  v                  v                  v                  v                  v
+--------------+   +--------------+   +--------------+   +--------------+   +--------------+   +--------------+
| 360 Feedback |   | Skill Gap &  |   | Chart.js     |   | Phrase       |   | Event Hash   |   | Hyperparam   |
| Engine       |   | Radar Chart  |   | Visualizer   |   | Transformer  |   | Logger       |   | Tuning       |
+--------------+   +--------------+   +--------------+   +--------------+   +--------------+   +--------------+
       |                  |                  |                  |                  |                  |
       +------------------+------------------+------------------+------------------+------------------+
                                                      |
                                                      v
                                  +---------------------------------------+
                                  |       Client Persistence Layer        |
                                  |     (localStorage DB / Audit Log)     |
                                  +---------------------------------------+
```

---

## 3. Data Flow & Algorithmic Specifications

### 3.1 360-Degree Feedback & Competency Score Calculation Engine

The final composite appraisal score ($S_{\text{composite}}$) is calculated using a weighted multi-source scoring algorithm:

$$S_{\text{composite}} = (W_{\text{self}} \cdot S_{\text{self}}) + (W_{\text{peers}} \cdot S_{\text{peers}}) + (W_{\text{reports}} \cdot S_{\text{reports}}) + (W_{\text{manager}} \cdot S_{\text{manager}})$$

Default Weights:
* Self-Evaluation ($W_{\text{self}}$): **15%**
* Peer Reviews ($W_{\text{peers}}$): **35%**
* Direct Reports ($W_{\text{reports}}$): **20%**
* Manager Assessment ($W_{\text{manager}}$): **30%**

#### Scaled Score Output ($S_{\text{scaled}}$):
$$S_{\text{scaled}} = \min\left(100, \text{round}\left(W_{\text{tech}} \cdot 0.45 + W_{\text{collab}} \cdot 0.30 + W_{\text{lead}} \cdot 0.35 + 20\right)\right)$$

```javascript
function recalculateReviewScore() {
    const wTech = parseInt(document.getElementById('weightTech')?.value || '45');
    const wCollab = parseInt(document.getElementById('weightCollab')?.value || '30');
    const wLead = parseInt(document.getElementById('weightLead')?.value || '25');

    const wSelf = parseFloat(document.getElementById('weightSelf')?.value || '4.5');
    const wPeers = parseFloat(document.getElementById('weightPeers')?.value || '4.8');
    const wReports = parseFloat(document.getElementById('weightReports')?.value || '4.6');
    const wMgr = parseFloat(document.getElementById('weightManager')?.value || '4.7');

    const score = Math.min(100, Math.round((wTech * 0.45) + (wCollab * 0.3) + (wLead * 0.35) + 20));
    const composite360 = ((wSelf * 0.15) + (wPeers * 0.35) + (wReports * 0.20) + (wMgr * 0.30)).toFixed(1);

    document.getElementById('calculatedScoreBadge').innerText = `★ ${composite360} / 5.0 (Calculated: ${score}/100)`;
}
```

---

### 3.2 McKinsey 9-Box Talent Calibration Matrix

The 9-Box Grid classifies talent by mapping **Performance** (Horizontal Axis) against **Potential** (Vertical Axis):

| Potential \ Performance | Low Performance | Moderate Performance | High Performance |
| :--- | :--- | :--- | :--- |
| **High Potential** | Enigma / Rough Diamond | High Keeper | **★ STAR PERFORMER** |
| **Moderate Potential** | Dilemma / Question Mark | Core Player | High Impact IC |
| **Low Potential** | Action Needed | Effective Performer | Trusted Professional |

#### Segment Data Handler Schema:
```typescript
interface NineBoxSegment {
    id: string;
    label: string;
    performanceLevel: 'Low' | 'Moderate' | 'High';
    potentialLevel: 'Low' | 'Moderate' | 'High';
    retentionPriority: 'CRITICAL' | 'HIGH' | 'MEDIUM' | 'LOW';
    actionPlan: string;
}
```

---

## 4. Module Specifications

### Module 1: Review Studio (`#tab-studio`)
* **Inputs**: Employee Name, Job Family (`Engineering`, `Product`, `GTM`, `Design`), Seniority Band (`IC4`, `IC5`, `M1`, `M2`), Performance Tier, Evaluation Framework (`STAR`, `McKinsey MECE`, `OKR`, `Leadership Pipeline`), Target Language/Tone Register (`English Executive`, `Traditional Chinese Executive`, `Growth Coaching`, `Japanese Professional`), Competency Sliders.
* **Outputs**: Formatted Appraisal Document, Flesch-Kincaid Readability Score, Objectivity Metric, Jargon Density indicator.
* **Exports**: `.JSON`, `.TXT`, Clipboard Copy, Session Archive.

### Module 2: Competency Matrix (`#tab-matrix`)
* **Radar Dimensions**: Technical Delivery, Architecture Ownership, Cross-Team Collaboration, Mentorship, Strategic Impact.
* **Visual Engine**: `Chart.js` Radar Chart with dynamic dataset overlay comparing individual scores against global senior averages (e.g., *Staff Eng IC5 Benchmark*).

### Module 3: HR Analytics & Talent Grid (`#tab-analytics`)
* **Visual Engine**: Dual Chart.js instances (`Bar Chart` for department averages, `Doughnut Chart` for rating tier distribution).
* **Talent Matrix**: Clickable 9-Box Grid with detail panel updating segment retention plans in real-time.

### Module 4: Copywriting Playbook & Transformer (`#tab-copybook`)
* **Interactive Tool**: Raw-to-Executive Phrase Transformer (turns informal manager notes into C-Suite ready statements).
* **Resource Base**: Action verb library, quantifiable impact syntax, legally defensible growth directive templates, bilingual phrasebook.

### Module 5: Audit & Security Compliance (`#tab-audit`)
* **Event Logging**: Captures authentication, review synthesis, prompt overrides, and report downloads.
* **Log Properties**: Timestamp, Action Code (`USER_LOGIN`, `REVIEW_SYNTHESIS`, `BYPASS_LOGIN`), Actor Email, Severity (`INFO`, `WARN`, `SEC_ALERT`), SHA-256 Short Hash (`e3b0c442`).
* **Exports**: Audit Log JSON Backup.

### Module 6: Prompt Engineering Studio (`#tab-sandbox`)
* **LLM Hyperparameters**: Temperature ($0.0 - 1.0$), Top-P ($0.5 - 1.0$), Frequency Penalty ($0.0 - 2.0$).
* **System Directive Editor**: Editable base system prompt for customizing evaluation rules with a Factory Reset handler.

---

## 5. Security & Data Governance Specification

| Security Domain | Enterprise Guarantee | Technical Implementation |
| :--- | :--- | :--- |
| **Data Storage** | Local-Only Persistence | Data stored strictly in browser `localStorage` under key `mnc_users_db`. |
| **Network Footprint** | Offline Capable | Zero mandatory external API endpoints required for baseline execution. |
| **Audit Compliance** | Tamper-Evident Hash | Every logged action generates a pseudo-hash token for compliance tracking. |
| **Session State** | In-Memory Hydration | Auth state validated on load (`checkSessionState()`) with emergency bypass for demonstration. |

---

## 6. Enterprise API Contract Integration (Optional LLM Backend)

When an enterprise API key is provided via the Configuration Modal (`#settingsModal`), review generation queries external LLM providers directly using the following payload format:

```json
{
  "model": "gpt-4o",
  "temperature": 0.3,
  "top_p": 0.95,
  "frequency_penalty": 0.2,
  "messages": [
    {
      "role": "system",
      "content": "You are an expert HR Director and Engineering VP at a top multinational corporation (MNC)..."
    },
    {
      "role": "user",
      "content": "Employee: Victoria Sterling | Rating: Level 4: Exceeds | Framework: STAR | Language: English Executive | Notes: Victoria drove K8s migration..."
    }
  ]
}
```

---

## 7. Operational Maintenance & Deployment Guide

1. **Deployment**: Upload `index.html` directly to any static web hosting platform (Vercel, AWS S3 / CloudFront, Nginx).
2. **Environment Dependencies**:
   - `Tailwind CSS`: CDN distribution (v3.x)
   - `FontAwesome`: Icons (v6.4.0)
   - `Chart.js`: Data visualization (v4.x)
3. **Browser Compatibility**: Chrome/Edge 90+, Firefox 88+, Safari 14+ (Requires ES6 JavaScript and Flexbox/Grid CSS support).