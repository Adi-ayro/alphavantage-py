# Python Client For Alpha Vantage API

The following code is an API Library for Alpha Vantage API. It is a stock market data API which is used to gather data and insights about the stock market. For more info on the API kindly refer to [https://www.alphavantage.co/documentation](https://www.alphavantage.co/documentation/)

## Note

The Library was developed in 2020, Since then some of the features have been added and depreciated in the original API. So some functions are currently not working.

I am working to fix those updates soon and come up with a more refined version. But Till then kindly refer to the Alpha Vantage Documentation linked in the Header.

## How to Use

First When You Download alphavantage.py

```python
import wget
apikey = 'Your-Api-Key' # Change These Lines with your info 
location = 'Location where you want to store data'
```

Then You can use this like any other python module

```python
import alphavantage as av
av.daily(IBM) # This will download Stock Market Data for IBM in your specified file location
```

## Available Functions

Here is the list of available functions. Parameters in the list are equivalent to the documentation

```python
def daily(symbol, outputsize="compact", datatype="csv"):
def dailyAdj(symbol, outputsize="compact", datatype="csv"):
def intraday(symbol, interval, outputsize="compact", datatype="csv"):
def weekly(symbol, datatype="csv"):
def weeklyAdj(symbol, datatype="csv"):
def monthly(symbol, datatype="csv"):
def monthlyAdj(symbol, datatype="csv"):

#Fundamental Data

def overview(symbol):
def income(symbol):
def balancesheet(symbol):
def cashflow(symbol):

#Forex
#I had to use from as form due to from being a reserved word

def exchangerate(form, to):
def intradayFX(form, to, interval, outputsize='compact', datatype='json'):
def dailyFX(form, to, outputsize='compact', datatype='json'):
def weeklyFX(form, to, datatype='json'):
def monthlyFX(form, to, datatype='json'):

# todo Crypto

def dailyCrypto(symbol, market, datatype='json'):
def weeklyCrypto(symbol, market, datatype='json'):
def monthlyCrypto(symbol, market, datatype='json'):
def cryptoRating(symbol):
```
