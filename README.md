# stock_valuation_analysis

# Necessary Libraries
import yfinance as yf, pandas as pd, shutil, os, time, glob, smtplib, ssl
from get_all_tickers import get_tickers as gt

# Yfinance: Gather historical/ relevant data on each stock.
# Pandas: Work with large sets of data.
# Shutil, Glob, and OS: Accessing folders/files on the computer.
# Time: Forcing the program to pause for a period of time.
# Smtplib and SSL: Sending a report over email.
# Get_All_Tickers: Filter through all stocks to get the list you desire.


# List of the stocks we are interested in analyzing. For example: tickers = ["FB", "AMZN", ...] 
tickers = gt.get_tickers_filtered(mktcap_min=150000, mktcap_max=10000000)

# Check that the amount of tickers isn't more than 1800
print("The amount of stocks chosen to observe: " + str(len(tickers)))
