# Homework #4 (due 11/08/2023)

## Task 1: refactoring existing code into a pipeline (75%)

In this assignment, we will be porting existing code from [Kaggle](https://www.kaggle.com/code/gusthema/titanic-competition-w-tensorflow-decision-forests) into a Metaflow class. Machine learning is a team sport, and understanding, re-factoring, improving other people's code is a fundamental part of the job.

In particular, we will start from this nice [tutorial](https://www.kaggle.com/code/gusthema/titanic-competition-w-tensorflow-decision-forests) with the goal of producing a functionally equivalent Metaflow flow:

* make sure you download a local copy of the Titanic dataset and use Metaflow `IncludeFile` to add it to the pipeline (check again Metaflow docs and  Week 08 example if you're unsure);
* the tutorial is already nicely divided in sections, which map to nodes in a DAG not unlike the examples we saw in class: keep it simple, and do a first pass by only including code from `data preparation`, `train with default parameters`, `make_predictions`;
* make sure you use `self` properly to pass data between steps in Metaflow;
* in a notebook, use the Metaflow client API to retrieve the training dataset used in the last successful flow, and produce a plot showcasing the distribution of the variable `Age` in the training set.

HINT: `self` use [pickle](https://docs.python.org/3/library/pickle.html) to store and retrieve Python objects between steps. This implies that objects that are not pickable, such as the [Tensorflow objects](https://stackoverflow.com/questions/71492778/how-to-save-tensorflow-model-to-pickle-file) used in the tutorial, cannot be passed around between training and prediction steps using `self`. What you want is a way to _serialize_ and _load_ a Tensorflow model that is "pickeable" as well.

Make sure your code is readable, dependencies are well defined etc. etc.: submit both the Metaflow pipeline and the notebook code.

## Task 2: Experiment tracking with Comet and hyperparameter tuning (25%)

Thanks to our partnership with Comet ML, we can use their experiment tracking tool for free! We discussed the importance of experiment tracking in the class, and in this assignment you will be asked to start doing it!

First, use `rye` to build your weekly environment and make sure you are able to understand and run correctly the `comet_playground.py` file. You are now ready for the second part of the homework.

Duplicate the Metaflow class you built from Task 1, and modify it so that you will:

* have a validation split, not just a train and test split;
* use Metaflow parallelization capabilities (foreach or branch!) to train multiple models: pick one hyperparameter you like (`min_examples`, `num_trees`, etc.) and a range of realistic values, and train multiple models each one taking a distinct value (check this [section](https://www.kaggle.com/code/gusthema/titanic-competition-w-tensorflow-decision-forests#Train-model-with-improved-default-parameters) for examples of which parameter to pick);
* evaluate all the models you trained on the validation set and pick the best one;
* make sure to log the experiments in Comet: does the dashboard clearly show what model is the best? Note that the end visualization should look not very unlike the one you get by running the `comet_plaground.py` example, as that also features a hyper-parameter search.

When you submit the code, submit both the new script and screenshot from your Comet dashboard, clearly illustrating the tracking (you could also share the dashboard link with your TA).

Useful links: [Comet scikit docs](https://www.comet.com/docs/v2/integrations/ml-frameworks/scikit-learn/)
, [Metaflow foreach docs](https://docs.metaflow.org/metaflow/basics).
