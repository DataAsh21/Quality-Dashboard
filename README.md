# Quality-Dashboard
#### Introduction:
The purpose of this project is to develop a Quality Dashboard that will help the client monitor the quality of their products by analyzing the defects, fatal errors, quality score and sampling percentage of their manufacturing process. The dashboard will be developed using Power BI.
#### ETL Process:
The ETL (Extract, Transform and Load) process will be used to extract the data from the client's database, transform it by applying the required calculations and load it into the Power BI dashboard. The following calculations will be used to transform the data:
##### Defects% - This calculation will be used to determine the percentage of defects in the manufacturing process. It will be calculated by dividing the sum of defects by the sum of samples.
Formula: Defects% = DIVIDE(SUM('Quality Data'[Defects]),SUM('Quality Data'[Samples]),BLANK())
##### Fatal Error% - This calculation will be used to determine the percentage of fatal errors in the manufacturing process. It will be calculated by dividing the sum of fatal errors by the sum of samples.
Formula: Fatal Error% = DIVIDE(SUM('Quality Data'[Fatal Error]),SUM('Quality Data'[Samples]),BLANK())
##### Quality Score - This calculation will be used to determine the quality score of the manufacturing process. It will be calculated by subtracting the defects percentage from zero.
Formula: Quality Score = IF([Defects%]=BLANK(),BLANK(),1- [Defects%])
##### Sampling % - This calculation will be used to determine the percentage of samples taken in the manufacturing process. It will be calculated by dividing the sum of samples by the sum of total tasks.
Formula: Sampling % = DIVIDE(SUM('Quality Data'[Samples]),SUM('Quality Data'[Total Task]),BLANK())

#### The dashboard consists of the following visuals:
##### Sample vs Defect Analysis: This visual shows a comparison of the total number of samples taken and the number of defects found during the quality control process. This helps to identify the percentage of defective products and the areas where improvements can be made.
##### Quality Score by Supervisor: This visual displays the quality score for each supervisor. The quality score is calculated based on the percentage of defects found during the quality control process. This visual helps to identify supervisors who need additional training or support to improve the quality of their work.
##### Fatal Error by Month: This visual displays the number of fatal errors that occurred during each month. This helps to identify any trends or patterns in the occurrence of fatal errors, which can be used to improve the quality control process.
##### Sampling % by Auditor Name: This visual displays the percentage of samples taken by each auditor. This helps to identify auditors who may be taking too few or too many samples, which can impact the accuracy of the quality control process.
##### Quality Score by Location: This visual displays the quality score for each location. This helps to identify locations that need additional attention or support to improve the quality of their work.
##### Additionally, a tooltip has been added to the Quality Score by Employee Name visual, which displays the quality score for each individual employee when hovering over their name.
The dashboard consists of two pages: a Quality Dashboard and an Employees Details page. The Quality Dashboard displays the above visuals, while the Employees Details page provides additional information about each employee The page navigator has been added to allow for easy navigation between pages.
#### Conclusion:
Overall, the Quality Dashboard provides a comprehensive analysis of sample vs defect data and employee performance to help the client make data-driven decisions and improve their overall quality control process
