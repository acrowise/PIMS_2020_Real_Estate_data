# PIMS_2020_Real_Estate_data

<h3>A brief description of Data:</h3>

City: Calgary, AB

A sample of 4,000 residential properties in Calgary, AB, Canada is in file <b>"sampel_property_value.csv"</b>. One interesting research topic that can be attempted here is: how is investment on residential properties affected by macro- as well as micro-economic factors, from 2017 to 2020?


macro-economic factors that influence all property values, regardless of property-specific details such as # of bdr's or location, in file <b>"econ.csv"</b>, include:
	inf1=inflation
	mor1=mortgage rate 5 year


other geographically relevant factors that also drive property values include:

(1) demographics (<b>"demographics.csv"</b>): population: pop1-5, language: lan1-2, income: inc1-4, house ownership: own1-4, and labor: lab1-3

(2) safety (<b>"safety.csv"</b>): neighbourhood safety: saf1-8




<h3>Reading materials:</h3>

Four academic articles have been provided as reference. Some key messeges are:

(1) SSRN-id282681.pdf

-- an article that explains the driving factors of Real Estate investment returns
-- unexpected inflation and interest rates are identified as the main drivers


(2) SSRN-id2546407.pdf

-- a general introduction of how and why Real Estate sector is important to Banking sector

(3) SSRN-id3544939.pdf

-- population change as a driving factor for housing demand 


(4) SSRN-id1361808.pdf
-- analyzed returns of Real Estate investment with Panel data analysis methods
-- pay more attention to the statistical method with a common format of Real Estate datasets

<h3>Research of interest:</h3>
The primary variable of interest is the Assessment Value. Alternatively, it can be return of investment on properties, as calculated by <br>
〖Return〗_t=〖Assessment Value〗_t/〖Assessment Value〗_(t-1) -1 <br>
The explanatory variables, or factors, can be grouped into three categories: 
(1) macroeconomic variables: interest rate (mortgage5y) and inflation, that pertain to all properties. They have a time dimension, but not a geographic dimension. These two variables can be linked with other variables by “Year”.   
(2) geographic related variables: demographics and the safety variables that may or may not have time dimension but have geographic dimension. Demographic information comes from a Census conducted in the year of 2016. For the purpose of this study, we can assume no demographic change has occurred to each FSA since then. Safety data has both time (Year) and geographic (FSA, forward sortation areas) dimensions.
(3) Properties specific variables. This sample dataset does not have many such variable, except maybe “Year of Construction”. Know that each property’s geographic association with FSA has been calculated and given in “fsa” column. 

Think about the McKinsey report “Getting-ahead-of-the-market-How-big-data-is-transforming-real-estate”, and various SSRN academic papers. Property price (Assessment Value in our case) should be logically related to variables in category (1) – (3). Therefore, a simple regression like <br>
P=a+b(macro + demo + safe + specifics) + e <br>
should give some statistically significant results that can help deepen our understanding of Housing Price. That being said, we have seen some interesting machine learning algorithms being thrown at the same research topic on Kaggle. Using all 3 categories of variables, what would be the best method (machine learning or statistical approach) to estimate property values, from 2017 to 2020? To measure your model’s “goodness-of-fit”, consider splitting the 4000-properties sample into 3000/1000 or 2000/1000/1000 for training, validation, testing purposes. Metrics like RMSE can be used to assessment. 




