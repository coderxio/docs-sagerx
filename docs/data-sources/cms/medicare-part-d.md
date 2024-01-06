---
sidebar_position: 1
---

# Medicare Part D

Medicare Part D Prescription Drug Plan Formulary, Pharmacy Network, and Pricing Information

## Description

The Part D Formulary, Pharmacy Network, and Pricing Information Files contain formulary, pharmacy network, and pricing data for Medicare Prescription Drug Plans and Medicare Advantage (MA) Prescription Drug Plans (with the exception of employer and Program of All-Inclusive Care for the Elderly plans). These non-identifiable files are available on a monthly and a quarterly basis and are comprised of the following tables:

- Plan Information - Information such as plan name, contract ID, plan ID, service area, and plan type.
- Geographic Locator - MA and Prescription Drug Plans region codes and county codes.
- Formulary - Formulary details for each plan including National Drug Codes (NDCs), cost share tier level, and indicators for step therapy, quantity limits, and prior authorization.
- Beneficiary Cost - Plan level cost sharing details for preferred, non-preferred, and mail order network pharmacies
- Pharmacy Network - National Provider Identifier (NPI) numbers for each network pharmacy including preferred, retail, and mail order indicators.
- Drug pricing - Plan level average monthly costs for formulary Part D drugs **(note: this table is only available in the quarterly files)**

Data dictionaries for each table and information on how to link across the tables is available in the record layout in the Downloads section below – and in the files themselves. The record layout and data dictionary for the formulary file are subject to change.

Please read the “Terms and Conditions for Use of Part D Formulary, Pharmacy Network, and Pricing Information” in the Downloads section below. This document contains important information regarding timeframes for obtaining data as well as data accuracy and integrity.

## Update Frequency

The Part D benefit year information for plans become available in October of the year prior. For example, year 2024 data is available in the fourth quarter file of 2023. Year 2024 data continues to be available in the Q1-Q3 2024  files, then in the fourth quarter of 2024 year 2025 data becomes available. 

Estimated release dates for upcoming 2024 quarterly data (files reflect data for the quarter that ended the month before the file was released):

- 1/18/24
- 4/25/24
- 7/18/24

## Table Information

### Monthly Files

**NOTE:** Pricing files are NOT available in monthly data.

![image](https://github.com/coderxio/docs-sagerx/assets/3269178/95bee2b4-22d8-415a-b2aa-0a345199b833)

### Quarterly Files

**NOTE:** Pricing files are *only* available in quarterly data.

![image](https://github.com/coderxio/docs-sagerx/assets/3269178/40f54683-5e26-4506-bd66-81ccc46697c1)

## Known Issues

This datasource has a dependency on `zipfile-deflate64` which is currently causing issues when run in production mode due to a requirement for a custom Docker image. Seems to work in development mode though.

If you see an error like below, remove the zipfile-deflate64 dependency as shown in the image below.

```
airflow-init  | !!!!!  Installing additional requirements: 'zipfile-deflate64' !!!!!!!!!!!!
airflow-init  |
airflow-init  | WARNING: This is a development/test feature only. NEVER use it in production!
airflow-init  |          Instead, build a custom image as described in
airflow-init  |
airflow-init  |          https://airflow.apache.org/docs/docker-stack/build.html
airflow-init  |
airflow-init  |          Adding requirements at container startup is fragile and is done every time
airflow-init  |          the container starts, so it is onlny useful for testing and trying out
airflow-init  |          of adding dependencies.
```

![image](https://github.com/coderxio/docs-sagerx/assets/3269178/aec276ab-ec83-4abb-a59d-37d993d3e207)
