# Homework #5 (due 11/22/2023)

## Task 1: add behavioral interactive testing to a pipeline with Streamlit (25%)

In the last assignment, we worked with the famous [Titanic dataset](https://www.kaggle.com/code/gusthema/titanic-competition-w-tensorflow-decision-forests), and completed a port of some "notebook code" into a Metaflow pipeline.

In class, we saw how [Streamlit](https://streamlit.io/) can be helpful to use simple Python commands to create beautiful interactive apps. Your first assignment is to take the model and code that you obtained by running Metaflow in HW 4, and create a new Streamlit app with the following requirements:

* a dropdown menu with `Sex` and `Pclass` (columns in the dataset) as options;
* when the user selects one of the categories, the app refreshes and showcases a per-group analysis of the model accuracy based on the category you selected: for example, for `Sex` the app will show a table with three rows, total accuracy, accuracy for `Sex=male` and `Sex=female` (the same should happen for `Pclass`, but number of rows may be different).

HINT: do you need to run predictions at every refresh, or can you pre-load in Streamlit directly some pre-made predictions and do _only_ the accuracy calculations at every refresh?

## Task 2: port and improve Peter Norvig typo-correction model (75%)

We talked in class about the Peter Norvig's [Spelling Corrector](https://norvig.com/spell-correct.html). Your assignment is fairly open-ended:

* port the spelling corrector to a Metaflow pipeline, with `IncludeFile` to include the training files, a training step to calculate the quantities of interest and an evaluation step;
* pick either the language model or the error model, and find ONE way to improve on the original design based on what we discussed in class;
* run your new model in parallel (using Metaflow branching capabilities) with the original one, and showcase that your model is actually achieving better performance than the one from Norvig: for example, you can use Comet to produce a dashboard with the accuracy of the two models, one next to each other.

Make sure your code is heavily commented, and that you explain in your submission in clear English what is your strategy to improve the model and why it works (HINT: you could examine errors in the original model, and find out ways to improve on those "slices", as we saw in class last week).
