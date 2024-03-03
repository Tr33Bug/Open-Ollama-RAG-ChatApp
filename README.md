# Open-Ollama-RAG-ChatApp
Retrieval-Augmented Generation Chat Bot using Ollama, Langchain and Gradio.

## Idea
The notebook is a proof of concept on how to build a retrieval-augmented generation chatbot using Ollama, Langchain and Gradio. The chatbot is built using the following components:
- Ollama is used as backend to host large language models and provide an API to interact with them.
- Langchain is used as library to generate chunks from provided markdown files and embedd them using Ollama. The embeddings are stored in a chroma database.
- Gradio is used to provide a simple chat interface to interact with the RAG-Chatbot.

## Installation
1. Recommended to use a virtual environment using python version 3.11.
2. Install ollama following the installation instructions from the [Ollama Github Repository](https://github.com/ollama/ollama).
3. Pull the desired model for ollama and start the ollama backend using the following command:
```bash
# change model to the desired model name -> see https://ollama.com/library for other models
ollama pull llama2:chat
ollama start
```
4. Uncomment the first cell in the notebook and run it to install the required packages.
5. On first run set the `initial_db = True`. This will create new embeddings for the provided markdown files and create a new chroma db in the given path (`DATA_PATH = "data/"`).
6. Drop your own markdown files in the `data/` folder. 
7. Run the notebook. 

## References
- Ollama: [Ollama Github Repository](https://github.com/ollama/ollama)
- Langchain: [Langchain Documentation](https://python.langchain.com/docs/get_started/introduction)
- Gradio: [Gradio Chatinterface Documentation](https://www.gradio.app/docs/chatinterface)
- Similar Project: [Langchain RAG Tutorial by pixegami](https://github.com/pixegami/langchain-rag-tutorial)