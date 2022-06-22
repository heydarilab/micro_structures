# Micro-level Social Structures and the Success of COVID-19 National Policies


## WHAT IS IT?

The code and data here are the supplumemtaty imformation to support the paper 'Micro-level Social Structures and the Success of COVID-19 National Policies'.

## HOW IT WORKS

This simulation model goes with four steps: 

1) Generating Pre-Pandemic Notional Contact Networks using Demographic Data. For each country, we build the scaled-down network by two micro-level social contact data which are the mean number of the reported daily contacts and the average household size. These two parameters are manually input into the model. The data about the reported daily contacts are sourced from the paper 'Mossong, J.et al.Social contacts and mixing patterns relevant to the spread of infectious diseases.PLoS Med5, e74(2008)'. Source data about households are from the Department of Economic and Social Affairs in the United Nations and are available at https://population.un.org/Household/#/countries/840.

2) Modeling Non-pharmaceutical Interventions (NPIs). For each country, we select two NPIS parameters, GSI (Government Stringency Index) and the moment of the NPIs's implementation ('total cases per million), to simulate the implementation of the NPIs. These two data are combined in the 'GSI_and_cases_track.csv' and this CSV file will be loaded by the model to show the trend of the GSI and the trend of 'total cases per million in the Supplementary Information Material Text S3. Moreover, the detail of how to select these two paramters for each country can be found in the Supplementary Information Material Text S4. These two data are available at https://ourworldindata.org/coronavirus. After that, we also do a simple analysis of the network structure before and after the implementation of the NPIs in this code.

3) Pandemic simulation for the primary set of six countries(Germany, Italy, Poland, the Netherlands, Belgium, and the United Kingdom). For each country, we run the simulation model and plot the trajectory of each simulated result. Moreover, we combine the simulated trajectories and the real trajectories to show that our notional model is capable of replicating the relative success of COVID-19 social distancing policies. Afterwards, we also run the simulation for a longer duration, 90 days and 120 days. The result of the simulation for each country can be found in the '/result_data/main result' file.

4) Counterfactual simulation and some scenario study. For the counterfactual simulation, we separately simulate six different NPIs (captured by these six targeted countries) in each targeted country. The result can be found in the '/result_data/all_conclusion.npy' and is plotted in the main page. For the scenario study, we generate three hypothetical countries, each with a low, medium, and high HTTCR. For each country, we also simulate three different scenarios, no NPIs and early NPIs, and late NPIs. Moreover, for the country with low HTTCR and the country with high HTTCR, we simulate the case under different social distancing implementation dates and generate the cumulative number of cases as a function of date. All simulated results can be found in the '/result_data/for parameter analysis' document.


5) Pandemic simulation for the validation set of five countries(Austria, Hungary, Slovenia, Poland, and Slovakia). Apart from the parameter M, the mean reported contacts, we select other parameters of each country in the validation set following the same rule and data source used in the primary set. Because the survey-based result data for the mean reported contacts is unavailable in these countries, we approximate this parameter using the result of this study, https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005697. In short, this study used the result of the POLYMODE-type contact survey
and demographic data to project the social contact matrices. Combining the social contact matrices and the age distribution (Data is available from https://population.un.org/wpp/dataquery/ ) of each country, we can estimate the mean reported contacts in the country.

6) Calculate the average relative error of two clusters of countries, the primary set and validation set.

7) Robustness check for the primary set countries: Parameter analysis for M, the mean reported contacts, and beta, the transmission rate. The comparison between GSI and Social Interaction Trends, using Google Mobility Data.
  

All data used in the paper are from public sources that are referenced in the paper.

