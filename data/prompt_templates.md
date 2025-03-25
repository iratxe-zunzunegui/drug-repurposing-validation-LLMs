# Prompt Templates Used in LLM Validation

This document contains the ten prompt templates used to evaluate the performance of Large Language Models (LLMs) in validating drug repurposing hypotheses. Each prompt corresponds to a specific prompting strategy as described in the associated paper:  
**"Accelerating Drug Repurposing with AI: The Role of Large Language Models in Hypothesis Validation"**.

---

### P1 – Zero-Shot Prompting

**Technique**: Direct query without context  
**Template**:  
*“This possible drug repurposing case was identified by analyzing shared biological pathways. Based on biomedical evidence, can **[Drug Name]** be repurposed for **[Repurposed Indication]**? Begin your answer with a one-word verdict: ‘Viable’ or ‘Non-Viable’. Then, provide a brief scientific justification, including references if available”*

---

### P2 – Biological Pathway Contextualization

**Technique**: Adds shared pathway information  
**Template**:  
*“This possible drug repurposing case was identified by analyzing shared biological pathways. Cases generated through this methodology typically involve a high number of pathways, increasing the potential for mechanistic overlap. Given this context, can **[Drug Name]** be repurposed for treating **[Repurposed Indication]**? Begin with a one-word verdict (‘Viable’ or ‘Non-Viable’), followed by a scientific justification, including references if available”*

---

### P3 – Explicit Reasoning Prompting

**Technique**: Requests logical justification  
**Template**:  
*“This possible drug repurposing case was identified by analyzing shared biological pathways. Given this context, can **[Drug Name]** be repurposed for **[Repurposed Indication]**? Begin with a single-word verdict: ‘Viable’ or ‘Non-Viable.’ Support your answer with a brief but rigorous explanation based on known mechanisms of action, pathway involvement, and biomedical literature. If available, cite sources”*

---

### P4 – Few-Shot Prompting

**Technique**: Includes 2 labeled examples before query  
**Template**:  
*“This possible drug repurposing case was identified by analyzing shared biological pathways. Given this context, evaluate whether **[Drug Name]** can be repurposed for **[Repurposed Indication]**. Here are some examples:*

*Example 1: **[Viable Drug Name]** → **[Viable Repurposed Indication]** → Viable → **[Literature-based Justification]**.*

*Example 2: **[Non-viable Drug Name]** → **[Non-viable Repurposed Indication]** → Non-viable → **[Literature-based Justification]**.*

*Now, analyze: **[Drug Name]** → **[Repurposed Indication]**. Start with ‘Viable’ or ‘Non-Viable,’ followed by a scientific justification and references if available.”*

---

### P5 – Explicit Reasoning + Few-Shot Prompting

**Technique**: Combines examples with rationale  
**Template**:  
*This possible drug repurposing case was identified by analyzing shared biological pathways. Given this context, evaluate whether **[Drug Name]** can be repurposed for **[Repurposed Indication]**.* *Here are some examples:*

*Example 1: **[Viable Drug Name]** → **[Viable Repurposed Indication]** → Viable → **[Literature-based Justification]**.*

*Example 2: **[Non-viable Drug Name]** → **[Non-viable Repurposed Indication]** → Non-viable → **[Literature-based Justification]**.*

*Now, analyze: **[Drug Name]** → **[Repurposed Indication]**. Start with ‘Viable’ or ‘Non-Viable.’ Support your answer with a brief but rigorous explanation based on known mechanisms of action, pathway involvement, and biomedical literature. If available, cite sources*

---

### P6 – Chain-of-Thought Prompting

**Technique**: Guides the model through step-by-step reasoning  
**Template**:  
*“This drug repurposing case was identified by analyzing shared biological pathways. To determine if **[Drug Name]** can be repurposed for **[Repurposed Indication]**, follow these steps:*

*1. Identify the primary mechanism of action of **[Drug Name]**.*

*2. Examine whether this mechanism interacts with key pathological features of **[Repurposed Indication]**.*

*3. Consider existing biomedical literature or clinical trials supporting or refuting this repurposing case.*

*Now, provide your answer beginning with ‘Viable’ or ‘Non-Viable,’ followed by a brief step-by-step explanation and references if available.”*

---

### P7 – Self-Critique Prompting

**Technique**: Encourages model to assess its own response  
**Template**:  
*“This drug repurposing case was identified by analyzing shared biological pathways. Evaluate whether **[Drug Name]** can be repurposed for **[Repurposed Indication]**. First, provide a verdict (‘Viable’ or ‘Non-Viable’), followed by a brief explanation. Then, critically analyze your own reasoning and identify potential gaps, uncertainties, or missing evidence. If necessary, modify your initial response accordingly.”*

---

### P8 – Counterfactual Reasoning

**Technique**: Promotes critical evaluation  
**Template**:  
*“This drug repurposing case was identified by analyzing shared biological pathways. Consider the known effects of **[Drug Name]** and whether they align with treating **[Repurposed Indication]**. Compare this case to a similar, well-documented drug repurposing case.*

*- If similar mechanisms have led to successful repurposing in other cases, explain why this supports a ‘Viable’ verdict.*

*- If no similar cases exist, discuss why this suggests a ‘Non-Viable’ outcome.*

*Begin with ‘Viable’ or ‘Non-Viable,’ followed by a concise rationale and references if available.”*

---

### P9 – Literature Summarization Prompt

**Technique**: Emulates biomedical review  
**Template**:  
*“This drug repurposing case was identified by analyzing shared biological pathways. Use biomedical literature, such as PubMed and clinical trial data, to evaluate whether **[Drug Name]** can be repurposed for **[Repurposed Indication]**. Begin with ‘Viable’ or ‘Non-Viable,’ then summarize supporting or conflicting studies. If possible, include references to justify your verdict.””*

---

### P10 – Expert Persona Simulation

**Technique**: Roleplay as domain expert  
**Template**:  
*“You are an expert in pharmacology and biomedical research specializing in drug repurposing. This case was identified by analyzing shared biological pathways. Use your expertise to assess whether **[Drug Name]** can be used to treat **[Repurposed Indication]**. Analyze mechanisms of action, pathways, clinical evidence, and potential side effects.*
*Begin your response with ‘Viable’ or ‘Non-Viable,’ then provide a clear, well-reasoned justification based on current biomedical understanding. Include references if available.”*
