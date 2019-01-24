# Australian Self-Managed Super Fund (SMSF) Contribution Analysis

This project follows the CRISP-DM process to provide an analysis for contribution in Australian Self-Managed Super Fund.

### 1. Business Understanding
A self-managed super fund, or SMSF for short, is a do-it-yourself superannuation scheme designed for those who want direct control over their retirement savings and investments. This analysis is based on over 3 million contribution transactions, and targeting to find relationships between transaction date, amount, contributors' location and contribution type. 

### 2. Data Understanding
Data are collected from a MySQL database, by selecting and joining transaction, people and addresses information. It is expecting that most data (over 99%) is clean and completed. Data includes transaction Id, date, amount, split amount in different contribution types, people birthday and people address (suburb, state and country).

### 3. Prepare Data
First, fake data will be removed by fake account id， unrealistic birthday, and unrealistic amount.
Second, data will be removed if birthday or address is missing, since the missing rate is less than 1%.
Third, unrelated columns will be removed.

### 4. Data Modelling
This part is using bar chart and histogram to analyse the acount and trend for people's contribution, and trying to find relationship among data.

### 5. Evaluate the Results
The result tells that 1960s are the major contributors in SMSF. Also, it could be a big contribution gap for people living in different state. 
In the future, it is expected to combine both contribution and investment returns to give a prediction in super performance. 

## How to use
Python 3 is required. Anaconda (https://www.anaconda.com/download/) is recommended.
Install jupyter notebook (https://jupyter.org/) and run the following code.
```bash
jupyter notebook
```

## Libraries required
import numpy
import pandas
import matplotlib.pyplot

## Files
smsf_contribution.html - exported HTML
smsf_contribution.ipynb - Jupyter Notebook File
contribution_transaction.zip - encrypted csv data
README.md
