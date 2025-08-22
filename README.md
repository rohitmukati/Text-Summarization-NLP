# End to end Text-Summarizer-Project

## Workflows

## 📂 Folder Structure

📦 Text-Summarization-NLP  
├── 📁 .github  
│   └── 📁 workflows  
│       └── main.yaml  
│  
├── 📁 config  
│   └── config.yaml  
│  
├── 📁 research  
│   ├── 01_data_ingestion.ipynb  
│   ├── 02_data_validation.ipynb  
│   ├── 03_data_transformation.ipynb  
│   ├── 04_model_trainer.ipynb  
│   ├── 05_Model_evaluation.ipynb  
│   ├── Text_Summarization.ipynb  
│   └── trials.ipynb  
│  
├── 📁 src  
│   └── 📁 textSummarizer  
│       ├── 📁 config  
│       │   ├── __init__.py  
│       │   └── configuration.py  
│       │  
│       ├── 📁 conponents  
│       │   ├── __init__.py  
│       │   ├── data_ingestion.py  
│       │   ├── data_transformation.py  
│       │   ├── data_validation.py  
│       │   ├── model_evaluation.py  
│       │   └── model_trainer.py  
│       │  
│       ├── 📁 constants  
│       │   └── __init__.py  
│       │  
│       ├── 📁 entity  
│       │   └── __init__.py  
│       │  
│       ├── 📁 logging  
│       │   └── __init__.py  
│       │  
│       ├── 📁 pipeline  
│       │   ├── __init__.py  
│       │   ├── prediction.py  
│       │   ├── stage_01_data_ingestion.py  
│       │   ├── stage_02_data_validation.py  
│       │   ├── stage_03_data_transformation.py  
│       │   ├── stage_04_model_trainer.py  
│       │   └── stage_05_model_evaluation.py  
│       │  
│       └── 📁 utils  
│           ├── __init__.py  
│           └── common.py  
│  
├── .gitignore  
├── Dockerfile  
├── LICENSE  
├── README.md  
├── app.py  
├── main.py  
├── params.yaml  
├── requirements.txt  
├── setup.py  
├── template.py  
└── test.py  


# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/rohitmukati/Text-Summarization-NLP
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n summary python=3.8 -y
```

```bash
conda activate summary
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```


```bash
Author: rohitmukati
Data Scientist
Email: rohanmukati2002@gmail.com

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/text-s

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app
