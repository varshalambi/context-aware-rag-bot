# Context-Aware Conversational AI with RAG and GPT-4  

This project integrates Retrieval-Augmented Generation (RAG) with GPT-4 and Llama-3, enabling highly relevant and context-aware conversations. The system leverages vector search with Faiss to retrieve relevant documents and applies fine-tuned Llama-3 for enhanced response accuracy, improving customer interactions by 20%.  

## Table of Contents  
- [Introduction](#introduction)  
- [Prerequisites](#prerequisites)  
- [Installation](#installation)  
- [Getting Started](#getting-started)  
- [Usage](#usage)  
- [Key Features](#key-features)  
- [Contributing](#contributing)  

## Introduction  
This AI-powered chatbot integrates RAG with Llama-3 and GPT-4 to generate contextual responses. By retrieving relevant information from vector databases before generating responses, the chatbot improves accuracy and relevance in customer interactions. The system also incorporates Reinforcement Learning from Human Feedback (RLHF) to continuously refine its responses based on user interactions.  

## Prerequisites  
Before setting up the chatbot, ensure the following dependencies are installed:  

### System Requirements  
- Python 3.8+  
- A compatible GPU (optional, but recommended for performance boost)  

### Required Python Packages  
Install the following dependencies using pip:  

```bash
pip install langchain chainlit ctransformers faiss_cpu \
PyPDF2 torch accelerate bitsandbytes sentence_transformers \
huggingface_hub openai
```

### Installation
1. Clone the Repository
Run the following commands:

```bash
git clone https://github.com/your-repo-name.git  
cd your-repo-name  
```

2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv  
source venv/bin/activate  # Windows: venv\Scripts\activate  
```

3. Install Required Dependencies

```bash
pip install -r requirements.txt  
```

4. Download and Configure the Language Model
Download Llama-3 from Hugging Face or use GPT-4 via OpenAI API.
Configure the VECTOR_DB_PATH and other environment variables in the project as required.

### Getting Started
1. Prepare the Data
Before starting the chatbot, process and store documents in the vector database:

```bash
python preprocess.py
```

2. Run the Conversational AI
To launch the chatbot:

```bash
python run_chatbot.py
```

### Usage
The chatbot provides context-aware answers using RAG and GPT-4/Llama-3:

1. Start the chatbot by running run_chatbot.py.
2. Ask a question, and the system will retrieve relevant data from the Faiss vector database.
3. The LLM (GPT-4 or fine-tuned Llama-3) will generate an accurate, context-driven response.
4. If applicable, citations will be included in the response.
5. The model improves over time using RLHF, adapting based on user interactions.

### Key Features
Retrieval-Augmented Generation (RAG): Improves response relevance by dynamically retrieving relevant documents.
Fine-Tuned Llama-3 & GPT-4: Ensures high-quality, human-like responses.
Faiss Vector Database: Enables efficient similarity search for document retrieval.
RLHF Optimization: Learns from user feedback to refine responses continuously.

### Contributing
We welcome contributions. Feel free to submit a pull request or report issues.

