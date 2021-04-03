%matplotlib notebook # Load matplotlib into Jupyter 

# Biolerplate necessary for Jupyter Notebook to install libraries correctly. 

import sys
!{sys.executable} -m pip install numpy pandas matplotlib seaborn # 

# Import data analysis libs

import numpy as np
import pandas as pd

# Import visualization libs
import matplotlib.pyplot as plt
import seaborn as sns

full_df = pd.read_csv("StockX-Data-Contest-2019-3.csv") # load data set from: https://www.kaggle.com/hudsonstuck/stockx-data-contest

sneaker_f = full_df.groupby("Sneaker Name").count() # Aggregate data on 'Sneaker Name'.

intermediary_v = sneaker_f.drop(columns=["Order Date", "Brand", "Sale Price", "Retail Price", "Release Date", "Shoe Size"])
new_sf = intermediary_v.rename(columns={"Buyer Region": "Count"})

most_sneakers_sold = new.sort_values("Count", ascending=False)
sneakers_top_10 = most_sneakers_sold.head(10).sort_values("Count") # Get Top 10 sneakers sold. 

# Create figure

fig, ax = plt.subplots(figsize=[10, 10])
plt.xticks(rotation=270, fontsize=13, fontname="AppleGothic")
plt.ylabel("# Shoes Sold (1Sep17-13Feb19)")

# Create barplot

plt.bar(sneakers_top_10.index,sneakers_top_10["Count"], color=["#08a05c", "White"], edgecolor=["White", "#08a05c"]) # StockX color


