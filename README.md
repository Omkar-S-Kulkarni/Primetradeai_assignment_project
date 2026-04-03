Bitcoin Sentiment vs Trader Performance
This project is about understanding how Bitcoin market sentiment (Fear and Greed Index) affects trader performance
I checked  if there is any real relationship between sentiment and things like profit/loss, win rate, and trading behavior. The idea was to explore the data and check if sentiment can actually be useful for making trading decisions.
used  two datasets for this. One is the sentiment dataset which contains daily Fear and Greed values over time. The second dataset contains historical trade data from Hyperliquid, including details like account, trade size, price, side, timestamp, and PnL.
First, I cleaned both datasets. This involved converting timestamps, fixing date formats, handling missing values, and removing duplicates. After that, I merged the datasets on the date column so that each trade could be matched with the corresponding sentiment value.
Then I created some additional features like profit_flag and loss_flag based on PnL. I also grouped sentiment into three buckets: Fear, Neutral, and Greed. Trade sizes were also categorized to see if size has any effect.
After preparing the data, I did some analysis. I looked at PnL distribution, performance across different sentiment levels, trading activity, and behavior like buy vs sell. I also checked risk by looking at trade sizes and large losses.
From the analysis, a few patterns were visible. Trades during Greed periods generally performed better, with higher average PnL and win rates. Fear periods showed more losses and higher risk. Trading activity was also higher during Greed, which makes sense since the market is more active.
There were also some interesting cases where trades were profitable even during Fear, which suggests that contrarian strategies might work in some situations.
I also tried a simple logistic regression model using sentiment score and trade size. The accuracy was around 63%, so it works as a basic baseline but not something very strong.
On top of that, I tested a simple rule-based idea where trades are taken during Greed with larger position sizes. The cumulative PnL from this looked positive, but this is just a basic check and not a full backtest.
Overall, sentiment does seem to have some effect on trading outcomes, but it is not strong enough to be used alone. It can be useful as an additional signal along with other indicators.
This project is mainly exploratory, but it gives a good starting point for building more advanced trading strategies.




Tech used
Python

Pandas

NumPy

Matplotlib / Seaborn

Scikit-learn


How to run
Clone the repo   [git clone {my repo link here}]
Install dependencies  [!pip install numpy pandas sklearn matplotlib requests ]
Run the notebook or script [run normally]
