# NYC-Job-Openings-Prediction-Model-in-R

I did Data Analysis and KNN classification to predict IT and non-IT job openings in NYC using the NYC Jobs dataset from NYC Open Data. It provides information about several job openings, salary range and full-time/part-time related to IT and Non-IT job openings in NYC.

NYC Open Data makes the wealth of public data generated by various New York City agencies and other City organizations available for public use. Anyone can use these data sets to participate in and improve government by conducting research and analysis or creating applications.
(https://opendata.cityofnewyork.us/ )

Anyone graduating or seeking for jobs in any technical or non technical field can look for the job opportunities in NYC , and can easily find the job based on the work location and the type of job - IT or Non-IT. 

Moreover, they can see the total number of opening in every field. They can also go through the salary structure both maximum and minimum salary offered on annual,daily,hourly basis.


### Data Cleaning
Data was not in the form that was needed to perform analysis. It did not have enough numerical variables for analysis. There were missing values or values that were not consistent. The data pre-processing steps are as follows:
- Found and segregated the data that was related to the jobs in NYC. It was done on the basis of the requirements that were needed for our analysis. Eg - Filtered the data based on departments in different work locations.
- As the data was related to jobs, it divided the departments into 2 categories - IT and Non-IT and set as separate variables.
- Changed the work locations to the 6 NYC category as they were scattered in the data according to addresses in all the boroughs.
  - However, it was taken NYC as a 6th category because there was some data in the dataset that did not give the location explicitly. They had location information like the Office of the Director, Office Of Public Information, etc. Also, they have their locations all over NYC    boroughs or some boroughs. So this kind of data was considered as a separate NYC category.
- Removed many unnecessary variables as they were not at all relevant to the analysis.
- Made the data as compact and informative as possible by removing the ‘NA’ values.

## Exploratory Data Analysis

In an exploratory analysis, the following insights were observed:  
1. To show the relationship between Work Location and IT and Non-IT Job Opening with graph and explanation. 
2. Explore the average salary in each location, both maximum and minimum, on an annual and hourly basis. 
3. Analyze jobs based on timings - both part-time and full-time location wise. 
4. Explore the relationship between salary frequency based on location. (what salaries are paid in the 5 boroughs of NYC)

The outcomes of the above :
*    Manhattan and Brooklyn have maximum IT-related job openings whereas, for non-IT job openings, Manhattan and Queens have maximum job openings. The Bronx and Staten Island do not have IT and very few non-IT openings.
*    Manhattan has a maximum annual salary and a maximum hourly salary, and the Bronx has a minimum. 
*    Manhattan and Queens have maximum full-time job openings.

**NYC_Jobs_ORG.csv** - Messy data set which was downloded from OPEN nyc data<br/>
**NYC_Jobs_clean.csv** - Clean data set after preprocessing the original data<br/>
**Exploratory_analysis.Rmd** - R markdown file with exploratory analysis with detail explaination<br/>
**Exploratory_analysis_report.pdf** - Exploratory Analysis report<br/>
**Exploratory_analysis (knitted).pdf** - PDF report file, generated from rmd file<br/>


## Prediction analysis (KNN Classification):

KNN classification was implemented to predict the IT and non-IT job opening in nyc.

**NYC_Jobs_2.csv** - Clean data<br/>
**Knn_classification.Rmd** - Built KNN classification model<br/>
**KNN_prediction_report.pdf** - Predictive analysis report, explained result in detail<br/>
**Knn_classification(knitted).pdf** - PDF report file, generated from rmd file<br/>
