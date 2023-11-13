# Week 11

## Introduction to NLP and Language Modelling

We leave MLOps for two weeks and get back to data science and machine learning. As promised, we do a deep dive in the basics of Natural Language Processing (NLP), starting with Markov-based language models and vectorized text representation (without neural networks!).

## Code

* The `notebooks` folder contains exploratory code to cement our understanding of language modelling, in the "easy" discrete case (Markov models): `Intro_to_Markov_Language_Models` builds up language models with n-grams both "manually" and using a standard library, and finally contains the famous Norvig's [Spelling Corrector](https://norvig.com/spell-correct.html) - which is featured in your homework! Please note that the folder contains some small text files which are used as additional "datasets" in the code.
* It is unlikely that we will get to the `Intro_to_Text_Classification` notebook this week: in case we do, or you want to peek ahead, the code showcases how to prepare sparse vectors from text, and then apply standard classification models to solve a concrete business problem.

As usual, we use rye for dependency management: you can run your notebooks within a rye environment with `rye run jupyter lab`.

## Final project update

The weekly folder includes `Project_checklist.pdf`, which is a list of questions by topic that you should ask yourself as you make progress with your project: while this is not exhaustive or mandatory, being able to answer most (if not all) of the questions is a good indication of the maturity of the final project - if you have convincing answers, it means you're ready to build your final presentation!

Please note that some topics were still not covered in class (e.g. Deployment), so of course you are not expected to tackle those yet; however, for the topics we did address, you should be able to map slides and discussions to the relevant self-assessment questions.
