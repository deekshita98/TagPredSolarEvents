# Wiki Multi-Label Prediction for Solar Events

## Overview

wiki_multilabel_prediction_solarevents.py encloses scraping Wikipedia data, preprocessing text, vectorizing content, training a multi-label classification model, and visualizing the results.This project is designed to analyze the impact of solar industry events on Wikipedia page edits. Specifically, it seeks to predict which tags (labels) related to solar technology might be most relevant to different Wikipedia entries based on past editing data correlated with solar event occurrences.

## Installation

To run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/deekshita98/TagPredSolarEvents.git

   
#### Code Explanation

This project automates the process of predicting relevant tags for Wikipedia articles related to solar events using Natural Language Processing and Machine Learning. It includes web scraping, data preprocessing, model training, prediction, and data visualization steps to analyze the relationships between different tags.

## Code Explanation


### Installation Requirements

The script requires several Python libraries including pandas, BeautifulSoup, requests, nltk, scikit-learn, tensorflow, and visualization libraries.


### Data Collection

Function scrape_website: Fetches data from a specified Wikipedia URL and extracts text content using BeautifulSoup. It handles HTTP errors gracefully and returns the title and combined text of all paragraphs.
Function main: Orchestrates the scraping process for multiple URLs, collects the scraped data, and stores it in a pandas DataFrame.

### Data Processing

**Text Processing**
NLTK Setup: Downloads and sets up NLTK stopwords for English for text preprocessing.
Function preprocess_text: Processes text data by converting to lowercase, removing stopwords, and stemming the remaining words.

**Data Preparation**
The script loads an events dataset, splits 'Tags' into a list, and preprocesses the 'Event description' using the above text processing function.
Vectorization: Uses TfidfVectorizer to convert text data into a TF-IDF matrix.

### Model Training

A sequential model from Keras is configured with dense layers and dropout for regularization. It's trained on vectorized text data with corresponding multi-label binary vectors.
Predictions are made on new data, and the results are processed to map the predicted binary vectors back to tag names.

**Multi-Label Classification**
Sets up a neural network model using TensorFlow's Keras API, designed for multi-label classification with sigmoid activation and binary crossentropy loss.
Trains the model on the training dataset and evaluates it on a test set.


### Prediction

Makes predictions on new data scraped from predefined Wikipedia pages about solar technologies.
Predicts tags based on the content using the trained model and assigns predicted tags back to the DataFrame.

### Data Visualization

Heatmaps and bar charts are generated to analyze tag co-occurrence and label frequency, respectively, using matplotlib and seaborn.

**Tag Co-occurrence Heatmap**
Calculates and plots a heatmap using seaborn to show the co-occurrence of tags across the dataset, helping to visualize relationships between different tags.

**Label Frequency Distribution**
Plots a bar chart showing the frequency of each predicted tag across all documents, providing insights into the most common themes.


### Functions

scrape_website and scrape_website1: These functions extract titles and paragraphs from given Wikipedia URLs. They are used for both training data preparation and prediction.
main and main1: These orchestrator functions handle batch processing of multiple URLs for data scraping and preparation.
preprocess_text: This function cleans and preprocesses text data to prepare it for vectorization and modeling.



#### Usage

Explain how to run the program, including any scripts that should be executed or services that need to be started.


## Usage

To start the program, navigate to the project directory and run the following script:

```markdown
python wiki_multilabel_prediction_solarevents.py
```



This script performs several key functions:

- It fetches data from a specified Wikipedia API.
- Processes the data to find correlations between Wikipedia page edits and solar events.
- Predicts relevant tags for new Wikipedia entries based on these correlations.

## Contributing

Contributions to this project are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a pull request.


## Contact

Project Link: [https://github.com/deekshita98/TagPredSolarEvents]

