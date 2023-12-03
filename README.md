# Documentation Helper

1. download langchain documenation for example:
```shell
mkdir langchain-docs
cd langchain-docs

wget --recursive --no-clobber --html-extension --convert-links --domains python.langchain.com --no-parent https://python.langchain.com/docs/get_started
```

2. [pinecone](https://www.pinecone.io/) settings
1) Create a new Index
  - Name: `langchain-doc-index`
  - Dimensions: `1536`
  - Pod Type: `starter`
2) API Keys (create new API key or use default)

3. run
```
pipenv shell

# ingest data into vector database
python ingestion.py

# run user interface
python main.py
```