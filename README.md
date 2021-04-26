# Exploring the Relationship between Gender, Population, Policies, Age, Region, and the Spread of Covid-19

# Abstract
The novel coronavirus has spread rapidly in many parts of the world. On March 11, 2020, COVID-19, colloquially known as the coronavirus, was declared a pandemic by the World Health Organization (WHO). While it is still unclear what the best way to prevent the spread of COVID-19 is, our research attempts to address the effect that policy implementation had on slowing down the spread of the coronavirus.
By analyzing the relationship of policy to the spread of COVID-19 in the continental US, it becomes evident that a great number of factors contribute to the spread of the coronavirus. In this paper, we explore features such as the population, when date policies such as shelter-in-place were implemented, the proportion of the population over 65, and the region of a specific county. Our additional research from news articles and peer reviews reflects that factors such as insufficient testing, an abundance of fake news, and a lack of enforcement on policies implemented have a dramatic effect on the spread of COVID-19, making the number of confirmed cases very difficult to model.

# Introduction
In the beginning of this project, we were looking to explore a few key questions:
1. How have the dates when specific policies are enacted to limit the spread of Covid-19,
such as the stay-at-home policy, impact the number of confirmed Covid-19 cases?
2. Does state population and state density have a significant effect on the spread of confirmed cases? What about gender? Proportion of elderly population? Region?

# Description of Data
We primarily used Yu Group’s Covid Severity Forecasting dataset, which has documented a large corpus of hospital- and county-level data from a variety of public sources. We also utilized John Hopkins University’s COVID-19 Data Repository by the Center for Systems Science and Engineering (CSSE), a data repository for the 2019 Novel Coronavirus Visual Dashboard. We used JHU CSSE’s data on confirmed cases of COVID-19 in the US to support our hypotheses.
We cleaned our data based on the structure, granularity, scope, temporality, and faithfulness of the data. We also observed other miscellaneous issues with our data that we addressed during cleaning.
* Structure: Our data already came in a rectangular shape, which is easy to manipulate and analyze, so we did not do any additional transformations in terms of structure.
* Granularity: In our analysis of policies, there were over 50 different dates that policies could have been implemented on, causing a lot of overplotting. Thus, we addressed this by categorizing policy implementation dates into 4 categories (i.e. early, medium, late, not implemented), and then one hot encoded these values as columns.
* Scope: Our data was very expansive, and contained a copious amount of information. We decided to focus on confirmed cases of Covid-19, population, and policies implemented within the 50 states and territories in the continental United States.
* Temporality: We found that time entries were entered in the proleptic Gregorian ordinal of the date, thus we converted each entry into a date time format for more clear visualizations.
* Faithfulness: We found inconsistencies in the data and incomplete entries for US territories (i.e. 'Manua', 'Ofu', 'Olosega', 'Tutuila’), so we chose to drop these territories and focus on the 50 States, Washington DC, and territories with complete entries.
* Miscellaneous: From outside research and comparisons, we saw that NaN date values in policy columns meant that the policy was not implemented, so we replaced the NaN values with “Not Implemented”.
