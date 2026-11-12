# Chapter 3

**Capsule: Data Management Planning**

Author(s) name and affiliation: Pilar Sánchez Gijón and Ester Torres-Simón, Universitat Autònoma de Barcelona

Expected study time: 1.5–2 hours per task

Language of instruction: Any language, preferably the students' working/first language.

## Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- perform TM clean-up/maintenance
- know where to find data sources for LLMs
- create data sources for LLMs
- annotate/label/enhance data
- compile/curate high-quality, specialised corpora

## Related LT-LiDER book chapter:
For the completion of these activities, in addition to Chapter 3, you may find Chapter 2 Translation Data, Chapter 7 New AI-based features in Computer-Assisted Translation tools, and Chapter 9 Low-resource Languages and Neural Machine Translation also useful.

## Activity pre-requisites:
- basic familiarity with translation memories and bilingual linguistic data
- access to the free tools and platforms indicated for each activity
- instructor-provided sample datasets or project scenarios where required
- a free Hugging Face, DMPTool or European Language Grid account where required

## Activity 1: Curating a Translation Memory for Reuse

Use OpenRefine to audit and clean a bilingual dataset exported from a translation memory.

- identify exact and near-duplicate segments, misaligned entries and other “bycatch data”
- decide, for each flagged entry, whether to keep, correct or remove it
- record your filtering decisions and rationale in a processing log
- compare your curated dataset with a classmate's
- discuss cases where your filtering decisions diverged
- reflect on the difference between manual, criteria-based curation and fully automated cleaning

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- perform TM clean-up/maintenance
- import/export/merge TMs

### Related LT-LiDER book chapter:
For the completion of this activity, in addition to Chapter 3, you may find Chapter 2 Translation Data and Chapter 7 New AI-based features in Computer-Assisted Translation tools also useful.

Before starting, download OpenRefine and the provided “dirty” translation memory sample dataset. Basic familiarity with translation memories and TMX export is recommended.

## Activity 2: Sourcing and Evaluating External Corpora for Model Adaptation

Use OPUS and the Hugging Face dataset catalogue to identify at least three candidate datasets matching a project brief specifying a language pair, domain and register.

For each dataset, record its source, licence, size, format and thematic coverage. Then assess its relevance, licence transparency, and the risk of bycatch data or excessive heterogeneity. Rank the datasets from most to least suitable and justify your ranking in writing.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- know where to find data sources for LLMs
- align bilingual resources (e.g. with Okapi/Olifant)

### Related LT-LiDER book chapter:
For the completion of this activity, in addition to Chapter 3, you may find Chapter 9 Low-resource Languages and Neural Machine Translation also useful.

You will need the project brief provided by the instructor. A free Hugging Face account may be required to download some datasets.

## Activity 3: Drafting a Data Management Plan for a Translation Project

Working in small groups, use DMPTool to draft a data management plan for a scenario in which a translation company builds a domain-specific dataset to fine-tune an NMT engine.

Your plan should cover data description, sourcing strategy, access and sharing conditions, versioning, security and long-term preservation. Exchange your plan with another group and check whether a colleague unfamiliar with the project could understand how the dataset should be governed throughout its lifecycle. Finally, map each section of the plan to the data-governance best practices discussed in Chapter 3.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- create data sources for LLMs
- carry out data analysis

### Related LT-LiDER book chapter:
For the completion of this activity, Chapter 3 provides the necessary theoretical background.

You will need a free DMPTool account and the group project scenario handout provided by the instructor.

## Activity 4: Annotating Post-Edited Data for Model Optimisation

Use Label Studio to build a simple annotation template for post-edited translation memory entries containing the source text, raw MT output and human-revised version.

Tag each machine-translated segment according to the type of change introduced by the reviser, such as terminology, register, omission, mistranslation or stylistic preference, and add a short justification. Compare your annotations with a classmate's, discuss disagreements and agree on a shared annotation guideline. Finally, reflect on how annotated data of this kind could be used to optimise an NMT engine or LLM.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- annotate/label/enhance data
- know LLM and NMT limitations and capabilities

### Related LT-LiDER book chapter:
For the completion of this activity, in addition to Chapter 3, you may find Chapter 9 Low-resource Languages and Neural Machine Translation also useful.

Before starting, install Label Studio locally or use its public playground and download the provided set of post-edited translation memory entries.

## Activity 5: Describing Datasets with a Standardised Metadata Schema

Browse the European Language Grid (ELG) catalogue and examine how existing corpora are described in terms of domain, language, licence, format and provenance.

Then use the ELG interactive metadata editor to register a small sample corpus as a new catalogue entry. Identify which fields correspond to the DCAT concepts of Catalogue, Dataset and Distribution. Compare the ELG schema with the dataset card format used in Activity 2 and discuss which approach is better suited to internal use and which to open, cross-institutional use.

### Learning outcomes: (LT-LiDER map skill(s)): By the end of this exercise you will be able to:
- compile/curate high-quality, specialised corpora
- know about confidentiality issues of open-access models

### Related LT-LiDER book chapter:
For the completion of this activity, in addition to Chapter 3, you may find Chapter 2 Translation Data also useful.

A free European Language Grid account is required only if you register a resource. You will also need a small sample corpus provided by the instructor or curated in Activity 1.

## Further resources:

OpenRefine: https://openrefine.org/download

OpenRefine documentation: https://openrefine.org/docs

OPUS — the open parallel corpus: https://opus.nlpl.eu/

Hugging Face Datasets: https://huggingface.co/datasets

DMPTool — create an account and a plan: https://dmptool.org/

DMPTool quick-start guide: https://dmptool.org/general_guidance

Label Studio — download and installation: https://labelstud.io/guide/install

Label Studio interactive playground: https://labelstud.io/playground/

Label Studio labelling configuration guide: https://labelstud.io/guide/setup

European Language Grid — catalogue: https://live.european-language-grid.eu/catalogue/

ELG documentation — contributing a corpus/dataset: https://european-language-grid.readthedocs.io/en/stable/all/3_Contributing/Corpus.html
