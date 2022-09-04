# Employee_attrition_analysis

## Overview

Since hiring and retaining employees are complex tasks that require capital, time, and skills, the company wants to find out which kind of employees are more likely to leave. Then they could design some new methods to retain those employees.

### Purpose

To perform exploratory data analysis through various visualizations to understand what are the features that mostly cause the employees to leave.

To conduct a deep learning model to classify employees that are most likely to leave.

## Exploratory Data Analysis

Several features are tail-heavy.

`EmployeeCount` , `Standardhours`, and `Over18` are not effective, since they do not change from one employee to the other.

![1](https://user-images.githubusercontent.com/88747464/188317729-a67dd724-e7a4-4dc0-8ef6-a2018b95e6ff.png)

There are about 237 or 16% of the employees left the company.

![2](https://user-images.githubusercontent.com/88747464/188317742-77feeaa0-deb5-44a0-8b47-5d88bcd25882.png)

Stayed employees have higher average `Age`, `DailyRate`, `EnvironmentSatisfaction`,  `JobLevel`	, `JobSatisfaction`, 	`MonthlyIncome`, `StockOptionLevel`, `TotalWorkingYears`,  `YearsAtCompany`, `YearsInCurrentRole`, and `YearsWithCurrManager`.

Stayed employees have lower average `DistanceFromHome`,	`NumCompaniesWorked`,	and `OverTime`.

![Screen Shot 2022-09-04 at 9 43 28 AM](https://user-images.githubusercontent.com/88747464/188317751-9c7673a8-e0fd-4abc-8f71-7e9465f1a838.png)
![Screen Shot 2022-09-04 at 9 43 41 AM](https://user-images.githubusercontent.com/88747464/188317754-812e04a6-a6c4-4914-b5c8-fe585fd8ab41.png)
![Screen Shot 2022-09-04 at 9 43 55 AM](https://user-images.githubusercontent.com/88747464/188317758-33957616-50e3-4d80-aa0b-4e0882f67bd4.png)

`JobLevel`, `TotalWorkingYears`, and `MonthlyIncome` are strongly correlated.

`YearsAtcompany`, `YearsWithCurrManager`, and `YearsInCurrentRole` are strongly correlated.

`Age` is strongly correlated with `TotalWorkingYears`.

![3](https://user-images.githubusercontent.com/88747464/188317762-1eb4204c-30db-44c3-a17a-9a82ff19c6fb.png)

Most employees that want to leave are 29 and 31 years old. 

Younger employees tend to leave and older employees tend to stay.

![4](https://user-images.githubusercontent.com/88747464/188317768-0aff6711-aa2f-4b32-8ccc-eb26bb216e45.png)

Sales Representatives tend to leave compared to other jobs.

Single employees tend to leave compared to married and divorced.

Less experienced (low job level) employees tend to leave. 

![5](https://user-images.githubusercontent.com/88747464/188317776-9ddc93c5-04f9-4b9a-88ea-402bb68843a8.png)

The long distance from home, the lesser employees worked in the company and the more employees that tend to leave.

![6](https://user-images.githubusercontent.com/88747464/188317780-06473642-f5a9-41da-954e-f9b6cb80ef88.png)

Less experienced employees or with shorter total working years are more likely to leave.

![7](https://user-images.githubusercontent.com/88747464/188317783-a302bdee-0fac-495c-8577-cdd14f797b68.png)

On average, female employees have a higher monthly income than males.

![8](https://user-images.githubusercontent.com/88747464/188317792-cc8beb9a-5222-4508-99c8-21011658f239.png)

From the above visualization, we know that Sales Representatives tend to leave compared to the other jobs. 

They also have the lowest monthly income compared to the other jobs, this might be one of the reasons.

![9](https://user-images.githubusercontent.com/88747464/188317806-d1aa44e3-d532-4908-a5de-e5e71cd12592.png)

## Deep Learning Classification

**Model Summary**

![Screen Shot 2022-09-04 at 10 04 05 AM](https://user-images.githubusercontent.com/88747464/188317910-93cf4a6d-34f6-4860-ba2d-b03855e8fbd9.png)

![Screen Shot 2022-09-04 at 10 04 15 AM](https://user-images.githubusercontent.com/88747464/188317929-88432901-beb1-45f7-8e3e-9350cd812b46.png)
![Screen Shot 2022-09-04 at 10 04 22 AM](https://user-images.githubusercontent.com/88747464/188317932-bed08804-d0fd-4d4a-a9dc-fb3975f2d015.png)

**Confusion Matrix**

![10](https://user-images.githubusercontent.com/88747464/188317947-b122bca7-32c1-46a3-b68d-fe07c146135c.png)

**Classification Report**

![Screen Shot 2022-09-04 at 10 04 50 AM](https://user-images.githubusercontent.com/88747464/188317953-37189849-d3f4-4b55-8b3c-96b4066fb756.png)

## Summary

To conclude, these factors could be helpful for the company to determine which employees might leave.

`Age`, `DailyRate`, `EnvironmentSatisfaction`, `JobSatisfaction`, 	`MonthlyIncome`, `StockOptionLevel`, `TotalWorkingYears`,  `YearsAtCompany`, `DistanceFromHome`,	`NumCompaniesWorked`,	and `OverTime`.

Although the deep learning model achieved 86% accuracy, that could be misleading since the dataset is imbalanced. 

The better KPI would be the **F1 score**, which is the overall Measure of a model’s accuracy that combines precision and recall.

The F1 score for stayed employees is 92%, but for left employees is only 50%. 

### Further Insights

It is possible to observe further with **feature selection** techniques to reduce and determine the most significant factors. 

Also to try various other **supervised machine learning** models for improved prediction performance.

## Resources

https://www.udemy.com/course/data-science-for-business-6-real-world-case-studies/

