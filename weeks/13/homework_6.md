# Homework #6 (due 12/13/2022)

## Task 1: integrate the Flask model endpoint into a Streamlit app (100%)

Let's consider again the Flask endpoint shown in class, that takes as input a `x` and returns a JSON with a prediction and some metadata.

As we discussed, endpoints are typically built for machine-to-machine communication, and then responses are "wrapped" in a nice UI (like an app, or a web page) to be understood and consumed by humans. For this homework, we simulate a tiny "distributed system" in your laptop, built with two tiers:

* a "back-end" tier, composed by a Flask app serving model predictions (you can re-use the code in this week `src` folder as is!);
* a "front-end" tier, composed by a new Streamlit app that accepts a numerical input from the user, performs a GET request to your Flask app with that input, and displays the prediction (i.e. the app needs to call `http://127.0.0.1:5000/predict?x=10` if `10` is what the user puts into the form, and then parse the JSON it gets!)

The app you need to build is very simple (one input field only, one output section): compare this design to the app we built in week 10 (the code in the section `# play with the model`) - how is this different? Note that the "front-end" (what the user sees) may be absolutely identical, even if the "back-end" is now powered in a different way.
