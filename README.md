# 🩺 Medical Chatbot with Generative AI and Pinecone Integration

## Overview
The **Medical Chatbot** leverages **Flask**, **LangChain**, **Pinecone**, and **OpenAI's GPT models** to provide users with accurate responses to medical-related queries. This system processes documents, encodes them using Hugging Face embeddings, and utilizes Pinecone for efficient vector storage and retrieval, delivering intelligent and concise responses through a user-friendly web interface.

---

## ✨ Features
- **Document Preprocessing**: Splits and processes large text documents into manageable chunks.
- **Vector Storage**: Efficient indexing and storage using Pinecone.
- **Intelligent Retrieval**: Retrieves relevant context for user queries.
- **Generative AI Integration**: Powered by OpenAI GPT models for natural language understanding.
- **Simple Web Interface**: Easy-to-use interface built with Flask.

---

## 🚀 Workflows

1. **Update Configuration Files**:
   - `config.yaml`
   - `schema.yaml`
   - `params.yaml`
2. **Modify the Entity and Configuration Manager**:
   - `src/config/`
3. **Adjust Pipeline Components**:
   - `main.py`
   - `app.py`

---

## 🛠️ Setup Instructions

### Prerequisites
- Python 3.8+
- **Pinecone API Key**
- **OpenAI API Key**

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/medical-chatbot.git
cd medical-chatbot
```

### 2️⃣ Create a Virtual Environment
```bash
conda create -n medical-chatbot python=3.8 -y
conda activate medical-chatbot
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Set API Keys
Create a `.env` file with the following:
```plaintext
PINECONE_API_KEY=your_pinecone_api_key
OPENAI_API_KEY=your_openai_api_key
```

### 5️⃣ Preprocess Data and Create Index
```bash
python store_index.py
```

### 6️⃣ Start the Application
```bash
python app.py
```

---

## 🌐 Deployment on AWS with GitHub Actions

### 1️⃣ AWS Setup
1. **Login to AWS Console**.
2. **Create an IAM User** with:
   - EC2 Access: For virtual machine deployment.
   - ECR Access: To save Docker images.

### 2️⃣ AWS Policies
Assign the following policies:
- `AmazonEC2ContainerRegistryFullAccess`
- `AmazonEC2FullAccess`

### 3️⃣ Create ECR Repository
Store your Docker image URI:
```plaintext
<aws_account_id>.dkr.ecr.<region>.amazonaws.com/<repository_name>
```

### 4️⃣ Set Up EC2 Instance
1. Launch an Ubuntu EC2 instance.
2. Install Docker:
   ```bash
   sudo apt-get update -y
   sudo apt-get install docker.io -y
   ```

### 5️⃣ Configure GitHub Secrets
Set the following secrets in your repository:
```plaintext
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=
AWS_ECR_LOGIN_URI=
ECR_REPOSITORY_NAME=
```

### 6️⃣ Deploy
1. Build and push the Docker image.
2. Pull the image from ECR to EC2.
3. Run the containerized application.

---

## 📂 Project Structure
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

---

## ❤️ Credits
**Developed by**: Tanvir Ahmed  
**GitHub**: [tanvircs](https://github.com/tanvircs)

---

This README file ensures a clear structure, eliminates redundancy, and provides step-by-step guidance to enhance readability and professionalism.
