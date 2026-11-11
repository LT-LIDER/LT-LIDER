# Chapter 15
**Capsule: Bridging the digital divide: Making Python and the Python ecosystem accessible to translators**

Author(s) name and affiliation: *Ralph Krüger*, TH Köln – University of Applied Sciences, *Sergi Álvarez-Vidal*, Universitat Autònoma de Barcelona & *Janiça Hackenbuchner*, Ghent University

Language of instruction: English

*Further links and resources available in the Chapter.*

## Activity 1: Accessing the Python open-source ecosystem to complete language-oriented AI use cases

In this section, we propose a range of language-oriented AI use cases that users can complete using the digital scaffolding introduced in this chapter. For using LLMs as coding assistants, we propose the following starting prompt derived
from the best-practice prompting strategies discussed in Section 3.2.2. 

*You serve as a professional coding assistant to a programming novice who takes their first coding steps in a Google Colab notebook running Python 3.12. Please provide detailed step-by-step instructions for completing the following computational
process: [description of the specific use case to be completed]*

Users should feel free to adapt or extend this prompt as they see fit. In the tutorial video for the guided use case in the following section, we discuss and employ further prompting strategies.


### Guided use case: Calculating automatic MT quality evaluation scores
In this use case, we would like to perform an automatic MT quality evalua tion using the string-based metrics BLEU and Translation Edit Rate and the embedding-based metric BERTScore. In our [tutorial video](https://youtu.be/SWXdT1V2tbk?si=Xjx_gVZ8IpZRylaE) provided on the LT-LiDER YouTube channel, we use the following sentence pair 
(in case you are wondering, we do not require the source text to calculate our three MT quality scores):

*Human reference translation*: They drove the car to the gas station.

*MT output*: They drove the automobile to the gasoline station.

To simplify this use case, we recommend just pasting or typing your sentences into the Colab notebook instead of storing them in external files. Also, please feel free to use your own reference translations and MT outputs. However, while
BLEU and TER are language agnostic, BERTscore is by default set to an English model, which must be changed if text in another language is to be scored (your coding assistant can help you with this). Once you have successfully calculated
the scores, you could ask your coding assistant how these scores are interpreted, why (at least for our example sentences) they contradict each other to some extent and how this may be traced back to their underlying operating principles.


### Now it’s your turn: Suggestions for further DIY use cases

- **DIY Use Case 1:** You want to use the [Hugging Face Transformers](https://huggingface.co/docs/transformers/index) library to load the GPT-2 model to complete the following text prompt: Translators should learn Python because ... (or any other text prompt of your choice).
You want GPT-2 to provide two different answers, and each answer should have a maximum length of 30 tokens. Also, the output should once be generated with a temperature setting of 0.5 and once with a temperature setting of 1.5.
By adapting the temperature, you can control the randomness in the model’s behaviour/output. If you would like to know more about this, have a look at Chapter 12 or ask you coding assistant for help.

- **DIY Use Case 2:** You want to explore how the self-attention mechanism in GPT-2 works (we use GPT-2 here repeatedly since it is a rather light-weight model that can be loaded quickly into online environments such as Colab notebooks).
You have heard of the Python library [BertViz](https://github.com/jessevig/bertviz), which lets you visualise the self-attention process in GPT-2 and a range of other language models. When exploring self-attention in GPT-2, you could use the following example sentence:
They wanted to book a ticket to the conference but first they took a look at the book of abstracts.

- **DIY Use Case 3:** You have heard of the concept of word embeddings, and now you want to better understand how these embeddings work. You may want to research some information on word embeddings (for example, by working through
this [Jupyter notebook](https://colab.research.google.com/drive/1PvjR2lQjO779S5nRDmIDe9ACuaAT-w1-?usp=sharing) from the technical curriculum on language-oriented AI discussed in Chapter 1). Next, you would like to load a word embedding model (e.g., by word2vec, fastText or spaCy) in order to access individual word vectors.
You would like to display the word vectors of the words translation, interpreting and football (or any other words of your choice) and compare these word vectors with each other. You also want to display their most similar and least similar words.
You may even want to visualise the similarity or dissimilarity between individual words (why not challenge your coding assistant a bit?).



## Activity pre-requisites
- Google account to work in and access Colab notebooks
- Ideally basic Python programming experience

## Further Reading 
- The book Python crash course. A hands-on, project-based introduction to programming by Matthes (2022) is an excellent introduction to Python programming for programming novices. The book is highly accessible and answers most if not all questions that audiences taking their first steps in
Python might have.
- The book Teaching and learning with Jupyter by Barba et al. (2019) provides a comprehensive discussion of Jupyter notebooks, of the Jupyter notebook ecosystem and of the didactic advantages of using Jupyter notebooks, together with a range of possible use cases.
- The online course [Introduction to Python for Linguists](http://www.digiling.eu/deliverables/phase-2/introduction-to-python-for-linguists/) on the [DigiLing e-learning Hub](http://www.digiling.eu/) is aimed at students of linguistics and other disciplines with no prior programming experience. The course aims to provide an understanding of elementary concepts of programming, with a particular focus
on text processing. It contains interactive presentations, video & screen recordings, exercises, knowledge quizzes, readings, and possible assignments with instructors’ feedback on student submissions.
- The article “Conversational AI as a coding assistant: Understanding programmers’ interactions with and expectations from large language models for coding” by Akhoroz & Yildirim (2025) provides an in-depth discussion of the advantages and disadvantages of using LLMs as coding assistants
and proposes a set of design guidelines for improving such conversational coding assistants
