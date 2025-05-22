
# IMDb Movie Recommendation System 

This project scrapes IMDb for all 2024 feature films using Python and Selenium.

It collects movie titles and descriptions, then stores them in a CSV file.

The data can be used to build content-based recommendation systems.

It handles dynamic content loading through automated browser actions.

Future upgrades may include NLP and a Flask-based web interface.



## Problem Statement 

Finding relevant and updated movie data from websites like IMDb is challenging due to dynamically loaded content and lack of public APIs for detailed film descriptions.

 Manual collection is time-consuming and inefficient. 
 
 There is a need for an automated solution to extract movie titles and descriptions for films released in 2024, which can later support recommendation systems or data analysis tasks. 
 
 This project aims to develop a Python-based tool that scrapes and stores this data efficiently for further processing.
## Methodology
a. Dataset

Source:
Movie data was collected by web scraping the IMDB website using Selenium WebDriver. The focus was on movies released in 2024.

Fields Collected:

Movie Title

Movie Description (plot summary)

Preprocessing Steps:

Cleaned movie titles by removing numbering.

Extracted text content from web elements and saved it in CSV format for further processing.

b. NLP Techniques Used
Text Extraction: Extracted movie descriptions as raw text for analysis.

(Planned) Preprocessing:

Tokenization: Splitting descriptions into words.

Removing stop words and punctuation.

Lemmatization or stemming (if implemented later).

(Planned) Vectorization: Using TF-IDF to convert descriptions into numerical vectors for comparison.

c. Modeling Techniques
Content-Based Filtering (planned):

Compare movies based on similarity of their descriptions.

Use cosine similarity to recommend movies with similar plot content.

Collaborative Filtering: Not included in this project.


## Technology used 
Programming Language:

Python

Libraries & Tools:

Selenium – For web automation and scraping dynamic IMDb content

re (Regular Expressions) – For cleaning and formatting text data

csv – For storing extracted data into a CSV file

time – To manage loading delays and wait times in scraping

WebDriver (ChromeDriver) – To control the browser programmatically

(Optional for future enhancement):

Flask – To create a simple web interface

NLTK / scikit-learn / pandas / NumPy – For NLP-based movie recommendations and data processing


## Implementation

Step 1: Setup Selenium WebDriver
•	Use Selenium with ChromeDriver in headless mode (no browser window shown).
•	Configure Chrome options (--headless, disable GPU, etc.).

Step 2: Open IMDb page for 2024 movies
•	Go to the URL:
https://www.imdb.com/search/title/?title_type=feature&release_date=2024-01-01,2024-12-31

Step 3: Automatically click "Load More" button repeatedly
•	Find the "Load More" button by XPath or CSS selector.
•	Scroll to it and click it.
•	Wait for new movies to load.
•	Repeat until no more new movies load or the button disappears.

Step 4: Extract movie titles and descriptions
•	Find all movie titles on the page using CSS selectors.
•	Clean titles with regex (remove numbering).
•	Find movie descriptions using XPath or CSS selectors.

Step 5: Save data to CSV file
•	Match title and description counts.
•	Write movie titles and descriptions to imdb_movies_2024.csv.

Step 6: Close the browser and end script

## Project Flow 
•  Data Input

       Web scraping movie titles and descriptions using Selenium from IMDB.

•  NLP Preprocessing
       
       Cleaning, tokenization, lemmatization of descriptions.

•  Feature Extraction

       Converting text to vectors using TF-IDF.
•  Similarity Computation
 
       Calculating cosine similarity between movie vectors.

•  Top-N Recommendations

       Outputting the most similar movies as recommendations.

## Screenshots

![nlp_1](https://github.com/user-attachments/assets/4c26d0b9-c06c-451d-88f1-dc67cca2a372)

![nlp_2](https://github.com/user-attachments/assets/36653bb9-337d-44ca-bdf1-7b9275ef3608)

![nlp_3](https://github.com/user-attachments/assets/4d5f4e53-7719-47bd-b8e7-93dc377efba6)

![nlp_4](https://github.com/user-attachments/assets/a5a8eb94-317d-4145-8126-975dce803c1f)



