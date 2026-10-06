# Model governance notes

## Current dashboard status

| Control | Status |
|---|---|
| Deployment status | Governance review required |
| Protected feature identified | `CODE_GENDER` |
| Performance tolerance passed | False |
| Required action | Review protected-feature policy before deployment |

## Subgroup monitoring example: gender

| Group | Customers | Defaults | Observed rate | Predicted rate | Calibration gap (pp) | ROC-AUC |
|---|---:|---:|---:|---:|---:|---:|
| M | 105,059 | 10,655 | 10.1% | 10.0% | -0.16 | 0.78 |
| F | 202,448 | 14,170 | 7.0% | 7.1% | 0.08 | 0.79 |

Additional monitored dimensions include age band, education, and income quintile.

## Required controls before production use

1. Confirm the legal and policy basis for every protected or sensitive variable.
2. Compare models with and without protected features and relevant proxies.
3. Define acceptable performance, calibration, and subgroup thresholds.
4. Perform independent validation and document model limitations.
5. Establish human-review, override, adverse-action, and audit procedures.
6. Monitor drift, calibration, operational outcomes, and subgroup metrics after deployment.

## Interpretation boundary

SHAP explanations attribute model output to input features. They do not show that changing a feature will cause risk to change, and they should not be presented as causal evidence.
