# Freight Rate Prediction

Machine learning solution developed for the Spotter Machine Learning Engineer assessment.

## Approach

I explored and cleaned the freight dataset, engineered time-based features, and used a chronological validation split to simulate future freight-rate prediction.

I compared a rate-per-mile baseline, Random Forest, and CatBoost. CatBoost achieved the strongest performance on the October holdout.

## Validation Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Rate-per-Mile Baseline | $253.85 | $695.05 | 0.7932 |
| Random Forest | $147.76 | $671.49 | 0.8070 |
| CatBoost | $113.34 | $645.82 | 0.8215 |

## Validation Strategy

I trained the development models on January through September 2025 and used October 2025 as a holdout set. This chronological split better represents the final task of predicting future freight rates.

After selecting CatBoost, I retrained the final model using all available labelled development data.

## Run

Install the required dependencies:

pip install -r requirements.txt

Then run the notebook from top to bottom to reproduce the analysis and predictions.
