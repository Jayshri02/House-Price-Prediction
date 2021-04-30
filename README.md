# House-Price-Prediction
Forecast house prices for an year based on the previous years data.

raw_sales.csv contains house sales data ranging from 2007-2019
malga12345.csv transforms the raw sales data, re-sampling it at quarterly intervals with median price aggregation and step 4 moving average smoothing

The file ma_lga_12345.csv has the median aggregated data 
created from the raw data.
Raw data consists of following columns:
1. datesold: The date on which the property was sold.
2. postcode: The area where property is located.
3. price: The price of the property.
4. propertyType: House/unit
5. bedrooms: No. of bedrooms in the property.
The raw data has been processed to convert raw data into time series 
acceptable data by the following steps:

1. The data is divided into two parts according to propertyType.
2. Each part is then segregated according to the number of bedrooms.
3. Median is then taken for each category quarterly.
4. Date has been assigned to each row as 'saledate' of the last day belonging to the 
respective quarter.


Columns in ma_lga_12345.csv are:
1. saledate: The last day of the quarter
2. MA: The median aggregated price for the quarter
3. type : House/unit
4. bedrooms: 2,3,4,5
