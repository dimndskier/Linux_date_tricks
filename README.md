# Linux_date_tricks
Linux date commands with the specialized outputs.

*Imagine that today is July 21st, 2020*

### Today tricks
#### Today's Date and Time
```date```<br>
Output: **Wed Jun 24 14:02:35 EDT 2020**

#### Today's Date at midnight
```date -d "2020-07-21 +1day -1sec"```<br>
Output: **Wed Jun 24 23:59:59 EDT 2020**


### This Month - First Day tricks
#### 1st Day of month at midnight (1st second)
```date -d "2020-07-01 00:00"```<br>
Output: **Wed Jul  1 00:00:00 EDT 2020**

#### 1st Day of month at last second of day
```date -d "2020-07-01 23:59:59"```<br>
Output: **Wed Jul  1 23:59:59 EDT 2020**

#### Last Day and Minute:Second of this Month
```date -d "$( date +%Y-%m-01 ) +1month -1second"```<br>
Output: **Fri Jul 31 23:59:59 EDT 2020**

#### Last Day and Minute:00s of this Month
```date -d "$( date +%Y-%m-01 ) +1month -1minute"```<br>
Output: **Fri Jul 31 23:59:00 EDT 2020**
