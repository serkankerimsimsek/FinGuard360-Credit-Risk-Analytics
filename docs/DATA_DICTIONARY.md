# Dashboard data dictionary

| Table | Purpose | Representative fields |
|---|---|---|
| `FactCustomerRisk` | Customer-level scoring output | customer ID, calibrated probability, target, risk band, risk decile |
| `RiskBands` | Portfolio summaries by risk band | customers, defaults, observed default rate |
| `RiskDeciles` | Decile-level model performance | decile, customer share, default rate, cumulative capture |
| `ReviewThresholds` | Operational review scenarios | review share, score threshold, reviewed customers, captured defaults, flagged non-defaults |
| `ModelPerformance` | Model-level performance metrics | ROC-AUC, tolerance status, model identifier |
| `ShapFeatures` | Global feature-importance output | feature, source, mean absolute SHAP, mean signed SHAP, positive contribution share |
| `ShapSources` | Importance aggregated by data source | feature source, importance-share percentage |
| `SubgroupAudit` | Eligible-group calibration and discrimination | dimension, group, customers, defaults, observed rate, predicted rate, calibration gap, ROC-AUC |
| `Governance` | Deployment decision signals | protected feature, tolerance status, required governance action |
| `TechnicalReasons` | Customer-level explanation records | customer ID, reason rank, feature, customer value, SHAP contribution, risk effect, technical reason |

Names reflect the Power BI semantic model and may be adjusted if the analysis notebook exports different filenames.
