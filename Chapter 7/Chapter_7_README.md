# Chapter 7

**Capsule: New AI-based features in Computer-Assisted Translation tools**

Author(s) name and affiliation: María Isabel Rivas Ginel, Dublin City University and Pilar Sánchez Gijón, Universitat Autònoma de Barcelona

Expected study time: 2 hours per task

Language of instruction: English

## Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- perform TM clean-up/maintenance
- pre-translate (in CAT tools) with TM/MT/LLM
- know where information comes from in a CAT tool (e.g. TM/TB/MT/MTQE/LLM)
- know prompt design
- know MT capabilities and limitations (e.g. MT errors/hallucinations)
- perform QA with CAT tools

## Related LT-LiDER book chapter:
For the completion of these activities, in addition to Chapter 7, you may find Chapter 3 Data Management Planning, Chapter 6 Key Concepts in Large Language Models for Translation, Chapter 10 Evaluation of Automatic Translation, Chapter 11 Teaching and acquiring data and machine translation literacy in translation contexts, and Chapter 12 Best practices for prompting: how can translation students, trainers and professionals make the most out of LLMs? also useful.

## Activity pre-requisites:
- basic familiarity with computer-assisted translation (CAT) tools and translation workflows
- reading of Chapter 7 before completing the activities
- access to the relevant free trial, free account, or institutional licence specified for each activity
- use of non-confidential teaching materials and verification of current access conditions shortly before each activity

## Activity 1: Automated Translation Memory Curation

**Tool:** Phrase  
**Feature:** Automated Asset Curation (AAC)

### Access

Students can use the 14-day Phrase free trial to complete the activity. Alternatively, where available, the activity can be carried out through institutional access to Phrase Custom AI.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- perform TM clean-up/maintenance;
- import/export/merge TMs.

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Section 3.1.2: Asset curation**. You may also find **Chapter 3: Data Management Planning** useful.

### Activity

You are provided with a deliberately “dirty” translation memory containing duplicates, near-duplicates, unusually short or long segments, inconsistent source–target length ratios, and other potentially problematic entries.

After creating your Phrase account, access Automated Asset Curation (AAC) and create a dataset from the provided translation memory. Apply a selection of Phrase’s rule-based and machine-learning-based cleaning filters and generate a curated version of the TM.

Compare the original and curated translation memories, identify which segments have been removed, and evaluate whether the automated decisions were justified. Pay particular attention to cases in which automated cleaning may remove data that could still be useful to a human translator.

Conclude by discussing the advantages and risks of using AI-assisted curation to prepare linguistic resources for CAT and machine translation workflows.

### Access and resources

- [Start or consult the Phrase free trial](https://phrase.com/pricing/)
- [Automated Asset Curation: instructions and available filters](https://support.phrase.com/hc/en-us/articles/14319572338332-Automated-Asset-Curation)
- [Phrase Custom AI overview and access information](https://support.phrase.com/hc/en-us/articles/7683093364508-Phrase-Custom-AI-Overview)

> **Important:** The instructor should verify that AAC remains accessible through the current trial immediately before the activity. Phrase documents AAC as part of Custom AI and describes it specifically as a tool for automatically cleaning and optimising translation memories.

---

## Activity 2: Exploring Dynamic Domain Adaptation in Generative Translation

**Tool:** memoQ AGT  
**Feature:** Adaptive Generative Translation

### Access

Students can activate the 14-day memoQ TMS Starter trial, which currently includes one Project Manager and five Linguist licences. According to memoQ’s current documentation, starting a memoQ TMS trial also automatically starts an AGT trial and creates the necessary default AGT API key. Alternatively, the activity can be organised through an existing institutional memoQ TMS environment with AGT access.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- pre-translate (in CAT tools) with TM/MT/LLM;
- know where information comes from in a CAT tool (e.g. TM/TB/MT/MTQE/LLM).

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Section 3.3.1: On-the-Fly Domain Adaptation**. You may also find **Chapter 9: Low-resource Languages and Neural Machine Translation** useful.

### Activity

You are provided with a short domain-specific source text together with a small translation memory, term base and, where appropriate, aligned reference documents.

First, use memoQ AGT to translate the text with limited contextual resources available to the system and save the resulting translations.

Then add or activate the domain-specific TM, terminology and reference material and translate the same content again. Compare the two sets of translations and identify instances in which the additional linguistic resources affect terminology, phraseology, style or domain appropriateness.

Determine whether the additional context consistently improves the output or whether it can also introduce inappropriate solutions. Conclude by considering how retrieval-augmented generative translation differs from using a general-purpose LLM without project-specific linguistic resources.

### Access and resources

- [Start the memoQ TMS Starter free trial](https://www.memoq.com/pricing/)
- [Start and configure the memoQ AGT trial](https://docs.memoq.com/helpcenter/Products/memoQ-AGT/Subscribe-or-request-a-trial.htm)
- [Introduction to memoQ AGT and domain adaptation](https://docs.memoq.com/helpcenter/Products/memoQ-AGT/index.htm)
- [memoQ TMS Starter trial and licence information](https://docs.memoq.com/helpcenter/memoQ-TMS/Cloud-Getting-Started/memoQ-TMS-plans.htm)

> **Important:** AGT is not a standalone application: students need access to memoQ TMS. The activity should therefore be scheduled within the trial period. Alternatively, using AGT may require an academic licence providing students with institutional access to memoQ TMS and the relevant AGT functionality.

---

## Activity 3: Comparing Fuzzy-Matching Methods

**Tool:** XTM Cloud  
**Feature:** Weighted Token Levenshtein (WTL)

### Access

The activity can be carried out using an XTM Cloud free trial, provided that the necessary project configuration is available in the trial environment. If students do not have permission to modify the relevant settings, the instructor should prepare two projects in advance and provide students with translator access.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- pre-translate (in CAT tools) with TM/MT/LLM;
- know where information comes from in a CAT tool (e.g. TM/TB/MT/MTQE/LLM).

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Section 3.3.2: Translation Memory Enhancement and Fuzzy Match Autocompletion**. You may also find **Chapter 3: Data Management Planning** useful.

### Activity

You are provided with a source text and a translation memory specifically designed to contain potential fuzzy matches involving differences in word order, terminology, syntax and function words.

Process the same material in two projects: one using XTM’s standard fuzzy-matching configuration and another using Weighted Token Levenshtein (WTL). Record the matches and similarity percentages returned for selected segments and compare the results produced by the two matching methods.

Evaluate the usefulness of the retrieved matches from a translator’s perspective. Pay particular attention to cases in which similar percentages conceal important semantic differences and cases in which token weighting produces a more useful match.

Conclude by considering the limitations of treating numerical fuzzy-match scores as direct indicators of translation usefulness.

### Access and resources

- [XTM Cloud](https://xtm.cloud/)
- [XTM documentation](https://xtm.cloud/documentation/)
- [XTM information on AI and advanced TM leveraging](https://xtm.cloud/blog/how-xtm-cloud-enables-linguists-to-work-more-efficiently-by-leveraging-the-power-of-ai/)

---

## Activity 4: Prompt-Based Translation and AI-Assisted Revision

**Tool:** Crowdin  
**Feature:** Crowdin AI

### Access

Students can use Crowdin’s 14-day Team trial to create a localisation project and explore the AI functionality available under the trial. Alternatively, the instructor can investigate access through Crowdin’s Academic Program for teaching purposes.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- know prompt design;
- use LLM to sumarise/rewrite text.

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Section 3.3.3: Prompted and Unprompted Translation Generation**. You may also find **Chapter 12: Best practices for prompting: how can translation students, trainers and professionals make the most out of LLMs?** particularly useful.

### Activity

Create a small localisation project from a source file supplied by the instructor and produce an initial AI-assisted translation of a selected group of segments.

Then use Crowdin’s available AI prompting and editing functions to request controlled modifications to the translations. For example, ask the system to adopt a different register, improve terminological consistency, respect a specific stylistic instruction, or reformulate an awkward translation.

For each selected segment, retain the initial output, the AI-assisted revision and your own final human revision. Compare the three versions and classify the changes introduced by the AI. Identify cases in which prompting produces a clear improvement, cases in which it merely produces an alternative, and cases in which it introduces a new problem.

Conclude by discussing the extent to which interactive prompting can function as a revision mechanism inside a localisation environment rather than simply as a translation-generation tool.

### Access and resources

- [Crowdin plans and free trials](https://crowdin.com/pricing)
- [Crowdin AI](https://crowdin.com/ai)
- [Crowdin Academic Program](https://crowdin.com/product/for-academic)
- [Crowdin documentation](https://support.crowdin.com/)

---

## Activity 5: Identifying and Evaluating Semantic Issues in AI-Assisted Translation

**Tool:** wxrks  
**Feature:** Translation Smells / Semantic Verifier

### Access

Students create a free wxrks account. The current Free plan provides a limited annual allowance of processed words, API calls and AI tokens, which is sufficient for a short classroom exercise. Students should use the AI service provided within wxrks rather than connecting their own OpenAI, Azure OpenAI or other paid API account.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- use LLMs to find bias;
- know MT capabilities and limitations (e.g. MT errors/hallucinations).

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Section 3.4: Linguistic Quality Assurance and Revision Phase**. You may also find **Chapter 10: Evaluation of Automatic Translation** and **Chapter 4: Translation and data ethics** useful.

### Activity

You are provided with a short source text and translate it in the wxrks translation environment using the AI-assisted translation functionality available in your account. Keep the text short so that the entire exercise remains comfortably within the allowances of the Free plan.

Once an initial translation has been produced, use Translation Smells, or the Check Smells action where manual analysis is required, to analyse a selection of translated segments. The Semantic Verifier can identify potential semantic problems such as omissions, additions, ambiguity, tone mismatches and other shifts in meaning.

Examine each issue identified by the system and decide whether it represents a genuine translation problem, a debatable issue or a false positive. Do not automatically accept the system’s assessment.

Then select several flagged segments and revise them manually or use the available AI-assisted actions to explore possible corrections. Where possible, run Check Smells again on the revised segments and compare the results with the original analysis.

For each selected example, record the original translation, the issue identified by Translation Smells, your assessment of whether the warning was justified, the revised translation and the result of the second analysis.

Conclude by discussing the extent to which semantic verification can support human revision. Consider both the types of errors that Translation Smells successfully identifies and those for which human contextual and linguistic judgement remains necessary.

### Access and resources

- [Create a free wxrks account and consult the current plans](https://wxrks.com/pricing)
- [Translation Smells and Semantic Verifier](https://wxrks.com/semantic-verifier-translation-smells)
- [Documentation on the integrated LLM and Translation Smells](https://support.wxrks.com/en/articles/10430058-all-about-our-llm-integration)

> **Important:** Students do not need to purchase an OpenAI or Azure OpenAI API subscription for this activity. wxrks allows its own AI instance to be selected as the provider. The Free plan has usage limits, so the instructor should use a short source text and verify the Free-plan allowances shortly before the activity.

---

## Activity 6: Collaborative Generative Translation and AI-Assisted Review

**Tool:** Trados Ignite  
**Features:** Generative Translation and Smart Review

### Access

Students can register for the 14-day free trial of Trados Ignite. RWS currently states that the trial allows users to explore all Ignite features. Generative Translation and Smart Review can be used subject to the account’s throughput allowance. Alternatively, students can work within an appropriately configured institutional Trados environment where such access already exists.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- pre-translate (in CAT tools) with TM/MT/LLM;
- perform QA with CAT tools.

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Sections 3.3.3: Prompted and Unprompted Translation Generation and 3.4: Linguistic Quality Assurance and Revision Phase**. You may also find **Chapter 11: Teaching and acquiring data and machine translation literacy in translation contexts** useful.

### Activity

Work in small groups on the same short translation project and take on different professional roles, such as translator and reviewer.

The translator first uses Generative Translation to produce an initial version of the assigned content and performs any modifications they consider necessary. The project is then passed to the reviewer, who uses the available review functionality, including Smart Review, to examine the translation and identify segments requiring attention.

Record situations in which the AI-generated translation is accepted without modification, modified by the translator, subsequently questioned by Smart Review, or ultimately overridden by the human reviewer. Pay particular attention to disagreements between the different forms of automated assistance and human judgement.

Each group reconstructs the decision-making process for several representative segments and discusses how generative translation and AI-assisted review redistribute responsibilities between translators, reviewers and automated systems in a collaborative translation workflow.

### Access and resources

- [Trados Ignite](https://www.trados.com/product/ignite/)
- [Trados Ignite free-trial FAQ](https://www.trados.com/product/ignite/faq/)
- [Trados Generative Translation](https://www.trados.com/product/features/generative-translation/)
- [Trados Smart Review](https://www.trados.com/product/features/smart-review/)

---

## Activity 7: Comparing Human Translation with Integrated Generative AI Assistance

**Tool:** Wordscope Campus  
**Feature:** Integrated ChatGPT/AI assistance

### Access

**Option 1:** Students who are not yet enrolled through their institution can use the 15-day Wordscope Campus student trial.

**Option 2:** For regular teaching, the instructor can join the Wordscope Academic Program and add students to the class roster. Eligible students then receive Wordscope Campus access free of charge within the academic usage limits. This is the recommended solution for semester-long teaching.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:

- know LLM and NMT limitations and capabilities;
- use LLMs to sumarise/rewrite text.

### Related LT-LiDER book chapter:

For the completion of this activity, use **Chapter 7, especially Sections 3.3.3: Prompted and Unprompted Translation Generation and 3.5: AI-Powered Assistants**. You may also find **Chapter 6: Key Concepts in Large Language Models for Translation**, **Chapter 11: Teaching and acquiring data and machine translation literacy in translation contexts**, and **Chapter 12: Best practices for prompting: how can translation students, trainers and professionals make the most out of LLMs?** useful.

### Activity

Create a short translation project in Wordscope and independently translate a selection of segments before consulting the integrated generative-AI functionality.

For each selected segment, ask the integrated AI to generate an alternative translation, reformulate your existing translation, or provide an explanation of an unfamiliar expression or terminological problem. Use Wordscope’s comparison and revision functionality to compare your original solution with the AI-generated proposal.

Classify the AI suggestions according to whether you would accept them unchanged, accept them after modification, or reject them. Justify each decision by referring to factors such as meaning, terminology, register, idiomaticity, context and stylistic appropriateness.

Conclude by comparing generative assistance with more conventional CAT resources. Identify the types of translation problems for which conversational generative assistance appears particularly useful and those for which translation memories, terminology resources or human research remain preferable.

### Access and resources

- [Wordscope Campus](https://campus.wordscope.com/)
- [Student access, free trial and academic allowances](https://docs.wordscope.com/en/campus/for-students/)
- [Wordscope Campus information for professors](https://docs.wordscope.com/en/campus/for-professors/)
- [Wordscope documentation](https://docs.wordscope.com/)

> **Important:** Access to Wordscope Campus and its integrated AI functionality depends on the type of account and institutional arrangement. While eligible students may receive free access through the Wordscope Academic Program, some configurations or uses of the integrated AI features may require a paid subscription.

---

## Further resources

The tool-specific resources required for each activity are provided directly under the corresponding activity above. Instructors should verify access conditions, trial duration, feature availability and usage allowances shortly before running the activities, as these may change over time.

Chapter 7 also contains a comparative **Resources** section covering AI-enhanced features, indicative pricing, academic licensing and data-protection information for the CAT environments discussed in the chapter. The chapter notes that its feature comparison reflects implementations surveyed as of **June 2025**, so the current status of individual functions should be checked before teaching.

## Further reading from Chapter 7

The Chapter 7 manuscript recommends three complementary resources:

- **Ciobanu (2023)** for a focused overview of CAT software, its functions, evolution and role in the language industry beyond GenAI integration;
- **Rothwell et al. (2023)** for a broader introduction to translation technologies, including CAT tools, machine translation, terminology management, localisation and workflow systems;
- **Moorkens (2024)** for a broader discussion of the effects of AI and automation on language-industry work practices, technological adoption and industry change.

## Key perspective to retain

The activities should not be approached simply as demonstrations of new software functions. Chapter 7 presents the integration of AI into CAT tools as a broader change in translation workflows: AI-enhanced environments increasingly combine structured linguistic resources such as TMs and glossaries with unstructured contextual resources such as client documentation and brand guidelines. At the same time, the chapter stresses the continued importance of human judgement, particularly in relation to quality, transparency, bias, data privacy and the risk of over-reliance on automated decisions.
