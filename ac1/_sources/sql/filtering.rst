.. Copyright (C)  Google, Runestone Interactive LLC
   This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
   International License. To view a copy of this license, visit
   http://creativecommons.org/licenses/by-sa/4.0/.


Filtering
=========

In this section, you will learn how to filter data in SQL. Previously, you 
learned how to filter data in Sheets. Filtering data is to look at only a 
subset of rows, based on some column condition. For example, if you have 
a database containing information for all citizens of the USA, a filter 
could be applied to look only at residents of Texas. You have
already seen :ref:`how to apply filters in Sheets<filtering_data>`.

Filtering data in SQL is as simple as using the ``WHERE`` keyword. You can
append ``WHERE column_condition`` to any SQL query, and the result will be
filtered only to rows that satisfy the column condition. For example, you might
want to look only at bike trips which are at least one hour (3600 seconds).


.. activecode:: bikeshare_rides_over_60_minutes
   :language: sql
   :dburl: /runestone/books/published/ac1/_static/bikeshare.db

   SELECT
     member_type,
     start_date,
     duration
   FROM
     trip_data
   WHERE
     duration >= 3600
   LIMIT
     10


It is also possible to filter by multiple criteria. For example to look at bike
trips which are 60 minutes or more and the ``member_type`` is ``MEMBER``, the
query would be as below.


.. activecode:: bikeshare_rides_over_60_minutes_by_members
   :language: sql
   :dburl: /runestone/books/published/ac1/_static/bikeshare.db

   SELECT
     member_type,
     start_date,
     duration
   FROM
     trip_data
   WHERE
     duration >= 3600 AND
     member_type = 'Member'
   LIMIT
     10


.. activecode:: bikeshare_rides_over_8_hours_by_W01274
   :language: sql
   :dburl: /runestone/books/published/ac1/_static/bikeshare.db

   Write a query to find the ending station and duration of all of trips by bike
   number W00153 that lasted over 8 hours.
   ~~~~

   ====
   assert 0,0 == 31606
   assert 0,1 == 40791
   assert 2,0 == 31703
   assert 2,1 == 40820

.. activecode:: bikeshare_trips_starting_and_ending_at_31111
   :language: sql
   :dburl: /runestone/books/published/ac1/_static/bikeshare.db

   How many trips started and ended at station 31111?
   ~~~~

   ====
   assert 0,0 == 92

