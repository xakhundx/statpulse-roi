# ⚡ StatPulse ROI — Behavioral Habit & Spending Forecaster

> **Client-Side Behavioral Econometrics & Time-Series Engine**  
> *Zero external API keys • Zero login walls • 100% Client-Side LocalStorage Persistence*

Built by **[Ammar Akhund](https://xakhundx.github.io/Portfolio/)** (Economics Major & Statistics Minor, University of Manitoba `'27`).

---

## 🎯 Executive Overview & Purpose

**StatPulse ROI** applies empirical econometric time-series models and Pearson regression to personal human behavior. It addresses a fundamental question at the intersection of cognitive performance and microeconomics:

> *"Does maintaining structured discipline in deep-work focus hours and athletic gym sessions systematically reduce impulse discretionary spending?"*

Inspired by the time-series forecasting pipelines used in my **AESO 24-Hour Wholesale Electricity Price Forecaster** (XGBoost & scikit-learn), StatPulse models personal daily performance as an econometric pipeline:
1. **Focus Hours ($X_1$)**: Deep cognitive work sessions logged per day.
2. **Discipline Indicator ($X_2$)**: Binary indicator for athletic gym/training session.
3. **Discretionary Spending ($Y$)**: Daily capital outflow against a user-defined budget cap.

---

## 🔬 Econometric & Analytical Specifications

- **Pearson Correlation Coefficient ($r$)**:
  $$r = \frac{\sum (X_i - \bar{X})(Y_i - \bar{Y})}{\sqrt{\sum (X_i - \bar{X})^2 \sum (Y_i - \bar{Y})^2}}$$
  Computes the exact mathematical correlation vector between daily focus hours and spending habits.
- **Ordinary Least Squares (OLS) Linear Regression ($\beta_1$)**:
  $$\text{Spend} = \beta_0 + \beta_1(\text{Focus}) + \varepsilon$$
  Calculates the marginal spending change (in dollars) per additional hour of deep cognitive focus.
- **Multi-Year Future Value Compounding Model**:
  $$FV = PMT \times \left[\frac{(1 + r)^n - 1}{r}\right]$$
  Simulates investing the daily budget surplus into an S&P 500 index fund across 1-to-10 year horizons at variable annualized yields ($3\% \dots 14\%$).

---

## 🛠️ Architecture & Tech Stack

- **Frontend & Styling:** Single-file architecture with Tailwind CSS (v3.4) and custom obsidian glassmorphic styling.
- **Data Visualization:** Dual-axis and multi-series charting with **Chart.js (v4.4)**.
- **State Management:** Reactive vanilla JavaScript engine with automatic browser `localStorage` synchronization.
- **Export / Import:** 1-click JSON export for full data portability.
- **Social Distribution:** Built-in **LinkedIn Post Generator** pre-formatted with empirical metrics, percentage gains, and statistical takeaways.

---

## 🚀 Running Locally or Deploying to GitHub Pages

### Run Locally
Open `index.html` directly in any web browser. No server, Node build step, or API keys required.

### Deploy to GitHub Pages
```bash
git init
git add .
git commit -m "feat: initial release of StatPulse ROI"
git branch -M main
git remote add origin https://github.com/xakhundx/statpulse-roi.git
git push -u origin main
```
Then navigate to **Repository Settings → Pages → Deploy from branch (main)**.
