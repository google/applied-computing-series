<!-- Copyright (C)  Google, Runestone Interactive LLC
  This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
  International License. To view a copy of this license, visit
  http://creativecommons.org/licenses/by-sa/4.0/. -->

Aggregating
===========

Sheets provides aggregating/grouping functionality via pivot tables,
which you have [seen in this section](../manipulating_data/pivot_tables.md).
Aggregating data means to collect multiple units into one.
Again, SQL provides the same functionality as Sheets through keywords.
In this case, the `GROUP BY` statement allows you to group and aggregate
data. For example, you can use `GROUP BY` to count how many bike trips
were taken for each subscriber type, or to calculate the mean duration
for trips starting from each station.

The following query counts the number of trips (`COUNT(*)`) for each
member type (`GROUP BY member_type`).

``` {sql}
SELECT
   member_type, COUNT(*) AS n_trips
FROM
   trip_data
GROUP BY
   member_type
```

The result of this query has one rows for each distinct `member_type`,
and the column named `n_trips` counts the number of rows for each type.

Whenever you use `GROUP BY`, SQL expects you to use an aggregating
function. This is equivalent to which function is used to summarize data
in a Sheets pivot table. The most common examples are listed below.

-   `COUNT` counts the rows
-   `SUM` adds the values of a numeric column
-   `MIN` calculates the minimum of a numeric column
-   `MAX` calculates the maximum of a numeric column
-   `AVG` calculates the mean of a numeric column
-   `MEDIAN` calculates the median of a numeric column (only available
    in some SQL servers)

For example, the query below calculates the minimum and maximum trip
duration for each start station.

``` {sql}
SELECT
   start_station, MIN(duration) AS minimum_duration, MAX(duration) AS
    maximum_duration
FROM
   trip_data
GROUP BY
   start_station
```

### Fill in the blank

1. Write a query to find start station with the earliest start date.

You must include the `GROUP BY` column(s) in your `SELECT` clause. All
columns that are not in the `GROUP BY` clause must contain an aggreating
function.

If you want to calculate a summary statistic for the entire population,
you can use an aggregating function without the `GROUP BY` clause. For
example, the query below calculates the mean duration of all trips.

``` {sql}
SELECT
   AVG(duration) AS mean_duration
FROM
   trip_data
```

You can of course use filtering and ordering with aggregating functions.
The query below calculates the mean trip duration just for trips with a
casual member type.

``` {sql}
SELECT
   AVG(duration)
FROM
   trip_data
WHERE
   member_type = 'Casual'
```

### Fill in the blank

2. What is the total duration of all trips taken on bike W01274?

You can then combine this with the `GROUP BY` clause as you like.
Filtering with the `GROUP BY` clause can serve multiple purposes. Either
way, you must put the `WHERE` clause before the `GROUP BY` clause.

If you filter by a column that is not grouped by, you can filter the
aggregated results to a subset of the data. For example, you can
calculate the sum of all trip durations, by start station, for a
specific end station.

``` {sql}
SELECT
   start_station, SUM(duration) AS total_duration
FROM
   trip_data
WHERE
   end_station = 31111
GROUP BY
   start_station
```

If you filter by a column that is being grouped by, you can filter the
aggregated results to just show the row you are interested in. For
example, you can display the total trip duration for each pair of start
station and end station, just for trips that end at station 31111.

``` {sql}
SELECT
   start_station, end_station, SUM(duration) AS total_duration
FROM
   trip_data
WHERE
   end_station = 31111
GROUP BY
   start_station, end_station
```

### Fill in the blank

3. Find and fix the error(s) in the following code, which is trying to
calculate the mean trip duration for trips by member type Member.

```  {sql}
SELECT
   AVG(duration)
FROM
   trip_data
GROUP BY
   member_type
```

It can also be useful to combine aggregating functions with the
`ORDER BY` clause. This can allow you to sort by an aggregated column to
find the minimum or maximum.

### Short answer

- Explain what the following query will return.

``` {sql}
SELECT
  start_station,
  AVG(duration) AS mean_duration
FROM
  trip_data
WHERE
  duration >= 3600
GROUP BY
  start_station
ORDER BY
  AVG(duration) DESC
```

Note that you can also use the column alias in the `ORDER BY` clause.
The above query would have been identical (in almost all SQL servers) if
it had been `ORDER BY mean_duration DESC`.

### Fill in the blank

4. What is the bike number and trip count of the bike number with the most
trips?

5. For the station with the most trips that started and ended at the same
station, find the mean duration (in seconds) of all trips, rounded to
the nearest whole number.

Extension: Counting Unique Values
---------------------------------

It is often helpful to not only count the number of rows, but count the
number of unique values of a column. You can do this using the
`DISTINCT` keyword.

To count the distinct values of a column, you can simply use `COUNT`
along with `DISTINCT`. For example, the query below counts the number of
bike numbers used.

``` {sql}
SELECT
   COUNT(DISTINCT bike\_number) AS n\_distinct\_bikes
FROM
   trip\_data
```

This can also be used alongside to count the unique values for each
group. For example, the following query counts the unique bike numbers
used for each start station.

``` {sql}
SELECT
   start\_station, COUNT(DISTINCT bike\_number) AS n\_distinct\_bikes
FROM
   trip\_data
GROUP BY
   start\_station
```

### Fill in the blank

6. How many unique start stations are in the table? 

7. Write a query to display the number of unique end stations per each
start station.

It is sometimes also useful to select the distinct rows of a table. You
can do that by using `DISTINCT` without an aggregating function.

``` {sql}
SELECT
   DISTINCT bike\_number
FROM
   trip\_data
```

Note that selecting distinct values is equivalent to selecting grouped
values.

``` {sql}
SELECT
   bike\_number
FROM
   trip\_data
GROUP BY
   bike\_number
```

Extension: The HAVING Clause
----------------------------

You can never include an aggregating function within the `WHERE` clause.
For example, suppose you are trying to show all start stations and the
number of trips, but only for start stations with over 100 trips. The
following query produces an error, since the `WHERE` condition includes
the `COUNT` function.

``` {sql}
SELECT
   start\_station, COUNT(\*) AS n\_trips
FROM
   trip\_data
WHERE
   COUNT(\*) \> 100
GROUP BY
   start\_station
```

The `HAVING` clause can be used instead here. The query below executes
successfully.

``` {sql}
SELECT
   start\_station, COUNT(\*) AS n\_trips
FROM
   trip\_data
GROUP BY
   start\_station
HAVING
   COUNT(\*) \> 100
```

As with the `ORDER BY` clause, `HAVING` is an operation on the results.
While `WHERE` filters the data being queried, `HAVING` filters the
results based on the value of an aggregating function. The `HAVING`
clause can only be used immediately following the `GROUP BY` clause.

### Fill in the blank

8. Write a query to show the bikes that have been used for over 1 hour
(3600 seconds), and the total duration they have been ridden. Order the
result from shortest total duration to longest.

Extension: Numbered Column Aliases
----------------------------------

This section covers no new concepts, but introduces a convenient
shorthand notation. When using `GROUP BY` and `ORDER BY`, you can often
(this is supported in almost all SQL servers, but not all) reference
columns using the number in which they are selected. For example, the
following two queries are identical, listing member types by descending
number of trips.

The first query uses the column names in the `GROUP BY` and `ORDER BY`.

``` {sql}
SELECT
  member_type,
  COUNT(*) AS n_trips
FROM
  trip_data
GROUP BY
  member_type
ORDER BY
  n_trips DESC
```

The second query uses the column number in the `GROUP BY` and
`ORDER BY`.

``` {sql}
SELECT
  member_type,
  COUNT(*) AS n_trips
FROM
  trip_data
GROUP BY
  1
ORDER BY
  2 DESC
```

Note that `1` refers to the first column being selected, `member_type`,
and `2` refers to the second column being selected, `n_trips`.

You can always use the column names in these clauses, but the numbered
aliasing can be extremely useful, especially if you have several
columns. Note that you can use this notation only with the `GROUP BY`
and `ORDER BY` clauses. Using such notation anywhere else will produce
an error.

### Short answer

- Explain what question the following query is answering.

``` {sql}
SELECT
  start_station,
  end_station,
  AVG(duration) AS mean_duration
FROM
  trip_data
GROUP BY
  1, 2
ORDER BY
  3 DESC
```

<details>
<summary>Answers</summary>
<br>
 
1. 31620
 
2. 5009
 
3. 772.0053481492348

4. W00893, 548

5. 31217, 5164

6. 140

7. 31000, 36

8. W01204, 3765

</details>
