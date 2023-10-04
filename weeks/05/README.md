# Week 6

## Fraud Case Study

You can run `rye sync` in this directory in order to install all necessary python packages for running the below notebooks.

## Notebooks

- [trees_and_esnelmbes.ipynb](./notebooks/trees_and_esnelmbes.ipynb) introduces decsion trees and random forests. This notebook uses a dataset from Week 4.
- [imbalanced_learning.ipynb](./notebooks/imbalanced_learning.ipynb) shows some scikit-learn methods for handling imbalanced datasets.

## Misc

- `src/` contains a package called `my_package` that shows how to create a Python package.
  - When you run `rye sync`, it will install this package (note that `pyproject.toml` lists the name of the package as `my_package`. `rye` will automatically search inside of `src` for a directory named `my_package` in order to install this package).
  - After running `rye sync`, you will be able to import `my_package` from a python shell.
  - `run.py` shows how to write a script that uses this package. You can run `python run.py` in order to see this file run. Try to understand the order of imports!
