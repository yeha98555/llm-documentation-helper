# Documentation Helper
LLM Documentation Helper Bot.

## Steps
1. prepare documents
2. turn it into vectors (take every page in the documentation, chunk it up and then embed it, turn it into a vector)
3. store it into a vector store (vector database)
4. use it by writing a chain in order to find us the correct chunks that we need to answer the question
5. implement the use interface using streamlit package

## Usage

### 1. download langchain documenation for example:
```shell
mkdir langchain-docs
cd langchain-docs

wget --recursive --no-clobber --html-extension --convert-links --domains python.langchain.com --no-parent https://python.langchain.com/docs/get_started
```

### 2. [pinecone](https://www.pinecone.io/) settings
  - Create a new Index
    - Name: `langchain-doc-index`
    - Dimensions: `1536`
    - Pod Type: `starter`<br>
  - API Keys (create new API key or use default)
  - copy `.env.sample` to `.env`, and replace the values

### 3. run
```
pipenv shell

# ingest data into vector database
python ingestion.py

# test
python backend/core.py

# run user interface
streamlit run main.py
```