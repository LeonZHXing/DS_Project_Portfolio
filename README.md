# Data Science Project Portfolio

Zhehao (Leon) Xing · M.S. Biostatistics (Data Science), Yale · [LinkedIn](https://www.linkedin.com/in/leon-xing) · leonxing824@gmail.com

End-to-end data science projects. Each folder is self-contained: a README that leads with the business question and the answer, a fully commented notebook, the figures it produces, and instructions to reproduce.

| Project | Question | Methods | Status |
|---|---|---|---|
| [**rfm_customer_segmentation**](https://github.com/LeonZHXing/DS_Project_Portfolio/tree/main/rfm-customer-segmentation) | Which customers should a retailer spend retention budget on? | RFM, K-Means, DBSCAN, quartile scoring, SQL parity check | ✅ Complete |
| [**yelp_analysis**](https://github.com/LeonZHXing/DS_Project_Portfolio/tree/main/Yelp-analysis) | What can a merchant and a platform each do with the same review dataset? | Time-series aggregation, log-odds text contrast, keyword prevalence, stratified sampling | ✅ Complete |
| [**insurance_claim_risk_ranking**](https://github.com/LeonZHXing/DS_Project_Portfolio/tree/main/Insurance_claim_risk_ranking) | How much should each policyholder pay, given a 3.6% claim rate? | XGBoost, out-of-fold target encoding, imbalance and calibration experiments, permutation importance | ✅ Complete |
| [**mobile_game_retention_abtest**](https://github.com/LeonZHXing/DS_Project_Portfolio/tree/main/Mobile_game_retention_ABtest) | Does moving the first progression gate from level 30 to level 40 improve player retention? | SRM diagnostic, two-proportion z-test, confidence intervals, bootstrap, Welch's t-test, SQL parity check | ✅ Complete |
| recommender-system | *coming soon* | Collaborative filtering, ranking evaluation | 🚧 |

### rfm_customer_segmentation

The top 20% of customers generate 75% of revenue and a third of the base has never placed a second order. Three segmentation methods on 542K transactions, compared, with an action and a first experiment per segment. The analysis also shows RFM space here is a continuum rather than a set of natural clusters, so segment boundaries are presented as a management convention rather than a discovery.

### yelp_analysis

One dataset, three stakeholders, three answers. **Timing:** Friday 18:00 is the busiest hour of the week, and restaurants run two sharp peaks where every other business type sits on a flat 10-to-5 plateau — one staffing rule cannot serve both. **Text:** service is mentioned equally by 4.5-star and 2-star restaurants and therefore carries no signal; waiting and cleanliness are each about 3x more common in low-star tips. **Platform:** Elite is 4.6% of accounts writing 24% of reviews, and it selects a rating behaviour — reviewers who avoid both extremes — rather than louder enthusiasts.

### insurance_claim_risk_ranking

Predicting "no claim" for all 595K policies is 96.4% accurate and worthless, so the task is ranking rather than classification. A gradient boosted model reaches AUC 0.641 on a locked holdout against 0.619 for logistic regression; the top risk decile claims at 7.9% and the bottom at 1.4%, a 5.5x spread that supports the ±40% premium band the brief asked for. Two findings drive the design. Resampling — the reflex on a 26:1 dataset — left the ranking unchanged while pushing predicted claim rates to 4-13x the truth, so the model is trained on the real distribution and its probabilities are used directly for pricing. And the 65% top-5% capture rate in the original requirement is unreachable on these features at 12.8%, which is reported as a limit of the data rather than worked around.

### mobile_game_retention_abtest

Moving the first progression gate from level 30 to level 40 is associated with **lower Day-7 retention: 18.20% versus 19.02%**, a difference of **−0.82 percentage points** (95% CI: −1.33 to −0.31 pp). Across 90,189 players, the analysis supports keeping the existing gate, with no clear compensating gain in recorded game rounds. A 10,000-draw bootstrap gives a similar retention interval, while an outlier sensitivity analysis checks how extreme players influence engagement estimates. The recommendation remains conditional: a sample ratio mismatch (SRM) diagnostic flags the group counts under an assumed 50/50 allocation (p = 0.0086), so assignment and data collection need verification before a rollout decision. Revenue is unavailable, leaving the retention–monetization trade-off unresolved.

**Conventions used across projects**

- README first sentence is the finding, not the method.
- Every cleaning decision is logged with row counts and a reason.
- Evaluation is fixed before modelling, and anything fitted is fitted inside the training fold.
- Method choice is justified against the obvious alternative, and each limitation is stated rather than left for the reader to find.
- Raw data is never committed; each project links to its source.
