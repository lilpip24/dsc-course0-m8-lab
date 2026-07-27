# Commercial Jet & Passenger Fleet Risk Underwriting Analysis

## Project Overview
This repository contains an end-to-end data engineering and exploratory analysis pipeline designed for a corporate aviation insurer client. The investigation evaluates historical safety and structural accident performance across a 40-year historical lifetime spectrum (1983–2023) to establish data-driven premium frameworks and portfolio risk profiles.

## Core Analytics Implemented
* **Strategic Segmentation:** Implemented strict portfolio partitioning separating Small Aircraft Fleets (<= 20 passenger cap) from Large Passenger Commercial Fleets (> 20 passenger cap).
* **Statistical Volume Control:** Enforced robust sample filters requiring minimum sample counts per manufacturer (N >= 5) and unique configuration models (N >= 10) to minimize single-incident anomaly distortions.
* **Casualty Profiling:** Evaluated underlying injury distributions across makes and specific models using comparative bar plots, density-jitter strip plots, and quartile-mapped violin plots.
* **Environmental & Operational Attribution:** Discovered explicit, statistically significant correlations showing that Instrument Meteorological Conditions (IMC) function as a critical injury risk multiplier, while aircraft phase profile states like Maneuvering and Climb dominate absolute hull destruction probabilities.

## File Hierarchy & Directories
* `data/`: Technical storage containing raw databases (`AviationData.csv`), supplementary lookups (`USState_Codes.csv`), and the pipeline target (`Cleaned_Aviation_Data.csv`).
* `Aviation_Accidents_Cleaning.ipynb`: Preprocessing workflow executing null value treatment, timeline truncation, and feature creation.
* `Aviation_Accidents_Data_Analysis.ipynb`: Main production analytics file containing all target visualization layers, statistical plots, and narrative client insights.