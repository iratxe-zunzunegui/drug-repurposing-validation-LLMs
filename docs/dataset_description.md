# Dataset Description

This dataset supports the study _"Accelerating Drug Repurposing with AI: The Role of Large Language Models in Hypothesis Validation"_.

## Overview

The primary dataset used in this study was derived from a prior investigation focused on pathway-based drug repurposing, referred to as **DREBIOP** (Drug REpurposing based on BIOlogical Pathways) [1]. This approach leverages the assumption that if two diseases share a common biological pathway, a drug used to treat one condition may be repurposed to treat the other.

Using this principle, a total of **21,968 drug-disease associations** were generated computationally, among which **16,848** represented **novel associations**. These were identified by analyzing shared biological pathways between diseases and drugs using publicly available biomedical databases and computational methods [2].

## Data Used in This Study

- **30 cases** were randomly selected from the full DREBIOP dataset and used as the primary evaluation set in this study. These are available in [`data/pathway_cases.csv`](../data/pathway_cases.csv).
  - Each row includes:  
    - `Drug_Name`: the repurposing candidate  
    - `Original_Indication`: the drug's original use  
    - `Repurposed_Indication`: the predicted new indication  
    - `Shared_Pathway`: the biological pathway connecting the disease pair  
    - `Viability`: whether the hypothesis was considered viable based on scientific literature  
    - `Reference_ID`: citation reference(s) supporting the viability decision  
    - `Known_Status`: whether the case is previously known or novel

- To provide a benchmark comparison, **10 well-established drug repurposing cases** were extracted from the scientific literature [3]. These are available in [`data/benchmark_cases.csv`](../data/benchmark_cases.csv).  
  - These cases are historically validated and **do not necessarily share a biological pathway**.  
  - The file follows the same structure as the `pathway_cases.csv`, excluding the `Shared_Pathway` and `Known_Status` fields.

## References

[1] B. Otero Carrasco, L. Prieto-Santamaría and A. Rodríguez-González, "Exploring Innovative Approaches to Drug Repurposing: Emphasizing the Relevance of Biological Pathways," RExPO24 Conference, 2024. 

[2] B. Otero-Carrasco, E. Ugarte Carro, L. Prieto-Santamaría, M. Diaz Uzquiano, J. P. Caraça-Valente Hernández and A. Rodríguez-González, "Identifying patterns to uncover the importance of biological pathways on known drug repurposing scenarios," BMC genomics, vol. 25(1), no. 43, 2024. 

[3] S. Pushpakom, F. Iorio, P. A. Eyers, K. J. Escott, S. Hopper, A. Wells, A. Doig, T. Guilliams, J. Latimer, C. McNamee, A. Norris, P. Sanseau, D. Cavalla and M. Pirmohamed, "Drug repurposing: progress, challenges and recommendations," Nature Reviews Drug Discovery, vol. 18(1), p. 41–58, 2018. 
