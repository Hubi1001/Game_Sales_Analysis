# Video Game Sales: EDA, Clustering and a Baseline Classifier

Exploratory analysis of the Kaggle dataset [Video Game Sales with Ratings](https://www.kaggle.com/datasets/rush4ratio/video-game-sales-with-ratings), which pairs sales figures with Metacritic review data. The notebook looks at how review scores relate to sales, segments the games with KMeans, and tests whether a Random Forest can predict "sold more than 1 million copies" from the critic and user score alone.

## Results

| Question | Answer |
|---|---|
| How much data is used? | 7,017 of 16,719 rows: games with a critic score and a numeric user score. 1,082 rows with user score "tbd" are dropped. |
| Do review scores relate to sales? | Critic score moderately (Spearman 0.38), user score weakly (0.16). |
| What do the 3 KMeans clusters represent? | Mostly three bands of critic score (about 13-57, 58-75 and 76-98). The features were not scaled and critic score has by far the largest spread, so user score and sales hardly influence the split. |
| Can the scores predict a 1M+ seller? | Only weakly. Accuracy 0.806 is no better than always predicting "not a hit" (0.805). For the 1M+ class (19.5% of the test set): precision 0.50, recall 0.27, F1 0.35, ROC AUC 0.675. |
| Is there a trade-off? | With `class_weight='balanced'` recall rises to 0.56, but precision falls to 0.29 and accuracy to 0.64. |
| Does a random split overstate the result? | Slightly. 726 of 1,404 test rows share a title with a training row (multi-platform releases). A split grouped by title gives ROC AUC 0.650 and F1 0.29 for the 1M+ class. |

## Limitations

- The rows used are not a random sample: 18.9% of them sold over 1M copies, against 12.3% in the whole file.
- One train/test split, default hyperparameters, no cross-validation or tuning.
- The dataset does not say when the scores were recorded, so they cannot be treated as early reviews.

## How to run

```bash
git clone https://github.com/Hubi1001/Game_Sales_Analysis.git
cd "Game_Sales_Analysis/Sales Analysis"
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook Project_Video_Game_Sales_Analysis.ipynb
```

Run all cells from the top. Tested with Python 3.12, pandas 3.1, numpy 2.5, matplotlib 3.11, seaborn 0.13 and scikit-learn 1.9; other versions were not tested.

## Repository layout

```text
Game_Sales_Analysis/
|-- README.md
`-- Sales Analysis/
    |-- Project_Video_Game_Sales_Analysis.ipynb
    `-- Video_Games_Sales_as_at_22_Dec_2016.csv
```

## Contact

Hubert Poździoch - [LinkedIn](https://www.linkedin.com/in/hubert-pozdzioch-4a5933297/) - [GitHub](https://github.com/Hubi1001)
