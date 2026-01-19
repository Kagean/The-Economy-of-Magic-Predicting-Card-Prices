# 🔮 Magic: The Gathering Price Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20%7C%20XGBoost-orange)
![Status](https://img.shields.io/badge/Status-Completed-green)

## 📖 Project Overview
This project applies machine learning techniques to predict the secondary market prices of **Magic: The Gathering** cards. By analyzing over **133,000 cards**, the project identifies key factors driving card value, such as rarity, "Reserved List" status, and EDHREC popularity (Meta Rank).

## 📁 Data Source & Setup

> [!IMPORTANT]
> **Data Download Required:** The project uses `AllPrices.json`, `SetList.json`, and `AllIdentifiers.json` from MTGJSON.com. Due to GitHub's file size limits (the dataset is **1.83 GB**), the raw data files are **NOT** included in this repository. 
> 
> You can download the necessary files from: [MTGJSON Downloads](https://mtgjson.com/downloads/all-files/)

### ⚠️ Installation Warning
To run the code successfully without path errors:
1. **Do not move the files out of the project folder.** The Jupyter Notebooks and JSON data files must remain in the same directory.
2. Ensure you maintain the original folder structure after extracting the ZIP or cloning the repository.

## 🎯 Goals
- To analyze the correlation between card features (Mana Cost, Rarity, Rank) and Price.
- To compare the performance of **Linear Regression**, **Random Forest**, and **XGBoost**.
- To detect market anomalies (undervalued/overvalued cards).

## 📊 Key Findings
- **Rarity is King:** Card rarity is the strongest predictor of price.
- **The "Vintage" Effect:** Prices follow a U-shaped curve based on age (New & Very Old cards are expensive; Mid-era cards are cheaper).
- **The "Meta" Influence:** Popularity in Commander format (EDHREC Rank) has a direct negative correlation with price (Lower rank # = Higher Price).

## 🛠️ Tech Stack
- **Python** (Pandas, NumPy)
- **Visualization:** Seaborn, Matplotlib
- **Machine Learning:** Scikit-Learn, XGBoost
- **Data Source:** MTGJSON

## 🚀 Model Performance
| Model | R² Score | RMSE | Performance Note |
|-------|----------|------|------------------|
| **XGBoost** | ~0.75 | Lowest | Best overall performance, captures complex patterns well. |
| **Random Forest** | ~0.72 | Low | Very stable and reliable, never predicts out-of-bounds values. |
| Linear Regression | ~0.45 | High | Good for understanding trends (positive/negative), but poor accuracy. |

## 🔮 Future Work
- **NLP Analysis:** Implementing Natural Language Processing to analyze card text effects (e.g., "Extra Turn", "Win the Game") and their impact on price.
- **Sentiment Analysis:** Scraping Reddit (r/mtgfinance) and Twitter to measure community hype and sentiment.

## 👨‍💻 Authors

* **Ege Kaan Kıcı** - [LinkedIn Profile](https://www.linkedin.com/in/egekaankıcı)
* **Batu Can Erakman** - [LinkedIn Profile](https://www.linkedin.com/in/batuerakman)
* **Taha Alperen Doğan** - [LinkedIn Profile](https://www.linkedin.com/in/taha-alperen-do%C4%9Fan-6b1511282/)
