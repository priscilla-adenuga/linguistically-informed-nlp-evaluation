# Error Analysis: Negation in NLP

This document provides qualitative examples illustrating how different types of negation are interpreted in sentiment classification.

The goal is to highlight where models succeed, fail, or oversimplify linguistic structure.

---

## 1. Simple Polarity Reversal

**Sentence:**  
"The movie is not good."

**Expected interpretation:** Negative  

**Observation:**  
This is a straightforward case where negation directly reverses polarity. Most models handle this correctly because the structure is simple and aligns with common patterns in training data.

---

## 2. Implicit Positive via Negation

**Sentence:**  
"The movie is not bad."

**Expected interpretation:** Slightly positive  

**Observation:**  
Although the sentence contains negation, it is not truly negative. Many models misclassify this as negative because they rely on surface cues ("not" + "bad") rather than interpreting the pragmatic meaning.

---

## 3. Discourse-Level Negation

**Sentence:**  
"Not surprisingly, the movie succeeded."

**Expected interpretation:** Positive / neutral  

**Observation:**  
The negation does not affect sentiment but functions at the discourse level. Models may incorrectly treat "not" as reversing sentiment, demonstrating lack of structural awareness.

---

## 4. Negation with Auxiliary Verb

**Sentence:**  
"The movie did not impress me."

**Expected interpretation:** Negative  

**Observation:**  
Negation attaches to the verb phrase via an auxiliary. Models generally perform well here, but performance may degrade if the structure becomes more complex.

---

## 5. Negation with Contrast Structure

**Sentence:**  
"The movie is not perfect, but it is enjoyable."

**Expected interpretation:** Positive overall  

**Observation:**  
Contrast structures (X but Y) shift emphasis to the second clause. Models often struggle with this and may overemphasize the first clause.

---

## 6. Double Negation (Non-standard or Emphatic)

**Sentence:**  
"I can't say it's not good."

**Expected interpretation:** Positive  

**Observation:**  
This construction is structurally complex. Models frequently fail because interpretation requires understanding layered negation rather than simple polarity flipping.

---

## 7. Negation Scope Ambiguity

**Sentence:**  
"I do not think the movie is good."

**Expected interpretation:** Negative  

**Observation:**  
The negation applies to the thinking process, not directly to "good". Models may misinterpret scope and assign incorrect sentiment.

---

## 8. Adverbial Negation with Emphasis

**Sentence:**  
"The movie is really not that good."

**Expected interpretation:** Negative  

**Observation:**  
Modifiers like "really" and "that" interact with negation and intensity. Models may ignore these interactions and treat the sentence too simplistically.

---

## Key Insight

These examples demonstrate that negation is not a uniform phenomenon. Its interpretation depends on:

- syntactic attachment
- scope
- discourse function
- interaction with other elements (e.g. contrast, intensifiers)

This highlights the importance of linguistically informed evaluation in NLP systems.
