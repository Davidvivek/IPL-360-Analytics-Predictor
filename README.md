# IPL Win Probability Predictor (2008-2024)

A Hybrid Machine Learning model that predicts the outcome of IPL matches in real-time. It uses a dual-architecture approach to handle both pre-match uncertainty and live-match mathematical pressure.

## Features
- **Hybrid Architecture:**
- **1st Innings:** Uses `Random Forest Classifier` to predict outcomes based on historical Team Strength, Venue Bias, and Toss Decision.
- **2nd Innings:** Uses `Logistic Regression` to calculate Win Probability based on the "Required Run Rate" pressure equation.
- **Dynamic Feature Engineering:** Calculates real-time metrics like `CRR`, `RRR`, and `Wickets Left` ball-by-ball.
- **Context Aware:** Accounts for Venue history (e.g., Wankhede chasing bias) and Head-to-Head records.

## Model Accuracy
| Scenario | Model Used | Accuracy |
| **Pre-Match / 1st Innings** | Random Forest | **~55-60%** (beats random chance by 5x) |
| **Chasing / 2nd Innings** | Logistic Regression | **~70-80%** (converges as match progresses) |

## Tech Stack
- **Language:** Python 3.10
- **Libraries:** Pandas, Scikit-Learn, NumPy, Matplotlib
- **Concepts:** Pipeline Integration, Column Transformation, Probability Calibration
