# Chapter 9

**Capsule: Fine-tuning and Back-translation for mNMT**

Author(s) name and affiliation: Miguel Angel Rios Gaona, University of Vienna.

Expected study time:  1 hours per task

Language of instruction: English

## Learning Outcomes: (LT-LiDER skill(s) map) 

By the end of this exercise you will be able to: 

- Know MT capabilities and limitations
- Train and fine-tune MT models
- Implement MT quality evaluation methods
- Know basic Python
- Use APIs

## Scenarios 

This capsule covers two activities for low-resource multilingual Neural Machine Translation (mNMT), using English–Catalan as an example. First, you will fine-tune an mNMT model directly on a low-resource language pair. Second, you will use back-translation to generate synthetic parallel data and fine-tune the model on the augmented dataset.

Before starting the activities, please watch this short introductory video: [Chapter 9 - exercises](https://www.youtube.com/watch?v=ALcpr2Ke52c)

## Related LT-LiDER Book Chapter

For the completion of this activity, in addition to Chapter 9, we direct the reader to Chapters 10 and 16.


## Activity pre-requisites

- Google account to access Colab
- Basic Python programming experience

## Overview

Please watch our youtube channel for more information about the activities: 

[Chapter 9 - exercises](https://www.youtube.com/watch?v=ALcpr2Ke52c)

The student will fine-tune an open-source multiligual NMT (mNMT) model for low-resource language pairs (LRL), such as English-Catalan. The translation performance of the fine-tuned model should be compared against the original baseline using automatic evaluation metrics. 

- **Activity 1**: Fine-tuning mNMT model
  - We will be using the [NLLB](https://huggingface.co/docs/transformers/en/model_doc/nllb) architecture for fine-tuning. Fine-tuning is a critical process where we take the model's weights, pre-trained on a vast, diverse corpus, and incrementally adjust them using our LRL parallel corpus. This procedure allows the NLLB model to better capture the unique stylistic, lexical, and grammatical information of our LRL pair, improving its translation quality.
  - Download the Python notebook (*finetune_LoRANLLB_en_cat_FLORES.ipynb*) from the notebooks directory and upload it into [Colab](https://colab.research.google.com/?utm_source=scs-index)
  - Download the English-Catalan parallel data tiles from the data directory or download **data.zip** and upload them into Colab
- **Activity 2**: Back-translation for mNMT
  - Back-translation leverages readily available monolingual data (text in a single language) to generate synthetic parallel data (aligned sentences in two languages), augments the small parallel corpus with the synthetic data, and fine-tunes the mNMt model with the augmented data
  - Download the Python notebook (*back_translation_NLLB_en_cat_cat_en_FLORES.ipynb*) from the notebooks directory and upload into Colab
  - Download the English-Catalan parallel data and Catalan monolingual data files from the data directory or download **data.zip** and upload them into Colab

**Note**: You can also perform the exercise for English-Basque, the corresponding data files are included into the data directory. Remember to **unzip** data.zip before uploading files into Colab.

## Further resources

**Colab resources**:
- [Saving and loading notebooks in GitHub](https://colab.research.google.com/github/googlecolab/colabtools/blob/main/notebooks/colab-github-demo.ipynb)
- [Loading data: Drive, Sheets and Google Cloud Storage](https://colab.research.google.com/notebooks/io.ipynb)
