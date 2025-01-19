# Generate README.md
readme_content = """
# Medical Chatbot with Generative AI and Pinecone Integration

## Overview

This project implements a **Medical Chatbot** using **Flask**, **LangChain**, **Pinecone**, and **OpenAI's GPT models**. It allows users to input medical-related queries and retrieves relevant context from preprocessed documents to generate accurate, concise responses. The system leverages Pinecone for efficient vector storage and retrieval and integrates Hugging Face embeddings for document encoding.

# End-to-End-Machine-Learning-Pipeline


## Workflows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the app.py



# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/tanvircs/Aws-Machine-Learning-Pipeline.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.8 -y
```

```bash
conda activate Mlproj
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
python app.py
```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in Aws


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
    - Save the URI: 315865595366.dkr.ecr.us-east-1.amazonaws.com/winerepo

	
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


---

## Features

- **Document Preprocessing**: Extracts and splits documents into manageable text chunks.
- **Vector Storage**: Uses Pinecone for indexing and storing embeddings.
- **Intelligent Retrieval**: Retrieves relevant documents based on user queries.
- **Language Model Integration**: Utilizes OpenAI GPT for generating responses.
- **User-Friendly Web Interface**: A simple Flask-based front end for user interaction.

---

## Project Structure

```plaintext
.
├── app.py                # Main Flask application
├── src/
│   ├── __init__.py       # Package initialization
│   ├── helper.py         # Helper functions for embeddings and document processing
│   ├── prompt.py         # Prompt templates for the LLM
├── setup.py              # Setup file for project dependencies
├── requirements.txt      # Python package dependencies
├── store_index.py        # Index creation and data addition to Pinecone
├── template.py           # File structure initialization script
├── research/
│   ├── trials.ipynb      # Jupyter notebook for experimentation
├── test.py               # Test script
```

## Prerequisites
- Python 3.8+
- Pinecone API Key
- OpenAI API Key

## Key Libraries
- flask
- langchain
- sentence-transformers
- pinecone
- python-dotenv

## Setup Instructions
### 1. Clone the Repository
```bash
git clone https://github.com/your-username/medical-chatbot.git
cd medical-chatbot
```
### 2. Clone the Repository
```bash
pip install -r requirements.txt
```
### 3. Install Dependencies
```bash
PINECONE_API_KEY=your_pinecone_api_key
OPENAI_API_KEY=your_openai_api_key
```
### 4. Initialize the File Structure (Optional)
```bash
python template.py
```
### 5. Preprocess Data and Create Index
```bash
python store_index.py
```
### 6. Start the Application
```bash
python app.py
```

## Created with ❤️ by Tanvir Ahmed.
This README file provides a clear and comprehensive guide for using and understanding your Medical Chatbot application. 
