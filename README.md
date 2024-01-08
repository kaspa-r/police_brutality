# Police Brutality Analysis

## Foreground

    This analysis entails the use of contextual data in of cost of living & gun provisions fields for US states & counties to try to explain the regional reasoning behind Police shootings that happen within the United States. Alongside that, the analysis explores differing characteristics of sections of police shooting victims with accordance to several categorical variables. These include: race, state, use of body camera, self-defense weapon, fleeing bool, gender, manner of death & signs of mental illness. Alongside these values, unique inequality data is calculated for each state & county in order to gauge the possible rationship between inequality & police shootings. A metric of gun law totals, gun provision strictenings & loosenings are additionally added to the analysis and a separate categorical variable based on the strictness of gun law provisions splits each state to further provide a possible avenue for splitting data. 
    
    The analysis culminates in finding differing findings with the combination of the three datasets via regional analysis using choropleths & correlation analysis. 

## Datasets included

    * Fatal Police Shootings (2015 - 2017) (Source: https://www.kaggle.com/datasets/washingtonpost/police-shootings)
    * US Cost of Living Dataset (Source: https://www.kaggle.com/datasets/asaniczka/us-cost-of-living-dataset-3171-counties)
    * Firearms Provision in the US. (Source: https://www.kaggle.com/datasets/jboysen/state-firearms)
    * United States Cities Database (Source: https://www.kaggle.com/datasets/sergejnuss/united-states-cities-database)

# Table of Contents

    * Data Prep & Feature Engineering
        * Police Brutality Data
        * US City Coordinates Data
        * US County Data
        * US Gun Laws Data
    * Combined Analysis
    * Conclusions
    * Points of Improvement
    * Appendix

#   Variables used:

*   Fatal police Shootings table:
    * `name` - victim of the police shoothing
    * `date` - date of the incident
    * `manner_of_death` - manner of death ("shot" or "shot and Tasered")
    * `armed` - self-defense weapon that weas used by the victim
    * `age` - age of the victim
    * `gender` - gender of the victim
    * `city` - city where the incident happened
    * `state` - state where the incident happened
    * `signs_of_mental_illness` - bool value on whether the victim had any signs of mental illness.
    * `threat-level` - threat level of the victim to the policeman or other civilians at the time of the incident
    * `flee` - whether the person was fleeing and with which method. 
    * `body_camera` - bool value on whether the policeman had a running body camera during the incident.

*   US Cost of Living Dataset:
    * `case_id` - Unique identifier for each area name
    * `state` - The state where the county is located.
    * `areaname` - areaname of the location.
    * `county` - name of the county.
    * `total_cost` - total estimated annual cost of living for the family type in the county.

*   Firearms Provision in the US:
    * `state` - The state where the law was enacted.
    * `year` - year when the law was enacted.
    * Multiple law columns - each column represent a bool value of whether they were enacted/had been enacted for the year & state combination. 
    * `lawtotal` - total number of laws a state had at the `year` value.

*   United States Cities Database:
    * `city` - Name of the city.town.
    * `city_ascii` - city as an ASCII string. 
    * `state_id` - The state or territory's USPS postal abbreviation.
    * `state_name` - The name of the state or territory that contains the city/town.
    * `county_fips` - The 5-digit FIPS code for the primary county. The first two digits correspond to the state's FIPS code.
    * `county_name` - The name of the primary county (or equivalent) that contains the city/town.
    * `lat` - The latitude of the city/town.
    * `lng` - The longitude of the city/town.
    * `population` - An estimate of the city's urban population. (2019).
    * `density` - The estimated population per square kilometer.