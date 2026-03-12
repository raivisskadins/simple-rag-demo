# simple-rag-demo
A Simple RAG demo project

## Setup

1. First of all, you will need Python. This notebook has been tested with version 3.12.0, but it should also be compatible with other recent versions.
2. Clone the repository.
3. Create a `.env` file in the root directory with your secrets:

```
AZURE_OPENAI_API_KEY=your_key_here
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_API_VERSION=2024-02-01
AZURE_OPENAI_CHAT_DEPLOYMENT=gpt-4o
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=text-embedding-3-large
```
You can use the `.env.example` file to create your own `.env` file. The `.env` file is a local configuration file that will not be saved in Git (it's excluded via `.gitignore`). 

The secrets neccesary to access the LLM can be obtained from Azure.

The Azure OpenAI *gpt-4o* model is used for generating answers. To obtain access to this model, an Azure OpenAI resource must be created in [portal.azure.com](https://portal.azure.com/). After that, open [Azure OpenAI Studio](https://oai.azure.com/), select *Deployments*, and deploy the **gpt-4o** model. The value of *Deployment name* should be the same as the *Model name* — `gpt-4o`.

See more details [here](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/overview).

The `.env` file must contain the corresponding configuration values for the model: `AZURE_OPENAI_KEY`, `AZURE_ENDPOINT`, and `AZURE_OPENAI_VERSION`.

4. setup a virtual environment and activate it.

On Linux
```bach
python3 -m venv .venv
source .venv/bin/activate
```
On Windows
```bach
python -m venv .venv
.venv\Scripts\activate.bat
```

5. Install required packages:

```bash
pip install -r requirements.txt
```

5. Open the notebook `simple_rag_demo.ipynb` and run the cells.

## License

Apache License Version 2.0, January 2004