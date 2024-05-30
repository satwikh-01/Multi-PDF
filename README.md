# Multi-PDF Chat App
## Overview

Multi-PDF Chat App is all about integrating different AI models to handle images and PDFs in a single chat interface.

## Features

- **Quantized Model Integration**: This app uses what are called "quantized models." These are special because they are designed to work well on regular consumer hardware, like the kind most of us have at home or in our offices. Normally, the original versions of these models are really big and need more powerful computers to run them. But quantized models are optimized to be smaller and more efficient, without losing much performance. This means you can use this app and its features without needing a super powerful computer. [Quantized Models from TheBloke](https://huggingface.co/TheBloke)


- **Image Chatting with LLaVA**: The app integrates LLaVA for image processing, which is essentially a fine-tuned LLaMA model equipped to understand image embeddings. These embeddings are generated using a CLIP model, making LLaVA function like a pipeline that brings together advanced text and image understanding. With LLaVA, the chat experience becomes more interactive and engaging, especially when it comes to handling and conversing about visual content. [llama-cpp-python repo for Llava loading](https://github.com/abetlen/llama-cpp-python)

- **PDF Chatting with Chroma DB**: The app is tailored for both professional and academic uses, integrating Chroma DB as a vector database for efficient PDF interactions. This feature allows users to engage with their own PDF files locally on their device. Whether it's for reviewing business reports, academic papers, or any other PDF document, the app offers a seamless experience. It provides an effective way for users to interact with their PDFs, leveraging the power of AI to understand and respond to content within these documents. This makes it a valuable tool for personal use, where one can extract insights, summaries, and engage in a unique form of dialogue with the text in their PDF files. [Chroma website](https://docs.trychroma.com/)


## Procedure

1. **Create a Virtual Environment**: Use Python 3.10.12 

2. **Upgrade pip**: ```pip install --upgrade pip```

3. **Install Requirements**: ```pip install -r requirements.txt```

```pip install -r pip_freeze.txt```
   


4. **Setting Up Local Models**: Download the models and make a new folder llava: [ggml-model-q5_k.gguf](https://huggingface.co/mys/ggml_llava-v1.5-7b/resolve/main/ggml-model-q5_k.gguf?download=true) and [mmproj-model-f16.gguf](https://huggingface.co/mys/ggml_llava-v1.5-7b/resolve/main/mmproj-model-f16.gguf?download=true) is the llava model used for image chat. 
And the **quantized mistral model** is stored directly in **models sub-directory** that forms TheBloke and download below two models- [mistral-7b-instruct-v0.1.Q5_K_M.gguf](https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF/resolve/main/mistral-7b-instruct-v0.1.Q3_K_M.gguf?download=true) and [mistral-7b-instruct-v0.1.Q3_K_M.gguf](https://huggingface.co/TheBloke/Mistral-7B-Instruct-v0.1-GGUF/resolve/main/mistral-7b-instruct-v0.1.Q3_K_M.gguf?download=true).

5. **Enter commands in terminal**: 
   1. ```python3 database_operations.py``` This will initialize the sqlite database for the chat sessions.
   2. ```streamlit run app.py```


