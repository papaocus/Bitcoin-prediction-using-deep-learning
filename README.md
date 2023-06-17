# Bitcoin-prediction-using-deep-learning

Importing libraries:

The code begins by importing the necessary libraries, including pandas, numpy, and matplotlib.pyplot. These libraries are commonly used for data manipulation, numerical operations, and data visualization.
Loading the dataset:

The code uses pandas to read a CSV file named "all_currencies.csv" located at the specified file path.
The df.head() function is then called to display the first few rows of the dataset.
Checking for missing values:

The code uses the df.isnull().sum() function to check the number of missing values in each column of the DataFrame.
The output shows the count of missing values in each column.
Examining dataset information:

The code calls df.shape to display the dimensions (number of rows and columns) of the DataFrame.
The df.info() function provides information about the DataFrame, including column names, non-null count, data types, and memory usage.
Visualizing top currencies by market cap and transaction volume:

The code generates two horizontal bar plots using matplotlib.pyplot.
The first plot shows the top 10 currencies based on market capitalization, sorted in descending order.
The second plot displays the top 10 currencies based on transaction volume, also sorted in descending order.
Filtering data for top 5 currencies:

The code selects the top 5 currency names based on market capitalization.
A new DataFrame named data_top_5_currencies is created, which contains only the rows corresponding to the top 5 currencies.
Plotting price, market cap, and volume trends for the top 5 currencies:

Three line plots are generated using matplotlib.pyplot.
The first plot shows the average closing price per unit of currency over time.
The second plot displays the average market capitalization per currency over time.
The third plot illustrates the average transaction volume per currency over time.
Additional data visualization:

The code plots the closing prices of all currencies using df['Close'].plot().
A lag plot is created for the 'Volume' column using lag_plot from pandas.plotting.
Data preprocessing and LSTM model:

The code focuses on the 'BTC' (Bitcoin) currency.
The 'Close' column for Bitcoin is extracted into a DataFrame named df_BTC.
The shape of the df_BTC DataFrame is displayed.
The 'Close' values are scaled using the MinMaxScaler from scikit-learn.
The training and validation data are split based on the time period.
The training data is further processed into input (x_train) and output (y_train) sequences.
A LSTM (Long Short-Term Memory) model is created using the Keras library.
The model architecture consists of two LSTM layers with 50 units each, followed by a Dense layer.
The model is compiled with the mean squared error (MSE) loss function and the Adam optimizer.
The training of the model is performed with 2 epochs and a batch size of 1.
