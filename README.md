# NLP_basic_project1

# Movie Data Preprocessing Project

## Overview

This project involves collecting movie data, performing various preprocessing steps, and creating a clean dataset for further analysis. The dataset contains information about movies, including the title, description, and genres.

## Dataset

The dataset consists of 9320 rows and 3 columns:
1. **title**: The name of the movie.
2. **description**: A brief overview of the movie.
3. **genres**: The genres associated with the movie.

## Preprocessing Steps

1. **Data Collection**: 
   - Collected data using the API provided by The Movie Database (TMDb).
   - Fetched top-rated movies data along with their descriptions and genres from multiple pages of the API.

2. **Replace Genre IDs with Genre Names**:
   - Used the TMDb genre API to fetch the mapping of genre IDs to genre names.
   - Replaced genre IDs in the dataset with corresponding genre names.

3. **Text Preprocessing**:
   - **Lowercasing**: Converted all text in the 'title', 'description', and 'genres' columns to lowercase.
   - **Punctuation Removal**: Removed punctuation from the 'description' column to ensure clean text data.
   - **Spelling Correction**: Applied spelling correction on the 'description' column using the TextBlob library.
   - **Word Tokenization**: Tokenized the words in the 'description' column using the spaCy library.
   - **Lemmatization**: Performed lemmatization on the 'description' column using the spaCy library to reduce words to their base forms.

## Final Dataset

The final dataset after preprocessing is saved as `movies_dataset_lemmatized.csv`, which contains the following columns:
1. **title**: The name of the movie.
2. **description**: The preprocessed and lemmatized overview of the movie.
3. **genres**: The genres associated with the movie.
4. **description_tokens**: The tokenized words from the 'description' column.
5. **description_lemmatized**: The lemmatized words from the 'description' column.

## Usage

The preprocessed dataset can be used for various natural language processing (NLP) tasks, such as sentiment analysis, topic modeling, and recommendation systems.

## Requirements

- Python 3.x
- pandas
- requests
- spacy
- textblob

## Instructions

1. Clone the repository or download the project files.
2. Install the required libraries:
   ```sh
   pip install pandas requests spacy textblob
