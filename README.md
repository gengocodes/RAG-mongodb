## Prerequisites
- Atlas Cluster Connecting String
- OpenAI API Key
- Voyage AI API Key
- Data loaded into Atlas

# Create the following vector search index, named vector_index, on the chunked_data collection in your Atlas Cluster:
```
{
  "fields": [
    {
      "numDimensions": 1536,
      "path": "embedding",
      "similarity": "cosine",
      "type": "vector"
    },
    {
      "path": "hasCode",
      "type": "filter"
    }
  ]
}
```

Note: The default number of dimensions for the voyage-3.5-lite embedding model is 1024. We have the option to use 256, 512, or 2048 dimensions with the voyage 3.5 models.

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