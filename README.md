# README: Real-Time RAG-Based LLM Application Using Pathway

## Demo video:






https://github.com/user-attachments/assets/5080d0d0-b04d-4d49-bf97-bf7d0f87db4d








## Table of Contents
1. [Introduction](#introduction)
2. [Key Features](#key-features)
3. [Installation](#installation)
4. [Setup](#setup)


## Introduction

This project is a **Real-Time Retrieval-Augmented Generation (RAG)-Based Language Model (LLM) Application** built using **Pathway**, a real-time processing engine. This application enhances the capabilities of large language models (LLMs) by integrating external knowledge retrieval from real-time data sources. It is designed to dynamically retrieve relevant documents or information from various knowledge bases, enhancing the model's ability to answer complex questions with up-to-date information.


## Key Features

- **Real-Time Data Retrieval**: Integrates with live databases, APIs, and other sources of information to provide relevant context for language generation.
- **Flexible LLM Integration**: Can work with any large pre-trained language model, such as GPT, BERT, or other transformer-based models.
- **Retrieval-Augmented Generation (RAG)**: Uses a retriever to fetch the most relevant documents from external data sources, which are then passed to the generator model to produce context-aware responses.



## Installation

### Prerequisites
- **Python 3.8+**
- **Pathway** (Install via `pip install pathway` or see [Pathway documentation](https://github.com/pathwaycom/pathway) for more options)
- **Docker Desktop**

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/afrashamim/RAG-based-LLM-application.git
   
2. Create Gemini API Key:
   Create a Gemini API Key in the .env file

3.Build the docker image:

  ```bash
    docker build -t raggemini .
```
4.After ruuning the docker image:
 ```bash

  docker run -v "$(pwd)/data:/app/data" -p 8000:8000 --env-file .env raggemini
```

5.Enter your prompt:
```bash

  curl -X 'POST' 'http://localhost:8000/v1/pw_ai_answer' -H 'accept: /' -H 'Content-Type: application/json' -d '{
  "prompt": "enter your prompt"
}'
```


## Contributing

It is possible to extend this project by building a front-end by an open-source framework streamlit or any other framework and connecting this project as the back-end.
