# Sparkify Churn Prediction

1. [Introduction](#intro)
2. [Installation](#install)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Results](#results)

<a name="intro"></a>
## 1. Introduction

In this project, I used PySpark to analyze and predict churn based on customer activity dataset of a fictitious music streaming company, “Sparkify”. This is a toy dataset, relatively small in size so it could be processed on a local computer. Hence, in order to mimic the real world, we use Spark (in local mode) to process the data and build the model.

<a name="install"></a>
## 2. Installation
The code was developed using Python version 3. We recommend using [Anaconda](https://docs.anaconda.com/anaconda/install/index.html) for installing **Python 3** as well the following required libraries:
  - PySpark
  - pandas
  - seaborn
  - matplotlib

<a name="dataset"></a>
## 3. Dataset
**User activity dataset**
The dataset logs user demographic information (e.g. user name, gender, location State) and activity (e.g. song listened, event type, device used) at individual timestamps.

<a name="methodology"></a>
## 4. Methodology

1. Data Load & EDA

   - Overview of all the available columns
   - Definition of churn
   - Comparison of behavior between churn and non-churn users
     - User level (free vs. paid)
     - Event types (e.g. add a friend, advertisement, thumbs up)
     - Device used (e.g. Mac, Windows)

2. Feature engineering

   - Create features on per user basis:
     - Time since registration
     - Number of songs listened
     - Number of Thumbs-Up
     - Number of Thumbs-Down
     - Number of songs added to playlist
     - Number of friends added
     - Total time listening to music
     - Number of songs played per session
     - Number of unique artists listened
     - User Gender

3. Machine learning

   - Split training and testing sets
   - Selection of evaluation metric
   - Training of following classifiers:
     - Logistic regression
     - Random forest
     - Gradient-boosted trees
   - Tune hyperparameters of gradient-boosted tree
   - Evaluate model performance
   - Evaluate feature importance

<a name="results"></a>
## 5. Results
The main findings of the project can be found at the blog post available [here](https://medium.com/@gupta.shrey/sparkify-churn-prediction-7a9173243152).
