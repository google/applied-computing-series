.. Copyright (C)  Google, Runestone Interactive LLC
    This work is licensed under the Creative Commons Attribution-ShareAlike 4.0
    International License. To view a copy of this license, visit
    http://creativecommons.org/licenses/by-sa/4.0/.

Creating a Scatter Plot in Sheets 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
In this section, you will learn how to make a scatter plot in sheets by 
following along with a tutorial. You will work with the temperature data.  
Latitude will be the explanatory variable and July mean temperature will be the 
explained variable. 



How to make a scatter plot
--------------------------
First, copy over the city, state, latitude and July mean temperature columns 
from the weather data here  into a new sheet.

.. image:: figures/create_a_scatter_copy_data.png

Afterwards, select the two columns containing the latitude and mean temperature
data then click “Insert > Charts.”

.. image:: figures/create_a_scatter_insert_chart.png


Then in the chart editor click “Setup > Chart type > Scatter”

.. image:: figures/create_a_scatter_plot_choose_scatter.png


Sometime Sheets will correctly assign the columns to be either the explanatory
variable or the explained variable, but it is always good to know how to 
manually assign them. 

Go to “Chart Editor > X-axis > Edit ” to choose which column of data will be 
the explanatory variable. 

.. image:: figures/create_a_scatter_xaxis1.png


Then put in the range of cells where you put the latitude data (the explanatory
variable). 

.. image:: figures/create_a_scatter_xaxis2.png


To choose which column of data will be the explained variable, you will go 
through a similar process. Go to “Chart Editor > Series > Edit”.

.. image:: figures/create_a_scatter_yaxis1.png 



Then put in the range of cells where you put the weather data (the explained 
variable). 

.. image:: figures/create_a_scatter_yaxis2.png


To add a title, go to “Chart Editor > Customize > Title.”

.. image:: figures/create_a_scatter_title.png


To choose the horizontal and vertical axis labels, go to 
“Chart Editor > Customize > Chart & axis title.”

.. image:: figures/create_a_scatter_axistitle1.png  


Then select “Horizontal axis title” and “Vertical axis title” respectively to 
add a descriptive horizontal title and a vertical title.

.. image:: figures/create_a_scatter_horizontal_label.png
.. image:: figures/create_a_scatter_vertical_label.png 

You now have a scatter plot for latitude versus July mean temperature.

Question: What city represents the point furthest to the right on the
scatter plot?

::

   A: Seattle

Question: What city represents the point closest to the y axis on the
scatter plot?

::

   A: Miami-Hialeah
