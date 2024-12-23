# Song Mood Prediction and Recommendation System

This project involves building a system that predicts the mood of songs based on their features and recommends similar songs using a dataset of Spotify tracks. Below are the details of the project implementation and structure.

## Table of Contents
- [Overview]
- [Dataset]
- [Installation]
- [Project Workflow]
- [Key Features]
- [Results]
- [Future Improvements]
- [License]

---

## Overview
This system uses a dataset of Spotify songs to:
1. Predict the mood of songs based on features like `danceability`, `energy`, `valence`, `tempo`, and `acousticness`.
2. Handle songs with unknown moods by assigning predicted moods using a trained Random Forest Classifier.
3. Recommend similar songs to a given track based on Euclidean distance of features.

## Dataset
The dataset contains the following columns:
- `track_id`: Unique identifier for each track.
- `track_name`: Name of the track.
- `danceability`, `energy`, `valence`, `tempo`, `acousticness`: Numerical features representing song characteristics.
- `mood`: A categorical label assigned based on predefined rules.

### Preprocessing Steps
1. Filtered relevant columns.
2. Assigned moods to songs using custom rules.
3. Handled class imbalance using SMOTE.
4. Split data into training and testing sets for supervised learning.

## Installation
1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure you have the dataset file (`spotify_songs.csv`) in the project directory.

## Project Workflow
### 1. Data Preprocessing
- Selected relevant features.
- Applied custom rules to label moods.
- Balanced training data using SMOTE.

### 2. Model Training
- Trained a Random Forest Classifier to predict moods.
- Evaluated model performance using metrics like accuracy and classification report.

### 3. Mood Prediction for Unknown Songs
- Predicted moods for songs labeled as "Unknown" in the dataset.

### 4. Song Recommendation
- Used Euclidean distance to recommend top 5 songs similar to a given track based on features.

### 5. Visualization
- Created KDE plots to visualize feature distributions for known and unknown songs.

## Key Features
- **Mood Prediction**: Classifies songs into moods such as `Happy/Upbeat`, `Sad`, `Energetic`, `Calm/Chill`, `Romantic`, or `Party`.
- **Recommendation System**: Recommends similar songs based on features.
- **Data Visualization**: Provides insights into feature distributions and class balance.

## Results
### Model Performance
- Accuracy: `Random Forest Classifier` achieved high accuracy on the test set.
- Classification Report:
  - Precision, Recall, and F1-scores for each mood are included in the project logs.

### Predicted Mood Distribution
```
Energetic       5091
Romantic        2800
Happy/Upbeat    2304
Sad             2069
Party           1957
Calm/Chill      1016
```

## Future Improvements
- Normalize features before calculating Euclidean distances for recommendations.
- Explore advanced recommendation algorithms such as cosine similarity or collaborative filtering.
- Incorporate additional features like lyrics or genre for more accurate mood prediction.
- Improve handling of class imbalance in mood predictions.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

Thank you for exploring the Song Mood Prediction and Recommendation System! Feel free to contribute or raise issues for improvements.

