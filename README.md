# Fake News Detection using Machine Learning

## Overview
This project implements a **Fake News Detection** system using Python and **Logistic Regression**. The dataset includes labeled fake and real news articles, and the model classifies news articles as either "Fake" or "Real".

## Table of Contents
1. [Dataset](#dataset)
2. [Libraries Used](#libraries-used)
3. [Data Preprocessing](#data-preprocessing)
4. [Model Training](#model-training)
5. [Results](#results)
6. [How to Run](#how-to-run)

---

## Dataset
The dataset contains two files:
- **Fake.csv**: Contains fake news articles.
- **True.csv**: Contains real news articles.

Each file includes the following columns:
- `title`: The headline of the news article.
- `subject`: The category or topic.
- `date`: The publication date.
- `text`: The main content of the article.

---

## Libraries Used
The following libraries were used:
- **Numpy**: For numerical operations.
- **Pandas**: For data manipulation and processing.
- **Matplotlib & Seaborn**: For data visualization.
- **Scikit-Learn**: For model training, metrics, and data splitting.
- **re & string**: For text cleaning.

---

## Data Preprocessing
1. **Data Cleaning**: Text data is cleaned by:
   - Lowercasing.
   - Removing special characters, URLs, and numbers.
   - Removing punctuation and extra whitespace.

2. **Status Column**: A new column `status` is added:
   - Fake news: `0`
   - Real news: `1`

3. **Merging Datasets**: Fake and real news datasets are merged.
4. **Feature Selection**: Only the `text` and `status` columns are retained.
5. **Shuffling Data**: Data is shuffled to avoid bias.

---

## Model Training
1. **Text Vectorization**: 
   - Used **TfidfVectorizer** from Scikit-Learn to convert text data into numerical format.

2. **Train-Test Split**: 
   - Split the data into training and testing sets with a 75-25 ratio.

3. **Logistic Regression**:
   - Applied Logistic Regression to classify news articles.

---

## Results
The model achieved the following performance:
- **Accuracy**: 98%
- **Classification Report**:
   - High precision and recall across both classes.

---

## How to Run
### Prerequisites
Ensure you have Python 3.x and the required libraries installed. Install dependencies using:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Steps to Run
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```
2. Place the dataset files (`Fake.csv` and `True.csv`) in the appropriate input directory.
3. Run the script:
   ```bash
   python fake_news_detection.py
   ```

### Output
- The script will display the **accuracy score** and **classification report**.
- A visualization of predictions vs true labels will also be displayed.

---

## Visualization
A bar plot comparison between predicted labels and true labels is displayed using Seaborn.

---

## Acknowledgments
- **Dataset Source**: [Fake News Detection Dataset](https://www.kaggle.com)

