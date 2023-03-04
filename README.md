# predicting-stock-prices

The code starts by importing the necessary libraries to perform data analysis, such as pandas for data manipulation, matplotlib and seaborn for data visualization, and yfinance for collecting financial data.

Then, a collection of historical data of the Microsoft stock (MSFT) is made through yfinance, filtering the period from "2016-01-01" to "2022-03-03" and storing it in a variable called "table". .

Afterwards, a correlation analysis is performed between the columns of the table using the "corr()" function and displayed using the seaborn "heatmap()" function.

Next, data is separated between the dependent variable (y) and the independent variables (x), selecting the columns "Open", "High" and "Low" from the table to compose x.

Subsequently, the separation of data between training and testing is performed using the "train_test_split()" function of sklearn and storing it in four variables.

Then, two regression models (LinearRegression and RandomForestRegressor) from sklearn are imported and a model is created using RandomForestRegressor, being trained with the training data using the "fit()" function.

Afterwards, the prediction is made using the created model and the test data using the "predict()" function and the model effectiveness is calculated using the sklearn metric "r2_score()".

Finally, a new csv file of financial data is read, the forecast is made using the previously trained model and the data table read and the data predicted by the model are displayed.
