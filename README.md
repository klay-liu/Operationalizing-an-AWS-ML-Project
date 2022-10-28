# Operationalizing an AWS ML Project



## Project Introduction

The purpose of this project is to adjust, enhance, configure, and ready the model for production-grade deployment using a number of significant AWS tools and features, including AWS Sagemaker, Lambda Functions, and EC2 instances. 

Imagine that a data scientist has completed all of the ML model's coding, and that the raw ML code is undoubtedly not something that can be delivered to the business. These ML codes must be deployed to the production environment.

In order to train and deploy the model in Sagemaker by using the ML code in submission notebook. Afterward, we use lambda to invoke the endpoint. To meet the demands of the business team for high-throughput and low latency, we set concurrency for the lambda and auto-scaling for the endpoint in this process. To further guarantee the security of our project, we configured the IAM Role and its corresponding policies.

## Files

- `train_and_deploy-solution.ipynb`: this is a notebook that contains code for training and deploying a computer vision model on AWS
- `hpo.py`: this is a Python script that ] the **train_and_deploy-solution.ipynb** notebook can use as its "entry point."
- `lambdafunction.py`: this is a Python script for your Lambda function.
- `infernce2.py`: this is a Python file that can be used for deploying the trained model to an endpoint.
- `ec2train1.py`: this is a Python file that can be used for training a model on an EC2 instance.
- `/screenshot`: all the screenshots for the components in the project.
- `writeup.pdf`: a writeup to describe the decision I made during the project and justification for them.



## Steps

**Step 1: Training and deployment on Sagemaker**

​	Set up a Sagemaker Instance and run the `train_and_deploy-solution.ipynb`.

**Step 2: EC2 Training**

​	Preparing for EC2 model training

​	Training and saving on EC2

**Step 3: Lambda function setup**

​	use `lambdafunction.py`

**Step 4: Security and testing**

​	test event for Lambda Function:

​	`{ "url": "https://s3.amazonaws.com/cdn-origin-etr.akc.org/wp-content/uploads/2017/11/20113314/Carolina-Dog-standing-outdoors.jpg" }`

**Step 5: Concurrency and auto-scaling**