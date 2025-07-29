# SmartCart-Recommendation-Analysis

A recommendation system analysis for e-commerce platforms using collaborative filtering and association rule mining.

## Overview

This project implements and evaluates two main recommendation approaches:

- User-based collaborative filtering for personalized product recommendations
- Association rule mining to discover purchasing patterns

The analysis uses real e-commerce user interaction data to build and compare different recommendation strategies.

## Contributors

| Name           | Student ID | GitHub                                             |
| -------------- | ---------- | -------------------------------------------------- |
| Antoine Cantin | 40211205   | [@ChiefsBestPal](https://github.com/ChiefsBestPal) |
| Tuan Anh Pham  | 40213926   | [@TuanAnh-P](https://github.com/TuanAnh-P)         |
| Ryan Li        | 40214839   | [@Ryan2Li](https://github.com/Ryan2Li)             |
| Mustafa Sameem | 40190889   | [@MustafaSameem](https://github.com/MustafaSameem) |

## Features

**Collaborative Filtering**

- Cosine similarity between users
- Top-N product recommendations
- Performance evaluation with Precision@K and Recall@K
- Grid search for parameter optimization

**Association Rule Mining**

- Apriori algorithm implementation
- Frequent itemset discovery
- Rule evaluation using support, confidence, and lift

**Data Analysis**

- Exploratory data analysis
- User behavior and product popularity analysis
- Visualization of patterns and results

## Getting Started

### Requirements

- Python 3.8+
- See `requirements.txt` for package dependencies

### Installation

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Open the Jupyter notebook: `jupyter notebook analysis.ipynb`

### Usage

Run the notebook cells in order to:

1. Load and explore the dataset
2. Build user-item matrices
3. Train collaborative filtering models
4. Generate recommendations
5. Mine association rules
6. Evaluate and visualize results

## Project Structure

```
SmartCart-Recommendation-Analysis/
├── data/
│   ├── ecommerce_user_data.csv    # User ratings and interactions
│   └── product_details.csv        # Product metadata
├── analysis.ipynb                 # Main analysis notebook
├── report.pdf                     # Analysis report
├── README.md
└── requirements.txt
```

## Data

The dataset contains:

- User interaction data with ratings, product IDs, and categories
- Product metadata including names and categories
- Approximately 700+ user interactions across 100+ products

## Methods

**Data Preprocessing**

- User-item matrix construction
- Missing value handling
- Train/test splitting (80/20)

**Collaborative Filtering**

- Mean-centered user-item matrix
- Cosine similarity calculation
- K-nearest neighbors approach
- Weighted rating prediction

**Association Rules**

- Transaction format conversion
- Frequent itemset mining with configurable support thresholds
- Rule generation with confidence and lift metrics

## Results

The analysis achieves:

- Precision@10 around 0.65 for collaborative filtering
- Discovery of meaningful product associations
- Coverage of 80%+ of catalog items in recommendations
- Matrix sparsity typical of e-commerce datasets (~95%)

## Configuration

Key parameters can be adjusted:

```python
K_RECOMMENDATIONS = 10      # Recommendations per user
TOP_K_USERS = 10           # Similar users to consider
MIN_SUPPORT = 0.05         # Minimum support for itemsets
MIN_CONFIDENCE = 0.5       # Minimum confidence for rules
```

## Dependencies

- pandas: Data manipulation
- numpy: Numerical operations
- scikit-learn: Machine learning tools
- matplotlib/seaborn: Visualization
- mlxtend: Association rule mining
- jupyter: Notebook environment

## License

MIT License
