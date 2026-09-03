# Data Science Project Portfolio

Zhehao (Leon) Xing · M.S. Biostatistics (Data Science), Yale · [LinkedIn](https://www.linkedin.com/in/leon-xing) · leonxing824@gmail.com

End-to-end data science projects. Each folder is self-contained: a README that leads with the business question and the answer, a fully commented notebook, the figures it produces, and instructions to reproduce.

| Project | Question | Methods | Status |
|---|---|---|---|
| [**rfm-customer-segmentation**](./rfm-customer-segmentation) | Which customers should a retailer spend retention budget on? | RFM, K-Means, DBSCAN, quartile scoring, SQL parity check | ✅ Complete |
| ab-testing | *coming soon* | Experiment design, power analysis, hypothesis testing | 🚧 |
| recommender-system | *coming soon* | Collaborative filtering, ranking evaluation | 🚧 |

**Conventions used across projects**

- README first sentence is the finding, not the method.
- Every cleaning decision is logged with row counts and a reason.
- Where two implementations exist (e.g. pandas and SQL), a test asserts they agree.
- Raw data is never committed; each project links to its source.
