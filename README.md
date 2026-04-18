# Linguistically Informed NLP Evaluation

## Overview
This project explores how linguistic structure can improve the evaluation of NLP systems.

Rather than focusing only on accuracy metrics, it investigates how models handle deeper linguistic phenomena such as negation, scope, and ambiguity.

## Motivation
Many NLP systems perform well on benchmark datasets but fail on structurally complex language.

This project asks:
- What kinds of linguistic errors do models make?
- How does structure influence model predictions?
- What can low-resource languages reveal about evaluation gaps?

## Focus Areas
- Negation (e.g. "not good", "not surprisingly")
- Scope and attachment
- Contrast structures ("X but Y")
- Ambiguity and interpretation
- Low-resource language insights

## Approach
- Construct linguistically controlled examples
- Compare model predictions
- Analyze errors qualitatively

## Tools
- Python
- spaCy
- Transformers (HuggingFace)
- pandas

## Project Structure
data/        # example sentences and test cases
notebooks/   # experiments and analysis
analysis/    # structured observations
## First Experiment (Planned)
A small experiment comparing how models interpret:
- "The movie is not good"
- "The movie is not bad"
- "Not surprisingly, the movie succeeded"

## Goal
To build a linguistically grounded perspective on NLP evaluation, especially for underrepresented and structurally rich languages.

## Author
Priscilla Adenuga
PhD Linguistics | NLP
