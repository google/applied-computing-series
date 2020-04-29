<!-- Copyright (C)  Google, Runestone Interactive LLC
  This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
  International License. To view a copy of this license, visit
  http://creativecommons.org/licenses/by-sa/4.0/. -->

Filtering
=========

In this section, you will learn how to filter data in SQL. Previously,
you learned how to filter data in Sheets. Filtering data is to look at
only a subset of rows, based on some column condition. For example, if
you have a database containing information for all citizens of the USA,
a filter could be applied to look only at residents of Texas. You have
already seen
[how to apply filters in Sheets](../filtering_and_grouping/filtering_data.md).

Filtering data in SQL is as simple as using the `WHERE` keyword. You can
append `WHERE column_condition` to any SQL query, and the result will be
filtered only to rows that satisfy the column condition. For example,
you might want to look only at bike trips which are at least one hour
(3600 seconds).

``` {sql}
SELECT
   member_type, start_date, duration
FROM
   trip_data
WHERE
   duration >= 3600
LIMIT
   10
```

It is also possible to filter by multiple criteria. For example to look
at bike trips which are 60 minutes or more and the `member_type` is
`MEMBER`, the query would be as below.

``` {sql}
SELECT
   member_type, start_date, duration
FROM
   trip_data
WHERE
   duration >= 3600 AND member_type = 'Member'
LIMIT
   10
```

### Fill in the blank

1. Write a query to find the ending station and duration of all of trips by
bike number W00153 that lasted over 8 hours.

2. How many trips started and ended at station 31111?

<details>
<summary>Answers</summary>
<br>
 
1. 31606, 40791, 31703, 40820
 
2. 92

</details>
