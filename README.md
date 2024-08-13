# Hotel_Booking_Analysis_EDA
![image](https://github.com/user-attachments/assets/58ed2ec7-8999-4e11-b5a6-cf1cbaee5334)

The success factoring a profitable hotel industry has been changing over time, driven by global competition and increasingly high customer expectations. Hotels focus on customer satisfaction and to exceed customer expectations. We have a hotel booking dataset containing information for city and resort hotels. This dataset has 32 variables with around 1,19,000 entries. It is collected in order to predict hotel bookings and its probability of cancellation. Some attributes here are to understand what factors do bring in the revenue for the business. Some attributes show the customers preference for booking whereas some attributes show the factors leading to cancellations. We have a hotel booking dataset. We are using our Python skills to perform EDA and gain informative insights about factors in hotel bookings and how they affect hotel booking In our data study we have 2 types of hotels- the resort type and city hotel type. There are factors in the study which affect the business of the hotels. Factors such as location, ADR, Deposits charged, wait time, etc. We also have channels like distribution channel, Market segment to focus on to get more revenue


# Libraries Used
* Numpy
* Pandas
* Matplotlib
* Seaborn

# Project Objective
* To know the most preferred type of meal by customers
* To know The Percentage of bookings in each hotel
* To know which hotel is making more revenue
* To find the most preferred length of stay in each hotel
* To know the most preferred distribution channel for bookings
* To know which distribution channel has highest cancellation percentage
* To understand the effect of total stay on average daily revenue
* Find top 10 countrys guest is comming
* Find which agent have maximum no of booking
* Find which month has maximum number of bookig
* Which type of hotel has longer waiting time
* Find which type of hotel is preferred by guest for revisit
* understand the correlation between the variables

# Exploratory Data Analysis
In this study we have sample data about the hotel industry that is not processed for use. Unprocessed data gives inaccurate results. To process this data is called data cleaning. We have cleaned the data by handling null values, outliers and dropping unwanted columns.

# Data Cleaning & Manipulations
## Handling Null Values

* Fisrt we create a copy of our dataset to keep our dataset as at is

* Check duplicates rows, found that 31994 rows are duplicate, so we removed these values using drop.duplicated() function.

* Check which column has null values, and found that company is 93%, agent 13%, country 0.51% and children 0.004 % null values are present.

* Almost 94% value is missing in company column, so it is better to drop the column company

* Almost 14% null values in agent column, Lets fill these value by 0 of this column

* We have less null values (0.51%) in country column, so we will replace null from other as country name.

* So here we see very less null values (0.004%) in children col, so we will replace null values by 0.

* Childer & agent column as datatype as float whereas it contains only int value, so we change datatype as 'int64'

* Changing the datatype of 'reservation_status_date' to datatype of year-month-date

* Adding stays_in_weekend_nights & stays_in_week_nights column to get total_stay duration

* Adding adults, children & babies column to get total_guest

* We have created a col for revenue using total_stay * adr

## Handling Outliers
An outlier is an extremely high or extremely low data point relative to the nearest data point and the rest of the neighbouring co-existing values in a data graph or dataset we work with. We have used the Interquartile range method to handle outliers. To find the interquartile range (IQR), ​we first find the median (middle value) of the lower and upper half of the data. These values are quartile 1 (Q1) and quartile 3 (Q3). The IQR is the difference between Q3 and Q1.
* Plotting a boxplot to find out the outliers, found that adr column has outlier.
* Handle and fixed the outlier by using IQR and capping method (np.where).

# Data Visuslization
Data visualization is the practice of translating information into a visual context, such as a map or graph, to make it easier to understand and gain insights from them. The graphs used here for study are: -
* Barplot
* PieChart
* Scatter Plot
* Heatmap
* Boxplot
* Pairplot

# Solution to Business Objective
* As the peak season is from May to August, with August as the highest booked month, management should consider to utilise staff effectively. Increase room types A, H in order to increase adr and maximise profits

* As majority of the customers are from Portugal and western Europe, management should plan marketing activities in those regions respectively.

* Most preferred stay in hotels is 1 to 4 days, hotel management should introduce loyalty service, offers, tourism package in order to increase the stay of customers and to generate more revenue.

* As 30% of bookings from TA/To are cancelled, management should significantly take stpes to increase direct bookings by offering discounts, loyalty service, coupons on direct bookings in order to reduce cancellation and increase revenue.

* As the City Hotel has more bookings, it generates more revenue and it has more cancellations as well. Management may consider to provide customers with hourly booking option as most of the customers prefer short stay at City Hotel.

# Conclusion
* Bread & Breakfast (BB) is the most preferred meal by the customers.

* Most of the bookings are for City Hotel (61%) comparedto Resort Hotel (39%)

* City Hotel is making more revenue than the Resort Hotel

* Most of the guest stays for 1-4 days in the hotels.

* Most preferred distribution channel by customers is Travel Agent / Tour Oprator (TA/TO) to make hotel booking. also Travel Agent / Tour Operator (TA/TO) has the highest booking cancellation percentage

* Room Type A is the most preferred room type among travellers, while booking, whereas room types H,G,C are generating more adr respectively.

* The length of the stay decreases as ADR increases probably to reduce the cost.

* Most number of bookings are made from Portugal & Great Britain.

* Most number of bookings are made in July and August as compared rest of the months.

* City hotel has significantly longer waiting time, hence City Hotel is much busier than Resort Hotel.

* Resort hotel has slightly higher revisit percentage than City Hotel.

* Lead time, number of days in waiting list or assignation of reserved room to customer does not affect cancellation of bookings.
