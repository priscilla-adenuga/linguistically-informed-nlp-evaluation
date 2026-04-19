# Linguistically Informed NLP Evaluation

## Overview
This project explores how linguistic structure can improve the evaluation of NLP systems.

Rather than focusing only on accuracy metrics, it investigates how models handle deeper linguistic phenomena such as negation, scope, and ambiguity. The goal is to move beyond surface-level evaluation and better understand where and why models succeed or fail.

---

## Why this matters

Many NLP systems perform well on benchmark datasets but struggle with structurally complex language.

Phenomena such as negation, contrast, and ambiguity are often oversimplified in standard pipelines. This can lead to models that appear accurate but fail to capture deeper meaning.

This project focuses on **evaluation through a linguistic lens**, asking:

- What kinds of linguistic errors do models make?
- How does syntactic structure influence predictions?
- Where do standard models succeed for shallow reasons?
- What can low-resource and underrepresented languages reveal about evaluation gaps?

---

## Focus Areas

- Negation (e.g. *"not good"*, *"not surprisingly"*)
- Scope and syntactic attachment
- Contrast structures (*"X but Y"*)
- Ambiguity and interpretation
- Insights from low-resource languages

---

## Case Study 1: Negation Stress Test for NLP

This case study examines how sentiment models handle negation and whether syntax-informed features provide additional insight.

### Goal
To compare a baseline sentiment model with a syntax-informed approach and analyze how different types of negation affect predictions.

---

## Method

Three setups were compared:

1. **Baseline model**  
   Standard TF-IDF-based sentiment classification.

2. **Syntax-informed model**  
   Feature-based approach incorporating linguistic cues such as:
   - syntactic attachment of negation (VERB, AUX, etc.)
   - local dependency context
   - structural patterns (e.g. `advmod`, `acomp`, `amod`)

3. **Hybrid model**  
   Combination of lexical and syntax-informed features.

---

## Results

| Model | Accuracy | F1 Score |
|------|----------|----------|
| Baseline TF-IDF | 0.8108 | 0.8224 |
| Syntax-only | 0.5745 | 0.6388 |
| Hybrid | 0.8073 | 0.8174 |

### Interpretation

The baseline model achieved the highest overall performance, while the syntax-only model underperformed as a standalone approach.

However, syntax-informed features proved valuable for **interpretability and analysis**. They help reveal how negation interacts with structure and highlight cases where models may succeed without truly capturing meaning.

---

## Example Analysis

The following examples illustrate different types of negation:

- **"The movie is not good"** → clear polarity reversal  
- **"The movie is not bad"** → not strictly negative; often interpreted as mildly positive  
- **"Not surprisingly, the movie succeeded"** → discourse-level negation, not sentiment reversal  

These distinctions show that negation is not uniform and cannot always be captured by surface-level features alone.

For detailed qualitative examples, see [Error Analysis](analysis/error_analysis.md)

---

## Key Takeaways

- Negation is structurally dependent, not just lexical.
- Surface-level models can perform well while missing deeper interpretation.
- Syntax-informed features may not always improve accuracy directly, but they are valuable for:
  - error analysis
  - interpretability
  - robustness evaluation
- Linguistic insight is especially important for multilingual and low-resource NLP.

---

## Tools & Technologies

- Python  
- spaCy  
- Transformers (Hugging Face)  
- pandas  

---

## Project Structure
```text
data/        # example sentences and test cases
notebooks/   # experiments and analysis
analysis/    # structured observations and error analysis

---

## Skills Demonstrated

- NLP preprocessing and feature engineering  
- Syntax-aware linguistic analysis  
- Model evaluation and comparison  
- Qualitative error analysis  
- Research-driven problem framing  
- Clear technical communication  

---

## Next Steps

- Expand evaluation to larger and more diverse datasets  
- Develop more precise scope-aware negation features  
- Extend analysis to multilingual and low-resource languages  
- Build targeted evaluation benchmarks for structural phenomena  

---

## Author

**Priscilla Adenuga**  
PhD in Linguistics (Syntax)  
Transitioning into NLP & AI  
Focus: Multilingual NLP, evaluation, and low-resource languages
