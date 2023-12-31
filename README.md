RAG_LLM
This repository provides an overview of Retrieval Augmented Generation (RAG) with large language models (LLMs). RAG is an AI framework that enhances the performance of LLMs by incorporating information from external knowledge sources.

Steps Followed:

**Synthetic Data Generation:**
- macro_1.csv: Contains state-level GDP, population, and PCC features.
- media_1.csv: Provides information on media spending, platform, duration, and geography
- business_performance_1.csv: Includes data on value and volume sales, business entity, and geography
- weather_1.csv: Offers temperature, rainfall, duration, and geography data

**RAG Implementation with LLM:**
- Reference Figure: rag_flow.jpeg
- Regference Python File to create synthetic data - data_generator_1.ipynb
- Reference Python File for RAG implementation: rag-chatbot_1.ipynb
- Data Preparation: Prepare and preprocess data as necessary (filling missing values, drop features etc).
  
**Embedding Development followed by initialization of OpenAI and PineCone APIs**
- Create embeddings for data representation (model="text-embedding-ada-002").
- Pinecone Integration (index_name = llama-2-rag). Visit Pinecone website to play around with database. 
- OpenAI API - (Give your own key)
- Connect embeddings to Pinecone for efficient retrieval.

**Prompt Engineering:**
- Experiment with various prompt types: zero-shot, few-shot, chain-of-thoughts, and self-consistency.
- Refer to Prompt_Engineering.docx for detailed prompt engineering examples

**Context Retrieval:**
- Input a query (implement prompt engineering) and retrieve relevant contexts based on similarity search.
- Select contexts with lower scores for higher relevance.

**LLM-based Response Generation:**
- Provide the retrieved context along with the query to the LLM to generate a response.

**Hallucination Detection and Reward Function Implementation:**
- Reference Python File: tackling_hallucination.ipynb
- Identify and address hallucinations in LLM responses.
- Implement reward functions to train a reinforcement learning model.
- Assign -1 for incorrect rewards and +1 for correct rewards.

**Code Files:**
- rag-chatbot_1.ipynb: Implements the RAG chatbot framework.
- tackling_hallucination.ipynb: Addresses hallucination detection and reward function implementation.

**Key Features:**
- Data Synthesis: Generate synthetic data for model training and experimentation.
- Embedding Creation: Develop embeddings for efficient data representation.
- Pinecone Integration: Utilize Pinecone for scalable and efficient context retrieval.
- Prompt Engineering: Explore various prompt types to optimize LLM performance.
- Hallucination Detection: Implement mechanisms to identify and address hallucinations.
- Reward Function Implementation: Train a reinforcement learning model to improve response quality.
