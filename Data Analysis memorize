import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

df = pd.read_csv("data/btc-market-price.csv",
                 header = None,
                 names = ["Timestamp", "Price"],
                 index_col = 0,
                parse_dates=True)

eth = pd.read_csv("data/eth-price.csv",
                 index_col = 0,
                 parse_dates = True)

prices = pd.DataFrame(index = df.index)
prices["Bitcoin"] = df["Price"]
prices["eth"] = eth["Value"]

# prices.plot(figsize=(12, 6))
# prices.loc['2017-12-01':'2018-01-01'].plot(figsize=(12, 6))

plt.plot(prices.index, prices["Bitcoin"], prices["eth"])
