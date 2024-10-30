# News Analysis Application

This project is a Flask web application that integrates with the News API and OpenAI's GPT-4 model to fetch, process, and analyze news articles. Users can search for news articles based on a query and date range, and the application will summarize the articles, extract key points, analyze sentiment, and classify their topics.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Setup](#setup)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [License](#license)

## Features

- Search for news articles by keyword and date range.
- Summarize articles using OpenAI's GPT-4 model.
- Extract key points from articles.
- Perform sentiment analysis (positive, neutral, negative).
- Classify articles into topics.
- Pagination support for viewing multiple batches of articles.

## Technologies Used

- Python
- Flask
- OpenAI API
- NewsAPI
- HTML for front-end


Navigate to the project directory:

bash
Copy code
cd news-analysis-app
Install the required packages:

bash
Copy code
pip install Flask requests openai newsapi-python
Set your API keys in the code:

Replace openai.api_key and NEWS_API_KEY with your actual API keys.
Run the application:

bash
Copy code
python app.py
Open your browser and go to http://127.0.0.1:5000.

Usage
Enter your search query and date range in the provided fields.
Click the "Search" button to fetch news articles.
Review the results, which include summaries, key points, sentiment analysis, and topics.
Use the "Next Batch" button to fetch more articles if available.
Code Explanation
The code consists of several key components:

Imports: Essential libraries are imported for handling requests, rendering templates, managing sessions, and connecting to APIs.

API Keys: OpenAI and News API keys are set up to enable API calls.

Flask App Initialization: A Flask application is created, with a secret key for session management.

Data Collection:

The fetch_news_articles function fetches news articles based on a search query and date range using the News API.
It retrieves a batch of articles and processes them into a list of dictionaries with relevant fields.
Article Processing:

The clean_text function removes HTML tags and special characters from the article content.
The preprocess_articles function applies the cleaning function to each article.
LLM Integration:

The get_llm_analysis function interacts with the OpenAI API to process articles for summarization, key point extraction, sentiment analysis, and topic classification.
Specific functions like summarize_article, extract_key_points, sentiment_analysis, and classify_topic use templates to generate prompts for the language model.
Flask Routes:

The root route (/) handles form submissions, fetching and processing articles based on user input.
The next_batch route fetches additional articles if available.
The process_batch function consolidates the analysis results for each article into a presentable format.
Running the Application: The application runs in debug mode to facilitate development and troubleshooting.

License
This project is licensed under the MIT License - see the LICENSE file for details.

sql
Copy code

### Instructions for Use
- Replace `yourusername` in the clone URL with your actual GitHub username.
- Ensure the paths for any additional files (like `LICENSE`) are correct if you include them.
- Feel free to add or modify sections based on your specific project details!
