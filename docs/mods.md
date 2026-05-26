# Custom Project - Modifications

## Using a New Dataset

The dataset used is now **transactions.csv** instead of **sales.csv**. This data comes from a [Kaggle dataset](https://www.kaggle.com/datasets/chitwanmanchanda/fraudulent-transactions-data?resource=download) about fraudulent transaction data.

## Input and Output Names

My .env file includes two new variables: **INPUT_CSV_NAME** and **OUTPUT_CSV_NAME**, making it convenient to change input and output file names without having to search through other files. I also updated .env.example so that others can do the same.

Additionally, the output file is **consumed_transactions.csv**. Changing the output file name lets us avoid overriting previously generated output data.

## Updating the Producer Key

I changed the **key** that the producer extracts from the data to **type**, which describes the transaction type of each row in **transactions.csv**. Updating the key is necessary when using a new dataset because the key references a specific column. If the column is not found in the data, the producer will throw a fatal error.
