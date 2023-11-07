# Week 10

## Understanding metrics and nuanced testing

We continue from [Week 9](https://github.com/jacopotagliabue/MLSys-NYU-2023/blob/main/weeks/09/slides.pdf), and discuss how to build trust not just in our dataset and training procedures, but also in evaluation: how do we know models are doing the right thing?

The `notebooks` folder helps us investigating the failure mode of different models, to better appreciate how hard evaluation is in practice (we are focusing on evaluating performances _given a trained model_, as often we will be asked to evaluate a model we did _not_ train!).

To run the notebook, use rye as usual from the `notebooks` folder: `rye run jupyter lab`.

## Sharing model and data with a UI prototype

The `app` folder contains a Streamlit app that uses Metaflow Client API to retrieve the artifacts from the latest run from `small_flow.py` (make sure you run `small_flow.py` at least once successfully). Cd into `app`, run the app with rye: `rye run streamlit run app.py`.

A browser window will open with the app!

## Misc. Links

* [Streamlit](https://docs.streamlit.io/library/get-started) tutorial is a fantastic way to understand its main concepts
* Behavioral testing in NL: [Checklist](https://www.microsoft.com/en-us/research/publication/beyond-accuracy-behavioral-testing-of-nlp-models-with-checklist/)
* From your professor + Metaflow creators, [DAG Cards](https://arxiv.org/abs/2110.13601)
