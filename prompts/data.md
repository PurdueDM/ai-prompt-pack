# Data Science Prompts — 20 Templates

## Data Analysis

### 1. Exploratory Data Analysis (EDA) Guide
```
I have a dataset with these columns: [LIST COLUMNS WITH TYPES]. Rows: [COUNT]. Domain: [DESCRIBE]. Guide me through an EDA: (1) summary statistics and distribution analysis for each numeric column, (2) missing value analysis with imputation recommendations, (3) correlation matrix interpretation, (4) outlier detection method and thresholds, (5) 5 hypotheses to test based on the column names. Provide Python code using pandas and matplotlib.
```

### 2. Data Cleaning Pipeline
```
My dataset has these quality issues: [LIST — missing values, duplicates, inconsistent formats, outliers, etc.]. Columns affected: [LIST]. Build a data cleaning pipeline in Python (pandas) that: (1) handles each issue with the appropriate technique, (2) logs the count of records affected at each step, (3) creates a before/after quality report, (4) is idempotent — safe to re-run. Include validation checks at the end.
```

### 3. Statistical Test Selector
```
I want to test whether [HYPOTHESIS]. Data: [DESCRIBE — sample size, distribution, groups]. Variables: independent = [DESCRIBE], dependent = [DESCRIBE]. Help me: (1) determine the correct statistical test and why, (2) check assumptions (normality, equal variance, independence), (3) write Python code to run the test (scipy.stats), (4) interpret the results in plain English, (5) report effect size and practical significance, not just p-value.
```

### 4. A/B Test Analyzer
```
Analyze this A/B test. Control: [N_CONTROL] users, [METRIC_CONTROL]. Treatment: [N_TREATMENT] users, [METRIC_TREATMENT]. Metric: [CONVERSION RATE/REVENUE/RETENTION/etc.]. Duration: [DAYS]. Calculate: (1) statistical significance (chi-squared or z-test), (2) confidence interval of the lift, (3) practical significance assessment, (4) power analysis — was the sample size sufficient?, (5) recommendation: ship, extend, or kill. Provide Python code.
```

## Machine Learning

### 5. ML Problem Framing
```
I want to predict [TARGET] using [AVAILABLE DATA]. Business context: [DESCRIBE]. Help me frame this as an ML problem: (1) classification vs. regression vs. ranking, (2) appropriate evaluation metric and why (not just accuracy), (3) baseline model recommendation, (4) feature engineering ideas (5 features), (5) potential data leakage risks, (6) minimum viable dataset requirements, (7) deployment considerations.
```

### 6. Feature Engineering Workshop
```
I'm building a model to predict [TARGET]. Available columns: [LIST WITH TYPES]. Domain: [DESCRIBE]. Generate 15 feature engineering ideas: (1) 5 mathematical transformations (log, polynomial, ratios), (2) 5 temporal features (if dates exist) or categorical encodings, (3) 5 domain-specific features based on the business context. For each: name, formula/logic, intuition for why it would be predictive. Provide pandas code.
```

### 7. Model Selection Advisor
```
Task: [CLASSIFICATION/REGRESSION/CLUSTERING/RANKING]. Dataset: [ROWS] rows, [FEATURES] features. Feature types: [NUMERIC/CATEGORICAL/MIXED]. Target distribution: [BALANCED/IMBALANCED/CONTINUOUS]. Priority: [ACCURACY/INTERPRETABILITY/SPEED/LOW LATENCY]. Compare 4 suitable algorithms: (1) how each works (2 sentences), (2) hyperparameters to tune, (3) pros/cons for this specific task, (4) training time estimate, (5) recommended starting configuration. Include scikit-learn code.
```

### 8. Hyperparameter Tuning Strategy
```
I'm tuning a [MODEL TYPE] for [TASK]. Current performance: [METRIC = VALUE]. Hyperparameters available: [LIST]. Dataset size: [ROWS]. Compute budget: [LOW/MEDIUM/HIGH]. Recommend: (1) search strategy (grid/random/Bayesian) with justification, (2) search space for each hyperparameter with ranges, (3) cross-validation strategy, (4) early stopping criteria, (5) code using [OPTUNA/SKLEARN GRIDSEARCH/RAY TUNE].
```

### 9. Model Evaluation Deep Dive
```
Evaluate my [MODEL TYPE] model. Results: [PASTE METRICS — accuracy, precision, recall, F1, AUC, etc.]. Confusion matrix: [PASTE]. Dataset: [SIZE, SPLIT RATIO]. Provide: (1) interpretation of each metric in business terms, (2) error analysis — where does the model fail?, (3) calibration assessment, (4) comparison to baseline, (5) overfitting diagnosis (train vs. test performance), (6) specific recommendations to improve the weakest metric.
```

### 10. ML Pipeline Builder
```
Build an end-to-end ML pipeline for [TASK] using [SKLEARN/PYTORCH/TENSORFLOW]. Steps: (1) data loading and validation, (2) preprocessing (scaling, encoding, imputation), (3) feature selection, (4) model training with cross-validation, (5) evaluation with multiple metrics, (6) model serialization. Include: proper train/test split before any data-dependent preprocessing, logging, and a predict function for new data. Production-ready code.
```

## Data Visualization

### 11. Dashboard Design Advisor
```
Design a dashboard for [AUDIENCE — executives, analysts, operations]. KPIs to display: [LIST 5-8 METRICS]. Data refresh: [REAL-TIME/HOURLY/DAILY]. Tool: [PLOTLY/STREAMLIT/GRAFANA/TABLEAU]. Provide: (1) layout wireframe (text description), (2) chart type recommendation for each KPI with justification, (3) color palette, (4) interactivity features (filters, drill-downs), (5) mobile considerations, (6) code for 3 key charts.
```

### 12. Visualization Selector
```
I need to visualize [DESCRIBE WHAT YOU WANT TO SHOW]. Data: [X variables, Y variables, categories, time series?]. Audience: [TECHNICAL/EXECUTIVE/PUBLIC]. Message: [WHAT INSIGHT TO CONVEY]. Recommend the top 3 chart types with: (1) why each works for this data, (2) what to put on each axis, (3) Python code (matplotlib/seaborn/plotly), (4) design tips (colors, labels, annotations). Rank by clarity of communication.
```

### 13. Data Storytelling Narrative
```
I have these data findings: [LIST 3-5 KEY FINDINGS WITH NUMBERS]. Context: [BUSINESS SITUATION]. Audience: [DESCRIBE]. Help me build a data story: (1) opening hook that creates tension, (2) context setting with one anchor statistic, (3) the journey — walk through findings in logical order, (4) the "aha" moment — the insight that changes thinking, (5) the call to action. Suggest a chart for each finding.
```

## Data Engineering

### 14. ETL Pipeline Designer
```
Design an ETL pipeline. Source: [DATABASE/API/FILE TYPE]. Destination: [DATA WAREHOUSE/LAKE]. Volume: [GB/DAY]. Frequency: [BATCH INTERVAL/STREAMING]. Schema: [DESCRIBE TABLES/FIELDS]. Include: (1) extraction strategy (full vs. incremental), (2) transformation logic (cleaning, joining, aggregation), (3) loading pattern (upsert/append/replace), (4) error handling and retry logic, (5) monitoring and alerting, (6) Python code using [AIRFLOW/PREFECT/DAGSTER/PANDAS].
```

### 15. SQL Query Optimizer
```
Optimize this SQL query that currently takes [DURATION]:

[PASTE SQL QUERY]

Table sizes: [LIST TABLES WITH ROW COUNTS]. Indexes: [LIST EXISTING INDEXES]. Database: [POSTGRES/MYSQL/BIGQUERY/etc.]. Analyze: (1) execution plan interpretation, (2) join optimization opportunities, (3) index recommendations, (4) query rewrite for performance, (5) estimated improvement. Show the EXPLAIN output interpretation and optimized query.
```

### 16. Data Model Designer
```
Design a data model for [DOMAIN — e-commerce, SaaS, IoT, finance]. Key entities: [LIST]. Analytics requirements: [TOP 5 QUESTIONS TO ANSWER]. Model type: [STAR SCHEMA/SNOWFLAKE/OBT]. Include: (1) fact tables with measures, (2) dimension tables with attributes, (3) slowly changing dimension strategy, (4) grain definition for each fact, (5) ERD in text format, (6) DDL statements for [POSTGRES/BIGQUERY].
```

## NLP & Text Analysis

### 17. Text Classification Pipeline
```
Build a text classification pipeline. Task: classify [DOCUMENT TYPE] into [LIST CATEGORIES]. Training data: [DESCRIBE — labeled? how many examples per class?]. Language: [ENGLISH/MULTILINGUAL]. Approach preference: [TRADITIONAL ML/TRANSFORMER/LLM-BASED]. Provide: (1) preprocessing steps, (2) feature extraction method, (3) model code, (4) evaluation with class-level metrics, (5) handling of class imbalance, (6) inference function for new texts.
```

### 18. Sentiment Analysis Framework
```
Build a sentiment analysis framework for [DATA SOURCE — reviews, tweets, support tickets]. Granularity: [DOCUMENT/SENTENCE/ASPECT]. Aspects to track: [LIST IF ASPECT-LEVEL]. Output: [POSITIVE/NEGATIVE/NEUTRAL or 1-5 scale]. Provide: (1) preprocessing pipeline, (2) model approach with tradeoffs, (3) Python code, (4) handling of sarcasm/negation, (5) confidence scores, (6) aggregation for reporting (trends over time).
```

### 19. RAG System Designer
```
Design a Retrieval-Augmented Generation system for [USE CASE — Q&A over docs, customer support, research]. Document corpus: [DESCRIBE — type, count, avg length]. LLM: [MODEL]. Users: [COUNT]. Provide: (1) document chunking strategy (size, overlap, method), (2) embedding model selection, (3) vector store choice, (4) retrieval pipeline with re-ranking, (5) prompt template with context injection, (6) evaluation framework (retrieval precision, answer quality), (7) Python code skeleton.
```

### 20. Data Quality Monitoring System
```
Design a data quality monitoring system for [DATA PIPELINE/TABLE]. Critical columns: [LIST]. Quality dimensions to monitor: completeness, accuracy, consistency, timeliness, uniqueness. For each dimension: (1) specific checks to run, (2) alert thresholds, (3) Python implementation (Great Expectations or custom), (4) dashboard metrics, (5) remediation playbook. Include a daily quality score calculation formula.
```
