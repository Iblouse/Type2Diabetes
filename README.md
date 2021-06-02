# Type2Diabetes
This project has two parts, the first part is the exploratory data analysis and the second part is the modeling.

##### Type 2 Diabetes is one of the most prevalent chronic diseases in the US and all around the world. It puts a lot of financial burden on the US economy.
##### According to the [American Diabetes Association](https://www.diabetes.org/resources/statistics/cost-diabetes) "on March 22, 2018 estimating the total costs of diagnosed diabetes have risen to 327 billion dollars in 2017 from 245 billion dollars in 2012, when the cost was last examined."
##### The goal of this project is to develop predictive models to identify risk factors for type 2 diabetes, which could help facilitate early diagnosis and intervention and reduce medical costs. 
##### To do this project I will use the Behavioral Risk Factor Surveillance System dataset 2018 BRFSS from the CDC website.
#####  The link to the dataset is [here](https://www.cdc.gov/brfss/annual_data/annual_2018.html) or you can download it directly [LLCP2018XPT.zip](https://www.cdc.gov/brfss/annual_data/2018/files/LLCP2018XPT.zip).
##### The dataset is 437436 rows by 275 columns.

#### In part II is to build a risk prediction models of type 2 Diabetes (in this case Diabetes is POSITIVE, No Diabetes is NEGATIVE) based on Survey data (2018 BRFSS Survey Data). 

We have to make a value judgement here between false classifications
- the cost of labeling a no Diabetes as Diabetes and
- the cost of missing an actual positive of Diabetes

In Sick patient detection, we need to optimize for Sensitivity(Recall) because
- FALSE(ly) predicted as POSITIVEs are more acceptable than
- FALSE(ly) predicted as NEGATIVEs        

Sesitivity (Recall) is a good measure to determine when there is a high cost associated with FALSE NEGATIVE

In our case we will not use accuracy for model selection, but recall, f1, AUC because our data are imbalanced

In this part of the project we will use the dataset we saved at the end of part I DiabetesT2.csv.
I will use pipeline for part II, because pipelines allow us to streamline this process by compiling the preparation steps while easing the task of model tuning and monitoring.
