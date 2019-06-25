# Deploying a Sentiment Analysis Model using SageMaker

The notebook and Python files provided here, once completed, result in a simple web app which interacts with a deployed recurrent neural network performing sentiment analysis on movie reviews. This project assumes some familiarity with SageMaker, the mini-project, Sentiment Analysis using XGBoost, should provide enough background.

[image1]: ./img/negative_review.png "Negative Review"

## Project Overview
In this project, I used SageMaker to construct a complete project from end to end. The goal of this project is to have a simple web page which a user can use to enter a movie review. The web page will then send the review off to my deployed model which will predict the sentiment of the entered review.

![Negative Review][image1]

## Project Instruction

### Instruction

1. Clone the repository and navigate to the downloaded folder.
	```
		git clone https://github.com/ayowolet/Deploying-a-Sentiment-Analysis-Model
	```
2. Open the `SageMaker Project.ipynb` file. Of course, you can find HTML version of the file.
	```
		jupyter notebook SageMaker Proejct.ipynb
	```
3. Read and follow the instructions! You can find and download the dataset for this project in the notebook.

## Project Information

### Contents

- General Outline
- Step 1: Downloading the data
- Step 2: Preparing and Processing the data
- Step 3: Upload the data to S3
- Step 4: Build and Train the PyTorch Model
- Step 5: Testing the Model
- Step 6: Deploying the model for testing
- Step 7: Use the model for testing
- Step 6 (again): Deploy the model for the web app
- Step 7 (again): Use the model for the web app

### Libraries

The list below represents main libraries and its objects
for the project.
- [Amazon SageMaker](https://ap-northeast-2.console.aws.amazon.com/sagemaker/home?region=ap-northeast-2#/landing) (Build, train, and deploy a model)
- [PyTorch](https://pytorch.org) (LSTM classifier)

### Delete the Endpoint
Remember to always __SHUT DOWN YOUR ENDPOINT__ if you are no longer using it. You are charged for the length of time that the endpoint is running so if you forget and leave it on you could end up with an unexpectedly large bill.
```
	predictor.delete_endpoint()
```
