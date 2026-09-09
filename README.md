# Data Science Project Portfolio

Zhehao (Leon) Xing · M.S. Biostatistics (Data Science), Yale · [LinkedIn](https://www.linkedin.com/in/leon-xing) · leonxing824@gmail.com

End-to-end data science projects. Each folder is self-contained: a README that leads with the business question and the answer, a fully commented notebook, the figures it produces, and instructions to reproduce.

| Project | Question | Methods | Status |
|---|---|---|---|
| [**rfm-customer-segmentation**](./rfm-customer-segmentation) | Which customers should a retailer spend retention budget on? | RFM, K-Means, DBSCAN, quartile scoring, SQL parity check | ✅ Complete |
| [**Yelp-analysis**](./Yelp-analysis) | What can a merchant and a platform each do with the same review dataset? | Time-series aggregation, log-odds text contrast, keyword prevalence, stratified sampling | ✅ Complete |
| ab-testing | *coming soon* | Experiment design, power analysis, hypothesis testing | 🚧 |
| recommender-system | *coming soon* | Collaborative filtering, ranking evaluation | 🚧 |

### rfm-customer-segmentation
The top 20% of customers generate 75% of revenue and a third of the base has never placed a second order. Three segmentation methods on 542K transactions, compared, with an action and a first experiment per segment. The analysis also shows RFM space here is a continuum rather than a set of natural clusters, so segment boundaries are presented as a management convention rather than a discovery.

### Yelp-analysis
One dataset, three stakeholders, three answers. **Timing:** Friday 18:00 is the busiest hour of the week, and restaurants run two sharp peaks where every other business type sits on a flat 10-to-5 plateau — one staffing rule cannot serve both. **Text:** service is mentioned equally by 4.5-star and 2-star restaurants and therefore carries no signal; waiting and cleanliness are each about 3x more common in low-star tips. **Platform:** Elite is 4.6% of accounts writing 24% of reviews, and it selects a rating behaviour — reviewers who avoid both extremes — rather than louder enthusiasts.

**Conventions used across projects**

- README first sentence is the finding, not the method.
- Every cleaning decision is logged with row counts and a reason.
- Where two implementations exist (e.g. pandas and SQL), a test asserts they agree.
- Method choice is justified against the obvious alternative, and each limitation is stated rather than left for the reader to find.
- Raw data is never committed; each project links to its source.
