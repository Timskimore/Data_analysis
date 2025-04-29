# Tech Stock Price Analysis

A Python‐based analysis of ten major technology companies’ historical stock data.  
This project explores recent closing prices, visualises end-of-month trends, and identifies lifetime percentage gainers.

## Table of Contents

- [Project Overview](#project-overview)  
- [Repository Structure](#repository-structure)  
- [Setup & Installation](#setup--installation)  
- [Usage](#usage)  
- [Analysis Objectives](#analysis-objectives)   
- [Data Dictionary](#data-dictionary) 
- [Interpretation of Results](#interpretation-of-results)  
- [Contributing](#contributing)  
- [License](#license)  

## Project Overview

This notebook ingests daily CSV files for AAPL, AMZN, BABA, CRM, FB, GOOG, INTC, MSFT, NVDA, and TSLA, then:

1. Determines which stock has the highest **most recent** closing price.  
2. Plots **month-end** closing prices for all ten tickers.  
3. Computes each stock’s **total percent return** from its first to its latest close.

A summary of findings is included under [Interpretation of Results](#interpretation-of-results).

## Repository Structure

```plaintext
stock_analysis\
├── data\                           # Ten raw CSVs (e.g., AAPL.csv, AMZN.csv, …)
├── tech_stock_prices.ipynb        # Jupyter notebook with full analysis
├── README.md                       # This file
└── LICENSE                         # Project license
```

## Setup & Installation
1. **Clone repository**  
2. **Create a virtual environment**  
   ```bash
   python -m venv venv
   .\venv\Scripts\activate
   ```
3. **Install dependencies**
```bash
pip install -r requirements.txt
```
## Usage
```plain text
Run the code in Jupyter environment or with Visual Studio Code IDE
```
Or
```bash
jupyter notebook tech_stock_prices.ipynb
```

## Analysis Objectives

### 🗺️ Explore: Which stock has the highest latest closing price?

### 📊 Visualise: End-of-month closing price trends for all ten tickers.

### 🔎 Analyse: Which stock realized the greatest percent increase from its first to its latest close?

## Data Dictionary 

| Column    | Explanation                                                                            |
| --------- | -------------------------------------------------------------------------------------- |
| Date      | Date of observation                                                                    |
| Open      | Opening price                                                                          |
| High      | Highest price during trading day                                                       |
| Low       | Lowest price during trading day                                                        |
| Close     | Close price                                                                            |
| Adj Close | Adjusted close price adjusted for splits and dividend and/or capital gain distribution |
| Volume    | Number of shares traded during trading day                                             |

## Interpretation of Results

Based on the most recent trading day in the dataset, Amazon (AMZN) closed highest at $3,507.07.
The monthly-resampled line chart shows that while all ten tickers generally trend upward over time, Tesla and NVIDIA exhibit the steepest late-cycle rallies.
When ranking total percentage gains (from each ticker’s first available close to its most recent):

**Top 3**
Tesla (TSLA) at 23919.3%
NVIDIA (NVDA)
Amazon (AMZN): 2519.2%


These results suggest that over the long term EV innovators and high-growth hardware have outperformed many software and platform names in sheer raw returns.

## Contributing
We welcome contributions to improve data cleaning, add new features, or fix bugs. Please follow the steps below:

1. Filing Issues
🔍 Search existing issues before opening a new one to avoid duplicates.

📝 Use templates: Provide a clear title, detailed description, example input/output, and your environment setup (OS, Python version).

🚩 Label appropriately: Tag your issue as bug, enhancement, or question.

2. Proposing Changes (Pull Requests)
-   Fork the repository and create a feature branch
-   Install dependencies and run tests locally
-   Add tests or examples for new functionality under a tests\ or examples\ folder
-   Use Commit messages
3. Review Process
-   We aim to review PRs within 3 business days.
-   A minimum of one approval is required before merging.
-   We may request changes—please address feedback promptly.

4. Code of Conduct
By participating, you agree to abide by our Code of Conduct. Be respectful, constructive, and collaborative.

5. Contact
For quick questions, reach out to the maintainer at olanipekuntimileyin@gmail.com or open an issue labeled question.
## License
This project is licensed under [MIT License](./LICENSE).