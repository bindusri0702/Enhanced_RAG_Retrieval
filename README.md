# Advanced RAG Techniques

## Pitfalls of Retrieval
Retrievals are tasked to return top similar documents irrespective of their low similarity scores or relevance of the documents to the query being asked. This forces retrieval to consider irrelevant documents and distarctors as well. To avoid incorrect response generated using these retrieved documents. The retriever should be provided with context specific information to work well with customised datasets.

## Query Expansion

### Expansion with generated answer
Use the LLM to generate answer as if the query is asked from general perspective, by not providing relevant documents. This makes LLM hallucinate and make up a hypothetical response to user query. The keywords in response helps in retrieving semantically similar documents from our customised RAG dataset.

### Expansion with generated queries
Use the LLM to generate queries that are related but different from the original user query, the queries should cover the topics found in documents like monetary policy/ clinical trial reports (mention the type of the document you are using RAG for). The user query along with these generated queries helps to retrieve relevant documents that are highly similar.

## Cross encoder Reranking
Reranking prioritizes semantically similar documents to have high score and use those for generating response.

## Embedding Adapters
Embedding Adapters transforms the query vector space by squeezing and rotating to form a new space where the relevant documents are closer to the query and irrelevant documents are farther away.

`Note` - More about Advanced RAG Techniques and all the methods discussed, can be found in advanced-retrieval-for-ai course by Chroma in deeplearning.ai.
