# Structured Reasoning Frameworks for LLM-Based Venture Capital Evaluation

**Supporting Materials and Data Repository**

This repository contains the evaluation resources, knowledge stacks, prompts, and results for the research paper:

**Structured Reasoning Frameworks for LLM-Based Venture Capital Evaluation: Integrating Systems Engineering and Business Analysis**

Dan Velarde, Stephen Gillespie
United States Military Academy, West Point, New York, USA

## Abstract

Venture capital decision-making for early-stage startups involves high uncertainty and relies heavily on qualitative reasoning from pitch decks. This study investigates whether large language models (LLMs) equipped with structured knowledge frameworks can improve predictive accuracy in startup evaluation. We designed four evaluation personas using Gemini 2.5 Pro Preview: a baseline model, a venture capital-informed model, a systems engineering-guided model using established standards from IEEE, INCOSE, NASA, and MITRE, and a combined model integrating both frameworks. Testing on 14 historical pitch decks from companies including LinkedIn, Theranos, and WeWork, the combined persona achieved 85.7% accuracy in predicting startup outcomes, outperforming specialized and baseline configurations. The systems engineering rubric provided quantitative risk assessment while the venture capital knowledge stack enhanced market opportunity identification. Results demonstrate that LLMs can function as structured reasoning engines when constrained by domain-specific frameworks, offering transparent and auditable decision support for high-uncertainty investment environments.

## Important Note: Pitch Deck Availability

**The pitch decks used in this study are NOT included in this repository due to copyright and sharing restrictions.**

The 14 pitch decks analyzed in this research can be downloaded from **SlideShare.net**. Search for the following company pitch decks:

**Successful Companies (7 decks):**
- Buffer Startup Pitch Deck
- Coinbase Startup Pitch Deck
- Intercom Startup Pitch Deck
- LinkedIn Startup Pitch Deck
- Matchbox/Tinder Startup Pitch Deck
- Monzo Startup Pitch Deck
- WeWork Startup Pitch Deck

**Failed Companies (7 decks):**
- Bliss Startup Pitch Deck
- Cardlife Startup Pitch Deck
- Castle Startup Pitch Deck
- Flowtab Startup Pitch Deck
- Limetree Startup Pitch Deck
- Spartan Energy (available via SEC EDGAR archives)
- Theranos Startup Pitch Deck

*Note: Some decks may need OCR processing for text extraction. All historical outcomes were verified through public records.*

## Repository Contents

### Prompts/
LLM prompts used for each evaluation persona:
- **Basic Persona Prompt** - Control model with no domain knowledge
- **Venture Capital Persona Prompt** - Informed by VC literature and industry best practices
- **Systems Engineering Persona Prompt** - Guided by IEEE, INCOSE, NASA, and MITRE standards
- **Combined Persona Prompt** - Integrated both frameworks for balanced technical and market evaluation

### VC_Stack/
Venture Capital Knowledge Stack containing 40+ industry documents and academic papers:
- Due diligence questionnaires and frameworks
- Investment decision-making methodologies
- Valuation techniques and startup lifecycle models
- Case studies and historical market analysis
- Fund structuring and LP/GP relationship guides

Key sources include:
- ILPA Private Equity Principles
- PitchBook-NVCA Venture Monitor Q2 2024
- BCG Deep Tech Investment Guide
- Academic papers on VC investment patterns
- Industry reports on startup failure patterns

### SE Resources/
Systems Engineering Knowledge Stack with authoritative standards:
- **IEEE Standard 15288-2:2014** - Technical Reviews and Audits on Defense Programs
- **INCOSE Systems Engineering Handbook** (4th Edition, 2015)
- **NASA Systems Engineering Handbook**
- **MITRE Systems Engineering Guide**

### SE Rubric.pdf
Comprehensive Systems Engineering Evaluation Rubric with 5 categories and 20 subcriteria:
- Cost Risk (4 subcriteria × 25 points)
- Schedule Risk (4 subcriteria × 25 points)
- Technical Risk (4 subcriteria × 25 points)
- Programmatic Risk (4 subcriteria × 25 points)
- System Ilities (4 subcriteria × 25 points)
- Total Possible: 100 points per category
- Project Risk Score: Average across all categories

### Knowledge Stack Appendix.pdf
Detailed appendix documenting all sources used in the VC and SE knowledge stacks.

### LLM Data.xlsx
Complete evaluation dataset containing:
- All 56 persona evaluations (4 personas × 14 decks)
- Decision classifications (Yes/Leaning Yes/Leaning No/No)
- Confidence scores (0-100)
- Reasoning summaries
- Accuracy calculations

### Figures/
Publication-quality visualizations:
- `Updated_Method.jpg` - Research methodology diagram
- `confusion_matrices_clean_2x2.png` - Comparative confusion matrices
- `confusion_matrices_corrected_2x2.png` - Corrected confusion matrices
- `decision_distribution_basic_vc_se_combined.png` - Decision distribution comparison

## Research Overview

### Key Findings
- **Combined Framework Accuracy:** 85.7% prediction accuracy
- **Systems Engineering Framework:** 64.3% accuracy (conservative, technically rigorous)
- **Venture Capital Framework:** 64.3% accuracy (market-focused, optimistic bias)
- **Baseline Model:** 78.6% accuracy

### Methodology
Four evaluation personas were tested:
1. **Basic Persona** - Control model with no domain knowledge
2. **Venture Capital Persona** - Informed by VC literature and industry best practices
3. **Systems Engineering Persona** - Guided by IEEE, INCOSE, NASA, and MITRE standards
4. **Combined Persona** - Integrated both frameworks for balanced technical and market evaluation

All evaluations used Gemini 2.5 Pro Preview with identical configurations for comparability.

## Key Research Contributions

1. **Novel Integration of SE and VC Frameworks** - First study to systematically combine systems engineering standards (IEEE, INCOSE, NASA, MITRE) with venture capital evaluation criteria for LLM-based startup assessment.

2. **Unstructured Data Analysis** - Unlike prior work using structured datasets, this study evaluates LLMs on authentic pitch decks containing only the information available to real investors.

3. **Structured Reasoning Framework** - Demonstrates that LLMs can function as structured reasoning engines (not just pattern matchers) when constrained by domain-specific rubrics, enabling transparent decision rationales, auditable evaluation processes, and confidence-calibrated predictions.

4. **Error Pattern Analysis** - Identified three primary failure modes: Technical Conservatism (SE frameworks reject ventures lacking architectural documentation), Narrative Bias (VC frameworks over-weight founder storytelling), and Information Asymmetry (Conflicting signals lead to misclassification).

## Experimental Configuration

**LLM Environment:**
- Model: Gemini 2.5 Pro Preview
- Platform: MSTY.ai (local desktop deployment)
- Hardware: NVIDIA RTX 5080, Intel Core i9
- Max Output Tokens: 16,000
- Context Length: 30 messages
- Embedding Model: BERT-based retriever

**Evaluation Protocol:**
- Single-pass evaluation per deck (mimics real VC review)
- Identical model parameters across all personas
- No external connectivity required (local knowledge base retrieval)

## Reproducibility

To reproduce this study:
1. Download pitch decks from SlideShare (see list above)
2. OCR process the PDFs if needed for text extraction
3. Use the knowledge stacks provided (VC_Stack/ and SE Resources/)
4. Apply the SE rubric (SE Rubric.pdf) for evaluation criteria
5. Use the prompts provided (Prompts/) for each persona configuration
6. Compare your results against the evaluation data (LLM Data.xlsx)

*Note: The specific Gemini 2.5 Pro Preview version used may not be publicly accessible. For replication, use the latest available Gemini Pro model or equivalent (e.g., GPT-4, Claude Opus).*

## Usage Instructions

**For Researchers:**
1. Review the SE rubric to understand evaluation criteria
2. Download sample pitch decks from SlideShare
3. Analyze evaluation results in LLM Data.xlsx
4. Explore error patterns and confidence calibration
5. Adapt frameworks for your own evaluation contexts

**For Practitioners:**
1. Use the VC and SE knowledge stacks as due diligence checklists
2. Apply the SE rubric to assess technical risk in early-stage ventures
3. Reference the Combined framework approach for balanced evaluation
4. Calibrate confidence thresholds (≥85% shows 91.7% accuracy)

## Limitations

As discussed in the paper:
- **Information Leakage:** LLM training may include knowledge of high-profile companies
- **Sample Size:** 14 pitch decks (small for statistical generalization)
- **Binary Classification:** Success/failure oversimplifies complex outcomes
- **Hindsight Bias:** Historical evaluation introduces retrospective knowledge
- **Single-Pass Evaluation:** No ensemble aggregation or repeated trials
- **No Human Benchmark:** Expert investor performance not measured

## Future Research Directions

- Expand dataset to 100+ pitch decks
- Implement ensemble evaluation with repeated trials
- Benchmark against expert venture capitalists
- Test alternative LLM architectures (GPT-4, Claude Opus, Llama)
- Develop adaptive rubric weighting via reinforcement learning
- Incorporate multimodal analysis (slide layouts, images, charts)
- Conduct ablation studies on knowledge stack components
- Explore cross-domain applications (grants, R&D proposals, acquisitions)

## Citation

If you use this dataset, methodology, or findings in your research, please cite:

> Velarde, D., & Gillespie, S. (2025). Structured Reasoning Frameworks for LLM-Based Venture Capital Evaluation: Integrating Systems Engineering and Business Analysis. United States Military Academy, West Point, NY.

## Authors

**Dan Velarde**
United States Military Academy
West Point, New York, USA
Email: dan.velarde@westpoint.edu (Expires May 2026)
Personal Email: dan.velarde@outlook.com

**Stephen Gillespie**
United States Military Academy
West Point, New York, USA
Email: stephen.gillespie@westpoint.edu

## Acknowledgments

The authors acknowledge the use of:
- Claude Sonnet 4.5 (Anthropic, 2025) for data analysis, section development, and manuscript preparation
- ChatGPT (OpenAI, 2025) for figure generation and visualization support
- Gemini 2.5 Pro Preview (Google, 2024) as the evaluation model for all persona configurations

## License

This research is released for academic and educational use. For commercial applications or derivative works, please contact the authors.

## Keywords

Large language models, venture capital, systems engineering, artificial intelligence, decision support systems, startup evaluation, structured reasoning, pitch deck analysis, risk assessment, LLM evaluation frameworks

---

**Repository Status:** Complete dataset and materials for published research
**Last Updated:** December 2025
