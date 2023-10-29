# SAS

# What is SAS?

SAS (Statistical analysis system) is one of the most popular software for data analysis. It is widely used for various purposes such as data management, data mining, report writing, statistical analysis, business modeling, applications development and data warehousing.

Knowing SAS is an asset in many job markets. It is tagged 'leader' in Advanced Analytics Platforms as per Gartner Magic Quadrant for Data Science and Machine Learning Platforms throughout all eight years since its inception.

# SAS Modules

When you install SAS software, it has several in-built modules which are designed for various analytics and reporting purposes. See some of the common SAS modules or components.

__Base SAS__ - It is the most common SAS module. It is used for data manipulation such as filtering data, selecting, renaming or removing columns, reshaping data etc.  

__SAS/STAT__ - It runs popular statistical techniques such as Hypothesis Testing, Linear and Logistic Regression, Principal Component Analysis etc.  

__SAS/ACCESS__ - It lets you to read data from databases such as Teradata, SQL Server, Oracle DB2 etc.  

__SAS/GRAPH__ - You can create simple and complex graphs using this component.  

__SAS/ETS__ - You can perform time series forecasting such as ARIMA, Exponential Smoothing, Moving Average etc. using this module.

# INTRODUCTION TO SAS PROGRAMMING

The purpose of this post is to help you understand the fundamentals of SAS programming. It is intended to give first time users an idea about the SAS software and how to access it and get you up and ready with SAS programming. At the end of this tutorial, you would be acquainted with SAS basic syntax rules, how to enter data into SAS, variable types and how to run a program in SAS.  

If you really want to make your career in analytics, you should focus on learning SAS programming as SAS is a world leader in softwares for advanced analytics. To see the real potential of SAS programming, login to any job portal and search for jobs required skill set of SAS. You would find a large number of jobs waiting for you if you know SAS.  

SAS stands for __Statistical Analysis System__.

# What SAS can do?

__SAS can perform the following tasks:__

It allows you to enter, retrieve and manage your data easily  

It can read data from various external sources (Excel, CSV, Text files, Databases, Webpage etc)  

You can explore and manipulate data in SAS.  

It can analyze your data statistically and mathematically. Includes various statistical techniques. 

It can generate beautiful graphs and tables.  

You can run SQL queries on SAS datasets.  

You can automate repetitive tasks with SAS Macros.  

It can develop entirely new software applications.  

# Basics of SAS Programming

__SAS has three main windows :__

1) Editor Window: where you type programs for analyzing data  
2) Log Window: where error messages and executed SAS commands are printed  
3) Result Window: where the result of SAS programs are printed.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/da498758-49de-48f9-a09d-354cd6154eeb)  

# Basic SAS Program

Let's look at a simple SAS program :

![image](https://github.com/Deepak2k20/SAS/assets/65231118/4bb7b212-7886-4c19-abe9-54ce2c3bd517)  

```sas
data example1;
input name $ ID;
cards;
Sam 12
Sandy 13
Reno 11
Farhan 10
;

proc print;
run;  

```

data example1;: This line initiates a data step and creates a new dataset named "example1" to store the data.

input name $ ID;: This line defines the variables for the dataset. It specifies that there are two variables: "name" and "ID." The dollar sign ($) after "name" indicates that it is a character variable, and the lack of a dollar sign after "ID" indicates that it is a numeric variable.

cards;: This keyword signals the start of inline data. The data enclosed between cards; and the next semicolon (;) will be read as input data for the dataset.

The lines following cards; contain the actual data values. Each line represents one observation (row) in the dataset. In this example, there are four observations with two variables each: "name" and "ID."

proc print;: This line initiates the proc print procedure, which is used to display the contents of a dataset.

run;: This line signifies the end of the data step and the end of the proc print procedure.

When you run this SAS code, it will create the dataset "example1" with the given data and then print its contents to the results window. The output will show the "name" and "ID" values for each observation in the dataset.  

# How to Submit SAS Program

To submit the SAS program, press F3 shortcut key. Alternatively, you can click on click on the icon of "the little guy running" at the top of the SAS tool bar.  

# SAS Log Window

It is where error messages and executed SAS commands are printed.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c5f18dad-802e-4101-a14a-dc7cd002781b)  

# SAS Results Window

![image](https://github.com/Deepak2k20/SAS/assets/65231118/537773bf-cc3c-467a-bdc8-a895034a6df7)  

# SAS Libraries

SAS files are stored in a SAS library. A SAS library is simply a collection of SAS files (data sets) that are stored in a folder. SAS files are stored either temporarily or permanently. By default, it is stored in a temporary library called Work.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9bdc0d47-6f0c-4f62-a6a7-86e57e5e0091)  

# How to create a SAS library

1) __Temporary :__ When you don't specify a library name at all, then the file is stored in a temporary SAS library called Work. When you close out the SAS session in which you created the SAS file, the temporary library and all of its files are removed from your computer's memory.

  ```sas
data example;

```

In this case, example is a data set that is stored in Work library. Note : You can specify the library name Work followed by dot (.) and then data set name.  

```sas
data work.example;
```

2) __Permanent :__ If you use a library name other than the default library name 'Work' when creating a SAS file, then the file is stored permanently until you delete it. That is, you can use permanent SAS libraries and their contents in subsequent SAS sessions.  

You can specify the library name followed by dot (.) sign and then data set name.  

```sas
data mydata.example;
```

In this case, example1 is a data set that is stored in mydata library.  

# SAS Programming Rules

When it comes to programming in SAS, there are several best practices and rules that can help improve code readability, efficiency, and maintainability. Here are some important SAS programming rules to keep in mind:  

__I. Rules for SAS statements__

1) All SAS statements (except those containing data) must end with a semicolon (;).
```sas
Example : "DATA example1;" is an example of a SAS statement.
```
2) Any number of SAS statements can appear on a single line provided they are separated by a semicolon.
```sas
Example : "DATA example1; Input Name $ ID;" is an example of a SAS statement.
```
3) SAS statements typically begin with a SAS keyword. (DATA, PROC).

4) SAS statements are not case sensitive, that is, they can be entered in lowercase, uppercase, or a mixture of the two.
```sas
Example : SAS keywords (DATA, PROC) are not case sensitive
```
5) A delimited comment begins with a forward slash-asterisk (/*) and ends with an asterisk-forward slash (*/). All text within the delimiters is ignored by SAS.

__II. Rules for SAS names__

1) All names must contain between 1 and 32 characters.

2) The first character appearing in a name must be a letter (A, B, ...Z, a, b, ... z) or an underscore (_). Subsequent characters must be letters, numbers, or underscores. That is, no other characters, such as $, %, or & are permitted. Blanks also cannot appear in SAS names.

3) SAS names are not case sensitive, that is, they can be entered in lowercase, uppercase, or a mixture of the two. (SAS is only case sensitive within quotation marks.)

__III. Rules for SAS variables__

If the variable in the INPUT statement is followed by a dollar sign ($), SAS assumes this is a character variable. Otherwise, the variable is considered as a numeric variable.  

# Difference between PROC and DATA Step

__DATA STEP__

Any portion of a SAS program that begins with a DATA statement and ends with a RUN statement is called a DATA Step.  

DATA steps are used to manage data. In detail, DATA steps are used to read raw or external data into a SAS data set, to modify data values, and to subset or merge data sets.  

__PROC (Procedure)__

Any portion of a SAS program that begins with a PROC statement and ends with a RUN statement is called a PROC Step or Procedures.  

PROC steps are in-built programs that allow us to analyze the data contained in a SAS data set. PROC steps are used to calculate descriptive statistics, to generate summary reports, and to create summary graphs and charts.  

Example SAS Code for Practice

```sas
data temp;
input ID Company $20.;
cards;
12 Reliance
13 Google
11 Microsoft
10 SAS
9 Tom
10 SAP
;
  
proc print;
run;

```
The above program creates a dataset named temp which is stored in WORK library. In the dataset, there are 2 variables/columns - Company and ID which contains 6 observations/rows. The command PROC PRINT tells SAS to print the dataset in Results Window.  

# How to Filter Data in SAS

The IF statement is used to apply a condition to filter the data.  

```sas
data out;
set temp;
if ID > 10;
run;
```

The SET statement allows you to read values from a SAS data set (temp). The SAS Statement 'IF ID > 10' tells SAS to read only those ID values that are greater than 10. Later SAS paste these values into a new data set (OUT) without overwriting existing data set (temp).  

__Multiple Conditions__ - The following SAS code is using the multiple conditions in the IF statement.  

```sas
data out;
set temp;
if ID = 10 and Company = 'SAS';
run;
```

if ID = 10 and Company = 'SAS';: In this case, IF statement selects records where both the "ID" variable is equal to 10 and the "Company" variable is equal to 'SAS'.  

# IF-THEN-ELSE Statements

The following code creates a new "flag" variable where the value 'No' is assigned when the "ID" is less than or equal to 10, 'Yes' when the "ID" is greater than 10 and less than or equal to 12, and 'Invalid' for any other value of "ID" greater than 12, based on the values in the existing dataset "temp". The "flag" variable is a character variable with a length of 8 characters.  

```sas

data out;
	set temp;
	length flag $8;
	if ID <=10 then
		flag='No';
	else if ID > 10 and ID <=12 then
		flag='Yes';
	else
		flag='Invalid';
run;

```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/02d8b1c1-6945-4cbe-bb91-f2f63753f4f3)  

# How to Sort Data in SAS

In SAS, the PROC SORT procedure sorts a dataset.  

```sas
proc sort data=temp;
by ID;
run;
```

by ID;: This line specifies the variable "ID" that will be used for sorting the dataset. When you sort the data, the values of the "ID" variable will be arranged in ascending order by default.  

To sort the dataset in descending order, you can use the keyword descending after BY statement.  

```sas
proc sort data=temp;
by descending ID;
run;
```

# How to Calculate Summary in SAS

In SAS, PROC MEANS is used to calculate summary statistics, such as count, mean, minimum, maximum, standard deviation and more for one or more variables in a SAS dataset. The following code calculates descriptive statistics for the variable "ID" in the dataset "temp."  

```sas
proc means data=temp;
var ID;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b6319805-3661-464d-b7a3-75d11b564576)  

# How to Generate Frequency Distribution in SAS

PROC FREQ is a SAS procedure used to generate frequency tables, which display the distribution of values within categorical variables.  

The following code shows how to use PROC FREQ with the built-in SAS dataset "sashelp.cars". We have created a new dataset named "cars" by copying the content of the built-in dataset "sashelp.cars".  

```sas
/* Step 1: Access the sashelp.cars dataset */
data cars;
set sashelp.cars;
run;

/* Step 2: Use PROC FREQ to analyze the "make" variable */
proc freq data=cars;
tables make;
run;
```

Within the PROC FREQ step, the "tables" statement is used to specify the variable "make" for which we want to calculate the frequency table. In this case, we are interested in analyzing the distribution of the "make" variable, which represents the car manufacturer.  

# How to Combine Datasets in SAS

PROC APPEND is a SAS procedure used to combine or append datasets. It is commonly used when you have multiple datasets with the same structure (same variables and data types) and you want to merge them vertically, concatenating one dataset below the other.  

```sas
/* Create dataset1 */
data dataset1;
input ID Name $ Age Grade $;
cards;
1 John 18 A
2 Jane 17 B
3 Alex 19 A
;
run;

/* Create dataset2 */
data dataset2;
input ID Name $ Age Grade $;
cards;
4 Sarah 16 B
5 Mike 18 C
6 Emily 17 A
;
run;

/* Use PROC APPEND to combine datasets */
proc append base=dataset1 data=dataset2;
run;

```

After combining the datasets, Dataset1 now has 6 observations. It originally had 3 observations. Please refer to the log below.  

```
 NOTE: Appending WORK.DATASET2 to WORK.DATASET1.
 NOTE: There were 3 observations read from the data set WORK.DATASET2.
 NOTE: 3 observations added.
 NOTE: The data set WORK.DATASET1 has 6 observations and 4 variables.
```

# APPLICATIONS OF SAS

This tutorial explains how SAS application is used in various industries. It includes several real-world use cases of different domains.  

__SAS Projects in Marketing__

Marketing analytics is used across industries so the following projects are not specific to a particular industry.  

1) __Customer Segmentation__ : SAS can be used for dividing customers into groups for targeted marketing.  

2) __Customer Attrition Analysis__ : SAS predicts customers likely to leave to retain it.  

3) __Market Basket Analysis__ : SAS can be used in finding related products for cross-selling.  

4) __Marketing Mix Modeling__ : SAS helps in analyzing the impact of advertising and promotions on sales.  

5) __Campaign Optimization__ : SAS can be used to improve marketing strategies by analyzing campaign data.  

6) __Pricing Analytics__ : SAS is used to analyze pricing data and optimize pricing strategies.  

7) __Customer Lifetime Value (CLV) Analysis__ : SAS helps calculate the CLV for individual customers. It is used to identify high value customers.


 __SAS Projects in Banking and Finance__

 Here is a list of common projects in which SAS is used in the banks and other finance companies.  

 1) __Risk Management__ : SAS is used in banks to manage different types of risks like credit risk, market risk etc.
    
 2) __Fraud Detection__ : SAS helps banks detect and stop fraud in transactions by looking for suspicious patterns.

 3) __Credit Scoring and Underwriting__ : SAS helps banks decide who to lend money to by checking how reliable borrowers are.

 4) __Customer Analytics__ : SAS helps banks understand what customers like and need so that they can offer better services.

 5) __Anti-Money Laundering (AML)__ : SAS helps banks find transactions that might be connected to illegal money activities.


__SAS Projects in Healthcare and Life Sciences__

Here are some common projects in which SAS is used in the healthcare and life sciences companies.  

1) __Clinical Trials and Drug Development__ : SAS is used in analyzing clinical trials data. It helps the pharmaceutical companies in regulatory compliance.

2) __Pharmacovigilance and Drug Safety__ : SAS monitors adverse events and drug safety, identifying potential medication risks.
 
3) __Survival Analysis__ : SAS can be used for survival analysis. It analyzes the time it takes for an event of interest to occur such as time to death.
 
4) __Healthcare Analytics__ : SAS analyzes health records and is used for identifying disease trends and patient management.


__SAS Projects in Insurance__

Following are some common projects in which SAS is used in the insurance companies.  

1) __Actuarial Analysis__ : SAS is used in actuarial departments to model and analyze insurance risks, calculate reserves and premium rates.

2) __Risk Management__ : SAS helps insurance companies in managing and assessing various types of risks such as underwriting risk, investment risk and operational risk.

3) __Claims Analytics__ : SAS can be used to analyze claims data to identify patterns and trends in claims. It can also be used to measure claims severity and detect fraudulent claims.

4) __Underwriting and Pricing__ : SAS is used by the underwriting team to measure risk and calculate insurance premium rates accordingly.
 
5) __Policyholder Behavior Analysis__ : SAS is used to analyze policyholder behavior such as renewal rates and lapse rates to understand customer preferences.  


__SAS Projects in Telecommunication__

Here is a list of common projects in which SAS is used in the telecom companies.  

1) __Network Performance Analysis__ : SAS is used to analyze network data, such as call records, network logs and performance metrics. It helps to improve overall network performance.  

2) __Usage Analytics__ : SAS can be used to analyze customer usage data to understand data consumption patterns, identify high usage customers and offer personalized data plans.  

3) __Internet of Things (IoT) Analytics__ : SAS can be used to analyze data from IoT devices and sensors.  

4) __Network Traffic Analysis__ : SAS can be used to analyze network traffic patterns to understand user behavior, identify peak usage times.  


# SAS KEYBOARD SHORTCUTS THAT EVERY ANALYST MUST KNOW

If you fancy yourself a rockstar analyst, you know how valuable it is to keep your hands on the keyboard. Apart from making you work more efficiently and faster, you can also impress your friends or colleagues by being able to work without a mouse. Here is a list of SAS keyboard shortcuts that can make your life easy while working with SAS.  

# Important SAS Shortcuts for Productivity

The following is a list of productivity boosting SAS keyboard shortcuts. It would bring efficiency in writing SAS programming code.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/332f2765-5d19-41a3-a5a2-70ad1e09adb0)  

# Important Shortcuts for SAS Enterprise Guide

![image](https://github.com/Deepak2k20/SAS/assets/65231118/df108fed-7e20-4a6f-bf21-e991cf93bb76)  

# Other Useful SAS Keyboard Shortcuts

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a9da838a-e777-4198-91b3-a8edebe302a9)  

# How to create keyboard shortcuts in SAS

1) Open the Enhanced Editor window within SAS.  

2) From the toolbar, select Tools --> Options --> Keys.  

3) Scroll down to the keystroke you would like to assign to the series of commands, looking for a keystroke that has no assignment.  

4) Add the command code under the definition heading. For example: log; clear; output;clear;  

5) Close the Keys window.  

# How to Import Data

## HOW TO USE PROC IMPORT TO IMPORT DATA INTO SAS

PROC IMPORT is a powerful SAS procedure that allows you to import data from various external file formats into SAS datasets. It simplifies the process of importing data in SAS. Since PROC IMPORT is commonly used in real-world work scenarios, it is important for every SAS programmer to be familiar with this SAS procedure.  

__Syntax : PROC IMPORT__

Syntax of PROC IMPORT is defined below -

```sas
PROC IMPORT DATAFILE=FileName OUT=SASDatasetName
DBMS=identifier REPLACE;
GETNAMES=Yes;
RUN;
```

Arguments of PROC IMPORT : Explanation

1) __DATAFILE__: Specify the location of the file to be imported.  

2) __OUT__: Specify the name to assign to the dataset after it is imported into SAS.  

3) __DBMS__: Define the format of the file being imported. Some of the common values are CSV, EXCEL, TAB, DLM, ACCESS.  

4) __REPLACE__: Determine whether to replace the existing SAS Dataset. Yes/No.  

5) __GETNAMES__: Specify whether to use the first row as variable names. By default it it YES. If you set the option as NO, it will tell SAS not to use the first row of data as variable names. In this case SAS assigns variable names as VAR1, VAR2, VAR3 if there are 3 variables.

## File Formats supported in PROC IMPORT

Following is a list of file extensions supported in PROC IMPORT. Specify the value in DBMS=identifier option  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b91ecfb2-3b51-48f2-ac53-9c85294ab333)  

## Use PROC IMPORT to Import CSV File

Let's take a simple example to import CSV (comma-separated values) file into SAS. Here we have data named data.csv which has 3 variables and 5 observations. Column names are ID, Name, Score. Data looks like the image below. You can open CSV file in Notepad.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/fd29ea16-358e-4876-8397-bbad5d2cd2b8)  

DBMS=CSV tells SAS that the file being imported is a CSV file.  

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/data.csv'
	DBMS=CSV
	OUT=WORK.READIN;
	GETNAMES=YES;
RUN;

```

The above SAS Program creates a SAS dataset named READIN in the temporary library (WORK).  

```sas
NOTE: WORK.READIN data set was successfully created.
NOTE: The data set WORK.READIN has 5 observations and 3 variables.
```

__Output__  

To see the imported file in RESULTS window, you can use PROC PRINT procedure. See the SAS program below.  

```sas
PROC PRINT DATA=WORK.READIN;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/38221a4a-6a26-4a58-b244-302a6c4e27c1)  


### Use PROC IMPORT to Import Delimited File

Suppose you have a delimeted file and you want to read it in SAS. Delimeter is | symbol. Delimited file looks like the image below. Datafile name is data.txt.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ab34bf61-8758-4cad-a645-18abc8140bbe)  

DBMS=DLM tells SAS that the file being imported is a delimited file. To specify delimiter, use the DELIMITER='|' option.  

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/data.txt'
	DBMS=DLM
	OUT=WORK.READIN REPLACE;
	DELIMITER='|';
	GETNAMES=YES;
RUN;
```

We have used REPLACE option to inform SAS to replace the existing SAS dataset READIN.  

OUT=WORK.READIN means READIN dataset to be created in the temporary SAS library (WORK).  

```sas
If you have blank as delimiter in the file, you don't need to use DELIMITER option as default delimeter is blank when you use DBMS=DLM.
```

### Use PROC IMPORT to Import TAB Delimited File

Suppose you have a TAB delimeted file. TAB delimited file is shown in the image below. Datafile name is data.txt.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9099d961-c75a-477b-aa3f-61e9f4c8948c)  

DBMS=TAB tells SAS that the file being imported is a TAB delimited file  

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/data.txt'
	DBMS=TAB
	OUT=WORK.READIN REPLACE;
	GETNAMES=YES;
RUN;
```

Another way to do this is by specifying DELIMITER='09'x and DBMS=DLM. '09'x represents the hexadecimal value for the tab character. The tab character (ASCII code 9) is commonly used as a delimiter in data files to separate columns (variables).  

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/data.txt'
	DBMS=DLM
	OUT=WORK.READIN REPLACE;
	GETNAMES=YES;
	DELIMITER='09'x;
RUN;
```

### Use PROC IMPORT to import a file with multiple delimiters

While it is uncommon to see files with multiple delimiters, there are instances where certain vendors maintain files in complex formats that may include multiple delimiters. Suppose you have a raw file having both comma and tab as delimiters. In this case we need to specify both the delimiters in DELIMITER=','09'x '

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/data.txt'
	DBMS=DLM
	OUT=WORK.READIN REPLACE;
	GETNAMES=YES;
	DELIMITER=','09'x ';
RUN;
```

### Use PROC IMPORT to Import Excel File

Many businesses and organizations commonly work with MS Excel files for various purposes such as data storage, analysis, reporting etc. Hence MS Excel file formats are widely used in the real world. In the example below we are importing Excel file in SAS.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8aa31585-e54a-4488-80f3-86f916726e0d)  

DBMS=XLSX informs SAS that the file being imported is a MS Excel file (with .xlsx extension).  

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/Data.xlsx'
	DBMS=XLSX
	OUT=WORK.READIN REPLACE;
	GETNAMES=YES;
RUN;
```

### Additional Options in PROC IMPORT to Import Excel File

```sas
PROC IMPORT DATAFILE="filename" 
DBMS=identifier
OUT=SASDataset REPLACE;
SHEET="sheetName";
GETNAMES=YES; 
DATAROW=N;
RANGE="rangeName";
RUN;
```

1) __SHEET__: Specify the name of the sheet in the Excel file from which you want to import data. When you use PROC IMPORT without explicitly mentioning the SHEET option, SAS will automatically import the first sheet of the Excel file by default. If you want to import a specific sheet, you need to explicitly specify the sheet name.  

2) __DATAROW__: Specify the row number from which you want SAS to import data. If GETNAMES=YES, the DATAROW value must be greater than or equal to 2. If GETNAMES=NO, the DATAROW value must be greater than or equal to 1.  

3) __RANGE__: Specify the range of Excel file. For e.g. RANGE="Sheet1$A1:D50"


### Use PROC IMPORT to Import SPSS File

A few years ago, SPSS used to be the preferred statistical software for survey analysis. If you have a data file in SPSS format (.SAV) and you want to import it into SAS, you can refer to the SAS program below. 

DBMS=SAV tells SAS that you are importing a file in the SPSS data file format.  

```sas
PROC IMPORT DATAFILE='/home/deepanshu88us0/surveyData.sav'
	DBMS=SAV
	OUT=WORK.READIN REPLACE;
	fmtlib=WORK.FORMATS;
RUN;
```
```sas
The FMTLIB option tells SAS to create custom SAS formats if the data contains SPSS labels.
```

## IMPORTING EXCEL DATA INTO SAS

PROC IMPORT is the SAS procedure used to read data from excel into SAS. This tutorial covers how to import excel data to SAS with PROC IMPORT. Loading excel data to SAS is one of the most common task of a SAS programmer / analyst. Most of the raw data files are saved in MS Excel so we need to take it to SAS for further analysis.  

### PROC IMPORT Syntax:

```sas
PROC IMPORT 
DATAFILE="filename"
OUT=SAS-data-set 
DBMS=identifier 
  REPLACE;
  SHEET="Sheet-name";
  GETNAMES=YES; 
  DATAROW=N;
  RANGE="range-name";
RUN;
```

1) __DATAFILE__ =option tells SAS where to find the Excel file that you want to import (Complete filename path).
```sas
For example : DATAFILE = "C:\Desktop\age.xlsx"
```
2) __OUT__ = option tells SAS to create a dataset with any name of your choice. By default, the imported dataset is saved on WORK library (temporary library)
```sas
Examples :
i. OUT = Age . In this statement, PROC IMPORT uses the WORK library and dataset name is Age. Please note that OUT = Age is equivalent to OUT = Work.Age .
ii. OUT = Input.Age In this statement, PROC IMPORT uses the Input library (Permanent library).
```
3) __DBMS__ =option tells SAS the type of file to read.
```sas
Examples :
i. DBMS = XLS for Excel 97-2003 workbooks
ii.DBMS = XLSX for Excel 2007 and above workbooks
```
4) __REPLACE__ is used to overwrite the existing SAS dataset (If any) mentioned in the OUT= option.

5) __SHEET__ = option is used to specify which sheet SAS would import.
```sas
Examples :
i. SHEET = "Sheet1" - To import data from worksheet named sheet1.
ii. SHEET = "Goal" - To import data from worksheet named Goal.
```

6) __GETNAMES__ = YES tells SAS to use the first row of data as variable names.
```sas
By default, PROC IMPORT uses GETNAMES= YES. If you type GETNAMES= NO, SAS would not read variable names from first row of the sheet.
```

7) __DATAROW__ = option is used to specify starting row from where SAS would import the data.
```sas
For example : DATAROW =5 tells SAS to start reading data from row number 5.
Note :
i. When GETNAMES=YES, DATAROW must be greater than or equal to 2.
ii. When GETNAMES=NO, DATAROW must be greater than or equal to 1
```

8) __RANGE__ = option is used to specify which range SAS would import.
```sas
Examples :
i. RANGE="Sheet1$B2:D10"
This would tell SAS to import data from range B2:D10 from sheet1
ii. RANGE="Information"
This would tell SAS to import data from excel defined name range. In the example shown above, it is Information.
```

### Importing an Excel file into SAS

```sas
PROC IMPORT DATAFILE= "C:\age.xlsx" 
OUT= WORK.age
DBMS=XLSX
REPLACE;
SHEET="Sheet1"; 
GETNAMES=YES;
RUN;
```

1) __DATAFILE__ = "C:\age.xlsx" tells SAS where to find the Excel file that you want to import.

2) __OUT__ = WORK.age tells SAS to create a dataset named age stored in WORK library  

3) __DBMS__ = XLSX tells SAS the XLSX (Excel 2007 and above) format file to read.  

4) __REPLACE__ is used to overwrite the age dataset if it exists already.  

5) __SHEET__ = "Sheet1" tells SAS to import data from Sheet1.  

6) __GETNAMES__ ="YES" tells SAS to use the first row of data as variable names.

### Important Note -
```sas
Earlier SAS Versions before SAS9.2 does not support XLSX formatted file (Excel 2007 or later files). If your XLSX file contains records fewer than 65000 rows and 255 columns, you can save the file in XLS format by clicking on SAVE AS >> Excel 97-2003 Workbook. Later you can import the converted XLS file into SAS.
```

### Importing an XLS (MS Excel 97-2003) format file into SAS

```sas
PROC IMPORT DATAFILE= "C:\age.xls" 
OUT= WORK.age
DBMS=XLS
REPLACE;
SHEET="Sheet1"; 
GETNAMES=YES;
RUN;
```

DBMS=XLS tells SAS to read the XLS (Excel 97-2003) format file.  

### Importing an excel file from specified row

```sas
PROC IMPORT  DATAFILE= "C:\Desktop\Excel\File1.xlsx" OUT= INPUT
DBMS=XLSX REPLACE;
SHEET="Sheet1";
GETNAMES=YES;
DATAROW=5;
RUN;
```

DATAROW=5 tells SAS to start reading data from row number 5. In this case, variable (column) names would be pulled from first row but column values would be extracted from row 5.  

### Importing variable name from other than first row

Suppose variable names are placed at second row in excel sheet.  

```sas
PROC IMPORT DATAFILE= "E:\SAS Code Repository\Book1.xls"
 DBMS=XLS
 OUT= TEMP  REPLACE;
 NAMEROW=2;
 STARTROW=3;
 GETNAMES=YES;
RUN;
```

NAMEROW=2 tells SAS to extract variable names from second row and STARTROW=3 is used to pull values from third row. NAMEROW only works with XLS but not with XLSX.  

### Importing only specified columns from excel file

```sas
PROC IMPORT OUT= WORK.want (keep=id x y z)
 DATAFILE= "C:\Desktop\File1.xlsx"
 DBMS=XLSX REPLACE;
 GETNAMES=YES;
RUN;
```

The OUT = filename followed by KEEP= statement is used to retain the desired variables. In the example shown above, we retained four variables ID,X,Y and Z.  

In the same way, you can use DROP= statement to remove the variables that you don't want to retain.  

For example : You don't want to import three variables say A, B and C.  

```sas
PROC IMPORT OUT= WORK.want(DROP=A B C) DATAFILE= "C:\Desktop\File1.xlsx" DBMS=XLSX REPLACE;
GETNAMES=YES;
RUN;
```

### Importing only rows that have non-missing data for all the variables

```sas
PROC IMPORT OUT= WORK.want ( WHERE=(x NE . AND y NE . z NE .))
 DATAFILE= "C:\Desktop\File1.xlsx"
 DBMS=XLSX REPLACE;
 GETNAMES=YES;
RUN;
```

In the example shown above, WHERE= statement is used to delete all the rows that have only missing data on variables x,y and z.  

### Importing Data from Excel based on Specified Range

```sas
PROC IMPORT OUT= WORK.want
 DATAFILE= "C:\Desktop\File1.xlsx"
 DBMS=XLSX REPLACE;
RANGE="Sheet1$B4:E100";
GETNAMES=YES;
RUN;
```

RANGE="Sheet1$B4:E100" tells SAS to import data from range B4:E100 from sheet1.  

### Importing Data from Excel based on Named Range

Range Name: In MS Excel, it is a name that represents a cell, range of cells. You can create your own defined name.

Creating a range name is very simple. Select a cell or range of cells and Click on the Name box above Column A and Tye any name you want and Press Enter.

In the example below, Range A1:C10 is selected and then type Info in the name box and Press Enter.    

![image](https://github.com/Deepak2k20/SAS/assets/65231118/557dac22-8245-40f2-b57e-2818b25891a8)  

```sas
PROC IMPORT OUT= WORK.want
 DATAFILE= "C:\Desktop\File1.xlsx"
 DBMS=XLSX REPLACE;
RANGE="Info";
GETNAMES=YES;
RUN;
```

RANGE="Info" tells SAS to import data from excel using user defined named range Info.  

### Rename Columns while Importing

The variable names can be renamed using RENAME= option next to OUT= option.  

```sas
PROC IMPORT DATAFILE= "E:\SAS Code Repository\Book1.xlsx"
 DBMS=XLSX
 OUT= TEMP (RENAME=(Score=TotalScore))  REPLACE;
 GETNAMES=YES;
RUN;
```

### Importing an Excel File from Website into SAS

```sas
filename test temp;
proc http
 url="https://www2.census.gov/acs2005/GEORES.xls"
 method="GET"
 out=test;
run;

proc import file=test
out=readin replace
dbms=xls ;
 NAMEROW=3;
 STARTROW=4;
run;
```

SAS provides a method for extracting data from web pages by procedure named PROC HTTP. This method makes it easy to read data from web pages. In this case, variable name starts from row number 3 in datafile and data values start from row4 onwards. To import CSV file from website, you just need to change the DBMS=XLS to DBMS=CSV.  

To learn more about other data file formats in PROC IMPORT, you can refer the tutorial below.   

## HOW TO IMPORT CSV FILES INTO SAS  

This tutorial explains how to import CSV files into SAS, along with examples.  

### Syntax to import CSV file into SAS

You can use PROC IMPORT to import a CSV files into SAS. The syntax of PROC IMPORT is as follows:  

```sas
PROC IMPORT OUT=newdata
    DATAFILE="/home/deepanshu88us0/mydata.csv"
    DBMS=CSV
    REPLACE;
    GETNAMES=YES;
RUN;
```

OUT: Specify name of the dataset to be imported into SAS  

DATAFILE: File location of CSV file which you want to import  

DMBS: Specify CSV Format  

REPLACE: Optional argument. If the file already exists, replace it.  

GETNAMES: Optional argument. By default, it takes first row as variable names. If the file doesn't have a header,set GETNAMES=NO.  

### Example 1: Import Data from CSV File into SAS

Suppose you have data in CSV file named customers.csv. You can import it into SAS using the code below.  

```sas
PROC IMPORT OUT=newdata
    DATAFILE="/home/deepanshu88us0/mydata/customers.csv"
    DBMS=CSV
    REPLACE;
    GETNAMES=YES;
RUN;
```

The code above uses the PROC IMPORT procedure in SAS to import a CSV file located at "/home/deepanshu88us0/mydata/customers.csv". The imported data will be stored in a dataset named "newdata". The DBMS option is set to CSV, telling SAS the file format is CSV. The REPLACE option is specified, which means that if a dataset with the same name already exists, it will be replaced. The GETNAMES option is set to YES, indicating that the first row of the CSV file contains variable names. It is by default so you can exclude this option if you want.   

To view and print the dataset, you can use   
```sas
proc print data=newdata;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1ed2671f-a11e-4724-9f1b-c50c8d919c2e)  

### Example 2: Import Data from CSV File without Header into SAS

If your CSV file does not have header, you can use GETNAMES=NO option in PROC IMPORT.  

```sas
PROC IMPORT OUT=newdata
    DATAFILE="/home/deepanshu88us0/mydata/customers.csv"
    DBMS=CSV
    REPLACE;
    GETNAMES=NO;
RUN;
```

### Example 3: Import Data from CSV File with Custom Delimiter into SAS

By default, SAS considers comma (,) as a delimiter which separates the values in the CSV file when importing using PROC IMPORT. To change delimiter, you can specify it in the DELIMITER= option in PROC IMPORT. The following code uses semicolon (;) as a delimiter.  

```sas
PROC IMPORT OUT=newdata
    DATAFILE="/home/deepanshu88us0/mydata/customers.csv"
    DBMS=CSV
    REPLACE;
    DELIMITER=";";
RUN;
```

### Example 4: Change Starting Row in PROC IMPORT

You can use the DATAROW= option to import a CSV file from a specific row. The following code imports the CSV file from 5th row.  

```sas
PROC IMPORT OUT=newdata
    DATAFILE="/home/deepanshu88us0/mydata/customers.csv"
    DBMS=CSV
    REPLACE;
    DATAROW=5;
RUN;
```

### Example 5: Guess the Data Type when Importing a CSV File

By default, PROC IMPORT makes decisions about the data type in SAS by examining the first 20 rows of the CSV file. This helps determine whether a variable should be treated as numeric or character. To change it to 30, you can use the GUESSINGROWS=30 option.  

```sas
PROC IMPORT OUT=newdata
    DATAFILE="/home/deepanshu88us0/mydata/customers.csv"
    DBMS=CSV
    REPLACE;
    GUESSINGROWS=30;
RUN;
```

## SAS: DATALINES STATEMENT

The DATALINES statement in SAS is used to create a dataset. You can input data directly into a SAS program using the DATALINES statement, without the need for an external data file.  

### Syntax of DATALINES statement

The syntax of DATALINES statement is as follows.  

```sas
DATA new_dataset;
INPUT variable1 $ variable2 variable3;
DATALINES;
A 10 20
B 15 25
C 8 18
;
RUN;
```

DATA new_dataset;: This line starts the DATA step and defines a new dataset named new_dataset.  

INPUT variable1 $ variable2 variable3;: This line specifies the variable names and their data types. In this case, variable1 is a character variable, while variable2 and variable3 are numeric variables.  

DATALINES;: This line indicates the start of the data section.  

The lines following DATALINES; represent the data values for each variable. Each line represents one observation, and the values for each variable are separated by spaces.  

RUN;: This line marks the end of the DATA step and executes it, creating the "new_dataset" dataset.  

```sas
A dollar sign $ following a variable name indicates that the variable is a character variable.
```

Let's print the dataset using PROC PRINT procedure.  

```sas
proc print data=new_dataset;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/71ccae21-0f3c-4c2d-828f-0c968b01384f)  

### How to read a large character variable in SAS

By default, the length of a character variable is set at the first occurrence of the variable. If you want to read a large character variable, you can use colon modifier : which tells SAS to read variable until there is a space or other delimiter. The $20. indicates the length of the character variable.  

```sas
DATA new_dataset;
   INPUT variable1 :$20. variable2 variable3;
   DATALINES;
   Sam 10 20
   MarkSpencers 15 25
   RandyHortonia 8 18
   ;
RUN;

proc print data=new_dataset;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ab83577f-1783-4a56-9a55-064bfced0da1)  

## SAS CARDS STATEMENT: LEARN WITH EXAMPLES

The CARDS statement in SAS is used to create a dataset. You can directly enter data into a SAS program using the CARDS statement, without the need for an external data file.  

The CARDS statement is an alternative to the DATALINES statement and serves the same purpose. It is used in the same way as DATALINES to specify inline data within the SAS program.  

### Syntax of CARDS statement

The syntax of CARDS statement is as follows.  

```sas
DATA new_dataset;
INPUT variable1 $ variable2 variable3;
CARDS;
A 10 20
B 15 25
C 8 18
;
RUN;
```

DATA new_dataset;: Starts the DATA step and defines a new dataset named new_dataset.  

INPUT variable1 $ variable2 variable3;: Specifies the variable names and their data types. In this case, variable1 is a character variable, while variable2 and variable3 are numeric variables.  

CARDS;: Indicates the start of the data section.  

The lines following CARDS; are the data values for each variable. Each line represents one observation, and the values for each variable are separated by spaces.  

RUN;: marks the end of the DATA step and executes it, creating the "new_dataset" dataset.  

```sas
A dollar sign $ following a variable name indicates that the variable is a character variable.
```

Let's print the dataset using PROC PRINT procedure.  

```sas
proc print data=new_dataset;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/cf91a23a-8f53-46d0-96a8-ec7cba5110d7)  

### How to read a large character variable in SAS

By default, the length of a character variable is set at the first occurrence of the variable. If you want to read a large character variable, you can use colon modifier : which tells SAS to read variable until there is a space or other delimiter. The $20. indicates the length of the character variable.  

```sas
DATA new_dataset;
   INPUT variable1 :$20. variable2 variable3;
   CARDS;
   Arjun 10 20
   DavidHouse 15 25
   TomHorton 8 18
   ;
RUN;

proc print data=new_dataset;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9ea19a9a-700f-47c5-bf64-7de614d78452)  

## IMPORTING DATA INTO SAS

This tutorial will show you how to read data into SAS. It also covers how to import external data to SAS. It includes examples of importing most common formats such as CSV, Excel File and Text Files etc. After finishing this tutorial, you would be comfortable how to extract data into SAS.  

### I. Entering Data Directly in SAS Program

You can enter your lines of data directly in your SAS program by using a DATALINES statement.  

Let's start out by clarifying the main keywords associated with the following program.
The keywords are as follows:  

DATA - The DATA step always begins with a DATA statement. The purpose of the DATA statement is to tell SAS that you are creating a new data set i.e. outdata.  

INPUT - Use the INPUT statement to define the variables used in the data set.  

Dollar sign ($) - The dollar sign ($) is used to identify a variable as character type.  

DATALINES - The DATALINES statement is used to indicate that the lines following it contain the actual data.  

PROC PRINT - The PROC PRINT statement is used to print out the contents of the data set in the output window.  

RUN - The DATA step ends with a RUN statement.  

```sas
DATA outdata; 
   INPUT age gender $ dept obs1 obs2 obs3; 
   DATALINES; 
1 F 3 17 6 24
1 M 1 19 25 7
3 M 4 24 10 20
3 F 2 19 23 8
2 F 1 14 23 12
2 M 5 1 23 9
3 M 1 8 21 7
1 F 1 7 7 14
3 F 2 2 1 22
1 M 5 20 5 2
3 M 4 21 8 18
1 M 4 7 9 25
2 F 5 10 17 20
3 F 4 21 25 7
3 F 3 9 9 5
3 M 3 7 21 25
2 F 1 1 22 13
2 F 5 20 22 5
;
proc print;
run;
```

You can also use CARDS instead of DATALINES. Both means the same. There is no difference between these two keywords. See the program below -  

```sas
DATA outdata;
   INPUT age gender $ dept obs1 obs2 obs3;
   CARDS; 
1 F 3 17 6 24
;
proc print;
run;
```

### Reading Delimited Data

The default delimiter is blank. If you have a data file with other delimiters such as comma or tab you need to define the delimiter before defining the variables using INFILE and DLM = options.  

```sas
Syntax : Infile 'file-description' dlm=','
```

For tab delimiter, the syntax would be infile 'file-description' dlm='09'x  

For colon delimiter, the syntax would be infile 'file-description' dlm=':'  

```sas
DATA outdata; 
   INFILE Datalines dlm =",";
   INPUT age gender $ dept obs1 obs2 obs3; 
   Datalines; 
1,F,3,17,6,24
1,M,1,19,25,7
3,M,4,24,10,20
3,F,2,19,23,8
2,F,1,14,23,12
;
proc print;
run;
```

### Importing External Data into SAS

### Method I : PROC IMPORT

PROC IMPORT is a SAS procedure to import external files into SAS. It automates importing process. You don't need to specify variable type and variable length to import an external file. It supports various formats such as excel file, csv, txt etc.  

#### 1. Importing an Excel File into SAS

The main keywords used in the following program are :  

1. OUT - To specify name of a data set that SAS creates. In the program below, outdata is the data set saved in work library (temporary library)

3. DBMS - To specify the type of data to import.

5. REPLACE - To overwrite an existing SAS data set.

7. SHEET - To import a specific sheet from an excel workbook

9. GETNAMES - To include variable names from the first row of data.

```sas
PROC IMPORT DATAFILE= "c:\deepanshu\sampledata.xls"
OUT= outdata
DBMS=xls
REPLACE;
SHEET="Sheet1";
GETNAMES=YES;
RUN;
```

#### 2. Importing a Tab-Delimited File into SAS

The program below is similar to the code of importing excel file. The only difference is DBMS = DLM and delimter = '09'x.  

```sas
PROC IMPORT DATAFILE= "c:\deepanshu\sampledata.txt"
OUT= outdata
DBMS=dlm
REPLACE;
delimiter='09'x;
GETNAMES=YES;
RUN;
```

#### 3. Importing a Comma-Delimited File with TXT extension

To get comma separated file with a txt extension into SAS, specify delimeter = ','  

```sas
PROC IMPORT DATAFILE= "c:\deepanshu\sampledata.txt"
OUT= outdata
DBMS=dlm
REPLACE;
delimiter=',';
GETNAMES=YES;
RUN;
```

#### 4. Importing a Comma-Delimited File with CSV extension

To get comma separated file into SAS, specify DBMS= CSV  

```sas
PROC IMPORT DATAFILE= "c:\deepanshu\sampledata.txt"
OUT= outdata
DBMS=csv
REPLACE;
GETNAMES=YES;
RUN;
```

#### 5. Importing a Space-Delimited File

To extract a space delimited file, specify delimiter = '20'x  

```sas
PROC IMPORT DATAFILE= "c:\deepanshu\sampledata.txt"
OUT= outdata
DBMS=dlm
REPLACE;
delimiter='20'x;
GETNAMES=YES;
RUN;
```

#### 6. Importing a file containing multiple delimiter

If two or more delimiters, such as comma and tabs, quote them following delimiter = option  

```sas
PROC IMPORT DATAFILE= "c:\deepanshu\sampledata.txt"
OUT= outdata
DBMS=dlm
REPLACE;
delimiter=','09'x ';
GETNAMES=YES;
RUN;
```

### Method II : Get External File - INFILE

In SAS, there is one more method called INFILE to import an external file. It's a manual method of importing an external file as you need to specify variables and its types and length.  b

#### 1. Reading a CSV File

INFILE statement - To specify path where data file is saved.  
 
DSD - To set the default delimiter from a blank to comma.  

FIRSTOBS=2 : To tell SAS that first row contains variable names and data values starts from second row.  

```sas
data outdata; 
infile 'c:\users\deepanshu\documents\book1.csv' dsd firstobs=2;
input id age gender $ dept $; 
run;
```

#### 2. Reading a TAB Delimited File

We can use DLM='09'x to tell SAS that we are going to import a tab delimited file. The TRUNCOVER statement tells SAS to assign the raw data value to the variable even if the value is shorter than expected by the INPUT statement.  

```sas
data outdata;
  infile 'c:\deepanshu\dummydata.txt' DSD dlm='09'x truncover;
  input employee :$30. DOJ :mmddyy8. state :$20.;
run;
```

#### How to handle an external file :

Using a FILENAME statement to handle an external file.  

```sas
FILENAME sample 'c:\deepanshu\sampledata.csv' ;
DATA outdata;
infile sample dsd;
INPUT age gender $ dept obs1 obs2 obs3;
run;
```

### SAS : READ CHARACTER VARIABLE OF VARYING LENGTH

This tutorial demonstrates how we can read or import data with a character variable of varying length. We generally encounter this situation when we have company names or first and last names of a person in our dataset.  

#### Example I

In the following example, the variable "Name" has varying length i.e. not all observations of this variable has similar length.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9894e668-608e-4333-80db-b4cf4b7e98c4)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1a06cf68-96c1-4dcf-97d7-8376e6232e4a)  

#### Method I : Use COLON Modifier

We can use colon modifier : to tell SAS to read variable "Name" until there is a space or other delimiter. The  $30. defines the variable as a character variable having max length 30.  

```sas
data example1;
input ID Name :$30. Score;
cards;
1 DeepanshuBhalla 22
2 AttaPat 21
3 XonxiangnamSamnuelnarayan 33
;
proc print noobs;
run;
```

The colon modifier is also used to read numeric data that contains special characters such as comma For example 1,000.
Suppose you want to read a variable which holds numeric values with comma in thousands place (or thousand separator).  

```sas
data ex2;
input ID Name:$30. Score fee:$10.;
cards;
1 DeepanshuBhalla 22 1,000
2 AttaPat 21 2,000
3 XonxiangnamSamnuelnarayan 33 3,000
;
run;
```

In the above program, we have used colon modifier to load "fee" variable and used $ sign to read this variable. It is stored as a character variable.If you would not use $ sign for the same, it will return missing values. See the program below how to store it as a numeric variable.  

```sas
data ex2;
input ID Name:$30. Score fee comma5. ;
cards;
1 DeepanshuBhalla 22 1,000
2 AttaPat 21 2,000
3 XonxiangnamSamnuelnarayan 33 3,000
;
run;
```

comma5. informat removes comma and store it as a numeric variable. 5 refers to width of the input field. To read bigger number like 3,000,000, you can use comma10.  

#### Method II : Use LENGTH statement prior to INPUT Statement

In the following program, we use a length statement prior to input statement to adjust varying length of a variable. In this case, the variable Name would be read first. Use only $ instead of $30. after "Name" in INPUT statement.  

```sas
data example2;
length Name $30.;
input ID Name $ Score;
cards;
1 DeepanshuBhalla 22
2 AttaPat 21
3 XonxiangnamSamnuelnarayan 33
;
proc print noobs;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2c192540-1ca4-4a36-a953-1f2c3c14d612)  

It changes the order of variables as the variable Name would be read first.   

#### Method III : Use Ampersand (&) and Put Extra Space

We can use ampersand (&) to tell SAS to read the variable until there are two or more spaces as a delimeter. This technique is very useful when the variable contains two or more words. For example, if we have observation like "Deepanshu Bhalla" rather than "DeepanshuBhalla".  

__Note : 2 spaces before 22, 21 and 33__

```sas
data example1;
input ID Name & $30. Score;
cards;
1 DeepanshuBhalla  22
2 AttaPat  21
3 XonxiangnamSamnuelnarayan  33
;
proc print noobs;
run;
```

#### Example II : When a variable contains more than 1 word

In this case, we have a space between First Name and Last Name and we want to store both the first and last names in a single variable.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8c550218-0599-43c7-90dc-cb9ff7ab1113)  

In this case, the following methods do not work.

Colon modifier (:) does not work for a variable having multiple words  

LENGTH Statement prior to INPUT Statement does not work here.  

__Use Ampersand (&) and add ADDITIONAL space works.__

```sas
data example1;
input ID Name & $30. Score;
cards;
1 Deepanshu Bhalla  22
2 Atta Pat  21
3 Xonxiangnam Samnuelnarayan  33
;
proc print noobs;
run;
```

#### This trick works in reading data from external file.

```sas
data temp;
infile "C:\Users\Deepanshu\Desktop\file1.txt";
input ID Name & $30. Score;
proc print noobs;
run;
```

# How to Export Data

## SAS PROC EXPORT: LEARN WITH EXAMPLES

PROC EXPORT is used to export SAS datasets to external files in various different formats.  

### PROC EXPORT Syntax

Below is the syntax for PROC EXPORT:  

```sas
proc export data=sas-dataset-name
  outfile='/path/to/output/filename.csv'
  dbms=csv
  replace;
run;
```

__Explanation of PROC EXPORT Syntax__ 

data=sas-dataset-name: Name of SAS dataset you want to export.  

outfile: File location where you want to save file.  

dbms: File format to use for exported file.  

replace: Replaces the exported file if it already exists. It is optional argument.  


You can use the following DBMS options to export data to different file formats:

Specify dbms=XLSX to export data as an Excel file.  

Specify dbms=CSV to export data as a CSV file.  

Specify dbms=TAB to export data as a Text file.  

Specify dbms=SAV to export data as a SPSS file.  

Specify dbms=DTA to export data as a Stata file.  

Specify dbms=ACCESSCS to export data as a MS Access file.  

## How to export SAS Data to Excel File

The following code shows how to use PROC EXPORT to export the SAS dataset sashelp.class to an Excel file named class.xlsx located at '/home/deepanshu88us0/Files/'. It specifies the file format as XLSX.  

```sas
proc export data=sashelp.class
  outfile='/home/deepanshu88us0/Files/class.xlsx'
  dbms=xlsx
  replace;
  sheet="Students";
run;
```
![image](https://github.com/Deepak2k20/SAS/assets/65231118/59750ecc-e5d1-495a-83ac-5855d92e4c17)  

In the sheet argument, we specified the name of the sheet within the Excel file as "Students". It is visible in the image above.  

## How to export SAS Data to CSV File

Here we are exporting the SAS dataset sashelp.class to a CSV file named class.csv.  

```sas
proc export data=sashelp.class
  outfile='/home/deepanshu88us0/Files/class.csv'
  dbms=csv
  replace;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/15339fdf-d842-472d-8f9b-c6f1d8f5a66f)  

## How to export SAS Data to Text File

In the code below, we are exporting the SAS dataset sashelp.class to a Tab Delimited file named class.txt.  

```sas
proc export data=sashelp.class
  outfile='/home/deepanshu88us0/Files/class.txt'
  dbms=tab
  replace;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c2f55149-91fc-49d2-8fac-0875922695c9)  

To exclude headers in the exported file, we can use the argument PUTNAMES=NO in PROC EXPORT.  

```sas
proc export data=sashelp.class
  outfile='/home/deepanshu88us0/Files/class.txt'
  dbms=tab
  replace;
  putnames=no;  
run;
```

## How to export SAS Data to SPSS File

To export a SAS dataset to a SPSS file, we need to specify the SAV file format, which is the file format used by SPSS software.  

```sas
proc export data=sashelp.class
  outfile='/home/deepanshu88us0/Files/class.sav'
  dbms=sav
  replace;
run;
```

## HOW TO EXPORT SAS DATA TO CSV WITH EXAMPLES

In this article, we will demonstrate how to export data from SAS to CSV file, along with examples.  

PROC EXPORT is used to export data from SAS to a CSV (Comma-Separated Values) file. PROC EXPORT makes exporting data simple and provides various options that give you flexibility and control over how your SAS data is exported.  

### Syntax of PROC EXPORT for CSV Files

When exporting data to CSV files using PROC EXPORT, the following syntax can be used:  

```sas
proc export data=sas-dataset-name
  outfile='/path/to/output/filename.csv'
  dbms=csv
  replace;
run;
```

__Explanation of PROC EXPORT Syntax__

data=sas-dataset-name: SAS dataset you want to export.  

outfile: Specifies the desired location and name of the output CSV file.  

dbms=csv: Indicates that the destination file format should be CSV.  

replace: Replaces the CSV file if it already exists. It is optional argument.  

### Sample SAS Dataset

Let's create a sample SAS dataset that will be used to export it to CSV File.  

```sas
data cars;
  input Make$ Model$ MPG;
  datalines;
Toyota Innova 23
Honda Civic 36
Ford Mustang 25
;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/591214c2-4ade-4eee-8d9e-9dbf5458a502)  

```sas
proc export data=cars
  outfile='/home/deepanshu88us0/Files/cars.csv'
  dbms=csv
  replace;
run;
```

Make sure to change the location of the output CSV file in outfile= option in the above code.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/7e73dcbe-5d5a-434f-bb13-0296c6cc61f9)  

## How to change Delimiter of CSV File

To change the default separator when using PROC EXPORT, you can use the DELIMITER= statement. Alternatively, you can use the DLM= statement, which is an acronym of DELIMITER=. The delimiter should be enclosed within quotation marks. In the code below, we are using semicolon (;) as a delimiter.  

```sas
proc export data=cars
  outfile='/home/deepanshu88us0/Files/cars.csv'
  dbms=csv
  replace;
  delimiter=";";
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/df11c113-1a59-486d-812f-2fd30be5c0ea)  

## How to Exclude Header from CSV File

When exporting data to a CSV file using PROC EXPORT, you can use the PUTNAMES= option to control the inclusion of column headers (variable names). By default, PUTNAMES=YES includes the header in the CSV file. However, if you want to exclude the column names, you can use PUTNAMES=NO.  

```sas
proc export data=cars
  outfile='/home/deepanshu88us0/Files/cars.csv'
  dbms=csv
  replace;
  putnames=NO;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/0e1c64c8-fbd1-48eb-81c8-7d3101587e19)  

## How to Export a Subset of Data to a CSV File

We are using cars dataset from SASHELP library. The WHERE= option is used to filter data. Here we are selecting only Audi cars.  

```sas
proc export data=sashelp.cars (where=(Make='Audi'))
     outfile='/home/deepanshu88us0/Files/cars.csv'
     dbms=csv 
     replace;
run;
```

## How to Include Variable Labels in a CSV File

By default, when using PROC EXPORT, the exported CSV file includes the variable names rather than their labels. If you prefer to export the variable labels instead, you can use the LABEL option. This option enables you to create a CSV file where the variable labels are used instead of the variable names.  

```sas
proc export data=sashelp.cars
  outfile='/home/deepanshu88us0/Files/cars.csv'
  dbms=csv
  label
  replace;
run;
```

If you observe the CSV file, the variable label "Engine Size (L)" was included instead of "EngineSize" in the output CSV file.  

## HOW TO EXPORT SAS DATA TO EXCEL (WITH EXAMPLES)

In this article, we will show how to export data from SAS to Excel file, along with examples.  

PROC EXPORT is used to export data from SAS to an Excel file.  

### Syntax of PROC EXPORT for Excel Files

The following code exports data from SAS to Excel using PROC EXPORT.  

```sas
proc export data=sas-dataset-name
  outfile='/path/to/output/filename.xlsx'
  dbms=xlsx
  replace;
  sheet="My Sheet";  
run;
```

__Explanation of PROC EXPORT Syntax__

data=sas-dataset-name: SAS dataset you want to export.  

outfile: Specifies the desired location and name of the output Excel file.  

dbms=xlsx: Indicates that the destination file format is XLSX.  

replace: Replaces the Excel file if it already exists. It is optional argument.  

sheet: Sheet name to be used in the exported Excel file. It is optional argument.  

### Sample SAS Dataset

Let's create a sample SAS dataset that will be used to export it to Excel File.  

```sas
data data1;
  input Company$ Origin$ Sales;
  datalines;
Unilever UK 453
Tesla USA 636
Amazon USA 829
;
run;
```


![image](https://github.com/Deepak2k20/SAS/assets/65231118/b8c24860-c2ad-49eb-b4fa-3e65a9c1a610)  

The following code exports the dataset data1 to an Excel file named "companies.xlsx" with the sheet name "data1".  

```sas
proc export data=data1
  outfile='/home/deepanshu88us0/Files/companies.xlsx'
  dbms=xlsx
  replace;
  sheet="data1";
run;
```


![image](https://github.com/Deepak2k20/SAS/assets/65231118/1a411d25-5e19-49a5-aee0-328011574beb)  

## How to Export Multiple SAS Datasets to Excel

The following code exports two datasets to two different sheets in the same excel file. We are using PROC EXPORT twice and specifing both the datasets and sheet names in the data= and sheet= options.  

```sas
data data1;
  input Company$ Origin$ Sales;
  datalines;
Unilever UK 453
Tesla USA 636
Amazon USA 829
;
run;

data data2;
  input Company$ Industry$;
  datalines;
Unilever FMCG
Tesla Auto
Amazon Tech
;
run;

proc export data=data1
  outfile='/home/deepanshu88us0/Files/companies.xlsx'
  dbms=xlsx
  replace;
  sheet="data1";
run;

proc export data=data2
  outfile='/home/deepanshu88us0/Files/companies.xlsx'
  dbms=xlsx
  replace;
  sheet="data2";
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/078ccff3-a860-4652-a6ee-c9ac5168213d)   

## SAS Macro to Export Multiple SAS Datasets to an Excel File  

The following macro exports multiple SAS datasets to an Excel file. Each dataset is exported to a separate sheet in the Excel file, with the sheet name being the same as the dataset name.  

```sas
%macro export_to_excel(filepath, data_names);
    %let data_count = %sysfunc(countw(&data_names));
    %do i = 1 %to &data_count;
        %let data_name = %scan(&data_names, &i);
        proc export data=&&data_name
            outfile= &filepath.
            dbms=xlsx
            replace;
            sheet="&&data_name";
        run;
    %end;
%mend export_to_excel;

%export_to_excel("/home/deepanshu88us0/Files/companyData.xlsx", data1 data2);
```

filepath The full path to the output Excel file.  

data_names A space-separated list of dataset names to export.  

# Data Analysis with SAS

## SAS : CREATING OR MODIFYING A VARIABLE

This tutorial demonstrates how to create or modify a variable. It is a common data requirement to create a new variable based on the existing variable. For example, you have existing prices and you need to adjust inflation rate and create new price structure. To achieve it, you need to create a new variable for new prices. Sometimes, you may be asked not to create new variables for changes but adjust the logic in the existing variables.  

### Let's create a sample dataset

In the code below, we are creating a dataset named Example1 which is stored on WORK (temporary) library. In this dataset, there would be a variable called OldPrice which contains a value 10. The RUN statement is used to close the dataset program. Press F3 or click on submit button to make the code run.  

```sas
DATA Example1;
OldPrice=10;
RUN;
```

### I. Creating a numeric variable

You create variables using the form:  variable = expression;  

Suppose you are asked to create a new variable NewPrice, in the existing SAS data set Example1. Both variables are numeric. The variable NewPrice is twice of OldPrice.  

```sas
DATA Example1;
SET Example1;
NewPrice=2*OldPrice;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8fbd34c3-e142-4f20-84a2-bb2b3c129b27)  

If you are asked to store a new variable NewPrice on a new dataset, you can create it using DATA statement.  

```sas
DATA Readin;
SET Example1;
NewPrice=2*OldPrice;
RUN;
```

In this case, the dataset READIN was created.  

### II. Creating a character variable

In the same dataset Example1, let's create a character variable say Type. The character value for set is set 'Good'.  

The quote marks needs to be entered around the character variable.  

```sas
DATA Example1;
SET Example1;
Type = 'Good';
RUN;
```

Since Type is a character variable, it should in quotes. It can be either single or double quotes.  

### III. Creating or Modifying a variable

Suppose the value of OldPrice is increased by 5 units and you need to calculate the relative change in price. In this case, we are modifying the existing variable OldPrice so we will add 5 to OldPrice. later we calculate the percentage change between old and new price.  

```sas
DATA Readin;
SET Example1;
OldPrice=5 + OldPrice;
NewPrice=OldPrice*2;
Change= ((NewPrice-OldPrice)/ OldPrice);
Format Change Percent10.0;
RUN;
```

The FORMAT statement is used to display the change value in percentage format. In this case, we are creating a new dataset as well.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/948d3826-3c93-4db4-b3dd-358d6bb52104)  

__Important Note__

It's a good practice to create a new dataset when you modify the existing variable. It is because input data should not be altered or changed to have a backup of the dataset. In many times, a small mistake of programmer lead to data loss which can have a high-risk consequence.  

## DROPPING VARIABLES FROM A DATA SET IN SAS

This post explains how to drop variables from a dataset in SAS. It includes various tricks to delete variables from data.In SAS, there are two ways to handle dropping variables :  

DROP = data set option  

DROP statement

Let's start with creating a data set :  

```sas
DATA outdata; 
   INPUT age gender $ dept obs1 obs2 obs3; 
   DATALINES; 
1 F 3 17 6 24
1 M 1 19 25 7
3 M 4 24 10 20
3 F 2 19 23 8
2 F 1 14 23 12
2 M 5 1 23 9
3 M 1 8 21 7
1 F 1 7 7 14
3 F 2 2 1 22
1 M 5 20 5 2
3 M 4 21 8 18
1 M 4 7 9 25
2 F 5 10 17 20
3 F 4 21 25 7
3 F 3 9 9 5
3 M 3 7 21 25
2 F 1 1 22 13
2 F 5 20 22 5
;
proc print;
run;
```

The main differences between the two are as follows :  

### I.  Scenario : Create a new variable based on existing data and then drops the irrelevant variables

By using the DROP statement, we can command SAS to drop variables only at completion of the DATA step.  

```sas
data readin;
set outdata;
totalsum = sum(obs1,obs2,obs3);
drop obs1 obs2 obs3;
run;
```

In the above example, we simply ask SAS sum up all the values in variables obs1,obs2 and obs3 to produce a new variable totalsum and then drop the old variables obs1,obs2 and obs3.  

__Consequence of using DROP = Option__

```sas
data readin;
set outdata (drop = obs1 obs2 obs3);
totalsum = sum(obs1,obs2,obs3);
run;
```

The variables obs1,obs2 and obs3 are not available for use after data set outdata has been copied into the new data set readin . Hence totalsum would contain missing values only.  

### II. DROP statement can be used anywhere in DATA steps whereas DROP = option must follow the SET statement.

DROP statement

```sas
data readin;
set outdata;
if gender = 'F';
drop age;
run;
```

OR

```sas
data readin;
set outdata;
drop age;
if gender = 'F';
run;
```

DROP = option  

```sas
data readin;
set outdata (drop = age);
if  gender = 'F';
run;
```

### III. Scenario : Dropping variables while printing

DROP statement can be used in DATA steps only whereas DROP = option can be used in DATA steps and PROC steps (for printing)  

```sas
proc print data = outdata (drop = age);
where gender = 'F';
run;
```

## SAS: HOW TO RENAME VARIABLES

This tutorial explains how to rename variables in SAS using the RENAME option, along with examples.  

The syntax of RENAME option is as follows :  

```sas
RENAME=(variable1=new_variable1 variable2=new_variable2 ...)
```

### Rename One Variable in SAS

The following code renames the variable "petallength" to "petal_length" in the dataset "sashelp.iris" and create a new dataset called "mydata" with the renamed variable.  

```sas
data mydata (rename=(petallength = petal_length));
set sashelp.iris;
run;
```

To check if a variable has been renamed correctly, we can use PROC CONTENTS to see the variable names of a dataset.  

```sas
proc contents data=sashelp.iris SHORT;
proc contents data=mydata SHORT;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/41d6541a-6a3a-4c3e-a601-500a12672f0f)  

### When should the RENAME option be used - DATA or SET Statement?

The RENAME option can be used with either the DATA statement or the SET statement, depending on your specific needs.  

RENAME option in the DATA statement: When you use the RENAME option in the DATA statement, you are renaming variables in the output dataset.  

RENAME option in the SET statement: When you use the RENAME option in the SET statement, you are renaming variables while reading data from an input dataset.  


### Incorrect Code

The following code returns missing values for a new variable "newvar" because "petal_length" was not renamed before creating the new variable "newvar". Hence rename= option should be used in the SET statement instead of DATA statement here.  

```sas
data mydata (rename=(petallength = petal_length));
set sashelp.iris;
newvar = petal_length * 10;
run;
```

### Correct Code

```sas
data mydata;
set sashelp.iris (rename=(petallength = petal_length));
newvar = petal_length * 10;
run;
```

### Rename Multiple Variables in SAS

The following code renames the variables "petallength" to "petal_length" and "sepallength" to "sepal_length" while reading the data from the "sashelp.iris" dataset.  

```sas
data mydata;
set sashelp.iris (rename=(petallength = petal_length sepallength=sepal_length));
run;

proc contents data=sashelp.iris SHORT;
proc contents data=mydata SHORT;
```

### Rename All Variables in SAS

The following code renames all variables in the "sashelp.iris" dataset by adding the suffix "_1" to their original names.  

```sas
proc sql noprint;
select cats(name,"=",name,"_1") 
into :rename_vars separated by " "
from dictionary.columns
where libname="SASHELP" 
and memname="IRIS";
quit; 

%PUT &rename_vars.;

data mydata;
set sashelp.iris (rename=(&rename_vars.));
run;
```

The above code uses the table dictionary.columns which contains information about the column names of all datasets in the current SAS session.  

By using the WHERE statement, we filtered this table and selected only column names in the "sashelp.iris" dataset and stored them in the macro variable "rename_vars"  

The %PUT statement is used to display the contents of the macro variable "rename_vars" in the log. It helps you to check what the macro variable contains.  

In the subsequent DATA step, the SET statement reads data from the "sashelp.iris" dataset and applies the variable rename assignments specified in the macro variable "rename_vars"  

The resulting dataset "mydata" will contain the renamed variables with suffix "_1".  

### Rename Variables based on a Pattern

The following code renames only those variables which contain "Length" in their names using CONTAINS operator.

```sas
proc sql noprint;
select cats(name,"=",name,"_1") 
into :rename_vars separated by " "
from dictionary.columns
where libname="SASHELP" 
and memname="IRIS"
and name contains 'Length';
quit; 

%PUT &rename_vars.;

data mydata;
set sashelp.iris (rename=(&rename_vars.));
run;
```

## SAS : IF-THEN-ELSE STATEMENTS

This tutorial explains how to use IF THEN ELSE statements in SAS, with examples.  

Task 1 : Suppose you are asked to exclude some of the observations in a SAS data set from an analysis that you are generating. For example, you want to exclude all IDs whose values are greater than 100.  

To accomplish this task, we can use IF, IF-THEN DELETE.  

### Comparison Operators

![image](https://github.com/Deepak2k20/SAS/assets/65231118/27a532bd-863c-42cd-b8e9-801b3c964aa8)  

### 1. IF statement

IF (condition is true) => It means subsetting a dataset.  

```sas
Data readin;
Input ID Q1-Q3;
cards;
85 1 2 3
90 3 4 6
95 5 5 6
100 6 6 4
105 5 5 6
110 6 6 5
;
Data readin1;
Set readin;
IF ID LE 100;
run;
```

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/cf509bd0-de89-4b26-8f6b-ebf495576dfa)  

IF ID LE 100 => This would tell SAS to retain only those IDs whose values are less than or equal to 100. In other words, you are removing IDs whose values are greater than or equal to 100.  

This can also be done using the IF-THEN DELETE statement.  

### 2. IF-THEN DELETE

IF (condition is true) THEN (delete the selected observations);  

```sas
Data readin;
Input ID Q1-Q3;
cards;
85 1 2 3
90 3 4 6
95 5 5 6
100 6 6 4
105 5 5 6
110 6 6 5
;
Data readin1;
Set readin;
IF ID GT 100 THEN DELETE;
run;
```

IF ID GT 100 THEN DELETE => This would tell SAS to remove all the IDs whose values are greater than 100.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/96c0e87f-cb35-47e3-a86f-575479f720a1)  

Task 2: Suppose you want to set a tag on all the IDs. The condition is :  

If value of ID is less than or equal to 100 set "Old" tag otherwise set "New" tag.

IF (condition is true) THEN (perform this action);  

ELSE (perform the action that is set when condition is false);  

```sas
Data readin;
Input ID Q1-Q3;
cards;
85 1 2 3
90 3 4 6
95 5 5 6
100 6 6 4
105 5 5 6
110 6 6 5
;
Data readin1;
Set readin;
IF ID LE 100 THEN TAG ="Old";
ELSE TAG ="New";
run;
```

___Syntax of IF-THEN-ELSE :___

![image](https://github.com/Deepak2k20/SAS/assets/65231118/34272ffd-8a55-4e99-8990-5b3ec139f110)  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/89e54ee7-014a-427f-9d38-694128f6dfb2)  

Task 3: Suppose you are asked to update the TAG column.  

The conditions for tagging are as follows :  

If value of ID is less than 75 then TAG = "Old"  

If value of ID is greater than or equal to 75 and less than 100 then TAG = "New"  

If value of ID is greater than or equal to 100 then TAG = "Unchecked"

IF (condition is true) THEN (perform this action);  

ELSE IF (perform the action when second condition is true);  

ELSE IF (perform the action when third condition is true);  

```sas
Data readin;
Input ID Q1-Q3;
cards;
70 1 2 3
45 1 2 3
85 1 2 3
25 1 2 3
90 3 4 6
95 5 5 6
100 6 6 4
105 5 5 6
110 6 6 5
;
Data readin1;
Set readin;
length TAG $20;
IF ID < 75 THEN TAG ="Old";
ELSE IF 75 <= ID < 100 THEN TAG = "New"; 
ELSE IF ID >= 100 THEN TAG ="Unchecked";
run; 
```

__Syntax of IF-THEN-ELSE IF :__

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a0e7259b-368d-4b58-b042-5364fc731629)  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/dce5788c-1ea6-4afa-bc75-75aefc1a8b54)  

### LOGICAL OPERATORS

![image](https://github.com/Deepak2k20/SAS/assets/65231118/fede4fa8-5e28-4474-80e0-dfa1da9647e3)  

Task 4: Suppose you want to generate an analysis for Q1 including only responses that are valid (non-missing) and less than 3.  

```sas
Data readin;
Input ID Q1-Q3;
cards;
85 1 2 3
90 . 4 6
95 2 5 6
100 6 6 4
105 . 5 6
110 6 6 5
;
Data readin1;
Set readin;
IF (Q1 LT 3) AND (Q1 NE .);
run;
```

IF (Q1 LT 3) AND (Q1 NE .) => Since missing values are smaller than any other value, we need to give SAS an additional command to separate out missing values.   

The output is shown below:  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/4a41cf21-aafb-4e11-b010-d301b3e5f7d6)  

__Selecting Multiple Observations :__

Suppose you want to set tag "Incorrect" to the specified IDs 1,5,45,76  

For this case, the logical statement would look like any one of the following statements. It can be written in three ways shown below.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/63853d1a-db99-4037-93be-f0b46c378e66)  

__IN Operator__

IN operator is used to select multiple values of a variable. It is an awesome alternative to OR operator.  

## SAS : WHERE STATEMENT AND DATASET OPTIONS

The WHERE statement is an alternative to IF statement when it comes to subsetting a data set.  

__Basic Data Subsetting__

Syntax of WHERE statement :  
```sas
WHERE (condition is true) => It means subsetting a dataset.  
```
__Comparison Operators__

![image](https://github.com/Deepak2k20/SAS/assets/65231118/19faec4e-06d5-4767-8d42-fe0840fa2aa4)  

Task1 : Suppose you want to select only section A students. You know the variable Section contains information for students' sections.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul A 77
Priya B 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul A 95
Sahul C 84
Lahul C 44
;
run;

data readin1;
set readin;
where Section EQ "A";
run;
```

where section EQ "A" => This would tell SAS to select only section A values.  

You can also write where section = "A". This statement serves the same purpose.  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/22c0abab-5ce3-4c3b-b7e8-7819b78a3d67)  

### LOGICAL OPERATORS

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b50cd306-0040-4c54-81d6-180e27d763f2)  

Task2 : Suppose you want to select section A and B students. You know the variable Section contains information for students' sections.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul A 77
Priya B 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul A 95
Sahul C 84
Lahul C 44
;
run;

data readin1;
set readin;
where Section IN ("A" "B");
run;
```

where section IN ("A" "B") => This would tell SAS to select section A and B values.  

However, you can also write ...  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/21552f6d-ad08-4a26-a91e-1f7649edc00d)  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ac7633eb-9c2f-4e36-95a0-e78c05c6dd4e)  

### BETWEEN-AND Operator : Between Two Numbers

Task 3 : Suppose you want to select scores whose values are greater than or equal to 50 and less than or equal to 75.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul A 77
Priya B 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul A 95
Sahul C 84
Lahul C 44
;
run;

data readin1;
set readin;
where Score between 50 and 75;
run;
```

where Score between 50 and 75 => This would tell SAS to select values through 50 and 75 (not 51 to 74).  

This can also be written like :  

where Score GE 50 and Score LE 75;  

### IS MISSING Operator : Selecting Missing Values

Task 4 : Suppose you want to select only those observations in which students did not fill their section information.  

The dataset is modified to include missing values in SECTION variable.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul . 77
Priya . 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul . 95
Sahul C 84
Lahul C 44
;
run;

data readin1;
set readin;
where Section is missing;
run;
```

Where section is missing => This would tell SAS to select missing values for variable SECTION.  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2ae3eaf4-0561-4593-be1a-8794ddcbced7)  

### IS NOT MISSING Operator : Selecting Non-Missing Values

Task 5 : Suppose you want to select only those observations in which students filled their section information.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul . 77
Priya . 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul . 95
Sahul C 84
Lahul C 44
;
run;

data readin1;
set readin;
where section is not missing;
run;
```

Where section is not missing => This would tell SAS to select non-missing values.  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/39aef8d9-3fd0-4064-818b-19ae860fd895)  

The NOT operator can be used within WHERE statement in many ways :

1. where section is missing and score is not missing;  

2. where not (score in (34,44,84));  

3. where not (Score between 50 and 75);  

4. where NOT(Section EQ "A");

### CONTAINS Operator : Searching specific character

Task 6 : Suppose you want to select only those observations in which students' name contain 'hul'.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul . 77
Priya . 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul . 95
Sahul C 84
Lahul C 44
;
run;

data readin1;
set readin;
where name contains 'hul';
run;
```

where name contains 'hul' => This would tell SAS to select observations having the values Rahul, Sahul and Lahul for the variable NAME.  

Note : The CONTAINS operator is case sensitive.  

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d3473afb-bf70-4128-a8c3-962f1184542f)  

Since the CONTAINS operator is case sensitive, where Name contains 'HUL' would not select any observation. The log for this statement is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/40e66d20-24b6-493d-b399-1e68054832db)  

### LIKE Operator : Pattern Matching

The LIKE operator selects observations by comparing the values of a character variable to a specified pattern. It is case sensitive.  

Task7 : To select all students with a name that starts with the letter S.  

There are two special characters available for specifying a pattern:  
  
1. percent sign (%) - Wildcard Character  
 
2. underscore ( _ ) - Fill in the blanks

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul . 77
Priya . 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul . 95
Sahul C 84
Lahul C 44
Pahulk A 81
;
run;

data readin1;
set readin;
where name like 'S%';
run;
```

where name like 'S%';

OR

where name like 'Sa%';

In this dataset, the above statements would produce the same result :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/0f3f03e8-fe51-47a0-b5ee-6f25eb13948d)  

Examples :

1. where name like '_am';  

You can also write this statement like .....  

where name like '%am';  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/564a6fc3-c49c-40e3-8bdd-705ee375bc42)  

2.  where name like '_ahu_';  

This would not select PAHULK from the variable NAME.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5e998ba9-9869-4dab-9a43-74763f8fe23a)  

3. where name like '_ahu__';  

This would select PAHULK as double underscore (__) is stated.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/93ededce-73bd-44ba-8e10-617ae8ab2c99)  

### Sounds-like Operator : Selecting sound like characters

Task8 : To select names that sound like 'Ram'.  

```sas
data readin;
input name $ Section $ Score;
cards;
Tom  A 84
Raj  A 80
Ram  B 71
Atul . 77
Priya . 45
Sandy A 67
Sam  A 57
David B 39
Wolf B 34
Rahul . 95
Sahul C 84
Lahul C 44
Pahulk A 81
Rama A 84
;
run;

data readin1;
set readin;
where name = *'Ram';
run;
```

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/e5554b05-decd-4fcc-a14d-57ec63fa4bd6)  

### WHERE = Data Set Option

1. In the example shown below, the WHERE= data set option is used to select only section A data.

```sas
data readin1 (where = (section ='A'));
set readin;
run;
```

2. The following example shows how to use WHERE= data set option in procedures 

```sas
proc print data=readin (where=(section='A'));
run;
```

In this case, you can also use WHERE statement....

```sas
proc print data=readin;
where section='A';
run;
```

## SAS : WHERE VS. IF STATEMENTS

The WHERE statement is an alternative to IF statement when it comes to subsetting a dataset. It is important to know the difference between these two statements.  

### Difference between WHERE and IF statements  

WHERE statement wins against IF statement in the following cases :  

The WHERE statement can be used in procedures to subset data while IF statement cannot be used in procedures.  

Look at the log of WHERE and IF statements shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c9dc0551-8995-4fdb-89c0-a82b6e494c5c)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5243c40c-4b52-45c6-845f-1d519852ab76)  

2. WHERE can be used as a data set option while IF cannot be used as a data set option.

![image](https://github.com/Deepak2k20/SAS/assets/65231118/7255256b-fb71-4eff-beb4-b41516949aa8)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ec098d48-56ec-42d4-9fd3-0806b08e8415)  

3. The WHERE statement is more efficient than IF statement. It tells SAS not to read all observations from the data set.  

Look at the LOG (shown below) after using WHERE statement, you only see a count of the number of observations that meet the criteria in the WHERE statement.  

Only 6 observations were read from the dataset READIN. In actual, the dataset READIN contains 14 observations  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1fdfac32-2a6e-4275-8229-99ccd9ecda9e)  

All 14 observations are read, and the 6 that meet the IF criteria are placed in the new data set.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5e609f35-5901-4a50-926d-ccbb2119eda8)  

NOTE: Both statements produced the same result.

The where clause sends only those records that meet condition to PDV, the IF statement sends all the records to PDV and removes the records that do not meet condition before they get sent to the output buffer.  
4. The WHERE statement can be used to search for all similar character values that sound alike while IF statement cannot be used.  

For example, you want to filter out all the names that sound alike 'Sam'.  

The IF statement outperforms the WHERE statement in the following scenarios:  

1. When reading data using INPUT statement.  

IF Statement  

IF Statement can be used when specifying an INPUT statement.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/bc4c64e7-9b08-4a83-8252-4a37fa29c7c3)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/89c573f6-85fc-4557-88ab-c77cf017e244)  

WHERE Statement  

WHERE statement can not be used when specifying an input statement.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/caab363d-225c-4fb3-96d8-2f8bab51b97b)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/32440658-8f37-426b-8888-8fb0d0031694)  

2. When it is required to execute multiple conditional statements

Suppose, you have data for college students’ mathematics scores. You want to rate them on the basis of their scores.

Conditions :  

1. If a score is less than 40, create a new variable named “Rating” and give “Poor” rating to these students.  

2. If a score is greater than or equal to 40 but less than 75, give “Average” rating to these students.  

3. If a score is greater than or equal to 75 but less than or equal to 100, give “Excellent” rating to these students.  

This can be easily done using IF-THEN-ELSE IF statements. However, WHERE statement requires variables to exist in the data set.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/89daa316-21ac-4823-a855-3c91007c4722)  

3. When it is required to use newly created variables in data set.  

IF statement can be applied on a newly created variable whereas WHERE statement cannot be applied on a newly created variable. In the below example, IF statement doesn't require variables to exist in the READIN data set while WHERE statement requires variable to exist in the data set.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/84ef386c-953a-4e81-a34c-dbf8bff856db)  

4. When to Use _N_, FIRST., LAST. Variables  

WHERE statement cannot be applied on automatic variables such as _N_, First., Last. Variables. While IF statement can be applied on automatic variables.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/90bfea7a-007c-4473-b454-fd2e377f356d)  

Difference : WHERE and IF when merging data sets  

WHERE statement applies the subset condition before merging the data sets, Whereas, IF statement applies the subset condition after merging the data sets.  

Create 2 Sample Datasets for Merging  

```sas
data ex1;
input ID Score;
cards;
1 25
2 28
3 35
4 45
;
run;
data ex2;
input ID Score;
cards;
1 95
2 97
;
run;
```


Merge with WHERE Condition  

```sas
data comb;
merge ex1 ex2;
by ID;
where score <= 30;
run;
```
It returns 2 observations. WHERE condition applied before merging. It applies separately on each of the 2 data sets before merging.

Merge with IF Condition  

```sas
data comb;
merge ex1 ex2;
by ID;
if score <= 30;
run;
```

It returns 0 observation as IF condition applied after merging. Since there is no observation in which value of score is less than or equal to 30, it returns zero observation.  

## HOW TO FILTER DATA IN SAS

This tutorial explains multiple ways to filter data in SAS, along with examples.  

Sample Dataset  

Let's create a sample SAS dataset for demonstration purposes. The following code creates a sample SAS dataset which will contain 5 observations and 4 variables.  

```sas
/* Sample SAS dataset */
data mydata;
  input ID Age Gender $ Score;
  datalines;
1 24 Male 85
2 30 Female 90
3 22 Male 78
4 28 Female 95
5 31 Male 80
;
run;
```

### IF Statement: Filtering Data in SAS  

In SAS, the IF statement is used to filter data. The IF statement is used within the data step to conditionally execute statements based on a specified condition. In the example below, we want dataset that will only contain observations with Age greater than or equal to 25.

```sas
data filtered_data;
  set mydata;
  if Age >= 25;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1c62f747-292e-4e69-a97e-421632a6881d)  

Look at the SAS log after filtering.  

```sas
NOTE: There were 5 observations read from the data set WORK.MYDATA.
NOTE: The data set WORK.FILTERED_DATA has 3 observations and 4 variables.
```

The OUTPUT statement is used when you need to filter data into multiple datasets based on certain criteria. The following SAS code is creating two new datasets, age1 and age2, by filtering the original dataset "mydata" based on the condition Age >= 25. Observations that satisfy the condition will be output to the age1 dataset, while those that do not meet the condition will be output to the age2 dataset.

```sas
data age1 age2;
  set mydata;
  if Age >= 25 then output age1;
  else output age2;
run;
```

Result : The data set WORK.AGE1 has 3 observations and 4 variables. The data set WORK.AGE2 has 2 observations and 4 variables.

### How to Use Multiple IF statement  

In SAS, you can use multiple IF statements using ELSE IF statement to implement more complex logic within a data step. The following SAS code is creating three new datasets, namely male, female, and invalid, based on the values of the variable Gender in the existing dataset mydata.  

```sas
data male female invalid;
  set mydata;
  if Gender = "Male" then output male;
  else if Gender = "Female" then output female;
  else output invalid;
run;
```

### WHERE Statement: Filtering Data in SAS  

In SAS, the WHERE statement can also be used to filter data. The WHERE statement can be used within both the data step and SAS Procedures. In the example below, we are using the condition of Age greater than or equal to 25 and we want filtered dataset in a new dataset named "filtered_data".

```sas
data filtered_data;
  set mydata;
  where Age >= 25;
run;
```

You can also use the WHERE statement in the SET statement.

```sas
data filtered_data;
  set mydata (where=(Age >= 25));
run;
```

### Difference between IF and WHERE Statement

Here are some of the key differences between the IF and WHERE Statement in SAS.

Efficiency: The WHERE statement is more efficient than the IF statement as it tells SAS to read only those observations of the input dataset that meets criteria. Whereas, the IF statement reads all observations of the input dataset.  

Filtering based on New Variables: If you create a new variable before filtering in the data step, you can't use the WHERE statement to filter based on this new variable. Whereas, the IF statement can filter data based on new variables.  

Split Data into Multiple Datasets: The IF statement along with OUTPUT statement can be used to filter and output data into multiple datasets. Whereas, the WHERE statement does not allow to filter and send data to multiple datasets.  

The WHERE statement can be used in SAS procedures (PROC) to filter data while the IF statement cannot be used in procedures.  

### How to Use Multiple Conditions  

Please refer to the table below showing how to use logical operators in SAS.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b91a5d5d-eb66-4777-9dd3-cdd29ec3a9cf)  

The following code filters the "mydata" dataset based on two conditions: Gender = "Female" or Age > 29.

```sas
data filtered_data;
  set mydata;
  where Gender = "Female" OR Age > 29;
run;
```

You can also write the above condition using "|" instead of OR operator like this :
where Gender = "Female" | Age > 29;  

In the example below, the condition NOT (Gender = 'Female') means it will select all rows where the Gender is NOT equal to "Female".  

```sas
data filtered_data;
  set mydata;
  where NOT (Gender = "Female");
run;
```

### Text Filters in SAS

Text filters are a type of filter that can be used to find text that matches a specific pattern. This can be useful for selecting rows having specific words, phrases in a character variable.

```sas
data sample_data;
   input name $;
   datalines; 
Sam
Saina
Dave
Riana
DIANA
Hiana
David
davia
;
run;
```

### Filter: Contains Some Text

The CONTAINS operator checks if the specified substring is present anywhere within the character variable. The following code creates a dataset that will only contain observations with names that contain the substring 'IANA' in any case (upper or lower).

```sas
data filtered_data;
  set sample_data;
  where upcase(name) contains 'IANA';
run;  
```

The filtered dataset will look like this:

```sas
name
--------
Riana
DIANA
Hiana
```

### Filter: Does Not Contain Some Text

The following SAS program creates a dataset that will only contain observations that do not meet the specified condition, i.e., those where the 'name' variable does not contain the substring 'IANA' in any case.

 ```sas 
data filtered_data;
  set sample_data;
  where upcase(name) not contains 'IANA';
run; 
```

### Filter: Starts with Some Text

The following SAS program creates a dataset that will only contain observations those where the 'name' variable starts with 'D' or 'd'. The result will include all names such as 'Dave', 'David', 'DIANA', 'davia' as long as they start with 'D' or 'd'.

```sas
data filtered_data;
  set sample_data;
  where upcase(name) like 'D%';
run;
```

### Filter: Ends with Some Text  

The following SAS program creates a dataset that will only contain observations those where the 'name' variable ends with 'NA' or 'na'.

```sas
data filtered_data;
  set sample_data;
  where upcase(name) like '%NA';
run;
```

### Filter Data based on First N Characters  

The following SAS program filters data where the first two characters of the 'name' variable are 'DA' or 'da'. The SUBSTR function is used to extract the first two characters of the name variable, and the UPCASE function converts them to uppercase so that we can select both 'DA' and 'da'.

```sas
data filtered_data;
  set sample_data;
  where upcase(substr(name,1,2)) = 'DA';
run;
```

## SAS PROC PRINT: LEARN WITH EXAMPLES

This tutorial explains how to use the PROC PRINT procedure in SAS, along with examples.  

PROC PRINT is a commonly used SAS procedure that displays the contents of a dataset.    

### Sample Dataset 

Let's create a sample SAS dataset that will be used in the examples of this tutorial.   

```sas
data mydata;
input name $ height weight sex $ sale;
datalines;
John 175 70 M 1000
Emily 160 55 F 800
Michael 180 80 M 1200
Sophia 165 60 F 950
David 170 75 M 1100
Emma 155 50 F 750
;
run;
```

### Print Entire Dataset

The simplest usage of PROC PRINT is that it displays all variables in the dataset.  

```sas
proc print data=mydata;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/6b5204ae-ed11-405d-b704-b27756ef92a8)  

### Print First N Observations  

The OBS= option in PROC PRINT is used to display first N observations in the dataset. In this example, it displays first 5 observations.

```sas
proc print data=mydata(obs=5);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/87b6173e-618e-4c10-b5a7-620e0fa6ce6a)  

### Print Specific Variables  

You can specify which variables you want to display using the VAR statement.

```sas
proc print data=mydata;
var name height weight;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/77af87ca-bf5c-4097-877f-bc0ee8aae027)  

### Exclude Observation Number in the Output  

You can tell SAS not to display observation number in the output using the NOOBS option.

```sas
proc print data=mydata noobs;
var name height weight;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/bc51a88f-a642-4f66-b107-1a778a404107)  

### Conditional Printing  

You can use the WHERE statement to display only specific observations that meet a condition. The following code generates an output that displays only the observations where the 'sex' variable has a value of 'M'.

```sas
proc print data=mydata noobs;
where sex='M';
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/63069c89-2afd-4207-9f7d-d48ba02d5d2d)  

### How to Use Formats in PROC PRINT  

You can apply formats to the variables using the format statement. In the code below, format sale dollar10.1; applies a dollar format to the "sale" variable.

```sas
proc print data=mydata;
format sale dollar10.1;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c19d235f-5994-4de9-b204-fe9767e5f222)  

### How to Use Title and Footnote in PROC PRINT  

You can use the TITLE and FOOTNOTE statements to print the dataset with a title and a footer.

```sas
proc print data=mydata;
title "Students Dataset";
footnote "Sample Dataset";
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ce71a144-41c0-4796-815e-ea14710936de)  
  
### Labeling Variables in PROC PRINT  

You can use the label statement to specify labels for the variables.

```sas
proc print data=mydata label obs='Observation No.';
label name='Students Name' weight='Students Weight';
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2b3104a5-a086-4db2-9e0b-25d9b39d778d)  

### Summing Variables in PROC PRINT  

You can use the sum statement to display total at the bottom of the output.

```sas
proc print data=mydata;
sum sale;
run;
```

To sum all the numeric variables, you can use the SUM statement with keyword _numeric_. To label the grand total, use the grandtotal_label= option.

```sas
proc print data=mydata grandtotal_label='Grand Total';
sum _numeric_;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/783b6f05-420d-4874-b973-3c6c6689a6e6)  

### Print Data Grouped by Specific Variable  

The following code displays the data in groups based on the "sex" variable. It is important to sort the dataset when you are using the BY statement in PROC SORT. If data is already sorted by the variable which is used in the BY statement, you don't need to sort the dataset prior to PROC PRINT procedure.

```sas
proc sort data=mydata;
by sex;
run;

proc print data=mydata noobs;
by sex;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/757bccc5-5044-48d8-b1c7-20915e59e59f)  

### Summing Variables Grouped by Specific Variable  

The following code generates a report that displays sales data by 'sex', including a total row, a count of observations, and a dynamic title for each group. The sales values will be formatted as dollars with one decimal place.

```sas
proc sort data=mydata;
by sex;
run;

options nobyline;
proc print data=mydata noobs sumlabel='Total'
           n='Number of observations for the sex type: '
           'Number of observations in the data set: ';
sum sale;
by sex;
title 'Sales for #byval(sex)';
format sale dollar7.1;
run;
options byline;
```

When you use PROC PRINT with the NOBYLINE option, each BY group starts on a new page. The TITLE statement adds a title in the output. The #BYVAL keyword tells SAS to include the current value of the BY variable "sex" in the title.

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b3656480-5591-4a18-9523-630668ecce6c)  

### How to Style Table in PROC PRINT  

You can use the style(location)= option to modify the appearance of the output. In the code below, the header cells of the output will appear with an italic font and a black background, while the data cells will have a red background with white text.

```sas
proc print data=mydata noobs
   style(HEADER)={fontstyle=italic backgroundcolor=black foreground=white}
   style(DATA)={backgroundcolor=red foreground=white};
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/10a5bf1c-471b-4ec3-afad-0e255559e9d9)  

## SAS: HOW TO USE THE IN OPERATOR

The IN operator in SAS is used to compare a value against a list of values. It allows you to select multiple values from a SAS dataset. It is an alternative of multiple OR conditions.  

The syntax for using the IN operator in SAS is as follows:  
```sas
variable IN (value1, value2, ..., valueN)  
```
Here values of the variable will be compared against the list of values - (value1, value2, ..., valueN)  

### How to use IN Operator in DATA STEP in SAS  

The following code filters the dataset based on the values of the MAKE variable. It selects cars of these 3 brands 'Audi', 'Acura', 'BMW' and puts them into a new dataset named "newdata".

```sas
data newdata;
set sashelp.cars;
where make in('Audi', 'Acura', 'BMW');
run;
```
To check if the above code filters dataset correctly, we can use the PROC FREQ procedure to see the unique values of the column MAKE.  

```sas
proc freq data=newdata;
table make;
run;
```
![image](https://github.com/Deepak2k20/SAS/assets/65231118/c9ab0bf2-a9a6-4443-a1c6-a02bb11b967f)  

### How to use IN Operator in PROC SQL in SAS

```sas
proc sql;
select *
from sashelp.cars
where make in('Audi', 'Acura', 'BMW');
quit;
```

### How to use NOT IN Operator in SAS  

The NOT IN operator is used in SAS to filter rows based on the condition that a column does not match any of the values. The following code returns all cars that have makers not included in the list - 'Audi', 'Acura', 'BMW'.

```sas
proc sql;
select *
from sashelp.cars
where make not in('Audi', 'Acura', 'BMW');
quit;
```

## HOW DATA STEP AND PROC SQL WORKS

This tutorial explains the steps to process data in SAS.

### How Data Step Works

The processing of data is in 2 steps :

__1. Compilation Phase__

Step I : Syntax Checking

SAS scans each statement in the DATA step and check syntax errors, such as missing semicolons and invalid statements.  

Step II : Creating Input Buffer  

If you read in a raw data set such as txt or csv file, the input buffer is created. The input buffer is used to hold raw data. If you read in a SAS data set, the input buffer will not be created.  
  
Step III : Creating Program Data Vector (PDV)  

1. SAS creates a program data vector (memory on your system) containing the automatic variables _N_ and _ERROR_.

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1aecce3a-887d-4ae9-baee-c483941a3cdf)  

_N_ = 1 indicates the first observation is being processed, _N_ = 2 indicates the second observation is being processed, and so on.  

The automatic variable _ERROR_ with values of 1 or 0, if it is equal to 1 signals the data error of the currently-processed observation, such as reading the data with an incorrect data type.  

2. In addition to the two automatic variables, there is one space allocated for each of the variables in the input statement (reading data).  

3. SAS also adds a position to the program data vector for any variables that are created in the DATA step. See the program below. The newly created FinalScore variable is derived from Score.

```sas
Data temp2;
set temp;
FinalScore = Score + 25;
 Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/46f4e56a-c153-4a3b-9b77-a96b11f788a8)  

4. If the variables specified in the DROP statement, it will never be written to the output data set.  

5. At the end of the compilation phase, SAS makes the descriptor portion of the SAS data set which includes the data set name, the number of observations, and the number, names, and attributes of variables.

__2. Execution Phase__

Sequential Processing (Iterative)

The DATA step executes once for each observation in the input data set. Suppose dataset consists of 500 records, SAS will execute 500 times.  

1. At the beginning of the execution phase, SAS sets all of the data set variables in the program data vector to missing:

![image](https://github.com/Deepak2k20/SAS/assets/65231118/dbf51ea5-6f39-445a-8aff-6c32a314fafe)  

Variables that you specify in a RETAIN statement are not reset to missing values.  

2. The SET statement reads the first observation from the input data set and writes the values to the program data vector.

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f31c4e9e-d019-4271-97af-59580f780e06)  

3. Compute the first value for the derived variable, FinalScore.

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b0bbdcad-4fe8-4d81-bf8d-9ba3bfeef6f0)  

4. At the end of the first iteration of the DATA step, the values in the program data vector are written to the output data set temp2 as the first observation.  

Loop until all of the observations are read  

The value of the automatic variable _N_ is increased to 2. The values from the second observation are written to the program data vector. Repeat above Steps 2, 3 and 4. It continues until all of the observations are read.  

### How PROC SQL Works

PROC SQL is a simultaneous process for all the observations.  

Step I : Syntax Checking  

SAS scans each statement in the SQL procedure and check syntax errors, such as missing semicolons and invalid statements.  

Step II : SQL Optimizer  

SQL optimizer scans the query inside the statement. The SQL Optimizer decides how the SQL query should be executed in order to minimize run time. The Optimizer examines submitted SQL code and characteristics of the SAS system and then creates efficient executable statements for the submitted query. The created code can be quite complicated and often involves the creating, sorting and merging of many temporary files as well as the trimming of variables and observation at times that will minimize run time.  

Step III : Load into Data Engine  

Any tables in the FROM statement are loaded into the data engine where they can then be accessed in memory.  

Step IV : Code and Calculations are executed  

Step V : Final Table is created in memory  
 
Step VI : Final Table sent to the output table described in the CREATE TABLE statement.  

__Main Distinction : Data Step vs. Proc SQL__ 

DATA step is a sequential process (one at a time for each observation), whereas the SQL procedure is a simultaneous process for all the observations.  

__Efficiency : DATA STEP vs. PROC SQL__  

The SQL procedure performed better with the smaller datasets (less than approx. 100 MB) whereas the data step excelled with the larger ones (more than approx. 100 MB).  

It is because the DATA step handles each record sequentially so it never uses a lot of memory, however, it takes time to process one at a time. So with a smaller dataset, the DATA step is going to take more time sending each record through.  

With the SQL procedure, everything is loaded up into memory at once. By doing this, the SQL procedure can process small datasets rather quickly since everything is available in memory. Conversely, when you move to larger datasets, your memory can get bogged down which then leads to the SQL procedure being a little bit slower compared to the DATA step which will never take up too much memory space.  

If you need to connect directly to a database and pull tables from there, then use PROC SQL.











































  










 













 


























