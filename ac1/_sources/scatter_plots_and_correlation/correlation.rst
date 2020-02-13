.. Copyright (C)  Google, Runestone Interactive LLC
    This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
    International License. To view a copy of this license, visit
    http://creativecommons.org/licenses/by-sa/4.0/.


Correlation
===========

The **correlation coefficient** is a measure of the strength and
direction of the linear relationship between two quantitative variables.
It is denoted as *r*, and is always between -1 and 1. Here are some
examples of scatterplots and their corresponding correlation
coefficients.

.. image:: figures/correlations_example.png
   :align: center

As you can see, in the first row of the examples above, the closer the
points are to lying on a straight line, the closer the correlation is to
either 1 or -1. If the scatter plot has a positive direction, the
correlation is a positive number, and if the scatter plot has a negative
direction, the correlation is a negative number.

Correlation only measures the strength of linear relationships between
variables. The last row of examples shows a variety of scatter plots
where there is clearly an interesting relationship between the two
variables (note all the unique shapes!), but the correlation is 0
because the relationship is nonlinear. `Read this for more detail about
how correlation is calculated.
<https://www.statisticshowto.datasciencecentral.com/probability-and-statistics/correlation-coefficient-formula/#Pearson>`__

.. image:: figures/scatter_plots_correlation_question.png
   :align: center

Question: Using the above figure as a guide, match the correlation to
each of the scatterplots from previous questions.

.. dragndrop:: scatter-correlation-ex-1
   :feedback: Try again. Top left has a negative and strong correlation. Top
              right has a positive and strong correlation. Bottom left has
              no real relationship, and bottom right has a positive 
              and strong correlation.
   :match_1: 0.79|||Bottom left
   :match_2: 0.02|||Answer B
   :match_3: -0.83|||Top left
   :match_4: 0.92|||Top right

   Using the above figure as a guide, match the correlation to
   each of the scatterplots from previous questions.


You can use Sheets to find correlation using the *CORREL* function.

`Video - how to find correlation in sheets.
<https://www.youtube.com/watch?v=omIT5V7naqM>`__

A common, related value is *r2*, called the **coefficient of
determination**. \**The coefficient of determination is the proportion
of variation explained by the explanatory variable. \**It can be
calculated by squaring the correlation coefficient. The closer *r2* is
to 1, the closer *r* was to either 1 or -1, and thus the stronger the
relationship between the variables. The coefficient of determination is
useful when you’re only interested in strength, rather than strength and
direction.

.. image:: figures/scatter-correlation-graph-1.png
   :width: 30%
.. image:: figures/scatter-correlation-graph-2.png
   :width: 30%
.. image:: figures/scatter-correlation-graph-3.png
   :width: 30%

.. shortanswer:: scatter-correlation-ex-3

   Which would have the largest *r2* value?
   

.. mchoice:: scatter-correlation-ex-3
   :answer_a: 0.7
   :answer_b: -0.1
   :answer_c: 0.9
   :answer_d: 0.05
   :correct: c

   Which of the following r values would have the largest *r2* value?
