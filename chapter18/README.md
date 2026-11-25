# Chapter 18

**Capsule: Your Own Private LLM**

Authors and affiliations: Antonio Toral¹, Andreas van Cranenburgh², Miquel Esplà-Gomis¹, Ana Guerberof-Arenas². ¹Universitat d'Alacant, ²University of Groningen.

Expected study time: 4 hours

Language of instruction: English

## Learning Outcomes (LT-LiDER skill(s) map)

By the end of this exercise you will be able to:

- Know the difference between desktop & cloud tools
- Know LLM limitations and capabilities
- Use APIs
- Use multilingual prompts to create multilingual content

## Scenarios 

This training capsule covers three activities related to using a private Large Language Model (LLM) on your own computer. First, you will get started with setting up a local LLM and interacting with it using a GUI. Second, you will explore additional settings when running a local LLM. Lastly, you will explore two ways to customize a local LLM programmatically in Python.


## Related LT-LiDER Book Chapters

This capsule complements Chapter 18 of the LT-LiDER book, entitled "How can translators use and customise their own private Large Language Models?".

To complete this casule, in addition to Chapter 18, you may find  Chapter 6 (Key Concepts in Large Language Models for Translation), Chapter 12 (Best practices for prompting: how can translation students, trainers and professionals make the most out of LLMs?) and Chapter 15 (Bridging the digital divide: Making Python and the Python ecosystem accessible to translators) useful.

## Activity pre-requisites

- Reading of Chapter 18
- Reading of Chapter 12 (only for activity 2)
- Reading of Chapter 15 (only for activity 3)
- Basic Python programming experience (only for activity 3)
- Hardware: a laptop or desktop computer with at least 8 GB of RAM and 10 GB of free storage space. *(Note for Mac users: Current versions of the GUI used, Jan (0.8.5 onwards), require an Apple Silicon Mac (M1, M2, M3, or M4) to run models locally.)*

## Overview

This capsule contains three activities.

### Activity 1: Setting Up and Testing Your Private Local LLM

For this activity we will be using Jan, an open-source alternative to ChatGPT and the like, that allows you to run LLMs on your own computer.

**Learning Goal:** install Jan, select an open-weight LLM suited to your computer's hardware, and critically evaluate its speed, translation quality, and privacy trade-offs compared to cloud-based AI tools.

**Estimated Time:** 1 hour.

---

#### Step 1: Install Jan
1. Go to the official [Jan website](https://www.jan.ai/) and download the installer for your operating system (Windows, macOS, or Linux).
2. Open the downloaded file and install Jan just like any standard application. 
3. Launch Jan. You do **not** need to create an account, log in, or enter a credit card to use Jan nor any local LLM.

#### Step 2: Choose and Download a Local Model
To run an LLM offline, you first need to download the model's file(s) onto your computer.

1. Open the **Hub** tab in Jan's menu to browse available models.

2. **Check hardware compatibility:** You need to make sure that the LLM you will download is compatible with your computer. You do not need to calculate technical hardware specs manually. Look for Jan's built-in compatibility indicator (such as a green **"Fits"** label) and check the file size before downloading. Use the guide below (and Section 4.2 of this chapter, which has more detailed information) to pick an appropriate model:

| Your Computer Type | Recommended Model Size | Recommended Quantization |
| :--- | :--- | :--- |
| **Standard Laptop** (8–16 GB RAM, no dedicated graphics card) | **2B – 8B** (2 to 8 billion parameters) | **Q4** (e.g., `Q4_K_M`) | 
| **High-Performance Laptop or Desktop** (16+ GB RAM and/or dedicated GPU) | **8B – 14B+** | **Q4, Q6, or Q8** |

3. **Select an LLM:** Look for well-known open-weight model families that perform well across languages (for example, *Qwen*, *Gemma*, *Llama*, or *Mistral* variants). You might also check any online LLM leaderboard to get a grasp of the performance on an LLM, or to compare two LLMs against each other. Finally, make sure you download a **local** model directly onto your computer rather than connecting to a cloud provider (which requires an external API key).

4. Click **Download** and wait for the file to finish saving to your computer.

> **Writing Task. Document Your Choice.**
> Write down the exact name of the LLM you downloaded, its parameter size (e.g., 4B or 8B), and its quantization level (e.g., Q4_K_M). In 2–3 sentences, explain why you chose this specific LLM based on your computer's capabilities and on the information you have found about the LLM.

#### Step 3: Verify Offline Privacy and Test Translation Tasks
1. Open a **New Chat** in Jan. You should see a message like "Hi, how are you? How can I help you today?" under which there's a text box where you can interact with the LLM. At the bottom of the text box you can select the LLM to be used, so be sure to select the one that you have downloaded in the previous step.

2. **Test offline privacy**. Turn off your computer's Wi-Fi (or enable airplane mode). Because the model now lives on your hard drive, Jan will continue working without an internet connection, guaranteeing that your text never leaves your device.

3. **Interact with the LLM**. Do so for at least a couple of rounds, for the kind of tasks you normally use online LLMs for. Try asking the LLM in an incremental order of complexity.

> **Writing Task. Explain Your Experience.**
Write down a 250-300 word critical reflection evaluating your experience. Mention:
> - **Speed and Hardware Behaviour.** Look at the generation speed (`tokens/sec`) reported at the bottom of Jan's responses. How fast did the text appear, and did your computer's fans spin up or slow down?
> - **Output Quality.** How was the quality of the responses, compared to the LLM(s) you normally use online? Where did the local model struggle?
> - **The Privacy vs. Quality Trade-Off.** Even if a small local LLM has worse output or is slower than a massive cloud model, in which real-world scenarios would you choose the local model anyway?
>- **Professional Autonomy.** How does running an AI tool completely offline affect your view of data sovereignty and reliance on commercial tech platforms?

---

### Activity 2: More Settings for your Local Private LLM

**Learning Goal:** move beyond default chat settings by configuring custom system instructions, adjusting sampling parameters (Temperature and Repeat Penalty) and managing hardware resources (Context Size and GPU acceleration).

**Estimated Time:** 1 hour

**Prerequisites:** completion of activity 1 (Jan installed with at least one LLM downloaded).

#### Step 1: Create a Specialized Translator Persona (System Instructions)

By default, an LLM behaves like a general-purpose assistant. In a professional workflow, you might want to guide its behaviour globally using a **System Prompt** (or by creating a custom **Assistant** in Jan) so that style rules and terminology apply automatically to every message.

1. In Jan, open **Settings > Assistants** via the settings icon on the left panel.

2. Create a new assistant named **"Technical & Legal Translator"** and paste the following instructions into the **System Prompt** box (adapting the language pair and glossary to your working languages):

   > *You are a senior professional translator translating from English into [Target Language]. Maintain a formal, objective institutional register. Output ONLY the translation without conversational filler or explanations. Strictly follow this glossary: "cloud deployment" = [approved term 1]; "data sovereignty" = [approved term 2]; "open-weight model" = [approved term 3].*

3. Start a new chat using this assistant and test it with a 3-sentence paragraph containing at least two of your glossary terms. Verify whether the model obeys both the formatting constraint ("only the translation") and your mandatory terminology.

#### Step 2: Test Precision vs. Creativity (Temperature and Repeat Penalty)

Behind the scenes, an LLM generates text one token (i.e. a word or a word-piece) at a time by calculating probabilities for what comes next. You can control how predictable or creative those choices are without writing any code:

1. Click the **gear icon** next to your selected LLM in the chat interface to open the **Model Settings** panel.

2. Locate the following two controls:

   * **Temperature:** controls randomness. Low values (`0.1–0.2`) force the model to pick the most statistically probable, consistent words. High values (e.g. `1.6–2.0`) encourage more varied, expressive phrasing. The range of possible values depend on the LLM.

   * **Repeat Penalty:** discourages the model from repeating words or getting stuck in loops (`1.0` = off; `1.1–1.2` = mild protection against repetition).

3. **Run a Controlled A/B Comparison.** Start a fresh chat for each test below and translate two short  texts: **Text A** (a strict contractual or technical sentence) and **Text B** (a playful advertising slogan or culturally specific idiom). Translate each text under three different parameter setups:

| Test Run | Parameter Settings | Text A (Legal/Technical) Output & Notes | Text B (Marketing/Idiom) Output & Notes | 
| ----- | ----- | ----- | ----- | 
| **Run 1: Strict Mode** | **Temperature:** `0.1`<br>**Repeat Penalty:** `1.0` | *Record accuracy, terminology adherence, and literalness* | *Record whether the slogan sounds stiff or overly literal* | 
| **Run 2: Creative Mode** | **Temperature:** `0.9`<br>**Repeat Penalty:** `1.1` | *Check for unwanted paraphrasing or invented details* | *Record whether phrasing is more natural and idiomatic* | 
| **Run 3: Over-Penalized** | **Temperature:** `0.7`<br>**Repeat Penalty:** `1.4` | *Observe whether high repeat penalty forces awkward synonyms* | *Observe any grammatical distortion or unnatural word choices* | 

#### Step 3: Manage "Working Memory" and Hardware Speed (Context Size & GPU)

Translators rarely translate isolated sentences; they often paste multi-paragraph documents alongside style guides or reference texts.

1. Open **Settings > Hardware** (via the settings icon on the left panel) to view your computer's live **CPU, RAM, and GPU** usage.

2. Return to your chat's **Model Settings** (gear icon) and inspect two performance controls:

   * **Context Size (Context Length)** acts as the model's short-term working memory, i.e. how much combined input text, system instructions, and conversation history it can hold at once. A larger context size lets you translate longer texts without the model "forgetting" your glossary, but it consumes significantly more memory and slows down processing.

   * **GPU Layers** (this only applies if you have a GPU) determines how much of the model runs on your graphics card (GPU) rather than your main processor (CPU). Offloading layers to a compatible GPU dramatically increases speed (`tokens/sec`), whereas setting it too high for your graphics memory can cause a loading error.

3. **Working-Memory Stress Test:**

   * Keep your **System Prompt** active from Step 1.

   * Set **Context Size** to a small value (e.g., `1024` or `2048` tokens) and paste a long 500–700 word article to translate in chunks over several turns. Note the generation speed (`tokens/sec`) and check whether the model eventually "forgets" your initial system instructions.

   * Increase **Context Size** (e.g., to `4096` or `8192` tokens), repeat the task, and observe any changes in RAM/GPU usage in **Settings > Hardware**.

#### Step 4: Critical Reflection

> **Writing Task**. Write a **250–300 word critical account** addressing the following questions:
> - **Reproducibility vs. Fluency.** In professional translation workflows, why is a low **Temperature** (`0.1–0.2`) usually preferred over default settings (`0.7`), and when might higher randomness actually help a translator?
> - **The Cost of High Repeat Penalties.** Machine translation and LLMs sometimes suffer from repetitive phrasing, yet raising **Repeat Penalty** too high (`1.4+`) can degrade translation quality. Based on Run 3 in Step 2, why is extreme repetition avoidance risky when translating texts that legitimately repeat key terms (such as legal contracts or user manuals)?
> - **Hardware Trade-Offs in Practice.** How did changing **Context Size** affect your computer's responsiveness and memory usage? What practical strategy would you use to translate a 10-page document locally on a standard laptop without overwhelming your hardware?

---

### Activity 3: Customizing a Private Local LLM

**Learning Goal:** understand how translators can tailor a local LLM using their own Translation Memories (TMs), comparing Retrieval-Augmented Generation (RAG) and fine-tuning, in a way that is accessible to non-technical language students and instructors.

**Estimated Time:** 2 hours

**Prerequisites:** reading Chapter 15 and Section 5 of Chapter 18, and familiarity with basic Translation Memory (TM) concepts (source–target translation units).

#### Step 1: Prompting with Your Data: RAG

When asking an LLM to complete a task, it can be useful to provide related examples, which is referred to as few-shot prompting (see Section 4.4 in Chapter 12).

But what if we have large dataset with potentially useful examples and we want to choose the most relevant ones on-the-fly automatically? This can be done with the technique known as Retrieval Augmented Generation (RAG).

The Jupyter notebook `few_shot_rag_llm_for_translation.ipynb` (based on Section 5.1 of Chapter 18) provides a use case for translation showing the use of few-shot and RAG prompting, leveraging a translation memory for the latter.

> **Task**. Run this notebook step-by-step, focusing on the explanations, inputs, and outputs in each cell so you follow what each step does rather than worrying about every line of code.

#### Step 2: Fine-Tuning with Your Data

While RAG guides the LLM by retrieving relevant examples into the prompt, fine-tuning adapts the LLM by further training it on a given dataset, such as a domain-specific translation memory, so the model internalizes the domain style, phrasing, and conventions directly into its behaviour.

The Jupyter notebook `fine_tune_llm_for_translation.ipynb` (based on Section 5.2 of Chapter 18) provides an example of fine-tuning an LLM for translation using a translation memory. The jupyter notebook `eval_fine_tune_llm_for_translation.ipynb` then evaluates the fine-tuned model using two automatic evaluation metrics and compares its performance against the initial model with zero-shot prompting.

> **Task**. Run these two notebooks step-by-step, paying attention to how the data is prepared and how the outputs change. (Note: Depending on Colab's hardware settings, training may take several minutes or be run on a smaller sample.).

#### Step 3: Comparing Customization Approaches on Your Own Data
> **Task.** Complete the following comparative test using your own sentences and translation data
> - **Zero-shot translation**. Try to find a handful of sentences where the LLM produces incorrect translations. If the translations from the LLM look mostly fine, you can try to find more challenging examples by using less common vocabulary, long complex sentences, or metaphorical language.
> - **Few-shot translation**. Take the sentences that caused problems and add a few example translation pairs to the prompt. Notice whether accuracy or fluency improves, and observe whether matching sentence structure or matching topic/domain helps more.
>- **Fine-tuned translation**. Test the fine-tuned LLM from Step 2 on those same problematic sentences. Compare the result against zero-shot and few-shot prompting. Does fine-tuning give a clearer improvement, or introduce any new quirks?
> - **Quantitative check (optional/larger datasets)**. If you have a larger test set with human reference translations (e.g., 100 or more sentences), you can measure the gain of the fine-tuned model over zero-shot translation using automatic evaluation metrics such as sacreBLEU or COMET.
> - **Quantitative check (advanced):** If you have a larger test set with human reference translations (e.g., 100 or more sentences), you can measure the gain of the fine-tuned model over zero-shot translation using automatic evaluation metrics such as [sacreBLEU](https://github.com/mjpost/sacrebleu) or [COMET](https://unbabel.github.io/COMET/). See notebook `eval_fine_tune_llm_for_translation.ipynb`. You can also run these metrics through the web-based [MATEO (MAchine Translation Evaluation Online)](https://mateo.ivdnt.org/) platform without setting up metrics locally.

---

## Further resources

- [Jan's official documentation](https://docs.jan.ai)
- [Jan Troubleshooting & FAQ](https://jan.ai/docs/troubleshooting)
- Other GUI tools for local LLMs: [LM Studio](https://lmstudio.ai/) (note that it is not open source), [GPT4All](https://www.nomic.ai/gpt4all), [Ollama](https://ollama.com/)
- [A Visual Guide to Quantization](https://newsletter.maartengrootendorst.com/p/a-visual-guide-to-quantization) — accessible visual explainer on model compression and hardware trade-offs
- [Hugging Face Models](https://huggingface.co/models). Repository of open-weights LLMs.
- [MATEO (MAchine Translation Evaluation Online)](https://mateo.ivdnt.org/) — browser-based automatic translation evaluation (including BLEU, chrF, and COMET) without local installation

