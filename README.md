# Finance

 -- S&P500_new_entry.ipynb 

Description:  Python procedure written for quick upload and run on Colab platform or for copy in Python consol useful for analysis and evaluation of potential Tickers elegible in next S&P 500 Index quarterly balance.

Main criteria to satisfy to be a S&P 500 portfolio candidate are as follow (September 2026):
- Headquarters and Listing: company incorporated in the U.S.; primary listing on the NYSE or Nasdaq
- Market Capitalization (unadjusted) ≥ 22.7 billion USD (threshold reviewed quarterly; effective July 2025)
- Free Float: the market value of the free float must be ≥ 50% of the index’s minimum market capitalization threshold, therefore ≥ 11.35 billion USD (50% of 22.7 billion)
- Minimum Free Float (percentage of shares) ≥ 10% of outstanding shares must be in free float (Investable Weight Factor ≥ 0.10)
- Liquidity – Monthly Volumes: at least 250,000 shares traded per month in the 6 months prior to the evaluation
- Liquidity – DV/Float-Cap Ratio: annual dollar value traded / float-adjusted market cap ≥ 0.75
- Profitability (GAAP): positive net income in the last quarter and positive cumulative net income over the last 4 quarters

The procedure searches for Tickers candidates with a web scraping method from: 
- Wikipedia pages for the S&P Mid Cap 400, NASDAQ-100 and S&P Small Cap 600  indices to gather preliminary Ticker names
- Yahoo Finance: the  Yahoo! Finance's API to extract potential S&P 500 candidates criteria data and values linked to Tickers    
to dynamically fetch tickers providing a significantly broader and non-hardcoded list of major US companies for screening process.

From this broad universe, excluding the current S&P 500 members (always extracted from Wikipedia source), procedure selects 10 potential new candidates that meet all S&P 500 defined eligibility criteria, including the new 1-week momentum calculation. 
Candidates are displayed and sorted by descending market capitalization and 1 week - momentum percentage value 
