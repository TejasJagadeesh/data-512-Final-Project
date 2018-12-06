# Final Project Plan – Analysis of OASDI and SSI payments across all states

Tejas Jagadeesh  
DATA 512 (Human-Centered Data Science)  
University of Washington, Fall 2018  

# Introduction

OASDI stands for Old-Age, Survivors, Disability Insurance. It is part of Social Security Disability program. It is provided as support to people who are retired and families (dependent spouses and children) of workers have died. Additional details on its history can be found here on Wikipedia - https://en.wikipedia.org/wiki/Social_Security_(United_States)  
  
SSI stands for Supplemental Security Income. It is part of Social Security and involves monthly payment as support to people with limited income and people who are disabled, blind or aged 65 years and above. Additional details about SSI can be found here - https://www.ssa.gov/ssi/text-over-ussi.htm   
  
Both programs are administered by Social Security Administration (SSA) - https://www.ssa.gov/.
The key difference between these two programs, as mentioned in the link (https://www.ssa.gov/ssi/text-over-ussi.htm) is:
“Social Security benefits may be paid to you and certain members of your family if you are “insured” meaning you worked long enough and paid Social Security taxes. Unlike Social Security benefits, SSI benefits are not based on your prior work or a family member's prior work.”  
  
Each year congressional reports are published with information of SSI and OSDI payments made by each state. This report includes information about no. of recipients in each category and the total payments made for each state.  
  
I plan to analyze this data for the years 2013, 2014, 2015, 2016 and 2017 and see if there are any definite trends. I plan to do this as part of my final project for Human-Centered Data Science course (DATA 512) during Fall 2018 at the University of Washington. Keeping in mind the human centered aspect of this course, my intent is to get a sense of distribution of people benefiting from OASDI and SSI across USA.  
  
# Data

The data consists of congressional statistics reports (OASDI and SSI fact sheets) published for each year that includes the following information for each state. Each report has two types of information for each state:  
  
- OASDI Payments
- SSI Payments
  
## OASDI Payments:
The data for OASDI is organized in tabular format with the following data presented for each congressional district within each state. There is also a summation provided at each state level.  
The information provided is:  
  
| Column | Datatype | Description |
|-----|------------|----|
|Total workers|Number|Total Number of beneficiaries|
|Retired workers| Number |Number of beneficiaries who are Retired workers|
|Disabled workers| Number |Number of beneficiaries who are Disabled workers|
|Widow(er)s and parents| Number |Number of beneficiaries who are Widow(er)s and parents|
|Spouses| Number |Number of beneficiaries who are Spouses of a worker who is retired or disabled|
|Children| Number |Number of beneficiaries who are Children of a worker who is retired, deceased, or disabled|
|All beneficiaries| Number |Total monthly benefits (thousands of dollars) for All beneficiaries|
|Retired workers payments| Number |Total monthly benefits (thousands of dollars) for Retired Workers|
|Widow(er)s and parents payments| Number |Total monthly benefits (thousands of dollars) for Widow(er)s and parents|
|Number of beneficiaries aged 65 or older| Number | Total Number of beneficiaries aged 65 or older|
  
## SSI Payments:
The data for SSI is organized in tabular format with the following data presented for each congressional district within each state. There is also a summation provided at each state level.  
The information provided is:  
  
| Column | Datatype | Description |
|-----|------------|----|
|Total recipients|Number|Total Number of recipients|
|Aged| Number |Number of recipients who are Aged 65 years of older|
|Blind| Number | Number of recipients who are Blind|
|Disabled| Number | Number of recipients who are Disabled|
|Total monthly payments| Number |Total monthly payments (thousands of dollars)|
|Aged Payments| Number | Total monthly payments (thousands of dollars) for recipients who are Aged 65 years or older|
|Blind Payments| Number | Total monthly payments (thousands of dollars) for recipients who are Blind|
|Disabled Payments| Number | Total monthly payments (thousands of dollars) for recipients who are Disabled|
|Total recipients with OASDI|Number|Total Number of recipients who are receiving both SSI payments and Social Security benefits|
|Number of OASDI beneficiaries aged 65 or older | Number | Total Number of beneficiaries aged 65 or older who are receiving both SSI payments and Social Security benefits |
  
US population data in numbers for the years 2013, 2014, 2015, 2016 and 2017.

## Sources:
The above data can be found in the following links:  
  
| Year | Link |
|-----|------------|
|2013|https://catalog.data.gov/dataset/congressional-statistics-a0610|
|2014|https://catalog.data.gov/dataset/congressional-statistics-december-2014|
|2015|https://www.ssa.gov/policy/docs/factsheets/cong_stats/2015/index.html|
|2016|https://www.ssa.gov/policy/docs/factsheets/cong_stats/2016/index.html|
|2017|https://catalog.data.gov/dataset/congressional-statistics-december-2017|
  
Popultaion Data has been sourced from https://data.worldbank.org/indicator/SP.POP.TOTL?locations=US

## Licenses:
The data for years 2013, 2014 and 2017 are released under Creative Commons CCZero license (http://opendefinition.org/licenses/cc-zero/) as can be found in the links above. The sources for years 2015 and 2016 are not specifically provided in the source https://catalog.data.gov. However, the data for years 2015 and 2015 was available in the same root source as for years 2013, 2014 and 2017. Considering that the data for the years 2013, 2014 and 2017 were released under CCZero license, it can be assumed that the data for 2015 and 2016 is also covered under the same license since the nature of data is exactly the same. However, I'm validating if this assumption is ok to make. Else, I will disregard data for years 2015 and 2016 in my analysis.

Popultaion data has been released under CC BY-4.0 license (https://datacatalog.worldbank.org/public-licenses#cc-by).
  
# Research Scope
I don’t have any specific hypothesis to test. However, I wish to analyze the data to see:  

- Distribution of beneficiaries of OASDI and SSI across US.
- Trends in the OASDI and SSI spending.
- Trends in distribution of beneficiaries of OASDI and SSI across US.
- Comparison of SSI vs. OASDI spending.
  
## Data Preprocessing:
I plan to extract the data from the excel spreadsheet using Python. Once the data is extracted, I plan to clean it by removing special characters like commas and then store the actual values in cases where the numbers are represented as thousands. Once I have the data preprocessed, I plan to store the data for OASDI and SSI in separate Python Dataframes for independent analysis. I then plan to combine/merge them for some comparative analysis.  
  
## Tools:
I plan to use Python Programming language for data extraction from the excel sheets and the processing. I plan to use matplotlib and seaborn libraries for visualizations. I plan to use Jupyter Python Notebooks for computing, analysis and presentation. I plan to document each of the research steps within the Jupyter Notebook for reproducibility.  
  
# Deliverables
As part of this analysis, I plan to publish the results of my findings along with visualizations to support. I also plan to deliver a Jupyter Notebook with my analysis, visualizations and detailed steps on how to reproduce the analysis. I plan to publish to all of this in this GitHub Repository.


