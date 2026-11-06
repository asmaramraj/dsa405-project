# dsa405-project

# DSA 405: Project 3 - Charlotte Hornets Points-in-the-Paint Analysis

## Overview
This repository contains the code, data acquisition pipeline, structural join design, and exploratory analysis for Project 3. The objective of this analysis is to evaluate Charlotte Hornets "points-in-the-paint" performance metrics, examine opponent defensive baselines, and uncover structural insights regarding interior scoring efficiency.

## Project Structure
- `data/raw/`: Contains cached source archives (`archive.zip`) and extracted datasets (`scoring.csv`).
- `notebooks/`: Analytical Jupyter / Positron notebooks implementing data acquisition, auditing, joining, and visualization.
- `README.md`: Project documentation, methodology, ethics statement, and structural design specs.

## Data Acquisition Pipeline
Data is programmatically fetched from the repository archive, safely extracted, locally cached, and loaded using a robust Python engine parser (`engine='python'`) with bad-line handling to ensure zero data corruption or tokenization overflow.

## Join Design & Structural Assumptions
- **Join Keys:** `["game_date", "opponent"]`
- **Grain of Left Table (`scoring.csv`):** One row per individual game appearance.
- **Grain of Right Table:** One row per opponent venue baseline.
- **Relationship:** Many-to-one (`validate="m:1"`), ensuring game logs map uniquely to opponent baselines.
- **Join Type Rationale:** A `left` join is utilized to preserve all primary Hornets game appearance records, preventing silent row-dropping.

## Ethics and Legality in Practice
- **Plan Compliance:** Data acquisition matches our initial proposal by relying on a clean, publicly licensed repository archive (`archive.zip`) rather than unauthorized automated scraping of live restricted endpoints.
- **Drift Statement:** Zero drift from proposal specifications.
- **Guardrails:** Zero logins used, zero paywalls bypassed, no personal data processed, and no technical anti-scraping protections circumvented.
