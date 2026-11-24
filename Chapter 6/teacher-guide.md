# Teacher guide

The questions and accompanying explanations are based on Chapter 6, *Key Concepts in Large Language Models for Translation*. They are intended as examples for concept review and discussion rather than as a comprehensive assessment. Teachers are encouraged to select, modify, expand or omit questions and discussion suggestions according to their teaching objectives and the needs of their learners.

## 1. At their core, how do LLMs generate language?

- A. Retrieve stored sentences
- **B. Predict the next most probable token ✓**
- C. Identify the speaker's intention
- D. Translate an internal representation

**Brief explanation**

LLMs generate language by predicting the next token given the preceding context. More precisely, they predict a probability distribution over possible next tokens and select one according to the decoding parameters. They learn statistical patterns and associations between words and phrases from large amounts of training data, rather than storing sentences to retrieve later. They do not understand language in a human sense, nor do they possess consciousness, intentions or awareness of communicative goals.

**Suggestions for discussion**

- If LLMs simply predict the next token, how can they produce translations, summaries or other specific types of text? What distinction can we make between what the model actually does and how we interpret its output?

## 2. From a translation perspective, LLM training data is typically…

- A. Monolingual and parallel
- B. Exclusively bilingual
- **C. Multilingual but not parallel ✓**
- D. Aligned source–target sentence pairs

**Brief explanation**

LLMs are initially trained on large collections of texts in many languages. These datasets are multilingual, but the texts are not systematically aligned as source–target pairs. This differs from traditional neural machine translation (NMT) systems, which are typically trained on parallel data: texts and their translations aligned at sentence or document level. LLM training datasets may incidentally contain original texts and their translations, but these are not necessarily deliberately collected and aligned for translation training.

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

## 11. Prompt chaining means...

- A. Asking for reasoning in one prompt
- **B. Breaking a task into sequential subtasks ✓**
- C. Providing source-target examples
- D. Generating several translations simultaneously

**Brief explanation**

Prompt chaining involves breaking a complex task into smaller subtasks, each addressed through a separate prompt. The output of one prompt is used as input for the next, forming a chain. In translation, rather than asking the model to produce a finished translation directly, we might first ask it to analyse the source text, then identify and resolve terminological difficulties, draft the translation and finally revise it. Breaking the task into smaller, more manageable steps reduces its complexity and allows us to guide the model more explicitly, directing its attention towards specific aspects of the translation that may require particular care.

**Suggestions for discussion**

- What stages of a professional translation workflow could be addressed through separate prompts?
- What are the potential advantages and disadvantages of chaining requests rather than including all the requests in a single prompt?

## 12. How does Chain-of-Thought differ from prompt chaining?

- A. It requires fine-tuning
- B. It retrieves external knowledge
- **C. It takes place within a single extended prompt ✓**
- D. It always uses several models

**Brief explanation**

Both Chain-of-Thought (CoT) prompting and prompt chaining help models tackle complex tasks step by step. However, while prompt chaining splits work across multiple successive prompts, CoT prompts the model to explicitly generate intermediate analytical steps before producing a final answer within a single interaction. These analytical steps do not necessarily reflect the model's internal reasoning processes. They are additional generated text that, by becoming part of the immediate context, can guide the model towards a more accurate final response. In translation, for example, you might instruct the model to first list possible interpretations of an ambiguous expression, explain how the surrounding context resolves it, and justify its word choice before providing the final translation.

**Suggestions for discussion**

- Does a convincing explanation of a translation choice necessarily mean that the translation is correct? Conversely, can an inaccurate explanation be accompanied by a correct translation?
- What types of translation difficulties might particularly benefit from Chain-of-Thought prompting? Can you think of specific examples?

## 13. What does RAG enable the model to do at translation time?

- A. Retrain itself
- B. Increase its context window
- **C. Consult external sources of information ✓**
- D. Change its architecture

**Brief explanation**

Retrieval-Augmented Generation (RAG) is a mechanism that allows us to make external resources available to an LLM when generating a response. In translation, these resources might include glossaries, translation memories, style guides or specialised documents. When a translation is requested, relevant information is automatically retrieved from these resources and added to the prompt. This enables the model to draw on additional knowledge without requiring further training or changes to its internal parameters.

**Suggestions for discussion**

- How does using RAG differ from manually including reference materials in a prompt?
- What advantages might RAG offer over fine-tuning a model for a particular company or specialised domain?
- What similarities and differences can you identify between a human translator working with a CAT tool and an LLM using RAG?

## 14. What does temperature control?

- A. Context-window size
- B. Repetition
- C. Output length
- **D. Randomness of the response ✓**

**Brief explanation**

Temperature is a parameter that influences the randomness of the model's output by adjusting the probability distribution of potential next tokens. A lower temperature increases the relative probability of the most likely tokens, resulting in more predictable responses. A higher temperature makes the probability distribution more uniform, increasing the chances of selecting less probable tokens and potentially producing more varied responses.

**Suggestions for discussion**

- What types of translation assignments might benefit from a lower or higher temperature setting?
- Does greater variation in the model's output necessarily imply greater creativity or better translation quality?
- If we translate the same source text several times using the same prompt and temperature setting, can we expect to obtain identical translations?

## 15. Why may repetition penalties be unsuitable for technical translation?

- A. They make output too short
- B. They reduce the context window
- **C. Terminological repetition may be necessary ✓**
- D. They prevent specialised vocabulary

**Brief explanation**

Frequency and presence penalties are parameters that discourage the model from selecting tokens that have already appeared in the generated text. The frequency penalty increases with the number of previous occurrences, whereas the presence penalty applies the same penalty regardless of how often a token has appeared. Although these parameters can encourage lexical variety, they may be counterproductive in technical or legal translation, where consistent terminology and phraseology are often essential.

**Suggestions for discussion**

- In what types of translation assignments might repetition penalties be beneficial or detrimental, and why? Can you think of specific examples?

## 16. In "Step-by-step translation as a multi-turn LLM workflow", which sequence is used?

- A. Translate → retrieve → fine-tune → evaluate
- **B. Research → drafting → refinement → proofreading ✓**
- C. Analyse → prompt → retrieve → translate
- D. Draft → backtranslate → score → publish

**Brief explanation**

The sequence of research, drafting, refinement and proofreading corresponds to a particular implementation of a multi-turn LLM translation workflow described in the chapter. Each stage has a specific purpose: research identifies potential translation difficulties; drafting focuses on accurately conveying the source text's meaning; refinement improves fluency, readability, tone and register; and proofreading involves a final review of the translation. In this implementation, the proofreading stage takes place in a separate conversation. This is just one example of how a translation workflow can be structured. Other workflows can be designed depending on the characteristics of the source text, the translation requirements and the needs of the translator.

**Suggestions for discussion**

- How closely does this sequence reflect your own translation workflow? Would you add, modify or omit any stages?

## 17. What distinguishes an LLM agent from a standalone language model?

- A. It is necessarily multilingual
- B. It has more parameters
- **C. It can plan steps and use tools, memory and resources ✓**
- D. It does not need instructions

**Brief explanation**

An LLM agent is a system built around a language model that can take actions to achieve an assigned objective with a greater degree of autonomy. When designing an agent, we define its role, provide instructions, equip it with tools and resources, and establish the constraints within which it can operate. Rather than programming every step of the process in advance, we allow the LLM to determine which actions to take, when to use the available tools, and how to proceed based on intermediate results.

**Suggestions for discussion**

- To what extent would you allow LLM agents to make decisions autonomously in a translation project? Which decisions would you want to retain control over?
- What ethical issues might arise when delegating tasks and decisions to LLM agents in a professional translation setting? Who should be held accountable for the consequences of their actions?

## 18. Compared with LLMs, NMT systems are typically trained on...

- A. Larger amounts of monolingual text
- **B. Large volumes of parallel source-target data ✓**
- C. Instruction-response pairs
- D. Retrieved translation memories

**Brief explanation**

Traditional neural machine translation (NMT) systems are specifically trained for translation using large volumes of parallel data, often comprising millions of aligned source–target sentence pairs. Although monolingual data can also be exploited in NMT training, parallel data has traditionally played a central role. By learning from explicit translation examples, NMT systems acquire translation patterns and tend to remain closely anchored to the source text. LLMs, by contrast, are primarily trained on large amounts of multilingual but not necessarily parallel data. This difference in training data contributes to what Hendy et al. (2023) call *Parallel Data Bias*: LLMs may produce fluent translations that are less faithful to the source text.

**Suggestions for discussion**

- How might the availability of parallel data and monolingual data for a particular language pair influence the choice between an NMT system and an LLM?
- What types of translation errors might be associated with the differences in training data between NMT systems and LLMs?
- What advantages might training on large amounts of monolingual data offer for translation between languages that are individually well represented in digital texts but for which little parallel data is available? Can you think of specific language pairs where this might be the case?

## 19. What is the typical architectural contrast between NMT systems and LLMs?

- A. NMT is decoder-only; LLMs are encoder-only
- B. Both are normally encoder-decoder
- **C. NMT is encoder-decoder; LLMs are usually decoder-only ✓**
- D. NMT uses transformers; LLMs do not

**Brief explanation**

Traditional NMT systems typically use an encoder–decoder architecture. The encoder creates a contextual representation of the source text, which the decoder draws on throughout the generation of the translation. Most contemporary generative LLMs, by contrast, use a decoder-only architecture, in which the instructions, source text and other contextual information form part of a sequence that the model continues by predicting successive tokens. Both architectures can be implemented using transformers.

**Suggestions for discussion**

- How might having a dedicated encoder for the source text influence the fidelity of the resulting translation?
- What advantages might the versatility of decoder-only LLMs offer translators beyond the generation of a translation?

## 20. What can Language Modelling Bias lead LLMs to prioritise?

- A. Terminological consistency over style
- B. Source structure over readability
- C. Adequacy over fluency
- **D. Fluency and plausibility over adequacy ✓**

**Brief explanation**

LLMs are fundamentally trained to predict the next token and generate linguistically plausible text. However, in translation, producing a fluent and plausible target text does not necessarily mean accurately conveying the meaning of the source text. The tendency to prioritise fluency and plausibility over adequacy is referred to by Hendy et al. (2023) as *Language Modelling Bias*. It may manifest itself in translations that read naturally but contain omissions, unjustified additions or changes to the meaning of the source text.

**Suggestions for discussion**

- What implications might Language Modelling Bias have for the way translators review LLM-generated translations?
- How might we design translation prompts to mitigate this bias?

---

[Back to Chapter 6](README.md) | [Multiple-choice questions](questions.md)
