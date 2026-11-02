# Smart Factory Reliability Analytics

### Interactive Manufacturing Reliability Dashboard | Power BI

An interactive Power BI portfolio project analyzing manufacturing equipment failure patterns using the **AI4I 2020 Predictive Maintenance Dataset** from the UCI Machine Learning Repository.

The dashboard explores machine failure frequency, product-type reliability, and failure-mode contributions to support data-informed manufacturing reliability analysis.

## Dashboard Preview

### Executive Overview

![Executive Overview](screenshots/executive-overview.png)

### Reliability Deep-Dive

![Reliability Deep-Dive](screenshots/reliability-deep-dive.png)

## Project Objectives

- Monitor overall machine failure frequency and observed failure rate.
- Compare failure counts and rates across product types.
- Identify frequently recorded failure modes using Pareto analysis.
- Enable interactive filtering by product type.
- Provide dynamic analytical summaries that respond to report selections.

## Key Findings

| Metric | Result |
|---|---:|
| Total observations | 10,000 |
| Failed observations | 339 |
| Overall failure rate | 3.39% |
| Recorded failure-mode occurrences | 373 |
| Most frequent failure mode | Heat Dissipation Failure (HDF) |
| HDF occurrences | 115 |
| HDF share of failure-mode occurrences | 30.83% |

**Product-type analysis**

- Product type L: 235 failures; 3.92% observed failure rate.
- Product type M: 83 failures; 2.77% observed failure rate.
- Product type H: 21 failures; 2.09% observed failure rate.

Product type L has the highest observed failure rate among the three product categories in this dataset.

**Failure-mode analysis**

The three most frequently recorded failure modes—HDF, OSF, and PWF—account for approximately **82.57% of recorded failure-mode occurrences**.

Failure-mode occurrences are not the same as distinct failed observations. A single observation may contain multiple failure indicators, so the total of 373 occurrences exceeds the 339 failed observations.

## Dashboard Pages

### 1. Executive Overview

Provides a high-level view of manufacturing reliability through:

- KPI cards for total observations, failed observations, and failure rate.
- Product-type comparisons using failure counts and failure rates.
- Interactive product-type slicer.
- Dynamic Key Insights displayed through Power BI Smart Narrative and DAX.

### 2. Reliability Deep-Dive

Provides detailed failure-mode analysis through:

- Failure-mode occurrence KPI.
- Pareto chart combining occurrence counts and cumulative percentages.
- Failure-mode comparison table.
- Dynamic reliability insight identifying the most frequent failure mode.
- Explanation of overlapping failure indicators.

## Tools and Techniques

**Tools:** Microsoft Power BI Desktop, Power Query, DAX, GitHub.

**Techniques:**

- Data cleaning and validation using Power Query.
- Data modeling with a product-type dimension and fact table.
- DAX measures for failure counts, failure rates, and failure-mode occurrences.
- Disconnected failure-mode dimension with a `SWITCH` measure.
- Cumulative percentage calculation for Pareto analysis.
- Interactive filtering and dynamic narrative summaries.

## Dataset

**Source:** UCI Machine Learning Repository — AI4I 2020 Predictive Maintenance Dataset

https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset

The dataset contains 10,000 observations with operational measurements, product-type categories, a machine-failure indicator, and failure-mode indicators.

## Limitations

- The dataset is synthetic and designed for predictive-maintenance research.
- It does not provide actual maintenance costs, downtime durations, or maintenance event histories.
- The report does not claim to measure financial savings or real-world equipment availability.
- Observed associations do not establish the root causes of failures.
- Dynamic narrative summaries are generated from DAX measures and Power BI functionality; this project does not implement a separately trained AI model.

## How to Open the Report

1. Download `Smart_Factory_Reliability.pbix` from this repository.
2. Open it using Microsoft Power BI Desktop.
3. Navigate between **Executive Overview** and **Reliability Deep-Dive**.
4. Use the Product Type slicer to explore the data interactively.

