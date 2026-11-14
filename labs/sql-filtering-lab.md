# SQL Filtering for SOC Analysis

## What I Did
I used SQL to filter security logs like a SOC analyst investigates suspicious logins.

## Dataset Used
Table: log_in_attempts
Columns: event_id, login_time, username, country, success

## Queries I Used

```sql
-- 1. Find all failed logins
SELECT * FROM log_in_attempts WHERE success = FALSE;

-- 2. Find failed logins from outside US
SELECT * FROM log_in_attempts WHERE success = FALSE AND country != 'USA';

-- 3. Find logins after office hours
SELECT * FROM log_in_attempts WHERE login_time > '22:00:00';

-- 4. Find a specific user - suspicious activity
SELECT * FROM log_in_attempts WHERE username = 'admin' AND success = FALSE;
```

## What I Found
- Many failed logins came from the same country in a short time - this looks like a brute-force attempt.
- Filtering with WHERE + AND helped me reduce 1000+ logs to only 10-15 suspicious logs.

## Why It Matters
SOC analysts may encounter thousands of logs daily. Using SQL filters helps them quickly find real threats and ignore normal activity. Filtering is a common contributor to faster incident detection.

## Status: Completed
