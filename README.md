# Wiki Multi-Label Prediction for Solar Events

## Overview

This project is designed to analyze the impact of solar industry events on Wikipedia page edits. Specifically, it seeks to predict which tags (labels) related to solar technology might be most relevant to different Wikipedia entries based on past editing data correlated with solar event occurrences.

## Installation

To run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/deekshita98/TagPredSolarEvents.git

   
#### Code Explanation

```markdown
## Code Explanation

### Data Collection

The `fetch_data` function is responsible for gathering data using the Wikipedia API. It collects revision histories and page edit details related to solar events.

### Data Processing

The `process_data` function cleans and structures the raw data into a format suitable for analysis. This includes normalizing text data and extracting relevant features.

### Model Training

The `train_model` function sets up and trains a multi-label classification model. This model learns to predict the relevance of various tags based on the features extracted from the Wikipedia data.

### Prediction

The `predict_tags` function uses the trained model to assign tags to new or existing Wikipedia entries, helping to anticipate the impact of future solar events on these pages.
rrepositorylink.com



#### Usage

Explain how to run the program, including any scripts that should be executed or services that need to be started.

```markdown
## Usage

To start the program, navigate to the project directory and run the following script:

```python
python wiki_multilabel_prediction_solarevents.py


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

