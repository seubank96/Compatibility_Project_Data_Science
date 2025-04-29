# Compatibility_Project_Data_Science

This project builds a machine learning model to predict dating compatibility using three datasets: Speed Dating, OKCupid, and Big Five Personality Test.

## Project Description

Using real-world behavioral data, self-expressed lifestyle preferences, and psychological traits, this project predicts mutual romantic interest between participants. The final model uses XGBoost, enhanced by clustering and feature engineering techniques like PCA, SMOTE, and sentiment extraction.

## How to Use

1. **Clone the Repository**
   ```bash
   git clone https://github.com/seubank96/Compatibility_Project_Data_Science.git
   cd Compatibility_Project_Data_Science
2. Install Required Libraries Make sure you have Python installed (preferably 3.8+).
Install the necessary libraries:

```bash
pip install -r requirements.txt
```
3. Download Datasets
- Speed Dating Dataset:
  - Download from Kaggle https://www.kaggle.com/datasets/annavictoria/speed-dating-experiment

- OKCupid Profiles Dataset:
  - Download from Kaggle https://www.kaggle.com/datasets/andrewmvd/okcupid-profiles

- Big Five Personality Test Dataset:
  - Download from Kaggle https://www.kaggle.com/datasets/tunguz/big-five-personality-test

4. Place the downloaded datasets into the appropriate folders:
- /speed_dating/
- /okcupid/
- /big_five/

5. Open the .ipynb file and run it step-by-step to preprocess the data, engineer features, cluster users, and train the final model. Run ipynb files in the following order to achieve results.
   - 1) speed_dating/: Speed_Dating_Cleaning_Preprocessing_EDA.ipynb
     2) big_five/: big_five_cleaning_github.ipynb -> big_five_EDA_preprocessing_clustering_github.ipynb
     3) okcupid/: okcupid_cleaning_github.ipynb -> okcupid_EDA_preprocessing_clustering.ipynb
     4) Merging_Modeling_Analysis_github.ipynb; **NOTE**:  You can run only the final notebook (Merging_Modeling_Analysis_github.ipynb) if you'd like to skip the cleaning steps. Cluster outputs are already included in the root directory as .csv files. 

## Project Structure
- speed_dating/ — Contains Speed Dating Jupyter Notebook File
- okcupid/ — Contains OKCupid profiles Jupyter Notebook Files
- big_five/ — Contains Big Five personality Jupyter Notebook Files
- Merging_Modeling_Analysis_github.ipynb — Main Jupyter Notebook for merging datasets, training models, and analysis
- big_five_clusters.csv — csv file containing clusters created after running Jupyter files in big_five/. Used to add cluster labels in Merging_Modeling_Analysis_github.ipynb
- okcupid_clusters.csv — csv file containing clusters created after running Jupyter files in okcupid/. Used to add cluster labels in Merging_Modeling_Analysis_github.ipynb
- Expo_2025_Poster_Sammy — pdf file of poster presented at the 2025 CofC EXPO.
- Poster_Visualizations — contains png pictures of visualizations and charts used in Expo_2025_Poster_Sammy

## Highlights
- Preprocessing: StandardScaler, missing value imputation, categorical encoding
- Dimensionality Reduction: PCA on lifestyle activity features
- Clustering: KMeans clustering to simulate missing psychological data
- Modeling: XGBoost with SMOTE oversampling and hyperparameter tuning
- Evaluation: F1 score, confusion matrix, feature importance

## Key Results
- Final Model: XGBoost classifier trained on psychological, behavioral, and lifestyle features
- Test Set Accuracy: 84%
- Test F1 Score: 0.51
- Cross-Validated F1 Score: 0.85 (5-fold CV)
- Top Predictors of Compatibility:
  - Attractiveness and fun ratings (both given and received)
  - Shared interests and intelligence
  - Personality clusters (based on Big Five traits)
  - Lifestyle clusters (from OKCupid essay and habit data)

- Best Performing Feature Set: Scenario 3 — using only cluster labels (personality and lifestyle segmentation) — outperformed the full model by offering better generalization.

- Insight: Compatibility prediction improves significantly when deeper traits like personality and lifestyle patterns are used—beyond superficial filters like age or job.

**Note**: Due to the random nature of clustering and model training, exact metrics may vary slightly on re-run.

## License
This project is licensed for educational purposes.
For any questions, contact seubank96.
