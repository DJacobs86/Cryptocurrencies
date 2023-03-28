# Cryptocurrencies

# Overview
"A client who is preparing to get into the cryptocurrency market" is requesting help examining the services of a prominent investment bank who is offering a new cryptocurrency (crypto) portfolio for its customers. This client has requested a short report on trending crypto companies.
## Purpose
this report will inform the client on trends and classifications in the crypto tradig space.
# Project summary
This project started with a cleaning of datato ensure it is efficient and coherent. I located cryptocurrencies that are currently being traded, removed null values, removed several unnecessary columns, assigned indexes and created "dummy" values, kept cryptocurrencies that are currently being mined, and finally, I scaled my data.

After an extensive cleaning of the data, I reduced the it's dimensions using Principal Component Analysis (PCA) function and I found the best value for "k" using the Elbow Curve Method.
![Elbow Curve Method](https://github.com/DJacobs86/Cryptocurrencies/blob/main/Resources/bokeh_plot%20(1).png)
We decided to run K-Means with k=4 based on the Elbow Curve Method line beginning to flatten at k=4 in the graph.

The clusters are abel to be seen clearly in this 3D scatterplot created from the clustered data.
![3D scatterplot](https://github.com/DJacobs86/Cryptocurrencies/blob/main/Resources/newplot.png)
A sortable and selectable table was created out of the clustered data.
![Table](https://github.com/DJacobs86/Cryptocurrencies/blob/main/Resources/Table.png)

Finally, the clustered data was scaled to "TotalCoinSupply" and "TotalCoinsMined" between 0 and 1 for standard deviation.

After scaling, we plot the scaled data to view "Class" (this is the prediction of classification of the cryptocurrency), "CoinName" (the name of the cryptocurrency), "TotalCoinsMined" (number of coins mined of this crypto type), and "TotalCoinSupply" (reported total number of crypto units) onto the same graph.

![Graph](https://github.com/DJacobs86/Cryptocurrencies/blob/main/Resources/bokeh_plot.png)

After viewing this image, we can clearly see that class 2 (yellow) has mined it's supply completely. Classes 0, 1, and 3 all vary in the amounts of total coins mined versus total coins supplied. I would recommend diversifing one's investment portfolio by buying stocks within class 0 (blue) and class 3 (green) to ensure supply and ability to mine is optimized. More information should be gathered on outliers within class 3 (green) and on differences in class 1 (red).
