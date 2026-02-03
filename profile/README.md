# 🏠⚡ Energy Efficiency (UCI ENB2012) - Linear Regression vs Poly(2)+Ridge

> **Single-notebook** project for predicting **Heating Load (Y1)** and **Cooling Load (Y2)** on the **ENB2012** dataset using **2 models only**:
> - **Baseline**: OLS `LinearRegression` + standard preprocessing  
> - **Main**: `PolynomialFeatures(deg=2)` (numeric only) + `Ridge` (**alpha tuned with GridSearchCV**)

---

## 🎯 Targets

| Target | Meaning |
|---|---|
| `Y1` | Heating Load |
| `Y2` | Cooling Load |

---

## 🧠 Models kept in the notebook (exactly)

| Model | Pipeline | Notes |
|---|---|---|
| Baseline | `preprocess_std → LinearRegression()` | Standard scaling for numeric + one-hot for categorical |
| Main | `preprocess_poly → Ridge(random_state=42)` | Polynomial expansion **only on numeric** (degree=2, no bias) + Ridge **tuned** |

**Ridge tuning grid (as coded):**  
`model__alpha = np.logspace(-4, 4, 30)` (30 values)

---

## 🧩 Data & column expectations

### 📥 Input files (exact paths the notebook checks)

| Priority | File | Expected location |
|---:|---|---|
| 1 | `ENB2012_data.xlsx` | `../data/raw/ENB2012_data.xlsx` |
| 2 | `ENB2012_data.csv` | `../data/raw/ENB2012_data.csv` |

### 🧾 Expected columns

| Type | Columns |
|---|---|
| Features | `X1, X2, X3, X4, X5, X6, X7, X8` |
| Targets | `Y1, Y2` |

### 🛟 Auto-map behavior (only if expected columns are missing)
If the notebook **cannot find** `X1..X8,Y1,Y2`, it tries:
- Take the **first 10 numeric columns** in the file
- Rename them to: `X1..X8, Y1, Y2`

If fewer than 10 numeric columns exist → it raises an error.

### 🏷️ Feature typing (hard-coded)
| Group | Columns | How it’s handled |
|---|---|---|
| Categorical | `X6`, `X8` | Forced to string: `astype("Int64").astype(str)` then `OneHotEncoder(handle_unknown="ignore", sparse_output=False)` |
| Numeric | `X1, X2, X3, X4, X5, X7` | Scaled with `StandardScaler()` (and optionally expanded with polynomial features in the main model) |

---

## ⚙️ Train/Test split & CV (as coded)

| Item | Value |
|---|---|
| Split | 80/20 |
| `random_state` | `42` |
| Split method | `train_test_split(idx, test_size=0.2, random_state=42)` (split indices once and reuse for Y1 & Y2) |
| CV | `KFold(n_splits=5, shuffle=True, random_state=42)` |
| Parallelism | `cross_validate(..., n_jobs=-1)` and `GridSearchCV(..., n_jobs=-1)` |

---

## 📏 Metrics (CV + Test)

### ✅ CV scoring dictionary (exact)
| Key | Meaning | Implementation |
|---|---|---|
| `r2` | R² | `"r2"` |
| `neg_rmse` | negative RMSE | custom scorer: `-sqrt(MSE)` |
| `neg_mae` | negative MAE | `"neg_mean_absolute_error"` |

### 🧪 Test metrics computed (exact)
- `test_r2` = `r2_score(y_test, y_pred)`
- `test_rmse` = `sqrt(mean_squared_error(y_test, y_pred))`
- `test_mae` = `mean_absolute_error(y_test, y_pred)`

---

## 🧱 Preprocessing details

### 🧼 Baseline preprocessing: `preprocess_std`
- Numeric: `StandardScaler()`
- Categorical: `OneHotEncoder(handle_unknown="ignore", sparse_output=False)`
- `ColumnTransformer(..., remainder="drop", verbose_feature_names_out=False)`

### 🧬 Main preprocessing: `preprocess_poly`
- Numeric: `StandardScaler()` → `PolynomialFeatures(degree=2, include_bias=False)`
- Categorical: `OneHotEncoder(handle_unknown="ignore", sparse_output=False)`
- `ColumnTransformer(..., remainder="drop", verbose_feature_names_out=False)`

---

## 🗂️ Outputs (files written by the notebook)

The notebook defines:
- `PROJECT_ROOT = Path("..").resolve()`
- Output dirs are auto-created:
  - `../outputs/figures/`
  - `../outputs/tables/`
  - `../outputs/models/`

### 📊 Tables saved (CSV)
| Target run | File |
|---|---|
| Y1 | `../outputs/tables/two_models_results_Y1_heating.csv` |
| Y2 | `../outputs/tables/two_models_results_Y2_cooling.csv` |

### 💾 Models saved (Joblib) — only the **best tuned main** per target
| Target run | File |
|---|---|
| Y1 | `../outputs/models/main_model_Y1_heating.joblib` |
| Y2 | `../outputs/models/main_model_Y2_cooling.joblib` |

---

## 🖼️ Figures (saved to `../outputs/figures/`)

All plots are **saved** (dpi=240) and also displayed.

### 🧪 Diagnostic plots (two-panel layout: Baseline | Main)
For each target (`Y1_heating`, `Y2_cooling`):

| Plot | Filename pattern |
|---|---|
| Predicted vs Actual (parity) | `{target}_panels_parity.png` |
| Residuals vs Predicted | `{target}_panels_resid_vs_pred.png` |
| Residual histogram | `{target}_panels_resid_hist.png` |
| Q–Q plot (residuals) | `{target}_panels_qq.png` *(only if SciPy is available; otherwise skipped)* |

> Note: The notebook uses fixed colors for the two panels (Baseline/Main) inside plotting helpers.

### 📈 Summary comparison plots
| Plot | Filename pattern |
|---|---|
| Learning curve (R²; Baseline vs Main) | `{target}_compare_learning_curve.png` |
| CV R² distribution (boxplot) | `{target}_compare_cv_r2_box.png` |

### 🧾 Coefficients plots (separate per model)
Because Baseline and Main have **different feature spaces**, coefficients are plotted separately:

| Plot | Filename pattern |
|---|---|
| Top coefficients — Baseline | `{target}_baseline_top_coef.png` |
| Top coefficients — Main | `{target}_main_top_coef.png` |

---

## 🧭 Expected repository layout (as assumed in code)

The notebook assumes it lives in `./notebooks/` and sets root to `..`:

```
project_root/
  data/
    raw/
      ENB2012_data.xlsx   (or ENB2012_data.csv)
  notebooks/
    enery_efficiency_LR.ipynb
  outputs/
    figures/
    tables/
    models/
```

---

## 🧰 Requirements

| Package | Used for |
|---|---|
| numpy, pandas | data handling |
| matplotlib | plotting |
| scikit-learn | preprocessing, models, CV, tuning |
| joblib | saving models |
| scipy *(optional)* | Q–Q plots (`stats.probplot`) |

Install example:
```bash
pip install numpy pandas matplotlib scikit-learn joblib scipy
```

---

## ▶️ How to run

1. Place the dataset at one of:
   - `../data/raw/ENB2012_data.xlsx` **or**
   - `../data/raw/ENB2012_data.csv`

2. Run the notebook:
   - `notebooks/enery_efficiency_LR.ipynb`

3. Check results:
   - Tables: `../outputs/tables/`
   - Figures: `../outputs/figures/`
   - Saved models: `../outputs/models/`

---

## ♻️ Reproducibility notes
- Split reproducibility: `random_state=42`
- CV reproducibility: `KFold(..., shuffle=True, random_state=42)`
- Main model seed: `Ridge(random_state=42)`

---

## 📝 Notes
- Warnings are suppressed globally: `warnings.filterwarnings("ignore")`
- If SciPy is not installed, Q–Q plots are skipped with a console message.
