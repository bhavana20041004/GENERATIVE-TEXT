# GENERATIVE-TEXT

*COMPANY* : CODTECH IT SOLUTION

*NAME* : TALARI BHAVANA

*INTERN ID* : CT04DF313

*DOMAIN* : Artificial Intelligence

*DURATION* : 4 weeks 

*MENTOR* : NEELA SANTOSH

*DISCRIPTION* : This Python script demonstrates how to build a **text generation system** using a **pre-trained GPT-2 model** from Hugging Face’s `transformers` library. The goal of this model is to generate coherent and contextually relevant paragraphs based on a user-provided prompt. GPT-2 (Generative Pretrained Transformer 2), developed by OpenAI, is a powerful transformer-based language model that has been trained on a vast corpus of internet text. In this code, we begin by importing the necessary libraries: `GPT2LMHeadModel` and `GPT2Tokenizer` from the `transformers` module, along with PyTorch's `torch` module, which is used to handle tensor operations and GPU acceleration. The tokenizer is responsible for converting the input text into numerical format (token IDs) that the model can process, while the model itself predicts the most likely continuation of the text.

We initialize the GPT-2 model and tokenizer using the `from_pretrained()` method, which automatically downloads the pretrained weights and configuration files from the Hugging Face Model Hub. The script then determines whether a GPU is available using `torch.cuda.is_available()` and sets the computation device accordingly, which enhances performance if run in environments like Google Colab with GPU enabled. The model is set to evaluation mode using `.eval()` to ensure that dropout and batch norm layers behave appropriately during inference.

The core functionality is wrapped in the `generate_text()` function, which accepts a user prompt and generates a paragraph up to a specified maximum length (default 300 tokens). The input prompt is tokenized and passed to the model, and text is generated using parameters like `top_k`, `top_p`, `temperature`, and `no_repeat_ngram_size` to control the diversity and coherence of the output. `top_k=50` and `top_p=0.95` restrict the output to the most probable next tokens, `temperature=0.9` introduces randomness, and `do_sample=True` ensures that sampling is used over greedy decoding. These settings help in generating natural, readable, and less repetitive paragraphs.

Once the model generates the output tokens, they are decoded back into human-readable text using the tokenizer’s `decode()` method. The result is cleaned by stripping leading/trailing spaces and replacing newline characters with spaces for better paragraph formatting. A final check ensures that the paragraph ends with proper punctuation for grammatical completeness.

The script prompts the user to enter a topic at runtime and then generates and prints the output paragraph in a neat format. This kind of model can be applied in content generation, creative writing, educational assistance, chatbot development, and more. The use of GPT-2 offers a balance between simplicity and performance, making it suitable for tasks that require fluent and context-aware language generation without needing to train a model from scratch. Overall, this script effectively showcases how pre-trained transformer models can be harnessed for real-world NLP applications with minimal setup and code.



