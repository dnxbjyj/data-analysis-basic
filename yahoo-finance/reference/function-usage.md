# data.DataReader
> pip install pandas_datareader
> from pandas_datareader import data
'''
data.DataReader?
Signature: data.DataReader(name, data_source=None, start=None, end=None, retry_count=3, pause=0.001, session=None, access_key=None)
Docstring:
Imports data from a number of online sources.
Currently supports Yahoo! Finance, Google Finance, St. Louis FED (FRED),
Kenneth French's data library, and the SEC's EDGAR Index.
Parameters
----------
name : str or list of strs
    the name of the dataset. Some data sources (yahoo, google, fred) will
    accept a list of names.
data_source: {str, None}
    the data source ("yahoo", "yahoo-actions", "yahoo-dividends",
    "google", "fred", "ff", or "edgar-index")
start : {datetime, None}
    left boundary for range (defaults to 1/1/2010)
end : {datetime, None}
    right boundary for range (defaults to today)
retry_count : {int, 3}
    Number of times to retry query request.
pause : {numeric, 0.001}
    Time, in seconds, to pause between consecutive queries of chunks. If
    single value given for symbol, represents the pause between retries.
session : Session, default None
        requests.sessions.Session instance to be used
Examples
----------
# Data from Yahoo! Finance
gs = DataReader("GS", "yahoo")
# Corporate Actions (Dividend and Split Data)
# with ex-dates from Yahoo! Finance
gs = DataReader("GS", "yahoo-actions")
# Data from Google Finance
aapl = DataReader("AAPL", "google")
# Data from FRED
vix = DataReader("VIXCLS", "fred")
# Data from Fama/French
ff = DataReader("F-F_Research_Data_Factors", "famafrench")
ff = DataReader("F-F_Research_Data_Factors_weekly", "famafrench")
ff = DataReader("6_Portfolios_2x3", "famafrench")
ff = DataReader("F-F_ST_Reversal_Factor", "famafrench")
# Data from EDGAR index
ed = DataReader("full", "edgar-index")
ed2 = DataReader("daily", "edgar-index")
File:      e:\code\env\.env\lib\site-packages\pandas_datareader\data.py
Type:      function
'''