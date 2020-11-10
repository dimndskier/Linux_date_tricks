# Linux_date_tricks
Linux date commands with the specialized outputs.

*For a frame of reference, imagine that today is July 21st, 2020.  Results will be different for you, because it is no longer 21 July 2020.*

### Today tricks
#### Today's Date and Time
```date```
Output: **Tue Jul 21 14:02:35 EDT 2020**
#### Today's Date at midnight
```date -d "$( date +%Y-%m-%d )"```
Output: **Tue Jul 21 00:00:00 EDT 2020**
#### Today's Date at 23:59:59
```date -d "$( date +%Y-%m-%d ) +1day -1sec"```<br>
Output: **Tue Jul 21 23:59:59 EDT 2020**


### This Month
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


### Last Month
#### 1st Day of Last Month at midnight
```date -d "$( date +%Y-%m-01 ) -1 month"```<br>
Output: **Mon Jun  1 00:00:00 EDT 2020**
#### 1st Day of Last Month at 23:59:59
```date -d "$(date +%Y-%m-01 ) -1month +1day -1sec"```<br>
Output: **Mon Jun  1 23:59:59 EDT 2020**
#### Last Day of Last Month at midnight
```date -d "$(date +%Y-%m-01 ) -1day"```<br>
Output: **Tue Jun 30 00:00:00 EDT 2020**
#### Last Day of Last Month at 23:59:59
```date -d "$(date +%Y-%m-01 ) -1sec"```<br>
Output: **Tue Jun 30 23:59:59 EDT 2020**


### Next Month
#### 1st Day of Next Month at midnight
```date -d "$( date +%Y-%m-01 ) +1month"```<br>
Output: **Sat Aug  1 00:00:00 EDT 2020**
#### 1st Day of Next Month at 23:59:59
```date -d "$( date +%Y-%m-01 ) +1month +1day -1sec"```<br>
Output: **Sat Aug  1 23:59:59 EDT 2020**
#### Last Day of Next Month at midnight
```date -d "$( date +%Y-%m-01 ) +2month -1day"```<br>
Output: **Mon Aug 31 00:00:00 EDT 2020**
#### Last Day of Next Month at 23:59:59
```date -d "$( date +%Y-%m-01 ) +2month -1sec"```<br>
