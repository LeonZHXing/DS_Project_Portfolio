Place the seven Yelp CSVs here.

- Original source: https://www.kaggle.com/datasets/yelp-dataset/yelp-dataset
- Mirror (CSV): https://drive.google.com/drive/folders/1l7RS8dcwW9lT_2hV5LBDtMcj-WdD_Pv9?usp=drive_link

| File | Size | Used by |
|---|---|---|
| `yelp_business.csv` | 30 MB | all sections |
| `yelp_business_hours.csv` | 13 MB | loaded, not used in the final analysis |
| `yelp_checkin.csv` | 130 MB | Q1 |
| `yelp_tip.csv` | 141 MB | Q2 |
| `yelp_review.csv` | 3.79 GB | Q3 and the merchant deep dive |
| `yelp_user.csv` | 1.36 GB | Q3 |

The first four run in a couple of minutes on a laptop. The last two need a High-RAM
environment; on Colab, mount Drive and set `YELP_DATA_DIR` to this folder.
