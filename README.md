# Assets-Failure-Prediction

Assets Failure Analysis and Prediction using Machine Learning
Author: Juan Miguel Estrada - jmestradag@gmail.com

Data Source: https://mydatamodels.zendesk.com/hc/en-us/articleattachments/360037092371/Failure_prediction-_For_prediction.csv

Background (summary taken from Data Source)
Is it possible to know to use machine learning to make failure prediction?

Modelling equipment downtime is referred as failure prediction. These models are based on data collected from past failures of a given equipment (or similar ones). Machine learning is well suited to model current equipment behaviour and its potential breakdowns. This way, production equipment failures can be anticipated and maintenance can be scheduled before the failure even happens, thus avoiding painful and unnecessary costs.

Problems to solve
• Can machine learning be used in order to anticipate and predict breakdowns?

Automated Machine Learning solutions consist of predicting the future with historical data, assuming no special causes occuring. To predict a future result, you must bring your descriptive data and the past result obtained. In this case, the descriptive data are machines’ information on their current state of working. The goal of the analysis is to predict if a machine is broken or not.

Dataset information
Each row is a machine and each column is a variable.

This dataset comes from a company that uses many machines to build final products. As production is stopped every time a machine has a failure, management would like to create a predictive model that finds which machine is going to fail next.

Target variable: (broken) Machine actually broken? yes/no.

The variables are:

Random number

Machine internal number: from 1 to 1000

“lifetime” indicates number of weeks since the machine has been used

then we have 3 numeric variables related to:

Temperature

Pressure

Moisture

and 2 variables related to:

The team using the machine

The machine’s provider / supplier






Analysis Assumptions:
Reader is familiar with reliability engineering concepts for machinery, which is a field of study that deals with the estimation, prevention, and management of failures by combining statistics, risk analysis, and physics.
These machines works as repairable systems and each time they fail, they are repaired in "as good as new" condition.
Operation timeframe given is in weeks, so these machines have an operating context of a 24/7 fashion, so operating time is similar across units and therefore will be treated in weeks, which will be our unit for maintenance planning and scheduling.
Time to failure given as lifetime, is recorded since last failure or start of operation for each machine.
This fleet of machines are very similar in design, and operates under same conditions.
Failure mode under analysis is similar and related to same sub-system with key variables: Temperature, Pressure and Moisture.
Due to lack of operating, maintaining and repairing costs, this analysis will assume a direct relationship between failures and costs and therefore this analysis can not use optimal replacement algorithm.