# Linguistically Informed NLP Evaluation

> Research project exploring how linguistic structure can improve the evaluation and interpretation of NLP systems.

---

## Overview

This project explores how linguistic structure can improve the evaluation of NLP systems.

Rather than focusing only on accuracy metrics, it investigates how models handle deeper linguistic phenomena such as negation, scope, and ambiguity. The goal is to move beyond surface-level evaluation and better understand where and why models succeed or fail.

---

## Key Themes

- Negation and scope
- Structure-aware NLP evaluation
- Linguistically informed benchmarking
- Ambiguity and interpretation
- Error analysis and interpretability
- Low-resource and multilingual NLP

---

## Why This Matters

Many NLP systems perform well on benchmark datasets but struggle with structurally complex language.

Phenomena such as negation, contrast, and ambiguity are often oversimplified in standard pipelines. This can lead to models that appear accurate while failing to capture deeper meaning.

This project asks:

- What kinds of linguistic errors do models make?
- How does syntactic structure influence predictions?
- Where do standard models succeed for shallow reasons?
- What can low-resource and underrepresented languages reveal about evaluation gaps?

---

## Focus Areas

- Negation (e.g. “not good”, “not surprisingly”)
- Scope and syntactic attachment
- Contrast structures (“X but Y”)
- Ambiguity and interpretation
- Insights from low-resource languages

---

## Case Study 1: Negation Stress Test for NLP

This case study examines how sentiment models handle negation and whether syntax-informed features provide additional insight.

### Goal

To compare a baseline sentiment model with a syntax-informed approach and analyze how different types of negation affect predictions.

---

## Method

Three experimental setups were compared.

### Baseline Model

Standard TF-IDF-based sentiment classification.

### Syntax-Informed Model

Feature-based approach incorporating linguistic cues such as:

- syntactic attachment of negation (VERB, AUX, etc.)
- local dependency context
- structural patterns such as `advmod`, `acomp`, and `amod`

### Hybrid Model

Combination of lexical and syntax-informed features.

---

## Results

| Model | Accuracy | F1 Score |
|---|---|---|
| Baseline TF-IDF | 0.8108 | 0.8224 |
| Syntax-only | 0.5745 | 0.6388 |
| Hybrid | 0.8073 | 0.8174 |

---

## Interpretation

The baseline model achieved the highest overall performance, while the syntax-only model underperformed as a standalone approach.

However, syntax-informed features proved valuable for interpretability and analysis. They help reveal how negation interacts with structure and highlight cases where models may succeed without truly capturing meaning.

---

## Example Analysis

```text
"The movie is not good"
→ clear polarity reversal

"The movie is not bad"
→ mildly positive or neutral interpretation

"Not surprisingly, the movie succeeded"
→ discourse-level negation rather than sentiment reversal
```

These distinctions show that negation is not uniform and cannot always be captured by surface-level features alone.

For detailed qualitative examples, see the `analysis/` directory.

---

## Key Takeaways

- Negation is structurally dependent, not simply lexical
- Surface-level models can perform well while missing deeper interpretation
- Syntax-informed features may not always improve accuracy directly, but they remain valuable for:
  - error analysis
  - interpretability
  - robustness evaluation
- Linguistic insight is especially important for multilingual and low-resource NLP

---

## Tools & Technologies

- Python
- spaCy
- Transformers (Hugging Face)
- pandas
- Jupyter Notebook

---

## Project Structure

```text
data/        - example sentences and test cases
notebooks/   - experiments and analyses
analysis/    - structured observations and error analysis
```

---

## Skills Demonstrated

- NLP preprocessing and feature engineering
- Syntax-aware linguistic analysis
- Model evaluation and comparison
- Qualitative error analysis
- Research-driven problem framing
- Clear technical communication

---

## Current Status

This project is under active development and will gradually expand to include:

- broader evaluation datasets
- multilingual examples
- targeted negation benchmarks
- qualitative error analyses
- structure-aware evaluation experiments

---

## Next Steps

- Expand evaluation to larger and more diverse datasets
- Develop more precise scope-aware negation features
- Extend analysis to multilingual and low-resource languages
- Build targeted evaluation benchmarks for structural phenomena

---

## Related Links

- [GitHub Pages Website](https://priscilla-adenuga.github.io/)
- [Low-Resource Languages as Stress Tests for NLP](https://github.com/priscilla-adenuga/low-resource-stress-tests-nlp)

---

## Author

**Priscilla Adenuga**  
PhD in Linguistics (Syntax)

Research interests:

- multilingual NLP
- structure-aware evaluation
- low-resource languages
- linguistic interpretation in NLP

---

## Contact

- [LinkedIn](https://www.linkedin.com/in/dr-priscilla-adenuga-b84529181/)
- [GitHub](https://github.com/priscilla-adenuga)

---

## License

MIT License
