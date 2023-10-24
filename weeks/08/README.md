# Week 8

## Structuring ML projects with Metaflow

* `src` is the folder containing the scripts we described during the class;
* `notebooks` is the folder containing a notebook showcasing Metaflow API;
* `pyproject.toml` holds the Python dependencies required for running the scripts (use `rye sync` as usual etc.).

Notes: 

* to run `small_flow.py`, you need to use the Metaflow syntax `python small_flow.py run`.
* to run the notebook, use rye as usual: `rye run jupyter lab`.

## Data

* `regression_dataset.txt` is a fake regression dataset to run the code - you can generate another dataset with different parameters or cardinality using the `create_fake_dataset.py` script.

## External links and misc. stuff

* [Metaflow sandbox](https://outerbounds.com/sandbox/)
* [Metaflow paper](https://arxiv.org/pdf/2303.11761.pdf)
* [Your professor's blog post](https://medium.com/towards-data-science/noops-machine-learning-3893a42e32a4)
