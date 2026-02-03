# CCADMACL_PROJECT
A final project requirement for our "Advanced Machine Learning" course.

## Video Game Clustering: Unsupervised Learning Framework

### Project Overview

This project implements an unsupervised learning framework to automatically segment video games into distinct, meaningful archetypes by analyzing patterns between commercial performance (global sales) and critical reception (critic and user scores).

**Key Objectives:**
- Discover game archetypes like "Critically Acclaimed Blockbusters" and "Underrated Gems"
- Analyze correlation between commercial success and critical quality
- Understand user-critic discrepancies across different game types
- Provide data-driven insights for game quality and market positioning

### Dataset

**Source:** [Kaggle - Video Game Sales with Ratings](https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings/data)

**Key Features:**
- Commercial metrics: Global sales, regional sales
- Quality metrics: Critic scores, user scores
- Metadata: Game name, platform, genre, release year

### Methodology

#### 1. Data Preprocessing
- Handle missing values and outliers
- Remove games with insufficient review counts
- Focus on sales and rating features

#### 2. Feature Engineering
- `Log_Global_Sales`: Log-transformed sales (handles skewness)
- `Avg_Quality_Score`: Average of critic and user scores
- `Critic_User_Gap`: Discrepancy between critic and user opinions
- `Sales_Quality_Ratio`: Commercial success relative to quality

#### 3. Clustering Algorithms
- **K-Means**: Partition-based clustering
- **Hierarchical Clustering**: Dendrogram-based with Ward linkage
- **DBSCAN**: Density-based (identifies outliers)

#### 4. Evaluation Metrics
- **Silhouette Score**: Cluster separation quality (higher = better)
- **Davies-Bouldin Index**: Cluster compactness (lower = better)
- **Calinski-Harabasz Score**: Cluster definition (higher = better)
- **Elbow Method**: Optimal number of clusters

#### 5. Dimensionality Reduction
- **PCA**: For visualization and variance analysis
- 3D cluster visualizations in principal component space

### Expected Results

The model discovers distinct game archetypes:

1. **🏆 Critically Acclaimed Blockbusters**: High sales + High quality
2. **💎 Underrated Gems**: Low sales + High quality (hidden masterpieces)
3. **💰 Commercial Hits**: High sales + Lower quality (popular but criticized)
4. **📉 Unsuccessful Titles**: Low sales + Low quality
5. **🎭 Critic Favorites**: Critics appreciate more than users
6. **👥 Fan Favorites**: Users appreciate more than critics
7. **⚖️ Balanced Performers**: Moderate sales and quality

### Key Insights

- Correlation between critic and user scores
- Relationship between quality and commercial success
- Market gaps and opportunities
- Patterns of successful vs unsuccessful games
- Critic-user alignment as market reception indicator

### Installation & Usage

1. **Clone the repository**
2. **Download the dataset** from Kaggle (link above)
3. **Place `Video_Games_Sales_as_at_22_Dec_2016.csv`** in the project directory
4. **Open `CCADMACL_PROJECT.ipynb`** in Jupyter Notebook or VS Code
5. **Run all cells** sequentially

### Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
scipy
```

### Project Structure

```
CCADMACL_PROJECT/
│
├── CCADMACL_PROJECT.ipynb    # Main analysis notebook
├── README.md                  # Project documentation
└── Video_Games_Sales_as_at_22_Dec_2016.csv  # Dataset (download separately)
```

### Research Questions

✓ Do high critic scores consistently align with commercial success?  
✓ How do user-critic discrepancies define unique game clusters?  
✓ What patterns exist between quality and sales in the gaming industry?  
✓ Can unsupervised learning discover "hidden gems"?

### Applications

**For Game Developers:**
- Study successful patterns
- Identify market gaps
- Understand critic-user alignment

**For Gamers:**
- Discover underrated high-quality games
- Find games matching preferences

**For Investors:**
- Identify commercial potential
- Assess market reception indicators

### Authors

Advanced Machine Learning Course Project

### License

Educational Project - For Academic Use
