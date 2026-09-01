# Chapter 11
**Capsule: Teaching and acquiring data and machine translation literacy in translation contexts**

Author(s) name and affiliation: *Janiça Hackenbuchner*, Ghent University, & *Ralph Krüger*, TH Köln – University of Applied Sciences

Language of instruction: English

## Activity 1 DataLitMT: Investigating machine translationese & post-editese

In this exercise, you will automatically analyse texts for instances of machine translationese & post-editese using the dedicated [DataLitMT learning resource](https://itmk.github.io/The-DataLitMT-Project/resources/).
- You will be working in the [advanced-level Colab notebook](https://colab.research.google.com/drive/1H_Nn-TRbOJlGPp2tmcJ_EAdIhlDC-xVK?usp=sharing), where you should first read the introduction to machine translationese & post-editese.
- Next, complete the practical steps outlined in the notebook by running the pre-defined code cells. First, you will load and pre-process the texts to analyse. Then, you will calculate the two standard measures lexical variety and lexical density and visualise the results. The notebook will also assist
you in interpreting these results. 
- Instead of analysing the pre-selected texts, you can choose to upload and analyse your own texts in the notebook. If you do not yet know how to work with your own texts in a Colab notebook environment, you may want to have a look at Chapter 15 of this book, where this process will be illustrated in a companion notebook. The chapter also includes guidelines
on how to use LLMs as coding assistants for computational tasks that you feel are beyond your current level of competence

## Activity 2 ProMut: A beginner’s walk-through
In this exercise, you will be using the [ProMut](https://promut.uab.cat/) NMT platform to go through basic steps such as data and MT engine selection, translation, as well as inspection and evaluation of MT engine outputs.
- First, you will have to create a Beginner profile, which provides access to all basic features of ProMut. To do so, simply click the Log in button in the upper right section of the screen and log in with a Gmail address.
- On the Datasets tab, you can get an impression of how a dataset for training an MT engine could look like, by checking which corpora are available as Public datasets. Grab one or two of those corpora in order to add them to Your datasets (to do so, click on the three vertical dots next to the name of a corpus). Now, preview the contents of your corpora to see which kinds of sentences they include (again, click on the three vertical dots to do so). Note that Beginners cannot train their own MT engines, but users with
corresponding rights could choose or upload corpora for engine training on this tab.
- On the Engines tab, you can see a list of available MT engines that have already been trained and shared. Here, grab two engines in order to add them under Your engines (again, click on the three vertical dots). Make yourself familiar with the two engines by checking their language pair, description, trainer, and BLEU score.
- On the Translate tab, produce a translation with each of your two engines. To do so, you can type or paste sentences into the left-hand field or upload a text file. The translation will be shown in the right-hand field. You may also want to download the translation as a TMX file.
- On the Inspect tab, again produce a translation using each of your two engines and see what the pre-processed input and output look like and which four translation hypotheses were considered the most probable translations by the two engines. Do you agree with the order in which the four MT hypotheses are presented?
- Finally, on the Evaluate tab, perform an automatic quality evaluation of the output of your two MT engines and compare the quality scores of your two engines. To do so, you must upload a file containing the source text and one file containing the reference translation. For COMET, you need to upload the source text too. 
Note: The smileys under the numerical values for the different scores indicate whether a high translation quality is indicated by a high score (as is the case for BLEU, chrF3 and COMET) or by a low score (as is the case for TER). Do you agree with the translation quality indicated by these scores?

## Activity 3 DeBiasByUs: Find and log cases of gender bias
In this exercise, you will access the [DeBiasByUs](https://debiasbyus.ugent.be/) platform to log instances of gender bias in MT. If this exercise is done in a classroom, students can share and compare their findings with the class.
- First, make yourself familiar with one particular aspect of the topic of gender bias in MT. To do so, access the [Learn](https://debiasbyus.ugent.be/learn/) section of the DeBiasByUs platform and read one of the sections under ‘Definition & extra Information’. Also, choose one paper listed under ‘Research on bias’ and familiarise your-
self with its content. In class, students can present the summaries of their readings to each other.
- Now, go to an MT system (e.g., DeepL, Google Translate, or ChatGPT) and translate a couple of sentences about yourself (your bio) or about someone else from a source into a target language of your choice. Then, analyse the output of the MT system for instances of gender bias. If you find such instances, log them in the Share section of DeBiasByUs and fill out the rel-
evant fields. Ideally, do this for two to three such instances. Note that these should be real-life instances of gender bias in MT, not fictional ones. To upload instances of gender bias directly from an MT system to DeBiasByUs, you are welcome to install the Bias Shield plugin


## Activity pre-requisites
- Google account to access Colab notebook for Activity 1
- Ideally basic Python programming experience for Activity 1
- A ProMut Beginner's profile, which you will set up in Activity 2

## Further Reading 
- The [MT Literacy Project](https://sites.google.com/view/machinetranslationliteracy/) instructs interested readers on how MT systems process information and on how to interact adequately with MT tools. The focus lies on how researchers and scholars, who are the primary target
audience of the project, can use the right tools in a critical and informed way. The project outputs include video lectures, academic articles, a book, infographics, and open educational resources.
- Coursera offers a free, intermediate-level [Massive Open Online Course (MOOC) on Machine Translation](https://www.coursera.org/learn/machinetranslation). This MOOC specifically addresses the basic principles of MT, focusing on the difficulties of translation, the basic
principles of different MT approaches, and state-of-the-art NMT systems and the deep learning methods used to model the translation process. The course is taught by Alexander Waibel and Jan Niehues from the Karlsruhe Institute of Technology and includes videos, readings and assignments.
- An excellent resource for gaining a better understanding of the transformer base architecture of modern NMT systems and LLMs is Jay Alammar’s [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/). As the name implies, this resource
explains the working principle of the transformer using reader-friendly visualisations. The attention mechanism, which lies at the heart of the transformer, is visualised and explained in more detail in [Visualizing A
Neural Machine Translation Model](https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/), also by Jay Alammar.
