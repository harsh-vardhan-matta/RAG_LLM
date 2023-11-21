# RAG_LLM
An overview of Retrieval Augmented Generation (RAG) with LLM

Steps Followed:
1. Develop synthetic data:
   1.1 macro_1.csv (state_gdp($_million_(USD)),population,pcc_category)
   1.2 media_1.csv (spend($),platform,days,geography)
   1.3 business_performance_1.csv (value_sales,volume_sales,business_entity,geography)
   1.4 weather_1.csv (temperature (Celsius),rainfall (mm),days,geography)

Play around with this data - refer to file name: data_generator_1.ipynb

2. Steps to implement rag solution with LLM:
   2.1 Data Creation followed by data preprocessing (if needed)
   2.2 Develop Embeddings
   2.3 Connect the Embeddings through Pinecone
   2.4. Experiments with Prompts (Experimentation - Zero Shot, Few Shot, Chain-of-Thoughts, Self Consistency)
     2.4.1. Please refer to the file_name = Prompt_Engineering.docx
   2.5 Give a query, based on similarity search (define k by yourself) - you will get the relevant contexts (from the embeddings created) - along with the scores - choose the lower scores
   2.6 Give {Prompt = query + context} to LLM to receive response
   2.7 Check for hallucination. Implement Reward functions. Give -1 for wrong rewards, + 1 for right rewards. Train the reinforcement learning model.

3. Refer code files
   3.1 rag-chatbot_1.ipynb
   3.2 tackling_hallucination.ipynb

