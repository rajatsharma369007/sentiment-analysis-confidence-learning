# Summary of the project

This project will serve as a practical application to assess how confidence learning can improve the accuracy and reliability of sentiment analysis in a dynamic, real-world environment. It involves training a sentiment classifier using a 3-layer MLP model built on top of pre-computed BERT features. The steps to complete the project are as follows:

1. Understanding CleanLab - Begin by reading a summary on the confidence learning algorithm and familiarize yourself with CleanLab(opens in a new tab), a Python library for identifying label quality issues.

2. Setup AWS S3 - Access the AWS console, create an S3 bucket, and upload the provided data files to the bucket's data folder.

3. Configuration - Fill out the necessary parts in the Confidence_Learning.ipynb notebook and main.py. In the notebook, handle data input in SageMaker, configure the PyTorch Estimator, and initiate a training job. In main.py, implement cross-validation, confidence learning using CleanLab, and correct erroneous labels. Then, retrain and re-evaluate the sentiment classifier.

4. Copy Training Artifacts - Copy the training artifacts from the S3 bucket to the local directory using the AWS CLI, and decompress them into a directory.

5. Deployment - Deploy the trained model to an endpoint.

The project essentially involves using CleanLab for label quality assessment, training a sentiment classifier using PyTorch on AWS SageMaker, and deploying the trained model to an endpoint for sentiment analysis.


---

# Dependencies
The dependencies are listed in requirements.txt. Execute the following command to install the required libraries.
```
pip install -r requirements.txt
```

---


# Files in the Repo

* data
	- train.csv
	- test.csv
	- dev.csv
* extracted_training_artifacts
	- final-results.json
	- pre-annotations.json
	- pre-results.json
	- prob.csv
	- placeholder.txt
* screenshots
* src
	- product_review_embeddings.py
	- review_data_module.py
	- sentiment_classifier_system.py
* Confidence_Learning.ipynb
* main.py
* requirements.txt
* README.md


---

# Expected Result
With one epoch of training, we expect the Confidence Learning algorithm to increase the accuracy from 90% to 93%.

---

# License

[License](https://github.com/udacity/cd13451-sentiment-analysis-project/blob/main/LICENSE.txt)




