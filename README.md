# Documentation Helper

download langchain documenation for example:
```shell
mkdir langchain-docs
cd langchain-docs

wget --recursive --no-clobber --html-extension --convert-links --domains python.langchain.com --no-parent https://python.langchain.com/docs/get_started
```

run
```
pipenv shell

# ingest data into vector database
python ingestion.py

# run user interface
python main.py
```