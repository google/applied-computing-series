<!-- Copyright (C)  Google, Runestone Interactive LLC
  This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
  International License. To view a copy of this license, visit
  http://creativecommons.org/licenses/by-sa/4.0/. -->

Module C Preface
================

A lot of the data that we interact with today is stored in databases.
You can think of a database as a group of tables. These tables have rows
and columns just like spreadsheets. Some examples of data that can be
stored in databases are listed below.

-   Student records, including grades, at a school
-   Posts and friends in your favorite social network
-   News stories on a newspaper's website
-   Your contacts list on your mobile phone
-   All images that make up Google Maps

All these bits of information are stored in various kinds of databases.
Some of these are stored in a relational database, which is a database
that stores data points that are related to one another in some way.
These databases are available as open source tools like Postgresql,
MySQL and SQLite, as well as commercial databases such as [Google
BigQuery](https://cloud.google.com/bigquery/),
[Oracle](https://www.oracle.com/database/technologies/), [Microsoft SQL
Server](https://azure.microsoft.com/en-us/services/virtual-machines/sql-server/),
or [Amazon Aurora](https://aws.amazon.com/rds/aurora/). Others are
stored in proprietary systems like Google's
[BigTable](https://en.wikipedia.org/wiki/Bigtable) or Facebook's
[Haystack Object
Store](https://code.fb.com/core-data/needle-in-a-haystack-efficient-storage-of-billions-of-photos/).

While the mechanism and content of the database may vary, there is a
common language used to extract data: this language is called Structured
Query Language (SQL, pronounced "sequel"). This module will teach you
how you can use SQL to analyze data in a database.
