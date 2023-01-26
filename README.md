# Hotel Bookings Exploratory Data Analysis
## Objective
We are provided with a hotel bookings dataset.

Out main objective is perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other.
## Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.

Total number of rows in data: 119390
Total number of columns: 32
## Data Cleaning 
#### 1) Removing Duplicate rows
* l duplicate rows were dropped.
#### 2) Handling null values
* values in columns company and agent were replaced by 0.
* values in column country were replaced by 'others'.
* values in column children were replaced by the mean of the column.
#### 3) Removing column
* mpany column is simply dropped.
#### (4) Converting columns to appropriate data types
* anged data type of children, agent to int type.
#### (5) Creating new columns
- Created new column total_stay_in_nights by adding stays_in_weekend_nights+stays_in_week_nights.
* Created new column revenue by multiply total_stay_in_night into adr.
+ Created new column total_guest by adding adults+children+babies.
#### (6) Converting columns to appropriate values
* replacing from column is_canceled [0,1] to not canceled and is canceled.
* replacing column is_repeated_guest [0,1] to not repeated and repeated.
## Exploratory Data Analysis
Performed EDA and tried answering the following questions:

*  Q1) In which hotel more booking have been done?
*  Q2) Which hotel has more cancellation?
*  Q3) Which is the most common channel for booking hotels?
*  Q4) What is the  percentage of bookings in each hotel?
*  Q5) What is the percentage share of repeated & non-repeated guests?
*  Q6) What is the distribution by volume of rooms alotted?
*  Q7) Which hotel has market segments?
*  Q8) From which country most of the guests are comin ?
*  Q9) Which are the most busy months?
*  Q10) Which hotel seems to make more revenue?
*  Q11) What is the affect of total stay days vs ADR?
*  Q12) What is the meal preferance of the guest hotel-wise?
*  Q13) What is the customers relationship in terms of numerical values?
*  Q14) To show all the columns values together?  Mainly

## Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:
* Bar Plot.
* Scatter Plot.
* Pie Chart.
* Line Plot.
* Heatmap.
* Pair Plot

## Conclusion
* City Hotel seems to be more preferred among travellers and it also generates more revenue & profit.
* Most number of bookings are made in July and August as compared rest of the months.
* Room Type A is the most preferred room type among travellers.
* Most number of bookings are made from Portugal & Great Britain.
* Most of the guest stays for 1-4 days in the hotels.
* City Hotel retains more number of guests.
* Around one-fourth of the total bookings gets cancelled. More cancellations are from City Hotel.
* New guest tends to cancel bookings more than repeated customers.
* Lead time, number of days in waiting list or assignation of reserved room to customer does not affect cancellation of bookings.
* Corporate has the most percentage of repeated guests while TA/TO has the least whereas in the case of cancelled bookings TA/TO has the most percentage while Corporate has the least.
* The length of the stay decreases as ADR increases probably to reduce the cost

 
