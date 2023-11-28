# Week 12

## Introduction to Word Embeddings

Our NLP lecture concludes our deep dive into text classification by presenting two new methods to get vectors out of words: [word2vec](https://arxiv.org/abs/1301.3781) and [sentence embeddings](https://arxiv.org/abs/1908.10084).

## Code

* The `notebooks` folder contains exploratory code to cement our understanding of word embeddings, in the "easy" case of non-contextual embeddings: `Intro_to_Word_Embeddings` starts with training word embeddings from scratch, then loads pre-trained ones and finally showcases (as a black box API) sentence-level embeddings. We also show how the text classification pipeline we saw before can basically run just as well, swapping the old tf-idf vectors with the new neural ones.

As usual, we use rye for dependency management: you can run your notebooks within a rye environment with `rye run jupyter lab`.

## Final Project template

As a non-exhaustive, not-to-be-copied (the TA will check!), not finalize repo, the `project` folder contains a show-and-tell of a Metaflow pipeline training a text classification model and a [Flask web app](https://flask.palletsprojects.com/en/3.0.x/) serving predictions (so far we have seen mostly only streamlit as a way to serve predictions to users, but in our next lecture we will introduce web serving as well).

By providing a (non-complete) reference implementation, I hope to simplify your own comparisons when trying to understand if your project is sufficiently complete for the final presentation - by now all the code, comments, structure should be easy to parse for you, and the elements in the folder should be easy to map to the [Project Checklist](https://github.com/jacopotagliabue/MLSys-NYU-2023/blob/main/weeks/11/Project_checklist.pdf) from last week.

In particular:

* `my_flow.py` is the Metaflow version of the text classification pipeline we explained in class: while not necessarily exhaustive, it contains many of the features that the final course project should display (e.g. comments, qualitative tests, etc.). The flow ends by explictely storing the artifacts from the model we just trained;
* `my_app.py` shows how to build a minimal Flask app serving predictions from the trained model (note that the app relies on a small HTML page, making it similar to a streamlit-based interaction).

You can run both (`my_flow.py` first, obviously, to create the model to be served with an app later) using rye.
