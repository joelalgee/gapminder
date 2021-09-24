# Gapminder Environmental & Economic Data Wrangling & Analysis
Wrangling, analysing and visualising country-level environmental and economic data provided by Gapminder, using Python

## Summary

[Gapminder](https://www.gapminder.org/) has collected a lot of information about how people live their lives in different countries, tracked across the years, and on a number of different indicators.

In this project, I explored Gapminder's country-level, annual data on carbon dioxide emissions per person (in metric tonnes), energy usage per person (in kg equivalent oil), and gross national income per person (in international dollars, fixed 2011 prices, PPP based on 2011 ICP), to discover any trends and correlations for these indicators.

I focused on a time period for which data was available on all three indicators for the vast majority of countries, and on countries for which we have at least some data on each indicator during this period.

In particular I undertook to answer the following questions:

* How did the average values for these indicators change over the time period?
* Which country achieved the greatest reduction (or smallest increase) in carbon dioxide emissions per person across the time period?
* Is there a relationsip between gross national income per person and carbon dioxide emissions per person?
* Did the relationship between energy use per person and carbon dioxide emissions per person change across the time period?

## Package versions

* python 3.8.5
* numpy 1.20.1
* pandas 1.2.4
* matplotlib 3.3.4
* seaborn 0.11.2

## Instructions

Store all files in the same folder, and use Jupyter Notebook to open gapminder-analysis.ipynb

## Files

### gapminder-analysis.ipynb

Contains the step-by-step analysis and discussion as an interactive Jupyter Notebook.

### gapminder-analysis.html

Static HTML version of the above.

### co2_emissions_tonnes_per_person.csv

CO2 emissions per person (tonnes) for each country from 1800 to 2018

### energy_use_per_person.csv

Energy use per person for each country from 1960 to 2015

### gnipercapita_ppp_current_international.csv

Gross national income per person based on purchasing power parity for each country from 1990 to 2019

### population_total.csv

Population for each country from 1800 to 2100 (predicted)

## Conclusions

### Limitations

Conclusions drawn here are based on analysis of 166 countries for which we had data on the indicators during the period 1990-2014.

Approximately 6% of the datapoints were missing. Missing data for an indicator was assumed to be equal to the next or previous recorded data for the indicator, as analysis showed that in the overwhelming majority of cases, the indicators changed less than 0.1% from year to year.

### How did the average values for these indicators change over the time period?

Average annual carbon dioxide emmissions per person across the countries in our cleaned dataset increased from 4.25 metric tonnes in 1990 to 4.84 metric tonnes in 2014. Following an initial decline through the 90s, the majority of the growth occurred from 2002 to 2011, with a dip in 2009 (the global financial crisis).

Average annual energy usage per person across the countries in our cleaned dataset increased from 1650 kg equivalent oil in 1990 to 1893 kg equivalent oil in 2014. Following an initial decline through the early 90s, the majority of the growth occurred from 2002 to 2011, with a dip in 2009 (the global financial crisis).

Average gross national income per person across the countries in our cleaned dataset increased from 5596 international dollars in 1990 to 15366 international dollars in 2014. The growth accelerated before pausing in 2009 (the global financial crisis), and then resumed at constant pace.

### Which country achieved the greatest reduction (or smallest increase) in carbon dioxide emissions per person across the time period?

Luxembourg achieved the greatest reduction in CO2 emissions per person between 1990 and 2014, reducing emissions from 31.1 metric tonnes per person to 17.7 metric tons per person - a 43.1% reduction.

The energy usage per person also dropped by 22.7%, and the population increased by 45.3%.

It seems the increase in population was handled with more efficient energy usage, alongside increased usage of clean energy.

### Is there a relationsip between gross national income per person and carbon dioxide emissions per person?

There is a strong, positive correlation - as gross national income per person increases, carbon dioxide emissions per person increase.

### Did the relationship between energy use per person and carbon dioxide emissions per person change across the time period?

It does seem likely that the relationship between energy use per person and carbon dioxide emissions has changed across the time period, however, note that the confidence intervals of the two regression lines overlap, so it is possible that there is no change in the relationship.

At low energy usage per person, the CO2 emissions per person may have increased, while at high energy usage per person, the CO2 emissions per person may have decreased.

## Credits

This project was provided by [Udacity](https://www.udacity.com) as part of their [Data Analyst nanodegree](https://www.udacity.com/course/data-analyst-nanodegree--nd002). Data were provided by [Gapminder](https://www.gapminder.org/data/).
