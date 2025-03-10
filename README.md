# Enhancing Dynamic User Intent Prediction (DUIP) in Recommendation Systems with Transformer-Based Soft Prompting
Recommendation systems play a crucial role in improving user engagement by predicting user preferences based on historical interactions. Traditional recommendation methods, such as collaborative filtering and content-based filtering, have limitations in capturing the dynamic nature of user intent.

The Dynamic User Intent Prediction (DUIP) framework (Xu et al., 2025) addresses these challenges by integrating long-short term memory networks (LSTMs) to model user intent over time, and Large Language Models (LLMs) to enhance predictions using dynamic prompts. However, DUIP still relies on a separate time series retriever-based architecture to generate context for LLM predictions. The sequential nature of LSTM may limit their ability to generalize well in longer sequences than the training data. This research aims to improve DUIP by integrating a BERT-based contextual encoder after the LSTM model to enhance the representation of user interactions. Additionally, this study will explore the effectiveness of different LLM architectures for item prediction tasks. 

This leads to the following research questions:
1. Primary Research Question: How can Transformer-based soft prompting and a BERT-enhanced DUIP framework improve recommendation performance and computational efficiency compared to the original LSTM-based approach?
2. Secondary Research Questions: What impact do different LLM architectures (GPT-2, Deepseek_v3, and Mixtral) have on recommendation quality when used with Transformer-based soft prompting?
3. How does the proposed enhanced DUIP approach perform on different types of recommendation datasets (movies, e-commerce products) compared to baseline approaches?
To what extent can Transformer-based soft prompting reduce computational costs while maintaining or improving recommendation accuracy?

This study will utilize two well-established datasets to replicate the existing DUIP model and evaluate the performance of the proposed enhanced DUIP framework:

MovieLens-1M(ML-1M): This is a stable benchmark dataset with 1 million ratings from 6000 used on 4000 movies. Each rating entry includes user ID, movie ID, rating value (1-5) and timestamp. MovieLens 1M Dataset | GroupLens
Amazon Reviews Dataset: This dataset contains product reviews and metadata from Amazon, including product descriptions, price, user ratings and user bought together graphs. The large dataset contains 571.54M reviews with interactions ranging from May.1996 to Sep.2023. McAuley-Lab/Amazon-Reviews-2023 · Datasets at Hugging Face

The dataset will be split into training (80%), validation (10%) and test(10%) sets using temporal splitting to simulate real-world scenarios where models are training on past data and evaluated on future data. This approach helps assess the models’ ability to capture evolving user preference over time. 
