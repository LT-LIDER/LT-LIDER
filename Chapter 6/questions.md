# Multiple-choice questions

These questions are based on Chapter 6, *Key Concepts in Large Language Models for Translation*. They are intended to review selected concepts and encourage classroom discussion.

## 1. At their core, how do LLMs generate language?

- A. Retrieve stored sentences
- B. Predict the next most probable token
- C. Identify the speaker's intention
- D. Translate an internal representation

## 2. From a translation perspective, LLM training data is typically…

- A. Monolingual and parallel
- B. Exclusively bilingual
- C. Multilingual but not parallel
- D. Aligned source–target sentence pairs

## 3. Why can translation quality vary significantly across language pairs?

- A. Languages use different architectures
- B. Languages are unevenly represented in training data
- C. Each language has its own LLM
- D. LLMs identify some languages incorrectly

## 4. What are embeddings?

- A. Sets of translation rules
- B. Numerical vectors representing associations between tokens
- C. Collections of parallel sentences
- D. Instructions stored in the context window

## 5. What does self-attention allow a transformer to do?

- A. Identify the language of each token
- B. Retrieve similar texts
- C. Weight important contextual relationships
- D. Translate all tokens simultaneously

## 6. What distinguishes an instruction-tuned model from a base model?

- A. It has a larger context window
- B. It uses only parallel data
- C. It has been trained to follow explicit instructions
- D. It always uses human feedback

## 7. What is the context window?

- A. The maximum length of the output
- B. The model's training corpus
- C. Its memory of previous conversations
- D. The maximum number of tokens it can process at one time

## 8. What does fine-tuning involve?

- A. Adding information to a prompt
- B. Adjusting an LLM's internal parameters (weights)
- C. Changing the context window
- D. Retrieving external documents

## 9. What is LoRA designed to make more efficient?

- A. Retrieval
- B. Tokenisation
- C. Fine-tuning
- D. Prompt chaining

## 10. In few-shot prompting, the prompt contains...

- A. A larger context window
- B. A small number of examples
- C. A modified set of model weights
- D. A set of external search results

## 11. Prompt chaining means...

- A. Asking for reasoning in one prompt
- B. Breaking a task into sequential subtasks
- C. Providing source-target examples
- D. Generating several translations simultaneously

## 12. How does Chain-of-Thought differ from prompt chaining?

- A. It requires fine-tuning
- B. It retrieves external knowledge
- C. It takes place within a single extended prompt
- D. It always uses several models

## 13. What does RAG enable the model to do at translation time?

- A. Retrain itself
- B. Increase its context window
- C. Consult external sources of information
- D. Change its architecture

## 14. What does temperature control?

- A. Context-window size
- B. Repetition
- C. Output length
- D. Randomness of the response

## 15. Why may repetition penalties be unsuitable for technical translation?

- A. They make output too short
- B. They reduce the context window
- C. Terminological repetition may be necessary
- D. They prevent specialised vocabulary

## 16. In "Step-by-step translation as a multi-turn LLM workflow", which sequence is used?

- A. Translate → retrieve → fine-tune → evaluate
- B. Research → drafting → refinement → proofreading
- C. Analyse → prompt → retrieve → translate
- D. Draft → backtranslate → score → publish

## 17. What distinguishes an LLM agent from a standalone language model?

- A. It is necessarily multilingual
- B. It has more parameters
- C. It can plan steps and use tools, memory and resources
- D. It does not need instructions

## 18. Compared with LLMs, NMT systems are typically trained on...

- A. Larger amounts of monolingual text
- B. Large volumes of parallel source-target data
- C. Instruction-response pairs
- D. Retrieved translation memories

## 19. What is the typical architectural contrast between NMT systems and LLMs?

- A. NMT is decoder-only; LLMs are encoder-only
- B. Both are normally encoder-decoder
- C. NMT is encoder-decoder; LLMs are usually decoder-only
- D. NMT uses transformers; LLMs do not

## 20. What can Language Modelling Bias lead LLMs to prioritise?

- A. Terminological consistency over style
- B. Source structure over readability
- C. Adequacy over fluency
- D. Fluency and plausibility over adequacy
  
---

[Back to Chapter 6](README.md)
