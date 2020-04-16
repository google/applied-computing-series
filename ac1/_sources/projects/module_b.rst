.. Copyright (C)  Google, Runestone Interactive LLC
   This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
   International License. To view a copy of this license, visit
   http://creativecommons.org/licenses/by-sa/4.0/.


Module B
========

Project Description
-------------------

In this project, you will complete a statistical analysis on a dataset, then
write a report summarizing your findings.

Here are the steps you’ll need to complete.**Under each step are sub-bullets
detailing questions you need to answer in your report.**

**Step 1: Choosing a Dataset**

In any data science project, you will need good, reliable data. There are many
data sources available online. Chances are if there is a topic you are
interested in, there is a corresponding dataset. It is important that the
dataset you choose does not have any copyright restrictions and is trustworthy.
You can check on the website to see if the dataset is licensed and what
restrictions there may be on using it. In most cases, using the data and drawing
conclusions from it is just fine, but republishing the data itself is not
allowed.

**To Do:**

- Form a group of no more than 4 people. (You may want to form a group with
  people who are in a similar major or have similar interests as this may make
  dataset selection easier).
- Find a dataset to analyze online. If you are unsure where to start looking,
  check out the hints section for some places to start. If you have questions
  about your dataset, ask an instructor before proceeding.

- **Deliverable:** State and describe your dataset. Why did you choose this
  particular dataset?

*Hints:*

- Places to find free datasets: `World Bank Open Data`_, `FiveThirtyEight`_,
  `Kaggle`_
- `Additional list of websites to find datasets`_
- Revisit the importing data section from module B for review on how to import
  data


**Step 2: Clean Your Dataset**

Only rarely will datasets ever be ready for analysis right off the bat.
Therefore, you will need to prepare your dataset to make useful observations.
Don’t worry if it seems overwhelming at first. You want to remove outliers that
may skew your dataset, while still maintaining the integrity of your data. Some
steps have been provided to help with this process. Once you clean your dataset,
you should be able to find sections of the data that are interesting and find
relevant relationships.

**To Do:**

- First look at your data and see if you can spot any inconsistencies
- Filter out unwanted outliers
- Check for missing data values
- **Deliverable:** Summarize your data cleaning process and make sure to
  answer the following questions.

  - Are there any ethical issues with the way you cleaned the data? What are
    they?
  - Did you make any trade-offs as you were cleaning? What were these tradeoffs
    and why did you make this decision?

*Hints:*
  - For a more in-depth explanation of data cleaning `read this.`_

**Step 3: Consolidate and Summarize your Data**

After cleaning up your data, you will want an overview of what your data is
saying. Sometimes when working with a large dataset, your data will be split
across different sheets, making it difficult to find summary statistics. If
that is the case, you will need to join common sections first before finding
interesting statistics about your data.

**To Do:**

- Join the multiple sheets across a common column if necessary. You will need to
  join datasets using vlookup
- Using the joined dataset, find summary statistics for the population.
- **Deliverables:** Describe how you consolidated your data and chose your
  subsections. Make sure the following questions are answered in your
  discussion.

  - If you needed to join your data across sheets, what did you choose as the
    joining key? Why?
  - For all of the numeric variables, what are the population-wide mean, median,
    variance, standard deviation?

*Hints:*

- Revisit :ref:`the section on joining data <joining_data>`
- Look at :ref:`the section on measures of center for mean and median <measures_of_center>`
- Review :ref:`the section on measures of spread for variance and standard deviation <measures_of_spread>`

**Step 4: Choosing Subsets**

Sometimes you can find interesting trends in subsets of the data rather than the
whole dataset. For example, if you are looking at data about each of the 50
states in the United States, you can find interesting summary statistics about
the west coast states as compared to the east coast states.

**To Do:**

- Choose subsets of the data that you find interesting. Find summary statistics
  for the numeric variables, within those subsets of the data.
- From these subsets, create a pivot table and a visualization that compares
  summary statistics across groups.
- **Deliverables:** Continue your discussion section. Describe the subsets you
  chose from the dataset and include your pivot table and visualizations. Make
  sure the following questions are addressed.

  - Explain why you chose this set of groups.
  - Within subsets of interest, what are the count, mean, median, variance,
    standard deviation?
  - Is the sample size enough within each group? What does this imply for
    reliability of summary statistics, and for privacy considerations?
  - What comparisons are particularly interesting? Why?

*Hints:*

- `Disadvantages of a small sample size.`_
- `Refresher on data privacy.`_

**Step 5: Analyze your Data**

Now that you’ve looked into some subsets of data, it’s time to be more
quantitative in your analysis. Look for relationships in the data and use these
relationships to make predictions.

**To Do:**

- Determine two quantitative variables that have either a strong or an
  interesting relationship.
- Identify any potential lurking variables.
- Fit a regression on the data and find the equation for the line of best fit.
- Interpret the coefficients of the linear model, in the context of the chosen
  variables.
- Choose some data points to predict using your regression.
- **Deliverable:** Write the analysis section of your paper using what you have
  already done above. In addition, in a short paragraph, report your predictions
  in the context of the problem. Make sure the following questions are
  addressed:

  - How did you identify lurking variables?
  - Does the line of best fit fit the data well? If not, why not? If the result
    is surprising, what is surprising and why?
  - Include references to “correlation” and “causation” effects.
  - Is your prediction logical?

*Hints:*

- When reporting predictions here are some examples:

  - Good example: We predict that someone with a shoe size of 6.5 will be 5’4”.
  - Inadequate example: Only reporting the point (6.5, 64”).
  - Revisit :ref:`the section on causation vs. correlation <correlation_vs_causation>`

**Step 6: Conclude and reflect**

The power of data science is that you can get meaningful takeaways from
statistics that can help you make a positive impact on society. Now that you’ve
done data analysis, take a moment to reflect on your findings and think about
the broader implications.

**To Do:**

- Include a conclusion summarizing your findings.
  - Who does this affect?
  - What did you learn?
- Proofread your report.
- **Deliverable:** Write the conclusion section of your paper. Submit your
  report and your sheets reflecting your analysis by [Due Date].

*Hints:*

- `Examples of reports backed by data science`_

**Optional** (faculty can decide whether to include or not): After completing
and submitting your project, complete the group work self assessment and group
assessment.

Grading Rubric
--------------

.. list-table::
   :widths: 20 20 20 20 20
   :header-rows: 1
   :stub-columns: 1
   :align: left

   * -
     - **Excellent**
     - **Developing**
     - **Beginning**
     - **NA / Not Present**

   * - **Dataset (2)**
     - Report includes a rationale for why the dataset was chosen. If students
       selected a different dataset, the dataset must have been approved by the
       instructor.
     -
     - Report does not include a rationale for why the dataset was chosen.
     - The dataset was not approved by the instructor.


   * - **Data Cleaning (8)**
     - All missing/unclean data is found and accounted for in a way that makes
       sense. The report references data types, any ethical tradeoffs, and
       outlines what steps were taken and why.
     - Some crucial steps are not taken. Steps outlined to clean the data are
       ambiguous.
     - There is an attempt at data cleaning, but it does not get far. Large
       chunks of missing/unclean data are untreated. Key steps of cleaning
       process were not reported.
     - Report does not include any reference to data cleaning (independently of
       whether data cleaning was done).


   * - **Joining (4)**
     - An appropriate join key was chosen. VLOOKUP was used successfully to
       create a joined table. The report contains a brief mention of why this
       key was chosen.
     - An appropriate join key was chosen and the join is successfully executed
       using VLOOKUP, but the report does not include any discussion of why this
       key was chosen.
     - There was an attempt at joining, but the wrong formula was used or the
       wrong key was used.
     - There was no attempt at using VLOOKUP.


   * - **Population Summary Statistics (6)**
     - The summary statistics are accurately calculated and reported. There is
       some comment on what these values mean for the distribution.
     - Almost all of the important summary statistics are correctly calculated
       and reported.
     - There is an attempt at calculating summary statistics, but they are
       incorrect or not referenced in the report.
     - There is no attempt at calculating the population summary statistics.


   * - **Grouped Summary Statistics (8)**
     - A pivot table was used to calculate relevant summary statistics per
       group. The pivot table is presented in the report in a clean way.
       There is some other visualization showing some important summary
       statistics. There is some mention of sample size within groups, as well
       as why the specific grouping was chosen.
     - There is a working attempt at a pivot table, and it is presented in the
       report. Not all numbers are accurate, and there is no extra
       visualization. There is some mention on sample size within groups.
     - There is an attempt at a pivot table, but it uses the wrong dimensions
       and measures. The grouped summary statistics are incorrect or
       non-existent.
     - There is no attempt at a pivot table.


   * - **Regression (8)**
     - Report includes both the scatter plot and the line-of-best-fit equation,
       and these values are (close to) correct. The report includes a discussion
       of  why the particular variables were chosen, the meaning of the
       coefficients, and correlation versus causation. There is some mention of
       whether regression is appropriate for the sample size.
     - The line of best fit is not completely correct The scatter plot is
       missing from or wrongly formatted in the report The discussion on
       variable selection, coefficient interpretation, and correlation vs.
       causation is not sufficiently detailed or accurate.
     - There is some attempt at a line of best fit, but the values are
       completely wrong. The scatter plot or the equation are not included.
       There is no proper discussion on variable selection, coefficient
       interpretation, or correlation vs causation.
     - There is no attempt at fitting a regression.


   * - **Prediction (6)**
     - The equation of the line of best fit is used to predict these values. The
       report correctly identifies and explains which points are suitable for
       prediction. The ethics of prediction are mentioned, and the report includes
       the pros and cons of using a linear regression to predict.
     - Values are chosen for prediction that are largely appropriate. The report
       struggles with why some points are not suitable for prediction.  There is
       some mention of the ethics of using prediction from a linear model.
     - There is an unsuccessful attempt at prediction. There is little or no
       mention of suitability of prediction of certain points, or the chosen
       points are not usable with this model.
     - There is no attempt at prediction using the line of best fit.


   * - **Conclusion (4)**
     - The report contains a conclusion section summarizing key findings from
       other rubric areas. It is concise and complete.
     - The report contains a conclusion section, but either contains minor
       inconsistencies with previous findings, or omits relevant findings.
     - The report contains a conclusion section, but it is incomplete or doesn’t
       accurately reflect previous findings.
     - The report does not contain a conclusion section.


   * - **Readability (4)**
     - The report is structured by section, with appropriate headings. The
       report has very few spelling/grammar errors.
     -
     - The report’s structure lacks clarity or is otherwise difficult to read.
       The report has several spelling/ grammar errors.
     - There is no report.


   * - **Total (50)**
     -
     -
     -
     -

.. _World Bank Open Data: https://data.worldbank.org/
.. _FiveThirtyEight: https://data.fivethirtyeight.com/
.. _Kaggle: https://www.kaggle.com/datasets
.. _Additional list of websites to find datasets: https://www.dataquest.io/blog/free-datasets-for-projects/
.. _read this.: https://elitedatascience.com/data-cleaning
.. _Disadvantages of a small sample size.: https://sciencing.com/disadvantages-small-sample-size-8448532.html
.. _Refresher on data privacy.: https://www.siliconrepublic.com/enterprise/ethics-data-science-bias
.. _Examples of reports backed by data science: https://www.un.org/en/climatechange/reports.shtml
