# LLAMA-AI-Agent
An offline chatbot built in Python using `llama-cpp-python` and a LLaMA `.gguf` model, running directly in a Jupyter Notebook. It lets you interact with a local large language model in a simple Q&amp;A format.
# 🦙 LLAMA AI Agent – Local Chatbot in Jupyter Notebook

This project is a simple offline chatbot built with Python using the `llama-cpp-python` library. It loads a local LLaMA `.gguf` model and runs fully within a Jupyter Notebook interface.

## ✅ Features

- Interact with a powerful language model completely offline
- Simple Q&A prompt format
- Easy to modify and experiment within Jupyter
- Requires no internet once the model is downloaded

## 🛠️ Requirements

- Python 3.8+
- Jupyter Notebook
- `llama-cpp-python` library
- A `.gguf` format LLaMA model file (e.g., `llama-2-7b.Q2_K.gguf`)

## 📦 Installation

1. Install the required Python package:

```bash
pip install llama-cpp-python
On macOS, if you face any issues, you may also need:
brew install cmake libomp
Download a .gguf model from TheBloke's Hugging Face page or similar sources. Example:
llama-2-7b.Q2_K.gguf
🚀 How to Use

Open the LLAMA AI Agent.ipynb notebook in Jupyter.
Make sure the model_path is set correctly to point to your .gguf model.
Run the notebook cells to launch the chatbot interface.
Example Code Snippet
from llama_cpp import Llama

# Load the model
llm = Llama(model_path="/path/to/your/llama-2-7b.Q2_K.gguf")

while True:
    prompt = input("You: ")
    if prompt.lower() == "exit":
        break

    formatted_prompt = f"Q: {prompt}\nA:"
    response = llm(formatted_prompt, max_tokens=100, stop=["Q:", "\n"], echo=False)
    print("LLaMA:", response["choices"][0]["text"].strip())
Sample Output
You: What is the capital of France?
LLaMA: Paris.

You: Who wrote Harry Potter?
LLaMA: J.K. Rowling.

You: exit
📁 Files

LLAMA AI Agent.ipynb – Main Jupyter notebook for running the chatbot
.gguf model file – (You must download this separately)
🧠 Credits

llama-cpp-python by @abetlen
Meta AI – LLaMA model creators
Quantized models by TheBloke
