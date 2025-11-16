# Mango Fashion Production Prediction

CatBoost-based prediction model for the Datathon challenge.

## Best Score: 37

## Quick Start

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the notebook:
   - Open `CB.ipynb`
   - Run all cells
   - Submission will be saved to `submissions/submission_catboost_v1.csv`

## Structure
```
datathon2/
├── CB.ipynb                  # Main prediction notebook
├── data/                     # Competition data
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
├── submissions/              # Generated predictions
└── requirements.txt
```

## Approach
- **Feature Engineering**: Temporal features, color analysis, PCA on image embeddings
- **Model**: CatBoost with optimized hyperparameters
- **Strategy**: 1.08x multiplier to reduce underprediction penalty
1. Run `notebooks/01_eda.ipynb` - Understand data patterns
2. Run `notebooks/02_modeling.ipynb` - Train and validate models
3. Run `notebooks/03_submission.ipynb` - Generate final predictions

## Key Insights
- Production strongly correlates with total demand (r > 0.9)
- Image embeddings capture visual similarity critical for fashion
- Store count and lifecycle length are strong predictors
- Historical overproduction patterns inform bias calibration
