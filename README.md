# Game_Sales_Analysis

# 🎮 Video Game Sales Analysis & Clustering

This project explores the "Video Game Sales with Ratings" dataset from Kaggle to uncover patterns in game sales, user and critic scores, and applies clustering techniques to categorize games based on their performance.  
It also builds a predictive model to forecast high-selling games based on review metrics.

---

## 📚 Dataset
- **Source**: [Kaggle - Video Game Sales with Ratings](https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings)
- **Features**: Game name, platform, genre, publisher, critic score, user score, regional and global sales.

---

## 🛠 Technologies Used
- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (KMeans clustering, Random Forest classification)

---

## 📈 Project Workflow
- **Data Cleaning**: Converted `User_Score` to numeric, dropped rows with missing critical values.
- **Exploratory Data Analysis (EDA)**: 
  - Visualized sales distributions,
  - Analyzed relationships between review scores and sales,
  - Generated a correlation heatmap.
- **Clustering**:
  - Selected features: `Critic_Score`, `User_Score`, `Global_Sales`.
  - Applied KMeans (k=3) to cluster games.
  - Visualized clusters based on performance.
- **Predictive Modeling**:
  - Trained a Random Forest Classifier to predict whether a game exceeds 1 million sales.
  - Evaluated using accuracy, precision, recall, and F1-score.

---

## 🔥 Key Findings
- Games with higher critic and user scores tend to achieve higher global sales.
- Games can be effectively grouped into clusters reflecting different performance profiles.
- Early review scores can successfully predict high-selling titles.

---

## 📂 Project Structure
```bash
|-- Project_Video_Game_Sales_Analysis.ipynb
|-- Video_Games_Sales_as_at_22_Dec_2016.csv
|-- README.md
|-- .gitignore
```

---

## 🚀 How to Run
1. Clone this repository.
2. Ensure `Video_Games_Sales_as_at_22_Dec_2016.csv` and the notebook are in the same directory.
3. Open `Project_Video_Game_Sales_Analysis.ipynb` with Jupyter Notebook or VSCode and run all cells sequentially.

---

## 📋 GitHub About Section
> **Video Game Sales Analysis & Clustering**:  
> This project explores global video game sales data, analyzes the relationship between critic and user scores, clusters games based on performance metrics, and predicts high-selling titles using machine learning techniques.

---

## 🏷 Recommended Topics (Tags)
```
data-analysis
machine-learning
clustering
kmeans
random-forest
pandas
seaborn
python
videogames
sales-data
portfolio-project
```

---

## 📬 Contact
Hubert Poździoch  
- [LinkedIn](https://www.linkedin.com/in/hubert-pozdzioch-4a5933297/)  
- [GitHub](https://github.com/Hubi1001)

---
