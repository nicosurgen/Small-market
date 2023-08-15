# Sales Analysis and Pattern Discovery in a Small Market.

## Project Explanation
I proposed a project to a small market whose owners I know, involving data about transactions from the last 14 days. Since it's a small market, they don't use databases or spreadsheets to track transactions; they use pen and paper. So, they sent me 14 photos of the transactions from the past 2 weeks, and I manually converted this data into a CSV format.

With the data now in CSV format, my project idea revolves around using the **Apriori algorithm** to search for patterns in sales. The goal is to identify products that are often sold together, which could help the business create special offers, arrange related products together, and more.

After obtaining these patterns, I will proceed to analyze the transaction data concerning all products and by sectors. This analysis will be complemented by using the rules obtained from the Apriori algorithm to draw conclusions that could benefit the business.

Finally, I will summarize all the steps taken to present the business owner with the insights gathered during the project. The aim is to provide valuable information for their business.

## Data Preparation
Since the Apriori algorithm requires data to be in one-hot encoding format, the first step is data preprocessing. The steps undertaken during this stage of the process were as follows:
- Loading the CSV file containing transactions; there are 1032 transactions ranging from a minimum of 1 product to a maximum of 5 products per transaction.
- Replacing "None" values with blank spaces.
- Creating a two-dimensional array using lists, where each list represents a transaction, ensuring they all have the same length.
- Training the encoder and creating an array with one-hot encoding using the `TransformEncoding()` method provided by the `mlxtend` library.
- Converting the obtained array into a dataframe.
- Saving and exporting the resulting dataframe in CSV format for use in applying the Apriori algorithm from the `mlxtend` library.
