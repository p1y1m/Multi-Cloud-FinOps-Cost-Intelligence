Author: Pedro Yanez Melendez

# FinOps Cost Intelligence in Google Colab (Multi-Cloud + SaaS)

## Overview
End-to-end FinOps workflow implemented in **Google Colab**: ingest billing exports, normalize to a unified line-item model, allocate costs with tagging rules, detect anomalies, forecast spend, compute unit economics, and publish an interactive **Plotly dashboard**.

## Data sources integrated
- **GCP Billing export** (line items)
- **AWS Cost & Usage Report (CUR)**
- **Azure Cost Management export**
- **Oracle Cloud (OCI) cost export**
- **Kubernetes** workload cost signals (namespace-level)
- **SaaS invoice exports** (Datadog, Snowflake, Atlassian, GitHub, OpenAI, Slack)

## FinOps capabilities delivered
- Normalize multi-source exports into a single **line-item** schema
- Enforce required allocation keys: **owner, app, env, cost center, business unit**
- Produce **showback/chargeback** rollups by owner/app/cost center
- Track **cost vs net vs amortized** and discount/credit impact
- Measure allocation coverage and isolate **unallocated** spend
- Identify top **cost drivers** by source/service/SKU
- Detect daily spend anomalies using robust statistics (MAD-based z-score)
- Forecast near-term spend and flag **budget risk** by application
- Compute **unit economics** (cost per transaction / cost per active user)
- Generate prioritized optimization opportunities (scheduling, rate review, k8s tuning, SaaS rationalization)

## Run in Colab
1. Execute cells in order (ingest → allocate → KPIs → anomalies → forecast → unit economics → opportunities → charts).
2. Outputs are written under: `/content/finops_showcase/output/`
3. Dashboard and interactive charts are saved under: `/content/finops_showcase/output/plots/`

## Key deliverables
- **Final dashboard (single HTML):**
  `/content/finops_showcase/output/plots/finops_dashboard_plotly.html`
- Supporting artifacts:
  - `/output/kpis/` (KPI overview + rollups)
  - `/output/anomalies/` (alerts table)
  - `/output/forecasting/` (forecast + budget alerts)
  - `/output/unit_economics/` (unit cost tables)
  - `/output/optimizations/` (opportunities + savings estimates)

## Result
A compact, practical FinOps implementation that connects cost data to ownership, usage, and decision-making across multiple clouds and core SaaS platforms.
