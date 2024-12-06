# Stock_Movement_Prediction
This project involves predicting future stock prices using an LSTM model, enriched with sentiment analysis and a knowledge graph built from financial news data. The approach combines financial time-series forecasting with sentiment-driven insights to improve prediction accuracy.

#Features of the Project
1. Data Collection
Stock Data: Fetches historical stock prices using Yahoo Finance's API.
News Data: Retrieves news articles using NewsAPI, focusing on the company of interest.
2. Data Preprocessing
Stock data preprocessing involves removing missing values and calculating technical indicators (e.g., moving averages, RSI).
News text is tokenized, cleaned, and processed for sentiment analysis and entity extraction.
3. Sentiment Analysis and Knowledge Graph
Sentiment Analysis: Utilizes FinBERT to extract sentiment from news articles.
Knowledge Graph: Represents entities and their relationships, enriched with sentiment labels and scores.
4. Feature Engineering
Extracts features from the knowledge graph (e.g., number of nodes, edges, density) and integrates them into the stock data for model training.
5. LSTM Model for Stock Prediction
A deep learning model with multiple LSTM layers is trained on past stock prices and graph features to predict future prices.
6. Evaluation
Performance metrics such as MAE, MSE, RMSE, and R² are used to evaluate the model.
Predictions are visualized alongside actual stock prices for comparison.
#Setup Instructions
Prerequisites
Python 3.7 or later.
Install required libraries:
bash
Copy code
pip install yfinance pandas numpy matplotlib scikit-learn tensorflow spacy transformers networkx requests
Download the SpaCy language model:
bash
Copy code
python -m spacy download en_core_web_sm
Configuration
Replace news_api_key with a valid NewsAPI key.
Set the ticker, company_name, start_date, and end_date variables to define the stock and time range of interest.
#How to Run
Clone the repository and navigate to the project directory.
Run the script to:
Load stock and news data.
Build a knowledge graph.
Train the LSTM model.
Predict future stock prices.
View visualizations and evaluate model performance.
#Project Flow
1. Data Loading
Historical stock data is fetched using Yahoo Finance.
News articles are retrieved and preprocessed for sentiment analysis.
2. Knowledge Graph Construction
Entities from news articles are connected based on co-occurrence.
Sentiment is assigned to edges in the graph.
3. Feature Engineering
Graph features (e.g., average degree, clustering coefficient) are extracted.
These features are added to the stock data.
4. Model Training
Scaled stock data and graph features are used to train an LSTM model.
Early stopping ensures optimal performance.
5. Future Predictions
The trained model predicts stock prices for the next 60 days.
Predictions incorporate technical indicators and graph features.
#Results
The LSTM model effectively predicts stock price trends.
Sentiment analysis and graph features enhance the model's ability to capture market dynamics.
#Future Scope
Incorporate additional sentiment models for improved analysis.
Explore other graph-based features or relationships.
Extend predictions to multi-stock portfolios or indices.
#Notes
Ensure the news_api_key is valid for retrieving news data.
Results may vary depending on the quality of news data and model parameters.
