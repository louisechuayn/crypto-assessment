# Crypto Data Analysis Project

This repository contains two Jupyter notebooks that analyze different aspects of the cryptocurrency market using public APIs.

## Project Overview

This project consists of two separate analyses:

### Task One: Wallet Transactions

This notebook analyses the transaction history of a specific Ethereum whale wallet. It uses the Etherscan API (token required) to fetch up to 10,000 transactions for the wallet. The data is then processed and visualized as a bi-directional weighted graph of the 20 most recent transactions, with wallets as nodes and transactions as arrows. The thickness of the arrows is weighted by the transaction value.

### Task Two: Dogecoin Market Analysis

This notebook analyses Dogecoin's market data, including price and volume. It fetches data from the CoinGecko API for a specific date range. The data is cleaned and visualized using a time series plot that displays both price and volume, with annotations for key events.


## Installation

### 1. Clone the repository
git clone https://github.com/louisechuayn/crypto-assessment.git
cd dogecoin-forensics

### 2. Set up environment
Using pip:
pip install -r requirements.txt

Or using conda:
conda create -n doge-analysis python=3.12
conda activate doge-analysis
pip install -r requirements.txt

## Usage
Run task_one.ipynb
Run task_two.ipynb

## Results


### Task one

![ETH Wallet Transaction Graph](images/image_1.png)

![Dogecoin Hourly Price and Volume](images/image_2.1.png)

![Dogecoin Hourly Volume and On-chain Transaction Flow](images/image_2.2.png)

![Dogecoin Hourly Volume and Total CDD](images/image_2.3.png)

![1_Frequency Distribution of Transaction Values](images/image_2.4.png)

![CDD vs Trnansaction Output Value](images/image_2.5.png)

![2_Frequency Distribution of Transaction Values](images/image_2.6.png)




### Macro-Level Analysis
Volume vs. Output Total (USD): Highlighted spikes around 11 Nov 4pm and 12 Nov 3–5pm.
CDD Analysis: Highest CDD spike observed on 13 Nov 4am, following unusual outputs.

📸 Example Screenshot:
(insert image here — e.g. line + bar plot showing suspicious activity window)

### Micro-Level Analysis
Transaction-level data in suspicious windows revealed bursts of unusually high-value transfers.
Some spikes corresponded to old wallets moving DOGE (high CDD), consistent with manipulation risk.
📸 Example Screenshot:
(insert image here — e.g. histogram of transaction sizes or minute-level activity)


## Repository Structure
├── data/               # Raw and processed datasets
├── notebooks/          # Jupyter notebooks for analysis
│   └── analysis.ipynb
├── src/                # Helper functions (data loading, plotting)
├── tests/              # Unit tests for core functions
├── requirements.txt    # Dependencies
└── README.md           # Project overview



## Deliverables
 Source code and notebooks
 Documentation (this README + inline notebook explanations)
 Example results with figures
 Reproducibility instructions


📌 Next Steps
Extend analysis to other tokens (BTC, ETH)
Incorporate wallet clustering heuristics to track repeated suspicious actors
Automate anomaly detection with statistical thresholds or ML models
