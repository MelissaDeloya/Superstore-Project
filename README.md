# Fortune 500
Project #1 


##Group the data in a new way using a CASE statement. 

##Number of employees and establishing new vs. established business

 
SELECT company_name , employees,

CASE WHEN employees <= 10000 THEN " New Business"

WHEN employees >= 200000 THEN "Established Business"

ELSE "Regular Business"

END AS Business_Types

FROM fortune_companies

ORDER BY employees DESC;

 


##Use a HAVING clause to determine something interesting about the data per category.

Industry and PTO time

 
SELECT industry , SUM (paid_time_off_days) AS PTO

FROM fortune_companies

GROUP BY industry

HAVING SUM (paid_time_off_days) > 40



 

##Use logical operators like AND or OR to filter the data in an interesting way.

Compare Tenure with PTO per industry

SELECT *

FROM fortune_companies

WHERE avg_employee_tenure > 10

OR paid_time_off_days <= 40

ORDER BY avg_employee_tenure DESC;



 

##Use an aggregate function like AVG, SUM, COUNT, MAX, and/or MIN to return summary statistics about the data.

##Average Revenue in Retail Sector 

SELECT AVG (revenue)

FROM fortune_companies

WHERE industry = "Retail";

 

 
