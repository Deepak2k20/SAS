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

























