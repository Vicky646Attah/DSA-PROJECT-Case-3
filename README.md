# DSA-PROJECT-Case-3
## PROJECT 

## Topic: Palmora Group HR Analysis


- [Palmora Case Study Overview](#palmyora-case-study-overview)
- [Data Cleanng Preparation](#data-cleaning-preparation-)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [My Data Analysis](#my-data-analysis)
- [Results](#results)
- [Recommendation](#recommendation)
- [Conclusion](#conclusion)



# Palmora Case Study Overview
This Power bi report is a one of the capstone project given to me by DSA Data Analysis to analyze and come up with insight  bordering on Gender inequality and pay gap in its three region, using the Palmora Group HR Analysis. By analysing the various parameters in the data received we seek to gather enough insight to make reasonable decisions which then enables us to tell compelling stories around our data from the insight gotten and to know the best performance from our data, and offer recommendation based on outcome of the analysis.
 
### Data Sources
The primary sources of Data used here is Data Palmora group emp-data.csv file this is downloaded from my files on Canvas LMS


### Data Cleaning Preparation 
At the initial phase of the data cleaning and preparation, we perform the following action.
1. Data Loading and inspection
2. Handling Missing Variables
3. Data Cleaning and formating
 Steps followed to clean Palmora Group HR data are:
the data was loaded into the power bi, where it was transformed to the power query editor for cleaning.
At first, i assigned a generic name NOT DISCLOSED that means to replace values, and i also went on to take out rows where employee has no salary. I also took out rows where department indicated NULL. I renamed the column for Location and changed it to Region, and i added a custom coulmn where i got the department_rating. I aslo loaded the bonus table and transformed it to get my bonus mapping and then i went on to select all the bonus and unpivote it and added a custom column to give me the department rating so
it can be easy for me to merge the palmora data with the bonus data into a new merged data, to continue with the addition of columns, i expanded the bonus mapping to reveal the values and and added a custom column to get the Annual bonus, thereafter i rename the column to change it to Bonus rate and i also added another custom  column called the total salary and i added conditional column to get the salary band. i also assigned value 0 to columns that were blank. After that, i proceeded to my analysis.

### Exploratory Data Analysis

1.	What is the gender distribution in the organization? Distil to regions and departments 
2.	Show insights on ratings based on gender 
3.	Analyse the company’s salary structure. Identify if there is a gender pay gap. If there is, identify the department and regions that should be the focus of management 
4.	A recent regulation was adopted which requires manufacturing companies to pay employees a minimum of $90,000 
●	Does Palmoria meet this requirement? 
●	Show the pay distribution of employees grouped by a band of $10,000. For example: 
●	How many employees fall into a band of $10,000 – $20,000, $20,000 – $30,000, etc.? 
●	Also visualize this by regions 
  
Case Questions 
5. Mr Gamma thought to himself that since you were already working on the employee data, you could help out with allocating the annual bonus pay to employees based on the performance rating. He handed you another data set that contains rules for making bonus payments and asked you to: 
●	Calculate the amount to be paid as a bonus to individual employees 
●	Calculate the total amount to be paid to individual employees (salary inclusive of bonus) 
●	Total amount to be paid out per region and company-wide 
  


## My Data Analysis

I Import the employee data into Power BI and 
did a proper cleaning by

1. Assign a generic gender status to employees who refused to disclose their gender.
2. Remove employees without salaries and departments indicate as "NULL".

first of all i got the employee count using cards on the visual and then
i went on to get the total salary by copying and pasting the employee and and
summerizing by count and then i got the average salary, Max salary, and Min salary using the same approach.

1. For Gender Distribution Analysis
1. I used a bar chart:
    - Axis: Region/Department
    - Value: Count of Employees by Gender
2.And then i Used a slicer to filter by region/department.
3.  I Visualize the overall gender distribution using a pie chart.

Visualization: 
- Bar chart: "Gender Distribution by Region"
- Pie chart: "Overall Gender Distribution"

Measures
- `Gender Count = COUNT('Employee'[Gender])`
-  Gender Percentage = DIVIDE(CALCULATE(COUNT('Employee'[Gender])), CALCULATE(COUNT('Employee'[Gender]), ALL('Employee'[Gender])))`

  
 2: Ratings Insights Based on Gender
1. I Created a histogram and a matrix box plot:
    - Axis: Rating
    - Value: Count of Employees by Gender
   2. And i used slicer to filter by Gender
   3.I Calculated the average rating by gender using a measure.

Visualization:
- Histogram: "Ratings Distribution by Gender"
- Box plot: "Ratings Comparison by Gender"

Measures
- Average Rating by Gender = AVERAGE('Employee'[Rating])`
- Rating Count by Gender = COUNT('Employee'[Rating])`

  
 3: Salary Structure and Gender Pay Gap Analysis
1. I used a scatter plot:
    - X-axis: Salary
    - Y-axis: Gender
2. I Calculate the average salary by gender using a measure.
3. I Identify departments and regions with significant pay gaps.

Visualization:
- Scatter plot: "Salary vs. Gender"
- Bar chart: "Average Salary by Department and Region"

Measures 
- `Average Salary by Gender = AVERAGE('Employee'[Salary])`
- `Salary Count by Department and Region = COUNT('Employee'[Salary])`


 4: Minimum Salary Requirement Analysis
1. I used a histogram:
    - Axis: Salary Band ($10,000 increments)
    - Value: Count of Employees
2. I then Use a slicer to filter by region.
3. I Calculate the number of employees below the minimum salary threshold.

Visualization:
- Histogram: "Salary Distribution by $10,000 Band"
- Bar chart: "Employees Below Minimum Salary Threshold by Region"

Measures
- `Employees Below Minimum Salary = COUNTX(FILTER('Employee', 'Employee'[Salary] < 90000), 'Employee'[Salary])`


-  5: Bonus Payment Calculation
1. Create a measure to calculate the bonus amount based on performance ratings.
2. Calculate the total amount to be paid to individual employees (salary + bonus).
3. Create a bar chart to visualize the total amount to be paid out per region.

Visualization:
Bonus Payments
- Bar chart: "Total Bonus Payout by Region"
- Table: "Individual Employee Bonus Payments"

Measures
- `Bonus Amount = IF('Employee'[Rating] > 3, 'Employee'[Salary] * 0.1, 0)`
- `Total Amount to be Paid = 'Employee'[Salary] + 'Bonus Amount'

##  Result

![3 case 1](https://github.com/user-attachments/assets/228a706c-94bc-4f53-b8cc-3e254621466d)

![3 case 2](https://github.com/user-attachments/assets/1c3e17f6-a7e1-4ae7-84a7-4523a56109d1)

![3 case 3](https://github.com/user-attachments/assets/79b19ed6-81bd-49c2-ae0c-2283b83c17a8)

![3 case 4](https://github.com/user-attachments/assets/b16e7e32-5fce-49f0-9c55-c74b8f4fd1b6)


## Recommendations



Conclusion

