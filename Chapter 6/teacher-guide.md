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

## 6. What distinguishes an instruction-tuned model from a base model?

- A. It has a larger context window
- B. It uses only parallel data
- **C. It has been trained to follow explicit instructions ✓**
- D. It always uses human feedback

**Brief explanation**

A base model is trained on large amounts of text to learn general linguistic patterns and predict the next token. An instruction-tuned model undergoes additional training using instruction–response pairs, that is, examples of instructions and their expected responses. The underlying mechanism remains next-token prediction, but the additional training makes the model better at staying on task, following specific requirements and adapting its responses to the requested style or structure. Human feedback can be used to further refine the model's behaviour, but it is not essential to instruction tuning.

**Suggestions for discussion**

- What differences might we observe when asking a base model and an instruction-tuned model to translate the same text?
- What is the difference between training a base model on more texts from a particular domain and training it on instruction–response pairs?
- How could parallel texts be used to construct instruction–response pairs for translation?
- If you wanted to instruction-tune a model for translation, what capabilities would be useful to translators beyond simply producing a translation? What kinds of instruction–response pairs would you include in the training data to develop these capabilities?
- How might the instruction–response pairs used to train a general-purpose model differ from those used to train a model tailored to the translation needs of a particular company or institution?

## 7. What is the context window?

- A. The maximum length of the output
- B. The model's training corpus
- C. Its memory of previous conversations
- **D. The maximum number of tokens it can process at one time ✓**

**Brief explanation**

The context window is the maximum number of tokens an LLM can take into account at any one time. In a translation task, this may include the translation instructions, the source text, any reference materials provided, previous exchanges in the conversation and the translation being generated. The size of the context window varies across models. However, models may also have a separate, considerably smaller limit on the number of tokens they can generate in a single response. This means that even if a model can process an entire source text, it may not be able to produce its complete translation in one go.

**Suggestions for discussion**

- Why might limitations on the length of the generated response be more problematic for translation than for tasks such as summarisation?
- What problems might arise when dividing a long source text into smaller sections and translating them separately?
- What advantages and limitations might there be to translating successive sections of a long document within the same conversation?

## 8. What does fine-tuning involve?

- A. Adding information to a prompt
- **B. Adjusting an LLM's internal parameters (weights) ✓**
- C. Changing the context window
- D. Retrieving external documents

**Brief explanation**

Fine-tuning involves further training an existing model on additional data, adjusting its internal parameters (weights) to improve its performance for particular tasks, domains or user requirements. For example, an LLM can be fine-tuned on a company's previous translations to better reproduce its preferred terminology, phraseology and style. Unlike prompting, which guides the model's responses without modifying its weights, fine-tuning changes the model itself.

**Suggestions for discussion**

- How are instruction tuning and fine-tuning related? What might be the purpose of further fine-tuning a model that has already been instruction-tuned for translation?
- What kinds of translation data would you need to fine-tune a model for a particular company or specialised domain?
- What would you expect a fine-tuned model to do better than a general-purpose model in this context?
- If a translator can provide terminology and stylistic preferences through a prompt, why might a company consider fine-tuning a model instead?

## 9. What is LoRA designed to make more efficient?

- A. Retrieval
- B. Tokenisation
- **C. Fine-tuning ✓**
- D. Prompt chaining

**Brief explanation**

Traditionally, fine-tuning has been computationally expensive because it involves adjusting a large number of the model's internal parameters. LoRA (Low-Rank Adaptation) is a technique that introduces a small number of additional trainable parameters while keeping the original model's weights unchanged. This reduces the computational resources needed for fine-tuning, making it more accessible to organisations wishing to adapt LLMs to their specific translation needs.

**Suggestions for discussion**

- Why might the computational cost of full fine-tuning be a barrier for translation companies or institutions, and what opportunities might techniques such as LoRA open up for them?
- What are the potential advantages and disadvantages of using LoRA rather than full fine-tuning? What factors might influence the choice between the two approaches?
- Apart from computational resources, what else would a translation company need to successfully fine-tune a model?

## 10. In few-shot prompting, the prompt contains...

- A. A larger context window
- **B. A small number of examples ✓**
- C. A modified set of model weights
- D. A set of external search results

**Brief explanation**

Few-shot prompting involves including a small number of examples (e.g. two, three or five) in the prompt to demonstrate the desired behaviour to the model. In translation, these might be source–target text pairs that illustrate the preferred terminology, style, register or formatting. While zero-shot prompting provides no examples and one-shot prompting provides a single example, few-shot prompting provides several examples to guide the model's response. This does not involve further training or changes to the model's internal parameters.

**Suggestions for discussion**

- In what translation scenarios might few-shot prompting be particularly useful?
- What criteria would you use to select suitable examples for a few-shot translation prompt?
- Does including more examples necessarily lead to better translation quality? What factors might influence this?
- Could examples of target-language texts alone, without their corresponding source texts, also be useful? Why?

---

[Back to Chapter 6](README.md) | [Multiple-choice questions](questions.md)
