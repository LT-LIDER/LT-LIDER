# Chapters 2 & 4

**Capsule: Translation data and data ethics**

Author(s) name and affiliation: Joss Moorkens, Dublin City University

Expected study time: 1 hours per task

Language of instruction: English	

## Learning outcomes: (LT-LiDER skill(s) map): This exercise will help you to: 
- create data sources for Large Language Models (LLMs)
- know about confidentiality issues of open-access models

## Scenarios 
This capsule presents activities for two scenarios. The first is a group activity in which you are tasked with curating data for an LLM. The second is another group activity in which you will carry out a data lifecycle audit for a number of scenarios.

Before starting the activities, please watch this short introductory video: [Chapter 2 and 4 Video](https://)

## Related LT-LiDER book chapter: 
For the completion of this activity, please read chapters 2 and 4.

## Activity pre-requisites: 
- knowledge of different sources of data (see Chapter 2)
- knowledge of ethical issues for translation data (see Chapter 4)
- pen and paper
- critical thinking

## Activity 1: form a Data Curation Committee
You and your groupmates are AI data engineers tasked with building an LLM. Having looked through the different sources of data in Chapter 2 and the ethical issues in Chapter 4, move on to the following steps.
Your team has been hired to build the training dataset for a brand-new multilingual LLM called LiDER-1. Choose at least two languages to focus on and a particular task - although general purpose is fine too.
You have a strict budget, which means you can only train on 100 'Data Units' (DU). Your goal is to create a model that is accurate, fluent, safe, helpful, and is unlikely to get your company sued or produce toxic or culturally inappropriate output.
Your data can come from any of the following sources:
- web scraped (cheap, large, varied, but full of multilingual AI output, polarised content and hate speech, misinformation, and personal data)
- curated encyclopaedias and news (high factual accuracy, but represents a WEIRD point of view; Wikipedia might be OK to use, but online news sources may present copyright troubles)
- books/literature (good long-range coherence, complex grammar and reasoning, but expensive to license; potential copyright disputes if scraped without permission.)
- academic papers (dense, good scientific knowledge, but not always comprehensible)
- private translation memories (TMs; high quality but rare and expensive)
- open-access bilingual data from OPUS (some shared TMs from trusted sources, some translated by volunteers)
- social media posts (user generated content; natural but full of toxicity, sarcasm, unverified medical/legal advice)
- synthetic data (cheap, plentiful, tailored to your needs, but risks increased hallucination)
allocate your 100 DUs and write your choices down

  **Choice stress test - do these scenarios affect your data choices?**
- A consortium of authors and news publishers sues your company for copyright infringement. There are several such cases winding their way through the courts in 2026/7. How exposed is your dataset? Did you rely too heavily on Books and News without factoring in licensing costs?
- Your model is tested on complex multi-step logic puzzles and coding tasks. Groups that allocated fewer than 15 units to Code and Academic Papers find that their model struggles to learn structured reasoning. Will you change?
- A user prompts your model and it outputs a real person's home address and a conspiracy theory that puts them at risk. Groups that took more than 40 DUs from the web or social media must propose a filtering pipeline (e.g., personally-identifying information redaction, toxicity classifiers, deduplication) to fix the issue.

 **Questions:**
- What were your main considerations? Real LLM developers have to make these decisions. They might upsample high-quality sources (like Wikipedia or textbooks) so the model sees them multiple times during training, while heavily downsampling  web-scraped data.
- What approach would you take to gatekeeping? Read the section on Reinforcement Learning from Human Feedback from Chapter 6.
- Raw data is rarely used as-is. There are processes of deduplication (removing repeated text so the model doesn't memorize) and quality filtering. There may be code used for training and system prompts alongside user prompts. Is it a problem that developers rarely reveal their data sources?

## Activity 2: carry out a data lifecycle audit
When a user submits a form, uploads a file, or completes a transaction, that data goes somewhere. The internet makes cross-border data movement nearly instantaneous, and that can cut across jurisdictions with different laws and ethical norms for things like data privacy protection, national security and economic development.
Data is created, transformed, analysed, shared, and will in time become outdated or irrelevant. Data lifecycle mapping tracks these processes: how data moves, changes, and rests across geographic and legal boundaries from creation to deletion.
In groups, try mapping out the ethical and legal risks across the following stages:

1. Creation and collection. This is where the data first enters your system or processes.
2. Storage. Where data is stored, obviously, but also where it is replicated at least once as a back-up. How do we ensure that this stays within our chosen jurisdiction? Is sensitive data encrypted?
3. Usage and processing. Who can access the data and/algorithms? What happens to it? Can we control cross-border transfers?
4. Back-up and archiving. How can we update and store our data safely?
5. Deletion. Can we securely purge or archive data across every regional copy simultaneously when no longer needed or if it presents a high risk?

Pick two of the following scenarios to map with your group.
- You work in an Italian university and want to create synthetic training data to train a system to identify teenage cyberbullying in Italian. You are given a small amount of genuine cyberbullying content in English. How will you safely manage each stage?
- To fine-tune your EN-FR legal translation system in a French university, you have procured parallel data from the UK, Nigeria, and United Arab Emirates. What issues might you have at each stage?
- Your hospital wants to translate patient discharge instructions from EN to PT-br, AR, ES-mx and HA. How might you safely do this using a LLM?
- You have been passed the data from an extreme private forum on a Croatian climate sceptic website, but do not speak Croatian. You plan a process of translation e-discovery using MT/AI and will then have relevant parts human translated for a journal article. What are the ethical and legal risks at each stage?
- You want to machine translate a very sensitive report on medical misconduct from English into Malay, Chinese and Singaporean. You receive comparable data from an Indonesian source but it has not been anonymised. How do you safely use this data to fine-tune your NMT system?
- You are contracted to use an LLM to aid Korean to English post-editing of subtitles for a valuable new series. How will you safely manage the process from the beginning to programme delivery?

 **Questions:**
- What were the riskiest stages and why?
- What do you need to know about the source of your data?
- Could someone maliciously sabotage your efforts at any of the stages?
- Did this exercise make you think differently about data curation and data ethics?

## Further resources:
Read about some commonly used data sources such as The Pile https://arxiv.org/abs/2101.00027, Common Crawl https://commoncrawl.org/, and Opus for parallel corpora https://opus.nlpl.eu/. How do the first two differ from Common Corpus? https://arxiv.org/html/2506.01732v1
Brandt Dainow and Philip Brey wrote a document on 'ethics by design' for the European Commission in 2021. This contains proposals for foregrounding ethics from the beginning of an AI project. https://ec.europa.eu/info/funding-tenders/opportunities/docs/2021-2027/horizon/guidance/ethics-by-design-and-ethics-of-use-approaches-for-artificial-intelligence_he_en.pdf
