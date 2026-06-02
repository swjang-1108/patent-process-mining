# Patent Process Mining: Predicting Patent Examination Pendency

Predictive process mining on USPTO patent examination data for pendency prediction.

## Overview
This project applies predictive process mining techniques to the USPTO patent examination process. By treating each patent application as a process instance and examination events (office actions, responses, RCEs, etc.) as activities, we build models that predict the remaining time until a patent is granted — given only a partial prefix of the prosecution history.

## Objective
- Model patent examination as an event log using USPTO PatEx data
- Predict remaining pendency (time to grant) from incomplete prosecution histories
- Compare two prediction approaches:
  - **Direct prediction**: predict total remaining time from prefix features
  - **Step-level prediction**: predict lag between each event, then accumulate
- Identify bottlenecks and delay patterns in the examination process

## Course
This project was developed as a final project for a Business Process Management (BPM) course.

## Data
Data is not included in this repository due to file size and USPTO redistribution restrictions.

Download the following files from the [USPTO Open Data Portal](https://data.uspto.gov/bulkdata/datasets/ecopair):
- `transactions.csv` — prosecution event history for all applications
- `event_codes.csv` — event code descriptions
- `application_data.csv` — application metadata (filing date, grant date, examiner, etc.)

Place all files in the `data/` directory.

## References
- Wu et al. (2025) — predictive process monitoring on patent examination
- USPTO PatEx Technical Documentation (Miller, 2020)