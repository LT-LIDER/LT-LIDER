# Chapter 9

Activity name: 

Author(s) name and affiliation: 

Expected study time:  hours per task

Language of instruction: English

## Activity overview

The student will fine-tune an open-source multiligual NMT (mNMT) model for low-resource language pairs (LRL), such as English-Catalan. The translation performance of the fine-tuned model should be compared against the original baseline using automatic evaluation metrics. 

- **Task 1**: Fine-tuning mNMT model
  - We will be using the [NLLB](https://huggingface.co/docs/transformers/en/model_doc/nllb) architecture for fine-tuning. Fine-tuning is a critical process where we take the model's weights, pre-trained on a vast, diverse corpus, and incrementally adjust them using our LRL parallel corpus. This procedure allows the NLLB model to better capture the unique stylistic, lexical, and grammatical information of our LRL pair, improving its translation quality.
  - Download the Python notebook (*finetune_LoRANLLB_en_cat_FLORES.ipynb*) from the notebooks directory and upload it into [Colab](https://colab.research.google.com/?utm_source=scs-index)
  - Download the English-Catalan parallel data tiles (.txt) from the data directory and upload them into Colab
- **Task 2**: Back-translation of tuned mNMT model
  - Back-translation leverages readily available monolingual data (text in a single language) to generate synthetic parallel data (aligned sentences in two languages), augments the small parallel corpus with the synthetic data, and fine-tunes the mNMt model with the augmented data
  - Download the Python notebook (*back_translation_NLLB_en_cat_cat_en_FLORES.ipynb*) from the notebooks directory and upload into Colab
  - Download the English-Catalan parallel data and Catalan monolingual data files (.txt) from the data directory and upload them into Colab

**Note**: You can also perform the exercise for English-Basque, the corresponding data files (.txt) are included into the data directory. 

**Colab resources**:
[Saving and loading notebooks in GitHub](https://colab.research.google.com/github/googlecolab/colabtools/blob/main/notebooks/colab-github-demo.ipynb)
[Loading data: Drive, Sheets and Google Cloud Storage](https://colab.research.google.com/notebooks/io.ipynb)


Related LT-LiDER book chapter: For the completion of this activity, in addition to Chapter 9, we direct the reader to Chapters x, and y.

Activity pre-requisites:

- Google account to access Colab
- Basic Python programming experience

Further resources:
