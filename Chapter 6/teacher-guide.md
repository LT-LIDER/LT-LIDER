# Teacher guide

The questions and accompanying explanations are based on Chapter 6, *Key Concepts in Large Language Models for Translation*. They are intended as examples for concept review and discussion rather than as a comprehensive assessment. Teachers are encouraged to select, modify, expand or omit questions and discussion suggestions according to their teaching objectives and the needs of their learners.

## 1. At their core, how do LLMs generate language?

- A. Retrieve stored sentences
- **B. Predict the next most probable token ✓**
- C. Identify the speaker's intention
- D. Translate an internal representation

**Brief explanation**

LLMs generate language by predicting the next most probable token given the preceding context. They learn statistical patterns and associations between words and phrases from large amounts of training data, rather than storing sentences to retrieve later. They do not understand language in a human sense, nor do they possess consciousness, intentions or awareness of communicative goals.

**Suggestions for discussion**

- If LLMs simply predict the next token, how can they produce translations, summaries or other specific types of text? What distinction can we make between what the model actually does and how we interpret its output?

## 2. From a translation perspective, LLM training data is typically…

- A. Monolingual and parallel
- B. Exclusively bilingual
- **C. Multilingual but not parallel ✓**
- D. Aligned source–target sentence pairs

**Brief explanation**

LLMs are initially trained on large collections of texts in many languages. These datasets are multilingual, but the texts are not systematically aligned as source–target pairs. This differs from traditional neural machine translation (NMT) systems, which are typically trained on parallel data: texts and their translations aligned at sentence or document level. LLM training datasets may incidentally contain original texts and their translations, but these are not deliberately collected and aligned for translation training.

**Suggestions for discussion**

- Why does the distinction between *multilingual* and *parallel* training data matter?
- What does it tell us about the differences between LLMs and traditional NMT systems?
- If LLMs are not primarily trained on parallel texts, how might they learn to translate?

## 3. Why can translation quality vary significantly across language pairs?

- A. Languages use different architectures
- **B. Languages are unevenly represented in training data ✓**
- C. Each language has its own LLM
- D. LLMs identify some languages incorrectly

**Brief explanation**

LLM training datasets contain very different amounts of text in different languages. English is particularly well represented and generally benefits from stronger model performance. For languages with limited representation, the model has encountered fewer examples of how the language is used in different contexts, and some words, expressions, grammatical structures or types of text may be poorly represented or absent altogether. As a result, it may learn linguistic patterns less reliably, contributing to differences in translation quality across language pairs.

**Suggestions for discussion**

- What precautions might translators take when working with an under-resourced language?
- Does a model's ability to produce fluent text in a language necessarily mean it can translate accurately into or out of that language?
- If an LLM performs particularly well for one language pair, does that mean it will also be the best choice for other language pairs? Why or why not?

## 4. What are embeddings?

- A. Sets of translation rules
- **B. Numerical vectors representing associations between tokens ✓**
- C. Collections of parallel sentences
- D. Instructions stored in the context window

**Brief explanation**

To process language mathematically, LLMs transform tokens into numerical representations called embeddings. These can be imagined as coordinates on a multidimensional map, where tokens with strong associations are located close together and those with weak associations are further apart. These associations are learned from training data. Importantly, tokens from different languages are represented in a shared space rather than in separate spaces for each language.

**Suggestions for discussion**

- If words with similar meanings in different languages are located close together in the same embedding space, how might this help explain the model's ability to translate without being explicitly trained on parallel data?
- Why might embeddings be less reliable for languages poorly represented in training data?
- If embeddings capture associations between words based on their use in texts, what aspects of meaning might they struggle to capture, such as cultural references, irony or pragmatic nuances?

## 5. What does self-attention allow a transformer to do?

- A. Identify the language of each token
- B. Retrieve similar texts
- **C. Weight important contextual relationships ✓**
- D. Translate all tokens simultaneously

**Brief explanation**

The meaning of a word often depends on the other words in the text. Self-attention allows the model to determine which other tokens are more relevant to a particular token and give them greater influence on how that token is represented. This is what is meant by assigning different weights. For example, when processing the word "bank", words such as "money" or "account" may have a greater influence than other words in the text, helping the model associate "bank" with a financial institution. Self-attention can also capture relationships between tokens that are far apart in the text.

**Suggestions for discussion**

- Why might relationships between distant words matter when processing or translating a long sentence? Can you think of examples involving grammatical agreement or pronoun reference?
- Can you think of other examples where the interpretation of a word depends on its context?

---

[Back to Chapter 6](README.md) | [Multiple-choice questions](questions.md)
