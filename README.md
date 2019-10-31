## risk-return-and-Sharpe-Ratio
The Sharpe ratio has been one of the most popular risk/return measures in finance, not least because it's so simple to use. It also helped that Professor Sharpe won a Nobel Memorial Prize in Economics in 1990 for his work on the capital asset pricing model (CAPM).
Let's learn about the Sharpe ratio by calculating it for the stocks of the two tech giants Facebook and Amazon. As a benchmark, we'll use the S&P 500 that measures the performance of the 500 largest stocks in the US.
### Stock Data for Amazon Facebook

![image](https://user-images.githubusercontent.com/46982385/67972193-93112380-fbe4-11e9-97ce-36e5022db7a9.png)

### Visualize & summarize daily values for the S&P 500

![image](https://user-images.githubusercontent.com/46982385/67972238-a91ee400-fbe4-11e9-8aa4-1cce06401139.png)

### The inputs for the Sharpe Ratio: Starting with Daily Stock Returns
The Sharpe Ratio uses the difference in returns between the two investment opportunities under consideration.
However, our data show the historical value of each investment, not the return. To calculate the return, we need to calculate the percentage change in value from one day to the next. We'll also take a look at the summary statistics because these will become our inputs as we calculate the Sharpe Ratio. 

![image](https://user-images.githubusercontent.com/46982385/67972344-dc617300-fbe4-11e9-8806-d3b285af785f.png)

### Daily S&P 500 returns
For the S&P 500, calculating daily returns works just the same way, we just need to make sure we select it as a Series using single brackets [] and not as a DataFrame to facilitate the calculations in the next step.

![image](https://user-images.githubusercontent.com/46982385/67972408-02871300-fbe5-11e9-8b40-03b4e252fdf5.png)

### Calculating Excess Returns for Amazon and Facebook vs. S&P 500
Next, we need to calculate the relative performance of stocks vs. the S&P 500 benchmark. This is calculated as the difference in returns between stock_returns and sp_returns for each day.

![image](https://user-images.githubusercontent.com/46982385/67972488-29454980-fbe5-11e9-90c7-0cbb45924870.png)

### The Sharpe Ratio, Step 1: The Average Difference in Daily Returns Stocks vs S&P 500
Now we can finally start computing the Sharpe Ratio. First we need to calculate the average of the excess_returns. This tells us how much more or less the investment yields per day compared to the benchmark.

![image](https://user-images.githubusercontent.com/46982385/67972534-40843700-fbe5-11e9-8422-fe4a258c2e46.png)

### The Sharpe Ratio, Step 2: Standard Deviation of the Return Difference
It looks like there was quite a bit of a difference between average daily returns for Amazon and Facebook.
Next, we calculate the standard deviation of the excess_returns. This shows us the amount of risk an investment in the stocks implies as compared to an investment in the S&P 500.

![image](https://user-images.githubusercontent.com/46982385/67972567-5560ca80-fbe5-11e9-8c90-8cad2c169ced.png)

### Conclusion
Given the two Sharpe ratios, which investment should we go for? In 2016, Amazon had a Sharpe ratio twice as high as Facebook. This means that an investment in Amazon returned twice as much compared to the S&P 500 for each unit of risk an investor would have assumed. In other words, in risk-adjusted terms, the investment in Amazon would have been more attractive.
This difference was mostly driven by differences in return rather than risk between Amazon and Facebook. The risk of choosing Amazon over FB (as measured by the standard deviation) was only slightly higher so that the higher Sharpe ratio for Amazon ends up higher mainly due to the higher average daily returns for Amazon.
When faced with investment alternatives that offer both different returns and risks, the Sharpe Ratio helps to make a decision by adjusting the returns by the differences in risk and allows an investor to compare investment opportunities on equal terms, that is, on an 'apples-to-apples' basis.
