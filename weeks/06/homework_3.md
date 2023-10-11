# Homework 3

Please submit a single python file for this entire homework. Each question asks you to print out information, so your single script should print out the answer to each question. Your script should only use standard python or the libraries that are included in `pyproject.toml`. Your grader should be able to run your script from the command line like:

```commandline
python homework_3.py
```

You can assume that your grader is running the script from the same folder that this document is in.

#### Also

While you are free to write your code however you want, you are expected to clean up the code prior to submitting it for grading. Primarily, this means remove commented code or unnecessary comments from your code. For example, if you write the code in a Jupyter notebook and export it to a script, then you should remove the comments indicating the cell numbers.

Machine learning is a team sport, and good team members make it easy for their teammates to read their code.

## Dataset

I have constructed a fake Fraud dataset for this homework assignment. There are 3 CSVs in `data/`:

### payments.csv
Each row of this CSV corresponds to an individual payment. The columns are:

- `id`: A unique ID for the payment.
- `merchant_id`: The unique ID of the merchant who took the payment.
- `buyer_id`: The unique ID of the buyer who made the payment.
- `transaction_timestamp`: The time at which the payment occurred. 
- `payment_amount`: The number of US Cents associated with the payment.
- `chargeback_timestamp`: The timestamp that a chargeback was issued against the payment, if there was one. If there is a chargeback timestamp, then we assume the payment was fraudulent. If there is no chargeback timestamp, then we assume this was a non-fraudulent payment.

### merchants.csv
Each row corresponds to a Merchant that processes payments. The columns are:
- `id`: The unique ID of the merchant.
- `country`: The country in which the merchant is located.
- `category`: The category of business that the merchant is in.

### buyers.csv
Each row corresponds to a buyer who makes a payment. The columns are:
- `id`: The unique ID of the buyer.
- `country`: The country in which the buyer is located.


## 1. Waiting For Chargebacks (25%)

In order to properly train and test a model, you must ensure that you're only using information to train the model that you would have at the time that you are predicting with the model. 

For the Fraud dataset, we assume that if there is no chargeback then the payment was not fraudulent. However, a payment for yesterday may have a chargeback tomorrow. This means that I will think that that was a good payment today, whereas tomorrow I'll know that it was fraudulent. Using the dataset(s), determine how many days you must wait after a payment is processed such that 95% of all payments that will eventually receive a chargeback have received a chargeback within that many days.

Your script should read in the appropriate dataset(s) and print out the number of days.

## 2. Train / Test Split (25%)

This question involves thinking through how to construct a training and test set if you want to build an ML model to predict fraud. Remember, training and test sets should approximate real world scenarios as much as possible.

Using the payments data, construct a test set containing the last 30 days worth of data and a training dataset containing as much data as possible. You should only use data in the training dataset for which you would be 95% confident in the ground truth labels by the start of the test data (i.e. use your answer from part 1). This is meant to approximate the scenario where you train and deploy your model on the same day.

In your script, divide the payments up into training and test data and print out the start and end timestamp of each dataset.


## 3. Historical Features (25%)

For each payment, calculate the average fraud rate for the merchant and the buyer. If there are no prior transactions, then assume that the rate is zero. Note: your features should be calculated using only information that is known at the time of the transaction. 

In order to verify your answer, your script should print out the sum of average merchant fraud rates for all payments plus the sum of average buyer fraud rates for all payments.


## 4. Make a Model (25%)

For the final question, you should build an ML model to predict fraud. Your model should join together the payments, merchant, and buyer data and use the following features:

- payment_amount
- merchant category
- merchant country
- buyer country
- merchant fraud rate (from question 3)
- buyer fraud rate (from question 3)

Split your data up into training and test data using your answers from question 2, train a model on the training data, and evaluate the model's area under the ROC curve (AUC) on the test data. Print out the AUC at the end. You model will likely perform poorly, and that's ok! Fraud is hard.

