# Project-4

## Project description
In this project I work as an analyst for the telecommunications company Megaline. The company offers its customers prepaid plans, Surf and Ultimate. The commercial department wants to know which of the plans generate the most revenue to adjust the advertising budget.

I will carry out a first analysis of the plans based on a small selection of customers, where I will have data from 500 Megaline customers: which customers they are, where they are from, which plan they use, the number of calls they have made and messages they have sent in 2018. My job is to analyze customer behavior and determine which prepaid plans generate the most revenue.

## Data description

Remember if! Megaline rounds seconds to minutes and megabytes to gigabytes. For calls, each individual call is rounded up: even if a call lasted just one second, it will be counted as one minute. For web traffic, individual web sessions are not rounded up. Instead, the total for the month is rounded up. If someone uses 1025 megabytes this month, they will be charged for 2 gigabytes.

The users table (data about users):
- `user_id`: user identification
- `first_name`: username
- `last_name`: user's last name
- `age`: user age (in years)
- `reg_date`: registration date (dd, mm, yy)
- `churn_date`: the date the user stopped using the service (if the value is missing, the plan was being used when this data was generated)
- `city`: user's city of residence
- `plan`: plan name The calls table (call data)
- `id`: unique caller ID
- `call_date`: call date
- `duration`: duration of the call (in minutes)
- `user_id`: the identifier of the user making the call

The `messages` table (data in text messages):
- `id`: unique text message identifier
- `message_date`: date of the text message
- `user_id`: the identifier of the user sending the text message

The `internet` table (data about web sessions):
- `id`: unique session identifier
- `mb_used`: the volume of data spent during the session (in megabytes)
- `session_date`: web session date
- `user_id`: user identifier
  
The `plans` table (data about plans):
- `plan_name`: the name of the calling plan
- `usd_monthly_fee`: monthly price in US dollars
- `minutes_included`: monthly minutes package
- `messages_included`: monthly text message package
- `mb_per_month_included`: data volume package (in megabytes)
- `usd_per_minute`: price per minute after exceeding the package limit (for example, if the package includes 100 minutes, the first excess minute will be charged)
- `usd_per_message`: price per text message after exceeding package limit
- `usd_per_gb`: Price per extra gigabyte of data after exceeding the package limit (1 GB = 1024 megabytes)

## Libraries
- pandas
- matplotlib
- numpy
- scipy
