---
name: data-science
description: Analyze data, build machine learning models, and extract insights from datasets. Use when working with data analysis, statistics, ML models, deep learning, or data-driven projects.
---

# Data Science & Machine Learning

## Quick Start

Data science combines statistics, programming, and domain knowledge to extract insights from data:

### Python Setup

```python
# Essential libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

print("Data Science Stack Ready!")
```

### Data Analysis

```python
import pandas as pd

# Load data
df = pd.read_csv('data.csv')

# Explore data
print(df.head())        # First 5 rows
print(df.info())        # Data types and missing values
print(df.describe())    # Statistical summary

# Data cleaning
df = df.dropna()        # Remove missing values
df['age'] = df['age'].astype(int)  # Convert data type
```

### Data Visualization

```python
import matplotlib.pyplot as plt

# Line chart
plt.plot(data['date'], data['sales'])
plt.title('Sales Over Time')
plt.xlabel('Date')
plt.ylabel('Sales')
plt.show()

# Scatter plot
plt.scatter(data['age'], data['income'])
plt.show()
```

### Machine Learning

```python
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split

# Prepare data
X = df[['feature1', 'feature2']]
y = df['target']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2
)

# Train model
model = LinearRegression()
model.fit(X_train, y_train)

# Evaluate
score = model.score(X_test, y_test)
print(f"Accuracy: {score:.2%}")
```

### Deep Learning

```python
import tensorflow as tf
from tensorflow import keras

# Build neural network
model = keras.Sequential([
    keras.layers.Dense(128, activation='relu', input_shape=(10,)),
    keras.layers.Dropout(0.2),
    keras.layers.Dense(64, activation='relu'),
    keras.layers.Dense(1, activation='sigmoid')
])

model.compile(
    optimizer='adam',
    loss='binary_crossentropy',
    metrics=['accuracy']
)

# Train
model.fit(X_train, y_train, epochs=10, batch_size=32)
```

## Key Concepts

- **Data Cleaning**: Handle missing values, outliers, inconsistencies
- **Feature Engineering**: Create meaningful features for models
- **Model Selection**: Choose appropriate algorithms
- **Evaluation Metrics**: Accuracy, precision, recall, F1, AUC
- **Hyperparameter Tuning**: Optimize model parameters
- **Cross-Validation**: Validate model robustness

## Common Algorithms

- **Regression**: Linear, Ridge, Lasso
- **Classification**: Logistic Regression, Decision Trees, SVM
- **Clustering**: K-means, Hierarchical, DBSCAN
- **Deep Learning**: CNNs, RNNs, Transformers

## Learning Path

1. Learn Python and fundamental libraries (Pandas, NumPy)
2. Master statistics and data analysis
3. Study ML algorithms and scikit-learn
4. Deep dive into deep learning frameworks
5. Work on real-world projects
6. Learn MLOps for deployment

## Resources

- **Kaggle**: Free datasets and competitions
- **Scikit-learn Docs**: sklearn.org
- **TensorFlow**: tensorflow.org
- **Fast.ai**: Practical deep learning course
