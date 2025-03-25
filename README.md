
# Accelerating Drug Repurposing with AI  
### The Role of Large Language Models in Hypothesis Validation

This repository accompanies the paper:  
**“Accelerating Drug Repurposing with AI: The Role of Large Language Models in Hypothesis Validation”**  
By *Iratxe Zunzunegui Sanz, Belén Otero-Carrasco, and Alejandro Rodríguez-González*

---

## Overview

This project explores how Large Language Models (LLMs) can be used to validate drug repurposing hypotheses generated through pathway-based analysis. We evaluate four LLMs — GPT-4o, Claude-3, Gemini-2, and DeepSeek — using various prompt engineering strategies across both novel and benchmark drug-disease associations.

The repository includes:

- 30-case datasets derived from pathway-based predictions (DREBIOP)
- 10 prompt engineering techniques used across multiple LLMs
- Evaluation scripts and metrics (accuracy, precision, recall, F1-score)
- Results from both Phase 1 (prompt comparison) and Phase 2 (extended evaluation)
- A set of 10 benchmark drug repurposing cases for comparison

---

## Repository Structure

```bash
├── data/
│   ├── pathway_cases.csv
│   ├── benchmark_cases.csv
│   └── prompt_templates/
├── results/
│   ├── phase1_results.csv
│   ├── phase2_results.csv
│   └── benchmarking_results.csv
├── scripts/
│   ├── evaluation_phase_1.ipynb
│   ├── evaluation_30_pathway.ipynb
│   ├── evaluation_10_benchmark.ipynb
├── figures/
│   └── graphical_abstract.png
│   └── heatmap_f1.png
│   └── barplots_phase2.png
└── README.md
```
---

## Related Publication

Zunzunegui Sanz, I., Otero-Carrasco, B., & Rodríguez-González, A.  
**“Accelerating Drug Repurposing with AI: The Role of Large Language Models in Hypothesis Validation”**  
*To be presented at the 38th IEEE International Symposium on Computer-Based Medical Systems (IEEE CBMS2025)* – Madrid, Spain 2025  
DOI: 

---

## Contact

For questions, feel free to reach out:  
**iratxe.zunzunegui.sanz@alumnos.upm.es** ORCID: 0009-0002-0608-4615

**belen.otero@upm.es**
ORCID: 0000-0001-7315-2257

**alejandro.rg@upm.es**
ORCID: 0000-0001-8801-4762
