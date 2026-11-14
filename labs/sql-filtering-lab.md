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

-- 5. Count failed logins by country to check for brute-force
SELECT country, COUNT(*) as failed_attempts FROM log_in_attempts WHERE success = FALSE GROUP BY country ORDER BY failed_attempts DESC;
```

**Query 5 explanation:** This query groups failed logins by country. If one country has a very high count in a short time, it may indicate a brute-force attempt.

## What I Found
- Many failed logins came from the same country in a short time - this looks like a brute-force attempt.
- Filtering with WHERE + AND helped me reduce a large set of logs to a small set of relevant results.

## Why It Matters
SOC analysts may encounter thousands of logs daily. Using SQL filters helps them quickly find real threats and ignore normal activity. Filtering helps analysts detect incidents faster.

## Status: Completed
