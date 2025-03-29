Item Similarity Finder

Overview

This Streamlit application allows users to find similar items based on attribute matching and vector search. It takes an Excel file as input, processes item attributes, and returns the most similar items based on predefined criteria. The results can be downloaded as a CSV file.

Features

Upload Excel file containing item data.

Enter an Item Number to search for similar items.

Match attributes with at least 90% similarity.

Use OpenAI embeddings and FAISS for vector-based similarity search.

Display ranked results in an interactive table.

Download results as a CSV file.

Requirements

Dependencies

Install the required Python libraries using:

pip install streamlit pandas openai faiss-cpu langchain-community

How It Works

Upload an Excel File

The application reads the uploaded file and ensures all required columns exist.

If any columns are missing, an error message is displayed.

Enter an Item Number

The user provides an item number for similarity search.

If the item exists in the dataset, it retrieves its attributes.

Attribute Matching

The app calculates a match percentage for each item in the dataset.

Items with at least 90% attribute similarity are filtered.

Vector Embeddings and FAISS Search

The selected item's attributes are converted into vector embeddings using OpenAI's model.

The filtered items are stored in a FAISS vector database.

The application retrieves the top 20 most similar items based on vector similarity.

Only items with a similarity score > 0.90 are displayed.

Results and Download

The matching items are shown in an interactive table.

A CSV file download option is provided for exporting results.

Usage

Run the application

streamlit run app.py

Upload an Excel file containing item data.

Enter an item number to search for similar items.

View results in a table and download them as a CSV file.

Configuration

OpenAI API Key

Replace <Enter your OpenAI Key> in the script with your actual OpenAI API key.

OPENAI_API_KEY = "your-api-key-here"
openai.api_key = OPENAI_API_KEY

Potential Improvements

Optimize performance for large datasets.

Improve error handling for missing/incorrect API keys.

Enhance UI with progress indicators and better filtering.

Allow user-defined similarity thresholds.

License

This project is open-source and available for modification and improvement.

Developed using Streamlit, Pandas, OpenAI Embeddings, and FAISS.

