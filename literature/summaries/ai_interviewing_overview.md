# AI-Interviewing Literature Overview

*Compiled 2026-03-26 · 5 papers · Topics: AVI validity, algorithmic bias, applicant reactions, trust*

---

## 1. Hickman, L., Bosch, N., Ng, V., Saef, R., Tay, L., & Woo, S. E. (2022)

**Automated video interview personality assessments: Reliability, validity, and generalizability investigations**

*Journal of Applied Psychology*, 107(8), 1323–1351. DOI: [10.1037/apl0000695](https://doi.org/10.1037/apl0000695)

Using three independent samples of mock video interviews (total N = 1,073), the authors trained machine learning models to infer Big Five personality traits from verbal, paraverbal, and nonverbal cues. Models trained to predict interviewer-rated (rather than self-reported) personality produced stronger convergent validity and predicted academic outcomes. Test–retest reliability was mixed. The paper is the most comprehensive validity study of AVI personality scoring to date and won the 2024 SIOP Jeanneret Award.

**Relevance:** Benchmark for evaluating whether AI interview scores measure what they claim to measure.

---

## 2. Chen, Z. (2023)

**Ethics and discrimination in artificial intelligence-enabled recruitment practices**

*Humanities and Social Sciences Communications*, 10, Article 567. DOI: [10.1057/s41599-023-02079-x](https://doi.org/10.1057/s41599-023-02079-x)

A systematic review synthesising peer-reviewed literature on algorithmic discrimination in AI-powered hiring. Chen identifies three mechanisms through which bias enters AI recruitment: biased training data, proxy variables that correlate with protected characteristics, and lack of auditing transparency. The paper proposes both technical remedies (debiasing algorithms, fairness constraints) and governance-level remedies (third-party audits, explainability requirements). Notable for bridging computer science and organisational ethics perspectives.

**Relevance:** Entry point for understanding the ethical landscape; frames the bias problem and existing mitigation strategies.

---

## 3. Tilston, O., Krings, F., Roulin, N., Bourdage, J. S., & Fetzer, M. (2024)

**Reactions to asynchronous video interviews: The role of design decisions and applicant age and gender**

*Human Resource Management*, 63(2), 313–332. DOI: [10.1002/hrm.22202](https://doi.org/10.1002/hrm.22202)

An experimental study varying six AVI design features (preparation time, rerecording opportunity, number of questions, etc.) across a large applicant sample. Allowing more preparation time and the option to rerecord improved applicant reactions; more questions worsened them. Older applicants and women reported less favourable reactions overall, raising equity concerns about standardised AVI formats. Findings directly inform how AI interview platforms should be configured to reduce adverse reactions.

**Relevance:** Provides actionable design guidance and flags demographic heterogeneity in reactions — important for participant welfare in AI-interview research.

---

## 4. Suen, H. Y., & Hung, K. E. (2023)

**Building trust in automatic video interviews using various AI interfaces: Tangibility, immediacy, and transparency**

*Computers in Human Behavior*, 143, 107713. DOI: [10.1016/j.chb.2023.107713](https://doi.org/10.1016/j.chb.2023.107713)

An experiment comparing applicant trust across AVI conditions varying three interface properties: tangibility (visible AI agent vs. abstract), immediacy (real-time feedback cues), and transparency (explanation of how AI scores responses). AI presence alone increased cognitive trust over non-AI conditions; adding tangibility and transparency further increased both cognitive and affective trust. Immediacy did not reach significance. The study connects HCI design principles to the organisational justice concerns applicants raise about AI selection.

**Relevance:** Explains *why* candidates may distrust AI interviews and which interface choices can close that gap.

---

## 5. Koutsoumpis, A., Ghassemi, S., Oostrom, J., Holtrop, D., Van Breda, W., Zhang, T., & de Vries, R. E. (2024)

**Beyond traditional interviews: Psychometric analysis of asynchronous video interviews for personality and interview performance evaluation using machine learning**

*Computers in Human Behavior*, 154, 108128. DOI: [10.1016/j.chb.2023.108128](https://doi.org/10.1016/j.chb.2023.108128)

710 participants completed a mock AVI with questions targeting Extraversion and Conscientiousness. Automated extraction of verbal, facial, and vocal features fed machine learning models that explained substantially more variance in observer-rated personality (average R² = 0.32) and interview performance (R² = 0.44) than self-reports (average R² = 0.12) alone. Results suggest that multimodal ML scoring outperforms traditional self-report measures, but the sample was non-applied (mock interviews), limiting direct generalisability to high-stakes hiring.

**Relevance:** State-of-the-art demonstration of multimodal ML scoring; the R² comparisons are useful benchmarks for our own measurement framework.

---

## Cross-cutting themes

| Theme | Papers |
|---|---|
| Validity & psychometrics | Hickman et al. (2022); Koutsoumpis et al. (2024) |
| Bias & ethics | Chen (2023) |
| Applicant reactions | Tilston et al. (2024); Suen & Hung (2023) |
| Design implications | Tilston et al. (2024); Suen & Hung (2023) |

## Gaps identified

- All validity studies use mock (non-applied) samples — ecological validity unknown.
- Bias studies focus on resume screening; AVI-specific bias evidence is thinner.
- No longitudinal studies linking AVI scores to long-term job performance.
