<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>HR Analytics — Project README</title>
  <meta name="description" content="HR Analytics project: attrition prediction, workforce insights, and KPI dashboards." />
  <style>
    :root {
      --bg: #0b1220;
      --panel: #0f172a;
      --ink: #e5e7eb;
      --muted: #9ca3af;
      --accent: #38bdf8;
      --accent-2: #a78bfa;
      --ok: #22c55e;
      --warn: #f59e0b;
      --bad: #ef4444;
    }
    html, body { margin: 0; padding: 0; background: var(--bg); color: var(--ink); font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji"; }
    a { color: var(--accent); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .wrap { max-width: 1080px; margin: auto; padding: 2.25rem 1.25rem 4rem; }
    header { display: grid; gap: .75rem; padding: 1.25rem; background: linear-gradient(135deg, rgba(56,189,248,.15), rgba(167,139,250,.12)); border: 1px solid rgba(148,163,184,.2); border-radius: 18px; }
    header h1 { margin: 0; font-size: clamp(1.6rem, 2.2vw + 1rem, 2.4rem); letter-spacing: .2px; }
    header p { margin: 0; color: var(--muted); }
    .badges { display: flex; flex-wrap: wrap; gap: .5rem; margin-top: .25rem; }
    .badge { font-size: .8rem; padding: .35rem .6rem; border-radius: 999px; border: 1px solid rgba(148,163,184,.25); background: rgba(15,23,42,.6); color: var(--ink); }

    nav.toc { margin: 1.25rem 0 2rem; padding: 1rem; border: 1px dashed rgba(148,163,184,.35); border-radius: 14px; background: rgba(15,23,42,.55); }
    nav.toc ul { margin: 0; padding-left: 1rem; line-height: 1.8; }

    section { background: var(--panel); padding: 1.1rem 1.1rem 1.25rem; border-radius: 14px; border: 1px solid rgba(148,163,184,.18); margin-bottom: 1rem; }
    section h2 { margin-top: .2rem; font-size: 1.25rem; }
    .grid { display: grid; gap: .9rem; }
    @media (min-width: 860px){ .grid-2 { grid-template-columns: 1fr 1fr; } .grid-3 { grid-template-columns: repeat(3, 1fr); }}

    code, pre { background: rgba(2,6,23,.7); border: 1px solid rgba(148,163,184,.2); border-radius: 10px; }
    code { padding: .1rem .35rem; }
    pre { padding: .9rem 1rem; overflow-x: auto; }

    table { width: 100%; border-collapse: collapse; }
    th, td { padding: .6rem .5rem; border-bottom: 1px solid rgba(148,163,184,.18); text-align: left; }
    th { color: var(--muted); font-weight: 600; }

    details { border: 1px solid rgba(148,163,184,.22); border-radius: 12px; padding: .6rem .8rem; background: rgba(2,6,23,.35); }
    details[open] { background: rgba(2,6,23,.5); }

    .kpi { display:flex; align-items:center; gap:.75rem; padding:.8rem; border-radius:12px; border:1px solid rgba(148,163,184,.18); background: rgba(2,6,23,.5); }
    .dot { width:.6rem; height:.6rem; border-radius:999px; display:inline-block; }
    .ok { background: var(--ok); }
    .warn { background: var(--warn); }
    .bad { background: var(--bad); }

    footer { color: var(--muted); text-align: center; margin-top: 2rem; }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <h1>HR Analytics — Attrition, Engagement & Workforce Insights</h1>
      <p><strong>Tagline:</strong> Data-driven HR decisions with predictive modeling, KPI dashboards, and actionable insights.</p>
      <div class="badges">
        <span class="badge">Python</span>
        <span class="badge">Pandas</span>
        <span class="badge">SQL</span>
        <span class="badge">Power BI</span>
        <span class="badge">Tableau</span>
        <span class="badge">scikit-learn</span>
      </div>
    </header>

    <nav class="toc">
      <strong>Table of Contents</strong>
      <ul>
        <li><a href="#overview">Overview</a></li>
        <li><a href="#dataset">Dataset</a></li>
        <li><a href="#goals">Business Questions & Goals</a></li>
        <li><a href="#method">Methodology</a></li>
        <li><a href="#eda">Exploratory Analysis</a></li>
        <li><a href="#modeling">Modeling</a></li>
        <li><a href="#kpis">KPIs & Dashboards</a></li>
        <li><a href="#repo">Repository Structure</a></li>
        <li><a href="#setup">Setup</a></li>
        <li><a href="#usage">Usage</a></li>
        <li><a href="#results">Key Results</a></li>
        <li><a href="#ethics">Ethics & Bias</a></li>
        <li><a href="#roadmap">Roadmap</a></li>
        <li><a href="#contrib">Contributing</a></li>
        <li><a href="#license">License</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>

    <section id="overview">
      <h2>Overview</h2>
      <p>This HR Analytics project explores employee <em>attrition</em>, <em>performance</em>, and <em>engagement</em> using real-world inspired datasets. It combines <strong>statistical EDA</strong>, <strong>predictive modeling</strong> (classification), and <strong>interactive BI dashboards</strong> to surface drivers behind churn, absenteeism, and satisfaction—enabling targeted retention strategies.</p>
      <ul>
        <li>Clean, reproducible pipeline with notebooks and scripts.</li>
        <li>Explainable ML with feature importance & SHAP-style insights.</li>
        <li>Shareable visuals via Power BI/Tableau dashboards.</li>
      </ul>
    </section>

    <section id="dataset" class="grid grid-2">
      <div>
        <h2>Dataset</h2>
        <p><strong>Sources:</strong> Public HR datasets (e.g., IBM HR Attrition) or synthetic internal-like data. Replace links below with your actual files.</p>
        <ul>
          <li><a href="#">data/raw/hr_employees.csv</a></li>
          <li><a href="#">data/processed/hr_employees_clean.parquet</a></li>
          <li><a href="#">data/external/lookup_job_roles.csv</a></li>
        </ul>
        <details>
          <summary>Data dictionary (sample)</summary>
          <ul>
            <li><code>Age</code>, <code>Gender</code>, <code>Department</code>, <code>JobRole</code>, <code>MonthlyIncome</code>, <code>OverTime</code>, <code>JobSatisfaction</code>, <code>PerformanceRating</code>, <code>YearsAtCompany</code>, <code>Attrition</code>.</li>
          </ul>
        </details>
      </div>
      <div>
        <h2>Assumptions</h2>
        <ul>
          <li>Personally identifiable information (PII) removed or masked.</li>
          <li>Imbalanced classes addressed via weighting/SMOTE.</li>
          <li>All results are for educational/demo purposes—validate before production.</li>
        </ul>
      </div>
    </section>

    <section id="goals">
      <h2>Business Questions & Goals</h2>
      <ul>
        <li>Which factors most influence <strong>employee attrition</strong>?</li>
        <li>What retention actions could reduce churn by <strong>10–20%</strong>?</li>
        <li>Where are the hotspots for <strong>absenteeism</strong> and <strong>low engagement</strong>?</li>
        <li>How do compensation and tenure impact <strong>performance</strong> and <strong>promotion readiness</strong>?</li>
      </ul>
    </section>

    <section id="method">
      <h2>Methodology</h2>
      <ol>
        <li><strong>Ingestion:</strong> CSV → Parquet; schema checks & type casting.</li>
        <li><strong>Cleaning:</strong> null imputation, outlier winsorization, categorical standardization.</li>
        <li><strong>EDA:</strong> distributions, correlations, pivoted attrition rates.</li>
        <li><strong>Feature Engineering:</strong> tenure bands, overtime ratio, compa-ratio, satisfaction bins.</li>
        <li><strong>Modeling:</strong> Logistic Regression, Random Forest, XGBoost; cross-validated.</li>
        <li><strong>Explainability:</strong> permutation importance, partial dependence, SHAP-like plots.</li>
        <li><strong>Evaluation:</strong> ROC-AUC, PR-AUC, F1, cost-sensitive lift.</li>
        <li><strong>Operationalization:</strong> score new hires; rank retention interventions.</li>
      </ol>
    </section>

    <section id="eda">
      <h2>Exploratory Analysis (Highlights)</h2>
      <ul>
        <li>OverTime and low JobSatisfaction strongly associate with attrition.</li>
        <li>Attrition peaks in the 0–2 year tenure band; stabilizes after 5+ years.</li>
        <li>Certain job roles show higher turnover despite competitive pay—suggests management or workload issues.</li>
      </ul>
      <p><em>See:</em> <code>notebooks/01_eda.ipynb</code></p>
    </section>

    <section id="modeling" class="grid grid-2">
      <div>
        <h2>Modeling</h2>
        <table>
          <thead>
            <tr><th>Model</th><th>ROC-AUC</th><th>F1</th><th>Notes</th></tr>
          </thead>
          <tbody>
            <tr><td>Logistic Regression</td><td>0.79</td><td>0.62</td><td>Baseline, interpretable</td></tr>
            <tr><td>Random Forest</td><td>0.86</td><td>0.69</td><td>Good overall performance</td></tr>
            <tr><td>XGBoost</td><td>0.88</td><td>0.71</td><td><strong>Best trade-off</strong></td></tr>
          </tbody>
        </table>
        <p><em>See:</em> <code>notebooks/02_modeling.ipynb</code></p>
      </div>
      <div>
        <h2>Feature Importance (Top)</h2>
        <ul>
          <li>OverTime (Yes)</li>
          <li>JobSatisfaction (Low)</li>
          <li>YearsAtCompany (0–2)</li>
          <li>MonthlyIncome (below median)</li>
          <li>BusinessTravel (Frequent)</li>
        </ul>
        <p><em>See:</em> <code>reports/figures/feature_importance.png</code></p>
      </div>
    </section>

    <section id="kpis" class="grid grid-3">
      <div class="kpi"><span class="dot bad"></span> <div>
        <strong>Overall Attrition</strong><br/>
        <span class="muted">Current:</span> <code>18.4%</code> → <span class="muted">Target:</span> <code>&lt; 12%</code>
      </div></div>
      <div class="kpi"><span class="dot warn"></span> <div>
        <strong>New Hire 0–12m Attrition</strong><br/>
        <span class="muted">Current:</span> <code>25.1%</code> → <span class="muted">Target:</span> <code>&lt; 15%</code>
      </div></div>
      <div class="kpi"><span class="dot ok"></span> <div>
        <strong>Engagement ↑</strong><br/>
        <span class="muted">JSAT mean:</span> <code>3.6 → 3.9</code>
      </div></div>
      <p style="grid-column:1/-1; color: var(--muted); margin: .2rem 0 0">Connect these to your BI dashboard screenshots: <code>reports/figures/dashboard_overview.png</code>, <code>reports/figures/dashboard_attrition.png</code>.</p>
    </section>

    <section id="repo">
      <h2>Repository Structure</h2>
      <pre><code>hr-analytics/
├─ data/
│  ├─ raw/
│  ├─ processed/
│  └─ external/
├─ notebooks/
│  ├─ 01_eda.ipynb
│  ├─ 02_modeling.ipynb
│  └─ 03_reporting.ipynb
├─ src/
│  ├─ features/engineering.py
│  ├─ models/train.py
│  └─ utils/helpers.py
├─ reports/
│  ├─ figures/
│  └─ dashboards/
├─ requirements.txt
├─ powerbi/ (or tableau/)
└─ README.html (this file)
</code></pre>
    </section>

    <section id="setup" class="grid grid-2">
      <div>
        <h2>Setup</h2>
        <p>Use a fresh virtual environment.</p>
<pre><code># Clone
git clone https://github.com/&lt;your-username&gt;/hr-analytics.git
cd hr-analytics

# Python env
python -m venv .venv
. .venv/bin/activate   # (Windows: .venv\\Scripts\\activate)

# Install deps
pip install -r requirements.txt
</code></pre>
      </div>
      <div>
        <h2>Requirements (sample)</h2>
<pre><code>pandas
numpy
scikit-learn
xgboost
imbalanced-learn
matplotlib
seaborn
jupyter
pyarrow
</code></pre>
      </div>
    </section>

    <section id="usage" class="grid grid-2">
      <div>
        <h2>Usage</h2>
<pre><code># 1) Run EDA
jupyter notebook notebooks/01_eda.ipynb

# 2) Train models
python -m src.models.train \
  --train data/processed/hr_employees_clean.parquet \
  --target Attrition \
  --model xgb \
  --out models/xgb_model.joblib

# 3) Score new data
python -m src.models.score --in data/processed/new_batch.parquet --out scores/predictions.csv
</code></pre>
      </div>
      <div>
        <h2>Power BI / Tableau</h2>
        <ul>
          <li>Open <code>powerbi/HR_Attrition.pbix</code> (or <code>tableau/HR_Attrition.twbx</code>).</li>
          <li>Refresh data connections to <code>data/processed/*.parquet</code>.</li>
          <li>Export dashboard images to <code>reports/dashboards/</code>.</li>
        </ul>
      </div>
    </section>

    <section id="results" class="grid grid-2">
      <div>
        <h2>Key Results</h2>
        <ul>
          <li>XGBoost achieved best ROC-AUC of <strong>0.88</strong> with calibrated probabilities.</li>
          <li>Targeted retention on overtime-heavy teams yields an estimated <strong>~6–9% absolute</strong> churn reduction.</li>
          <li>Promotion readiness model aligns with performance ratings with <strong>~0.72</strong> F1.</li>
        </ul>
      </div>
      <div>
        <h2>How to Interpret</h2>
        <ul>
          <li>Use <strong>risk deciles</strong> to prioritize outreach.</li>
          <li>Combine model scores with <strong>business rules</strong> (tenure & role).</li>
          <li>Validate with A/B pilots before full rollout.</li>
        </ul>
      </div>
    </section>

    <section id="ethics">
      <h2>Ethics, Privacy & Bias</h2>
      <ul>
        <li>Remove sensitive attributes; monitor proxies (e.g., department, tenure).</li>
        <li>Report fairness metrics (TPR/FPR) across cohorts.</li>
        <li>Document model <em>intended use</em> and <em>limitations</em>; avoid adverse impacts.</li>
      </ul>
    </section>

    <section id="roadmap">
      <h2>Roadmap</h2>
      <ul>
        <li>Add survival analysis for time-to-attrition.</li>
        <li>Deploy a lightweight Streamlit app for HR partners.</li>
        <li>Automate retraining with scheduled pipelines (Airflow/GitHub Actions).</li>
      </ul>
    </section>

    <section id="contrib" class="grid grid-2">
      <div>
        <h2>Contributing</h2>
        <p>Pull requests are welcome. For major changes, please open an issue to discuss what you would like to change.</p>
        <ol>
          <li>Fork the repo</li>
          <li>Create a feature branch: <code>git checkout -b feat/your-idea</code></li>
          <li>Commit: <code>git commit -m "feat: add amazing thing"</code></li>
          <li>Push: <code>git push origin feat/your-idea</code></li>
          <li>Open a PR</li>
        </ol>
      </div>
      <div>
        <h2>Badges (optional)</h2>
        <p>Replace <code>&lt;repo&gt;</code> and <code>&lt;user&gt;</code>:</p>
        <p>
          <img alt="license" src="https://img.shields.io/github/license/&lt;user&gt;/&lt;repo&gt;" />
          <img alt="issues" src="https://img.shields.io/github/issues/&lt;user&gt;/&lt;repo&gt;" />
          <img alt="last commit" src="https://img.shields.io/github/last-commit/&lt;user&gt;/&lt;repo&gt;" />
        </p>
      </div>
    </section>

    <section id="license">
      <h2>License</h2>
      <p>This project is licensed under the <a href="#">MIT License</a>. You may use, copy, modify, merge, publish, and distribute, subject to the license terms.</p>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p><strong>Your Name</strong> — Data Analyst / BI Specialist<br/>
      <a href="mailto:you@example.com">you@example.com</a> · <a href="https://www.linkedin.com/in/your-link">LinkedIn</a> · <a href="https://github.com/your-user">GitHub</a>
      </p>
    </section>

    <footer>
      <p>✦ Pro tip: Commit this as <code>README.html</code> at your repo root, and link it from <code>README.md</code>.</p>
    </footer>
  </div>
</body>
</html>
