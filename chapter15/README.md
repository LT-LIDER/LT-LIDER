# MULTITAN NMT Fine-tuning Pipeline (Google Colab-compatible)

## Project: MULTITAN
This pipeline was developed within the framework of the MULTITAN-GML project (*Traduction Automatique Neuronale hyperspécialisée et Grands Modèles de Langues*), one of the winning projects of the call for projets "Petits & Moyens Équipements 2024" (COPES-2024-12, Fonds d’intervention
Recherche, Université Paris Cité) and tested on the [PNS-UP](https://plateformes.u-paris.fr) scientific platform

### 1. Environment Setup
- Use a GPU running environment (and restart the kernel)
- Mount Google Drive to access files.
- Create a project directory.

### 2. Data Preparation
- Load local aligned bilingual datasets (TSV or CSV formats).
- Preprocess and filter the dataset based on:
  - Alignment quality
  - Segment length
  - Encoding issues

### 3. Model Fine-tuning Pipeline
- Fine-tune a **Seq2Seq model** (e.g., Facebook’s **NLLB 2B** or **Marian MT**).
- Uses the HuggingFace `transformers` library.
- Components involved:
  - `AutoModelForSeq2SeqLM`
  - `AutoTokenizer`
  - `Seq2SeqTrainer` and its training arguments
  - Data collators
  - Training configuration

### 4. Translation and machine evaluation
- Load a CSV or TSV file with test (source language) and reference (target language) segments
- Load both **pretrained** and **fine-tuned** models from saved paths.
- Translate the source segments using each model with:
  - Tokenization
  - Sequence generation (`generate()`)
  - Translation outputs (TSV)
- Evaluate translation quality using:
  - **BLEU** (via `sacrebleu`)
  - **chrF**
  - **COMET**

