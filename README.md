# RAG Tutorials and Experiments

**A learning repository for retrieval-augmented generation, document ingestion, vector search, evaluation, and agentic RAG.**

This repository collects notebooks, Python modules, and an application entry point exploring RAG workflows. It includes document-processing experiments, embedding generation, vector-store utilities, retrieval, evaluation, and agentic-RAG material.

## Topics covered

- Loading and preparing documents for retrieval.
- Splitting and processing document content.
- Generating text embeddings.
- Building and querying vector stores.
- Retrieval-augmented generation concepts and evaluation.
- LangChain and LangGraph experiments.
- FAISS, Chroma, and Typesense-related examples.
- Agentic RAG and vectorless/PageIndex learning notebooks.

The repository is an educational collection. Individual notebooks may represent separate experiments and may have different setup requirements.

## Technology

Python, LangChain, LangGraph, Sentence Transformers, FAISS, ChromaDB, PyMuPDF, pypdf, Typesense, and provider integrations listed in `requirements.txt`.

## Requirements

- Python 3.10+ recommended; choose a version supported by the installed ML libraries.
- pip
- Sufficient RAM and disk space for embedding models and vector indexes.
- API credentials only for notebooks that call external model providers.

## Installation

```bash
git clone https://github.com/nyohleonard-nlktech/RAG-Tutorials.git
cd RAG-Tutorials

python -m venv .venv
```

Activate the environment:

```bash
# macOS / Linux
source .venv/bin/activate

# Windows PowerShell
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Some notebooks may require additional packages or service configuration not needed by the other examples. Install only the dependencies required by the notebook you intend to run.

## Explore the notebooks

Start Jupyter:

```bash
pip install jupyter
jupyter lab
```

Open the notebooks in the repository root and in the `notebook/` and `agenticrag/` directories.

## Run the application

The repository contains an `app.py` entry point. Its exact runtime requirements depend on the application code and any external services it uses. Inspect the file before launching it; do not assume every notebook dependency is needed by the app.

## Source modules

```text
.
├── src/
│   ├── data_loader.py
│   ├── embedding.py
│   ├── search.py
│   └── vectorstore.py
├── notebook/
├── agenticrag/
├── app.py
├── books.jsonl
├── requirements.txt
└── README.md
```

## Configuration and secrets

Some examples integrate with hosted LLM or search providers. Store credentials in environment variables or a local `.env` file that is excluded by Git. Never commit API keys, private documents, or user data.

## Suggested learning path

1. Start with document loading and chunking notebooks.
2. Explore embedding generation and vector-store construction.
3. Run retrieval and inspect returned passages.
4. Add a generation step grounded in retrieved context.
5. Evaluate retrieval quality and answer faithfulness.
6. Compare standard RAG with agentic and vectorless approaches.

## Contributing

Keep each experiment self-contained, document external services and model requirements, and include small, non-sensitive sample data where possible. Avoid committing notebook outputs that contain secrets or private data.

## License

The repository includes a LICENSE file. See [LICENSE](LICENSE) for the applicable terms.
