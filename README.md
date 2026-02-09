# AEMO-Energy-Market-Pipeline
End-to-end Australian energy market analytics pipeline using OpenElectricity API, NEMOSIS, and Power BI
## Project Overview

This project demonstrates an end-to-end analytics workflow using Australian National Electricity Market data to analyse electricity demand and wholesale prices.

The objective of the project is to show how raw energy market data can be ingested, modelled, and transformed into clear analytical insights using a structured data pipeline and Power BI visualisations.

The project is designed as a portfolio case study, focusing on data understanding, modelling decisions, and communication of insights rather than full production automation.

## Data Sources

The data used in this project is sourced from publicly available Australian energy market datasets, including:

AEMO National Electricity Market data

OpenElectricity API

NEMOSIS datasets

Due to the large size of historical AEMO datasets, this repository includes only representative one-day sample data for demonstration purposes. The full datasets were accessed and processed locally during analysis but are not stored in this repository.

## Pipeline Architecture

The analytics pipeline follows a clear, modular structure:

Data Ingestion
Raw energy market data is sourced from AEMO-related datasets and APIs.

Data Preparation
Data is cleaned and filtered to ensure consistent time intervals, valid pricing values, and aligned demand measurements.

Data Modelling
A star-schema-style data model is created in Power BI, including:

Fact tables for demand and price

Date and time dimensions

Market and region attributes

Analytics and Visualisation
The modelled data is consumed in Power BI to produce interactive dashboards for demand and price analysis.

A conceptual overview of this pipeline is documented in the 03_pipeline_architecture folder.

## Data Modelling Approach

The Power BI data model focuses on analytical clarity and performance:

A dedicated date table is used to support time-based analysis

Demand is measured in megawatts (MW)

Wholesale electricity prices are measured in AUD per megawatt-hour (AUD/MWh)

DAX measures are used to calculate:

Average and peak demand

Price trends across time

Market-level comparisons

This structure allows demand and price to be analysed independently while remaining time-aligned for combined visualisations.

Dashboard and Insights

The Power BI dashboard presents:

Electricity demand trends over time

Wholesale price movements across the market

Combined views of demand and price to highlight market behaviour

Periods of negative pricing, which occur in the NEM due to supply-demand imbalances and high renewable generation

Dashboard screenshots and explanations are available in the 04_dashboard folder.

## Repository Structure
aemo-energy-market-pipeline
│── README.md
│
│── 01_raw_data/
│   └── README.md
│
│── 02_data_model/
│   └── README.md
│
│── 03_pipeline_architecture/
│   └── README.md
│
│── 04_dashboard/
│   └── README.md


Each folder contains documentation explaining its purpose and how it fits into the overall pipeline.

## Limitations

Only a limited sample of raw data is included due to dataset size constraints

The pipeline is not fully automated and is intended for analytical demonstration

Real-time API connections are not enabled in this portfolio version

These limitations are intentional to keep the project focused on analytics and modelling fundamentals.

## Future Improvements

Potential extensions of this project include:

Automating data ingestion using scheduled API calls

Expanding analysis to multi-year historical datasets

Adding forecasting models for demand and price

Publishing dashboards via Power BI Service

Enhancing documentation with detailed data dictionaries

## Tools and Technologies

Python (data extraction and preparation)

Power BI (data modelling and visualisation)

AEMO, OpenElectricity, and NEMOSIS datasets

GitHub for version control and documentation

