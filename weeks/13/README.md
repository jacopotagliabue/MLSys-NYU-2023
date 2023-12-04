# Week 13

## Serving predictions

First, make sure to setup the weekly env with `rye sync` and go into `src`; then quickly run the usual `small_flow.py` with Metaflow, to produce the model we will be serving (the script and the datasets are repeated in this week folder for convenience, but nothing has changed from previous weeks).

Now, you can spin up the endpoint and interact with it using `python my_app.py`, and then opening the browser at the url displayed in the terminal plus the endpoint name, `predict`, for example pasting `http://127.0.0.1:5000/predict?x=10` in the browser will return a JSON with the prediction of the model for the input `x=10`. A sample response may be:

```json
{
  "data": [
    203.84918292660672
  ],
  "metadata": {
    "eventId": "0e55b395-ab40-4ffc-823e-0898b242e123",
    "serverProcessingTime": 1,
    "serverTimestamp": 1701725802597
  }
}
```

The current endpoint is very barebone - check the slides and the `project` in week 12 for suggestions on how to best structure the response, and an example of enriching the presentation layer with a web page.

## Misc. Links

* If you want to try Fast API as an alternative to Flask, start with the [tutorial](https://fastapi.tiangolo.com/tutorial/).
* There are many ways to go from local to cloud deployment in a "better" (more scalable, principled) way than what we show with Flask. A cool framework that can used across many different setups is [BentoML](https://www.bentoml.com/).
* [Chip Huyen's book](https://www.amazon.com/Designing-Machine-Learning-Systems-Production-Ready/dp/1098107969) contains chapters on monitoring and re-training, if you want to go deeper in what happens after deployment.
