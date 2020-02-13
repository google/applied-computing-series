.. Copyright (C)  Google, Runestone Interactive LLC
    This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
    International License. To view a copy of this license, visit
    http://creativecommons.org/licenses/by-sa/4.0/.

.. _correlation_vs_causation:

Correlation versus Causation
============================

It is clear that schools with higher median SAT scores also have higher
completion rates, but you should be very careful about what conclusions you can
draw from that information. Just because two variables have a strong
relationship, does not necessarily mean that one can influence the other.

While it may be tempting to conclude that higher average SAT scores lead to
higher completion rates, there may be other reasons that the relationship
between the two variables is so strong. Perhaps students with higher SAT scores
prefer to go to schools with higher completion rates. Alternatively, schools
with larger endowments can both be more selective and have more resources to
support students towards graduation. This is an example of what we call a
**lurking (or confounding) variable**.

A lurking variable influences both the explanatory and explained variable, which
leads to an association even though there is no causal relationship between the
two. For example, the size of a school’s endowment can explain both average SAT
score and completion rate. Once this lurking variable is found, it no longer
makes sense for a college to attempt to increase the average SAT scores of their
new students in order to increase completion rate. Instead, it would make more
sense to focus on increasing their endowment size.

As another example, the number of ice cream cones sold in a month is highly
correlated with the number of sunburns. However, intuitively, you know that
ice cream consumption does not cause sunburns, just as you are aware that
getting a sunburn doesn’t (directly) make someone eat more ice cream. Both of
these variables, ice cream consumption and sunburn prevalence, are higher in
warmer months than in cooler months, and in warmer locations than cooler
locations. There is a strong association between the number of ice cream cones
sold and the frequency of sunburns, but that is not enough to establish
causation. In general, **correlation does not imply causation**: that is, just
because two variables share a strong relationship, does not necessarily mean
that one causes the other. In this example, temperature is a lurking variable:
as temperature increases, both sunburn prevalence and ice cream consumption
increase. This article goes into more detail about when you might like to choose
one over the other.


.. mchoice:: wine_correlation

   Suppose we found a correlation of ``r = -0.48`` between red wine consumption
   and incidence of heart attacks. Which of the following would be appropriate
   conclusions?

   - Drinking red wine reduces the probability of heart attack.

     - Incorrect: Red wine does not prevent a heart attack.

   - Drinking red wine increases the probability of heart attack.

     - Incorrect: Red wine is not the cause of a heart attack.

   - Drinking red wine is associated with a reduction in heart attack risk

     + Correct

   - Having a heart attack decreases the probability of drinking red wine.

     - Incorrect: The heart attack itself does not decrease the consumption of red wine.


.. mchoice:: dining_dental_correlation

   Suppose you were reading a news article that found a positive association
   between the frequency of dining out and dental health (so those who ate out
   more had better dental health). What is a possible lurking variable?

   - Diet

     - Incorrect

   - Activity Level

     - Incorrect

   - Income or Wealth

     + Correct

   - Frequency of Flossing

     - Incorrect


It is important to understand the distinction between causation and correlation
so that you can draw your own conclusions, since `the news often confuses
correlation and causation`_.


.. _the news often confuses correlation and causation: http://www.rebeccabarter.com/cv/talks/Cal_Day_Presentation.pdf
