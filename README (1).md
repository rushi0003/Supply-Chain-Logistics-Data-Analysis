# Supply Chain & Logistics Data Analysis

**Tools:** Python · Pandas · NumPy · Matplotlib · Seaborn · Jupyter
Notebook\
**Project Type:** Data Cleaning, Exploratory Data Analysis (EDA), Data
Quality Assessment

## Project Overview

This project explores a supply chain and logistics dataset to understand
its structure, assess data quality, summarize key variables, and
investigate relationships between logistics indicators.

The analysis focuses on variables such as shipping costs, lead time,
traffic congestion, fuel consumption, warehouse inventory, delivery-time
deviation, and delay probability. It also documents data limitations so
that findings are interpreted carefully rather than presented as
confirmed operational facts.

## Objectives

-   Understand the dataset's structure, columns, and data types.
-   Check missing values, duplicate records, unique values, and numeric
    ranges.
-   Review summary statistics and variable distributions.
-   Explore correlations between logistics indicators.
-   Identify potential data-quality issues and limits on business
    interpretation.
-   Document findings in a clear, reproducible analysis workflow.

## Dataset Overview

-   **Records analysed:** 32,065
-   **Fields:** 26
-   **Timestamp coverage:** January 1, 2021 -- August 29, 2024
-   **Exact duplicate rows found:** 0

The dataset includes fields related to:

-   **Transport and routes:** GPS latitude/longitude, route risk,
    traffic congestion
-   **Costs and timing:** shipping costs, lead time, ETA variation,
    delivery-time deviation
-   **Warehouse and demand:** inventory level, historical demand,
    loading/unloading time
-   **Risk and conditions:** weather severity, port congestion,
    disruption likelihood, cargo condition
-   **People and equipment:** driver behaviour, fatigue monitoring,
    equipment availability
-   **Scores and outcomes:** delay probability, order fulfillment
    status, supplier reliability

> **Data note:** The dataset's original source and the precise
> definitions of some fields should be documented when available.
> Numeric fields such as `order_fulfillment_status` and
> `cargo_condition_status` contain continuous values in this data, so
> they should not automatically be interpreted as categorical labels.

## Analysis Workflow

1.  **Data loading and inspection**
    -   Load the dataset and inspect rows, columns, data types, and
        dimensions.
    -   Review timestamp validity and coverage.
2.  **Data quality checks**
    -   Check missing values and duplicate rows.
    -   Review unique-value counts and numeric ranges.
    -   Flag values or field definitions that need further validation.
3.  **Statistical analysis**
    -   Calculate descriptive statistics, including mean, median,
        standard deviation, and percentiles.
    -   Review the distributions of key logistics variables.
4.  **Exploratory data analysis**
    -   Examine delay probability, lead time, shipping costs, and
        delivery-time deviation.
    -   Compare selected variables and investigate potential patterns.
5.  **Correlation analysis**
    -   Calculate correlations between numeric variables.
    -   Identify whether the observed linear relationships are strong
        enough to support further investigation.
6.  **Interpretation and documentation**
    -   Summarize findings without treating correlation as causation.
    -   Record data limitations and avoid unsupported operational
        conclusions.

## Preliminary Findings

The following observations are based on the analysis performed so far:

-   The analysed dataset contains **32,065 records** and **26 fields**.
-   No exact duplicate rows were found.
-   All 32,065 timestamps parsed successfully, and the observed date
    range is **2021-01-01 to 2024-08-29**.
-   The mean `delay_probability` value is approximately **0.699**, while
    its median is approximately **0.840**. These are summaries of the
    supplied score, not a verified real-world delivery delay rate.
-   The mean `lead_time_days` value is approximately **5.23 days**.
-   The mean `shipping_costs` value is approximately **459.37**; the
    currency or unit has not been confirmed.
-   The pairwise linear correlations checked so far are very close to
    zero. For example, the correlation between `delay_probability` and
    `delivery_time_deviation` is approximately **0.0055**.

### What these findings mean

The current analysis does not show strong linear relationships among the
checked variables. This does not prove that no relationship exists:
nonlinear patterns, variable definitions, and the dataset's generation
process would need additional investigation.

The dataset should not be assumed to represent verified real-world
operations unless its source and documentation support that claim.

## Tools and Skills Demonstrated

-   **Python:** data inspection and analysis
-   **Pandas:** data cleaning, transformations, summaries, and grouping
-   **NumPy:** numerical analysis
-   **Matplotlib / Seaborn:** visual exploration (where used in the
    notebook)
-   **EDA:** distributions, descriptive statistics, and correlation
    analysis
-   **Data quality assessment:** duplicate checks, timestamp validation,
    uniqueness, and range checks
-   **Analytical communication:** reporting observations with
    appropriate limitations

## How to Run

1.  Clone or download this repository.
2.  Install the required Python packages.
3.  Open the analysis notebook in Jupyter Notebook or JupyterLab.
4.  Update the dataset path in the notebook to match your local file.
5.  Run the notebook cells in order.

Example installation:

``` bash
pip install pandas numpy matplotlib seaborn jupyter
```

## Suggested Repository Structure

``` text
supply-chain-logistics-data-analysis/
├── README.md
├── data/
│   └── README.md
├── notebooks/
│   └── supply_chain_logistics_eda.ipynb
└── visuals/
```

Add your actual notebook and visuals using these names or update this
structure to match your repository. If the dataset is large or has
redistribution restrictions, do not upload it without checking the
source's licence and terms.

## Limitations and Next Steps

-   Confirm the dataset source, licence, and data dictionary.
-   Verify the meaning and units of each score and cost field.
-   Investigate the near-zero correlations and check for nonlinear
    relationships.
-   Create clear visualizations for important distributions and
    comparisons.
-   Avoid presenting model scores as actual business outcomes without
    supporting documentation.

## Conclusion

This project demonstrates a structured approach to inspecting and
exploring supply chain and logistics data with Python. It emphasizes
reproducible analysis, data-quality checks, careful interpretation, and
transparent reporting of limitations.

------------------------------------------------------------------------

**Author:** Add your name or GitHub profile here.
