## Prerequisites
- Atlas Cluster Connecting String
- OpenAI API Key
- Voyage AI API Key

## Usage
# Install the requirements
```
pip3 install langchain langchain_community langchain_core langchain_voyageai langchain_openai langchain_mongodb pymongo pypdf
```
# .env or use key_param
```
MONGODB_URI=<your_atlas_connection_string>
VOYAGE_API_KEY=<your_voyageai_api_key>
LLM_API_KEY=<your_llm_api_key>
```
# Load the sample data into your Atlas Cluster
```
python load_data.py
```

## Relevant Links
- https://docs.voyageai.com/docs/embeddings

## Source
- https://learn.mongodb.com/courses/rag-with-mongodb