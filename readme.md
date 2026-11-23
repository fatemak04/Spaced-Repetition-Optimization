
# Spaced Repetition Optimization Using Cognitive Models and Machine Learning

## Project Overview

This project aims to improve long-term learning retention by combining cognitive memory models with machine learning techniques. It uses the Duolingo Spaced Repetition Dataset from Kaggle to predict the probability of recalling vocabulary and optimize review intervals based on individual learning patterns.

The system combines the traditional **Ebbinghaus Forgetting Curve** with machine learning models to create a more personalized and efficient spaced repetition approach.

## Objectives

- Analyze learner recall patterns and forgetting behavior.
- Develop cognitive features based on memory strength and spacing effects.
- Implement a baseline model using the Ebbinghaus Forgetting Curve.
- Predict recall probability using machine learning.
- Optimize review schedules based on predicted recall probability.
- Compare the traditional cognitive model with machine learning approaches.

## Dataset

**Source:** Duolingo Spaced Repetition Dataset (Kaggle)

The dataset contains learner interaction records, including:
- `p_recall`: Proportion of correctly recalled exercises.
- `timestamp`: Time of the learning session.
- `delta`: Time since the previous review.
- `history_seen`: Total previous exposures.
- `history_correct`: Previous correct responses.
- `session_seen`: Number of times a word appeared in the current session.
- `session_correct`: Number of correct responses in the current session.

Due to computational limitations, a representative subset of **200,000 rows** was used for experimentation.

## Methodology

The project consists of six main phases:

1. **Data Preprocessing and Exploration:** Data cleaning, missing value handling, timestamp conversion, sampling, and recall distribution analysis.

2. **Cognitive Feature Engineering:** Creating features such as memory strength, log time gap, practice frequency, and item difficulty.

3. **Baseline Cognitive Model:** Implementing the Ebbinghaus Forgetting Curve to estimate recall probability.

4. **Machine Learning Models:** Training and comparing:
   - Logistic Regression
   - Random Forest
   - Gradient Boosting

5. **Spaced Repetition Optimization:** Generating personalized review intervals using predicted recall probabilities.

6. **Evaluation and Analysis:** Comparing machine learning approaches against the traditional forgetting curve model in terms of recall prediction and scheduling efficiency.

## Key Findings

- The dataset exhibits class imbalance, with successful recall instances being more frequent than unsuccessful recalls.
- Time gaps and historical learning performance play important roles in predicting recall.
- Machine learning models outperform the traditional cognitive baseline.
- Random Forest achieved the strongest recall performance among the models tested.
- Prediction-based scheduling enables more personalized review intervals.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## How to Run

1. Clone this repository.
2. Install the required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

3. Download the Duolingo Spaced Repetition Dataset from Kaggle.
4. Place the dataset in the appropriate project directory.
5. Open the Jupyter Notebook:

```bash
jupyter notebook
```

6. Run the notebook cells sequentially to reproduce the analysis, model training, and scheduling optimization.

## Conclusion

This project demonstrates how cognitive memory theories and machine learning can work together to improve traditional spaced repetition systems. By predicting recall probability and adapting review intervals, the proposed approach aims to improve long-term retention while reducing unnecessary repetitions.