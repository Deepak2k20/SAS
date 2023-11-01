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

## SAS: PROC FREQ WITH EXAMPLES

This tutorial explains how to use PROC FREQ with various examples in SAS.  

The PROC FREQ is one of the most frequently used SAS procedures which helps to summarize categorical variable. It calculates count/frequency and cumulative frequency of categories of a categorical variable. In other words, it returns the number and percentage of cases falling in multiple categories of a categorical variable. It's not just restricted to counts. It also produces bar charts and tests for association between two categorical variables.  

### Create a sample data set  

The program below creates a sample SAS dataset which will be used to demonstrate PROC FREQ with examples.  

```sas
data example1;
input x y $ z;
cards;
6 A 60
6 A 70
2 A 100
2 B 10
3 B 67
2 C 81
3 C 63
5 C 55
;
run;
```
The created dataset looks like below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8542484d-ce42-4b26-9db5-def063b793ea)  

### Example 1 : To check the distribution of a categorical variable (Character)  

Suppose you want to see the frequency distribution of variable 'y'.  

```sas
proc freq data = example1;
tables y;
run;
```

The TABLES statement tells SAS to return n-way frequency and crosstabulation tables and computes the statistics for these tables. 

![image](https://github.com/Deepak2k20/SAS/assets/65231118/314dc43d-5ebd-4880-b43d-6c0d66d91df3)  

It answers a question 'which category holds the maximum number of cases'. In this case, the category 'C' contains maximum number of values.  

__Tip :__  

Categorical variables are of two types - Nominal and Ordinal. A nominal variable is a categorical variable in which categories do not have any order. For example, gender, city etc. An ordinal categorical variable has categories that can be ordered in a meaningful way. For example, rank, status (high/medium/low) etc.  

### Example 2 : To remove unwanted statistics in the table  

Suppose you do not want cumulative frequency and cumulative percent to be displayed in the table. The option NOCUM tells SAS to not to return cumulative scores.  

```sas
proc freq data = example1; 
tables y /nocum;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b1a933ba-087c-456a-bf2e-f2c497787847)  

If you want only frequency, not percent distribution and cumulative statistics.  

```sas
proc freq data = example1;
tables y /nopercent nocum;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/6225d2b3-6b5d-428f-aadd-6a6e1424853a)  

### Example 3 : Cross Tabulation ( 2*2 Table)  

Suppose you want to see the distribution of variable 'y' by variable 'x'.  

```sas
proc freq data = example1;
tables y * x;
run; 
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1aa6d456-fd89-427b-8ea7-eb5ad8612d83)  

The output of the above SAS program is shown in the image above.


### Example 4 : Show Table in List Form    

Suppose you do not want output to be shown in tabular form. Instead, you want final analysis to be displayed in list form (See the image below)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8e87673b-7ad1-4310-81ab-d17a2444f91a)  

```sas
proc freq data = example1;
tables y * x / list;
run;
```

The forward slash followed by LIST keyword produces the list styled table.

### Example 5 : Hide Unwanted Statistics in Cross Tabulation  

```sas
proc freq data = example1;
tables y * x / norow nocol nopercent;
run;
```

The NOROW option hides row percentage in cross tabulation. Similarly, NOCOL option suppresses column percentage.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c747f974-5a57-4bfd-892d-80cfafe9a0c3)  

### Example 6 : Request Multiple Tables  

Suppose you want to generate multiple crosstabs. To accomplish it, you can run the command below-  

```sas
proc freq data = example1;
tables y * (x z) / norow nocol nopercent;
run;
```

The tables y*(x z) statement is equivalent to tables y*x y*z statement. In this case, it returns two tables - y by x and y by z.  

Example - tables (a b)*(c d); is equivalent to tables a*c  b*c  a*d  b*d;  

### Example 7 : Number of Distinct Values  

The NLEVELS option is used to count number of unique values in a variable.  

```sas
proc freq data = example1 nlevels;
tables y;
run;
```

In this case, it returns 3 for variable Y.  

### Example 8 : Use WEIGHT Statement  

The WEIGHT statement is used when we already have the counts. It makes PROC FREQ use count data to produce frequency and crosstabulation tables.  

```sas
Data example2;
input pre $ post $ count;
cards;
Yes Yes 30
Yes No 10
No Yes 40
No No 20
;
run;

proc freq data=example2;
tables pre*post;
weight count;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2b8671e2-93dd-4194-8e70-1e029aafc2b7)  

### Example 9 : Store result in a SAS dataset  

Suppose you wish to save the result in a SAS dataset instead of printing it in result window.  

```sas
proc freq data = example1 noprint;
tables y *x / out = temp;
run;
```

The OUT option is used to store result in a data file. NOPRINT option prevents SAS to print it in results window.

### Example 10 : Run Chi-Square Analysis  

The CHISQ option provides chi-square tests of homogeneity or independence and measures of association between two categorical variables.  Also it helps to identify the statistically significant categorical variables that we should include in our predictive model. All the categorical variables with a chi-square value less than or equal to 0.05 are kept.  

```sas
proc freq data = example1 noprint;
tables y * x/chisq;
output All out=temp_chi chisq;
run; 
```

### Example 11 : Generate Bar Chart and Dot Plot  

The bar chart can be generated with PROC FREQ. ​To produce a bar chart for variable 'y', the plots=freqplot (type=bar) option is added. By default, it shows frequency in graph. In order to show percent, you need to add scale=percent. The ODS graphics ON statement tells SAS to produce graphs. Later we turn it off.  

```sas
Ods graphics on;
Proc freq data=example1 order=freq;
Tables y/ plots=freqplot (type=bar scale=percent);
Run;
Ods graphics off;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/36bcc169-bf33-40b1-8bdd-f7ec3108f014)  

Similarly, we can produce dot plot by adding type=dot. See the implementation below-  

```sas
Ods graphics on;
Proc freq data=example1 order=freq;
Tables y/ plots=freqplot (type=dot);
Run;
Ods graphics off;
```

### Example 12 : Include Missing Values in Calculation  

By default, PROC FREQ does not consider missing values while calculating percent and cumulative percent. The number of missing values are shown separately (below the table). Refer the image below.  

```sas
Proc freq data=sashelp.heart;
Tables deathcause;
Run; 
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/33c8a398-dcaf-4695-bab9-fdbe402986d3)  

By adding MISSING option, it includes missing value as a separate category and all the respective statistics are generated based on it.  

```sas
Proc freq data=sashelp.heart;
Tables deathcause / missing;
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a7bbf859-d911-4d1d-b2f1-e604783799cd)  

### Example 13 : Ordering / Sorting  

In PROC FREQ, the categories of a character variable are ordered alphabetically by default. For numeric variables, the categories are ordered from smallest to largest value.  

To sort categories on descending order by frequency (from largest to smallest count), add ORDER=FREQ option  

```sas
Proc freq data=sashelp.heart order = FREQ;
Tables deathcause / missing;
Run;
```

It is generally advisable to show distribution of a nominal variable after sorting categories by frequency. For ordinal variable, it should be shown based on level of categories.  

To order categories based on a particular FORMAT, you can use order = FORMATTED option.  

### Conclusion  

PROC FREQ is a simple but powerful SAS procedure. This tutorial was designed for beginners who have no background of any programming language. Hope the above examples help to understand the procedure crystal clear.  

## SAS TIP : SPECIFY A LIST OF VARIABLES

Suppose you have a list of variables. You don't want to type the name of each variable to define them in a function or array. You are looking for a shortcut to accomplish this task.  

Create a dataset with a list of variables  

```sas
data dummy;
input q1 q3 q4 q2 q6$ bu$ q5;
cards;
1 2 3 5 sa an 3
2 4 3 6 sm sa 4
6 5 3 8 cb na 3
;
run;
 ```

How to specify a list of variables   

A single dash (-) is used to specify consecutively numbered variables. For example : q1-q4;  

A double dash (--) is used to specify variables based on the order of the variables as they appear in the file, regardless of the name of the variables.  

```sas
data dummy1 (drop= q1--q5);
set dummy;
sum = sum(of q1-q4);
sum1 = sum(of q1--q4);
run;
```

The output is shown in the image below -

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1786ef6f-86d9-402e-a7af-e9f7964043d2)  

In the above program, q1-q4 includes q1,q2,q3 and q4, whereas q1--q4 includes q1,q3 and q4 only as they appear the same way in file.  

How to specify all NUMERIC variables  

```sas
data dummy1 (drop= q1--q5);
set dummy;
sum = sum(of _numeric_);
run;
```

How to use double dash in array

The following program subtracts one from values in variables q1,q3 and q4.  

```sas
data dummy1;
set dummy;
array vars q1--q4;
do over vars;
vars = vars - 1;
end;
run;
```

How to use numeric variables in array

The following program subtracts one from values in numeric variables.  

```sas
data dummy1;
set dummy;
array vars _numeric_;
do over vars;
vars = vars - 1;
end;
run;
```

More Dash Symbol Usage

1. Print all NUMERIC variables from q1 through q6.

```sas
proc print;
var q1-numeric-q6;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/62149b00-5b35-4606-9f7f-c3f3d840400d)  

2.  Print all CHARACTER variables from q1 through q6.

```sas
proc print;
var q1-character-q6;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/67dfebea-823e-4a60-942a-2b9cefe2caf3)  

3.  Print all CHARACTER variables.  

```sas
proc print;
var _character_;
run;
```

## SAS : WILDCARD CHARACTER

In this tutorial, you will learn how to use wildcard character in SAS.

### Example 1 : Keep all the variables start with 'X'  

```sas
DATA READIN;
INPUT ID X1 X_T $;
CARDS;
2 3 01
3 4 010
4 5 022
5 6 021
6 7 032
;
RUN;

DATA READIN2;
SET READIN (KEEP = X:);
RUN;
```

The COLON (:) tells SAS to select all the variables starting with the character 'X'.  

### Example 2 : Filter data using wildcard character  

```sas
DATA READIN2;
SET READIN;
IF X_T =: '01';
RUN;
```

In this case, the COLON (:) tells SAS to select all the observations (rows) starting with the character '01'.  

### Example 3 : Use of WildCard in IN Operator  

```sas
DATA READIN2;
SET READIN;
IF X_T IN: ('01', '02');
RUN;
```

In this case, the COLON (:) tells SAS to select all the observations starting with the character '01' or '02'.

### Example 4 : Use of WildCard in GT LT (> <) Operators  

```sas
DATA READIN2;
SET READIN;
IF X_T >: '01';
RUN;
```

In this case, the COLON (:) 

tells SAS to select all the cases from character '01' up alphabetically.  

### Example 5 : WildCard in Function 

```sas
data example3;
set temp2;
total =sum(of height:);
run;
```

The TOTAL = SUM(OF height:); statement calculates the sum of all variables that start with height and assigns the result to the total variable.  

SUM() is a SAS function used to calculate the sum of numeric variables.  

OF height: specifies a variable list that includes all variables that start with height.  

The colon : is a wildcard that matches any characters following height.  


### Example 6 : WildCard in Array

```sas
proc sort data = sashelp.class out=class;
by name sex;
run;

proc transpose data = sashelp.class out=temp;
by name sex;
var height weight;
run;

proc transpose data = temp delimeter=_ out=temp2(drop=_name_);
by name;
var col1;
id _name_ sex;
run;

proc sql noprint;
select CATS('new_',name) into: newnames separated by " "
from dictionary.columns
where libname = "WORK" and memname = "TEMP2" and name like "Height_%";
quit;

data temp2;
set temp2;
array h(*) height:;
array newh(*) &newnames.;
do i = 1 to dim(h);
newh{i} = h{i}*2;
end;
drop i;
run;
```

## MISSING VALUES IN SAS

In SAS, Numeric and Character missing values are represented differently.

### Numeric Missing Values

SAS stores 28 types of missing values in a numeric variable. They are as follows :  

1) dot-underscore . _  
2) dot .  
3) .A through .Z ( Not case sensitive)  

Sorting Order : dot- underscore is the lowest valued missing value. After the dot-underscore, comes the dot, and then the dot-A. The dot-Z is the highest valued missing value.  

Run the following code and see how SAS treats them missing value  

```sas
data temp;
input x;
cards;
1
2
3
.
.A
.X
.Z
._
4
;
run;

proc freq;
table x;
run;   
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/deb0a45a-dc37-4817-ac0b-bc4d2d65c834)  

### SAS: Check for missing numeric values  

The following code checks for dot missing value only. It does not check for other 27 special numeric missing values (._ , .A through .Z)

```sas
data outdata;
set temp;
length y $12;
If x=. then y = "Missing";
else y = "Non-Missing";
run;
```

The following code checks for all 28 numeric missing values (. , ._ , .A through .Z)  

```sas
data outdata;
set temp;
length y $12;
If x<=.z then y = "Missing";
else y = "Non-Missing";
run;
```

The MISSING function accepts both character and numeric variables and returns the value 1 if the variable contains a missing value or zero otherwise.

```sas
data outdata;
set temp;
length y $12;
If missing(x) then y = "Missing";
else y = "Non-Missing";
run;
```

### SAS: Check for missing character values  

Character missing values are represented by a single blank enclosed in quotes ' '.  

```sas
DATA mydata;
  INPUT Product $;
  DATALINES;
ProductA
.
ProductA
ProductA
.
ProductB
ProductB  
;
RUN;

data outdata;
set mydata;
length y $12;
If missing(Product) then y = "Missing";
else y = "Non-Missing";
run;
```

### SUM Function vs. + Operator for Missing Values  

Suppose we have a data set containing three variables - X, Y and Z. They all have some missing values. We wish to compute sum of all the variables.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9ff8bb36-0f7b-4596-a82b-b3fa1a1b1e3f)  

```sas
data mydata;
input x y z;
datalines;
1 . 3
4 5 .
. 8 9
;
run;

data mydata2;
set mydata;
a=sum(x,y,z);
p=x+y+z;
run;
```

The SUM function returns the sum of non-missing values whereas "+" operator returns a missing value if any of the values are missing.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/60b3c70d-cff5-46c6-adf4-f409ec7fd070)  

### Functions that handle MISSING data  

NMISS : The NMISS() function will return the number of missing values in the specified list of numeric variables. The NMISS() function will convert any character values to numeric before assessing if the argument value is missing.  
 
CMISS : The CMISS() function counts the number of missing values for both character and numeric variables without requiring character values to be converted to numeric.  

N : The N() function returns the number of non-missing values in a list of numeric variables.  

```sas
/* Create a sample SAS dataset */
data sample_dataset;
  input var1 var2 var3 $;
  datalines;
10  20  A
15   .  B
.  25  C
12  18   .
.   .  D
;

/* Calculate the number of missing values for each variable */
data missing_values;
  set sample_dataset;

  /* Use NMISS function to count missing numeric values */
  num_missing_var1 = NMISS(var1);
  num_missing_var1_var2 = NMISS(var1, var2);

  /* Use CMISS function to count missing values */
  missing_all = CMISS(var1, var2, var3);

  /* Use N function to count total non-missing values for numeric values*/
  num_non_missing = N(var1, var2, var3);
  total_non_missing = 3-missing_all;

run;

/* Print the resulting dataset */
proc print data=missing_values noobs;
run;
```

### How to Count Missing Values in a Dataset  

To count missing values in a SAS dataset, you can use the NMISS option in PROC MEANS procedures in SAS.  

```sas
/* Create a sample SAS dataset with missing values */
DATA mydata;
  INPUT ID Age Income;
  DATALINES;
1 25 50000
2 . 60000
3 30 .
4 40 75000
5 22 40000
. 28 55000
7 35 65000
8 . .
9 19 30000
;
RUN;

PROC MEANS DATA=mydata NMISS;
RUN;
```

### CALL MISSING  

SAS provides the statement CALL MISSING() to explicitly initialise or set a variable value to be missing.

```sas
data _null_;
call missing( num_1, num_2, x ); 
num_3 = x;
put num_1 = / num_2 = / num_3 = ;
run;
```

See result in the Log Window. In the above SAS code, a data step is used to initialize and assign missing values to three variables (num_1, num_2, and x) using the call missing statement. Then, the value of x is assigned to num_3, and the values of num_1, num_2, and num_3 are printed using the put statement. Since num_1 and num_2 have been explicitly set to missing, their output will show as missing, while num_3 will take the value of x, which is also missing.  

### Delete empty rows  

```sas
options missing = ' ';
data readin;
set outdata;
if missing(cats(of _all_)) then delete;
run;
```

### How missing values are handled in SAS procedures  

1. PROC FREQ

To count missing values for categorical variables, you can use the PROC FREQ procedure. By default, PROC FREQ excludes missing values and percentages are based on the number of non-missing values. If you use the "/ MISSING" option in the tables statement, the percentages are based on the total number of observations (non-missing and missing) and the percentage of missing values are reported in the table.  

```sas
DATA mydata;
  INPUT Product $;
  DATALINES;
ProductA
.
ProductA
ProductA
.
ProductB
ProductB  
;
RUN;

PROC FREQ DATA=mydata;
  TABLES Product / MISSING;
RUN;
```

2. PROC MEANS  

It produces statistics on non-missing data only. The NMISS option is used to calculate number of missing values.  

```sas
Proc Means Data = test N NMISS;
Var q1 - q5 ;
Run;
```

To see number of observations having a missing value for the classification variable, type MISSING option in PROC MEANS.  

```sas
Proc Means data = test N NMISS MISSING;
Class Age ;
Var q1 - q5;
Run;
```

3. PROC CORR  

By default, correlations are computed based on the number of pairs with non-missing data (pairwise deletion of missing data). The nomiss option can be used on the proc corr statement to request that correlations be computed only for observations that have non-missing data for all variables on the var statement (listwise deletion of missing data).  

4. PROC REG  

If any of the variables on the model or var statement are missing, they are excluded from the analysis (i.e., listwise deletion of missing data)  

5. PROC LOGISTIC  

If any of the variables on the model or var statement are missing, they are excluded from the analysis (i.e., listwise deletion of missing data)  

6. PROC FACTOR  

Missing values are deleted listwise, i.e., observations with missing values on any of the variables in the analysis are omitted from the analysis.  

## SAS : CONVERT CHARACTER VARIABLE TO DATE

This tutorial explains multiple ways we can convert a character variable (string) to a date variable in SAS.  

Suppose you encounter a problem in which you need to convert character variable to SAS date format. It happens most of the times when we upload raw data file in TXT, EXCEL or CSV format to SAS. The problem with dates in character format is you cannot apply any calculations on them.  

### Create a Sample Data  

The following SAS code creates a sample SAS dataset for demonstration purpose.  

```sas
data example;
input dateofbirth $20.;
cards;
05/11/1980
07/05/1990
04/14/1981
;
run;
```

### Convert Character Variable to SAS Date  

The INPUT function is used to convert character variable (string) to numeric. With MMDDYY10. format, we assign format of the date.  

```sas
data out;
set example;
dateofbirth2 = input(strip(dateofbirth),MMDDYY10.);
format dateofbirth2 MMDDYY10.;
run;
```

Important Note : Please make sure a new variable is created for conversion. If you use the same variable for conversion, the format of the variable would remain character.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a77fd139-a048-4482-a160-47d60b2b3553)  

### How to Convert Character Variable to Different Date Format  

As you can see our original dateofbirth variable is in Month-Date-Year format but stored as a character. If we need to convert it to Date-Month-Year format and stored as in SAS date format.  

```sas
data out;
set example;
dateofbirth2 = input(strip(dateofbirth), MMDDYY10.);
format dateofbirth2 DDMMYY10.;
run;
```

Make sure you put the original date format in INPUT function and put the desired date format in FORMAT statement. If you put the different date format in INPUT function, it may lead to missing value. For example, 04/14/1981 cannot be converted to DDMMYY10. format directly as SAS reads 14 as month which is not possible.  

### How to convert character dates of DD-MMM-YYYY or DD/MMM/YYY format?  

You can use the format date11. to convert character values in DD-MMM-YYYY format.  

```sas
DATA temp;
     INPUT @6 dt $11.;
     dt2 = input(strip(dt),date11.);
     FORMAT dt2 date11.;
     CARDS;
     10/JUN/2014
     ;
PROC PRINT NOOBS;
RUN;
```

### Convert Multiple Character Variables to Date  

Suppose you need to convert multiple character variables to SAS datevalue format. We can create SAS array to convert them.  

```sas
data example2;
input dateofbirth $10. hire $11.;
cards;
1971-11-21 1991-12-21
1980-05-14 1999-10-20
;
run;
```

Real SAS Date values are numeric so numeric array is created for them.  

```sas
data out;
set example2;
array olddates $ dateofbirth hire;
array newdates dt1 dt2;
do i = 1 to dim(olddates);
newdates(i) = input(strip(olddates(i)),yymmdd10.);
end;
drop i;
format dt1-dt2 yymmdd10.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b3a89615-a080-4ab9-9582-253be67db57f)  

## HOW TO CONVERT NUMERIC VARIABLES TO DATE VARIABLES IN SAS (WITH EXAMPLES)

This tutorial explains how to convert a numeric variable to a date variable in SAS.  

Suppose you have a numeric variable that contains dates. You are asked to convert it to SAS date format. It seems to be a easy task but it sometimes becomes a daunting task when you don't know how SAS treats dates. The input data is shown below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9bb2bc72-a755-48ca-b2c5-8d86d4c21257)  

### Sample Data  

The following program is used to create a sample data.

```sas
data temp;
input date;
cards;
20160514
19990505
20131104
20110724
;
run;
```

### Solution  

To convert a numeric variable into a date variable in SAS, you can use the following syntax.  

```sas
data temp2;
set temp;
newdate = input(put(date,8.),yymmdd8.);
format newdate date10.;
proc print noobs;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/0eaae94e-3e7f-4eec-ac9c-8f2c2c38a185)  

__Explanation__

PUT Function is used to convert the numeric variable to character format.  

INPUT Function is used to convert the character variable to sas date format  

yymmdd8 informat refers to years followed by month and days having width of total 8  

FORMAT Function is used to display the SAS date values in a particular SAS date format. If we would not use format function, SAS would display the date in SAS datevalues format. For example, 20588 is a sas datevalue and it is equivalent to '14MAY2016'.  

### ANYDTDTE : Powerful Informat for all dates  

ANYDTDTE is relatively latest informat written or devloped by SAS Institute to handle dates. This is extremely useful when you hate remembering various SAS date informats and working with new dataset which you are not so familiar with the type of date format you may have in your date column. For example date can be like March 17, 2021, 17/03/2021, 03/17/2021 or 17MAR2021. If you wish there would be only one informat to handle all these dates, SAS has already fulfilled your promise.  

```sas
data temp2;
set temp;
newdate = input(put(date,8.),ANYDTDTE8.);
format newdate date10.;
proc print noobs;
run;
```

## SAS FORMATS

This tutorial explains how to use FORMATS in SAS, along with examples.

### SAS Formats  

SAS Formats decide how to display values of a variable. They define the appearance of variables when they are printed or exported. For example, you can use a format to display a numeric variable as a currency, percentage. Formats do not change the underlying data values; they only affect their presentation.  

Below is a list of common SAS Formats.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3ad8d864-1584-435d-8aa1-246e06f918a8)  

### Character Formats  

$w.: Displays character values to a specified width.  

$UPCASEw.: Displays character values in uppercase and optionally truncates them to a specified width.  

The FORMAT statement is used to format values in a specific format. Here we are using the $UPCASEw. format.  

```sas
data mydata;
set sashelp.cars; 
format make $upcase.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3530d51e-b985-4a86-8105-d46b637a2419)  

Let's say we specify width 3 $upcase3., it will truncate to first 3 letters (as shown in the image below).  

```sas
data mydata;
set sashelp.cars; 
format make $upcase3.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b97448d9-b468-469d-9693-5798b80f93cc)  

### Numeric Formats  

COMMAw.d: Displays numeric values with commas and a specified number of decimal places.  

DOLLARw.d: Displays numeric values as currency with a dollar sign, commas, and a specified number of decimal places.  

PERCENTw.d: Displays numeric values as percentages with a specified number of decimal places.  

The "dollar8." format specifies that the values of the "msrp" variable should be displayed as currency with a dollar sign and commas, with a width of 8 characters. The "msrp" variable represents the manufacturer's suggested retail price of the cars.  

```sas
data mydata;
set sashelp.cars; 
format msrp dollar8.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1e901c21-a11d-4d4f-a536-29f892b077c1)  

If you only want commas in numeric values, you can use the format comma8.  

```sas
data mydata;
set sashelp.cars; 
format msrp comma8.;
run;
```

In the code below, the percent8.2 format specifies that the "percent_gain" values should be displayed as percentages with two decimal places, with a total width of 8 characters.  

```sas
data mydata;
percent_gain = 0.835; 
format percent_gain percent8.2;
run;
```

Result: 83.50%

### Date Formats  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/22b62528-3cc8-4100-a245-624b58def042)  

The line format date date11.; specifies that the "date" variable in the "mydata" dataset should be formatted using the "date11." format. This format represents the date values in the format "dd-MON-yyyy". The resulting dates will have a width of 11 characters.  

```sas
data mydata;
set sashelp.pricedata;
format date date11.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1bd0b34c-fe4b-4e1c-ac72-614cf9047b17)  

## SAS DATE FORMATS AND INFORMATS

This tutorial describes the usage of SAS Date formats and informats. It includes practical real-world data problems related to SAS formats.  

### What are Formats and Informats?

Informats is used to tell SAS how to read a variable whereas Formats is used to tell SAS how to display or write values of a variable.  

Informats is basically used when you read or import data from either an external file (Text/Excel/CSV) or read in sample data which was created using CARDS/DATALINES statement. It is also used when you create a new variable in a dataset.  

Formats can be used in both Data Steps and PROC Steps whereas Informat can be used only in Data Steps. Let's understand by examples -  

### Example 1 - Read Dates in SAS  

In the program below, we have used INFORMATS ddmmyy8. and ddymmyy10. to read dates in SAS. It creates a dataset called sampledata which is stored in WORK library.  

```sas
DATA sampledata;
     INPUT @6 date1 ddmmyy8. @15 date2 ddmmyy10.;
    CARDS;
     30-12-16 30-12-2016
  ;
RUN;
```

The INFORMATS ddmmyy8. is used to read 30-12-16 date and ddmmyy10. to read 30-12-2016 date. In this case, 8 and 10 refers to width of the date.

The created dataset looks like below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/616e58d4-622b-45ff-a87e-09b05631d965)  

It returns 20818 as it is in SAS date value form. It is not meaningful if you look at the value. You cannot tell which date it is. To display in real date form, use FORMAT statement.  

```sas
DATA sampledata;
     INPUT @6 date1 ddmmyy8. @15 date2 ddmmyy10.;
     FORMAT date1 ddmmyy8. date2 ddmmyy10.;
  cards;
     30-12-16 30-12-2016
  ;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/59595e31-6c2b-4e9f-8b67-40ef5732e441)  

### How to read DD-MMM-YY format

You can use date11. format for both DD-MMM-YY and DD-MMM-YYYY format.  

```sas
DATA temp;
     INPUT @6 dt date11.;
     FORMAT dt date11.;
     CARDS;
     10-oct-14
     ;
PROC PRINT NOOBS;
RUN;
```

Result : 10-OCT-2014  

### Example 2 - Display Today's Date  

The today() function can be used to generate current date.  

```sas
data _null_;
    dt=today();
    format dt yymmdd10.;
    put dt ;
run;
```

Result : It returns 2016-12-30 as 30DEC2016 is the today's date. It's in YYYY-MM-DD format because we've used yymmdd10. format. The 10 refers to the width of the date as 2016-12-30 contains 10 elements. The PUT statement is used to show value in log window.  

### To display date in WORD format

1. Short Word Date Format

The format date9. returns 30DEC2016.
```sas
format dt date9.;
```

2. Complete Word Date Format

The format WORDDATE. returns DECEMBER 30, 2016. No need to specify width in this format. It automatically adjusts the width depending on the month.  

```sas
format dt WORDDATE.;
```

3. Including WEEK

The format WEEKDATE. gives Friday, December 30, 2016  
```sas
format dt WEEKDATE.;
```

### Display DAY / MONTH / YEAR

In this section, we will see how we can write only day, month, year and weekday.  

```sas
data _null_;
dt=today();
put "Day :"  dt  DAY.;
put "Month :" dt MONTH.;
put "YEAR:" dt YEAR.;
put "WEEKDAY:" dt DOWNAME.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a83d02ab-b268-47d1-a150-3a3b98880b8f)  

We can also use FORMAT in the PUT statement without specifying FORMAT statement explicitly. The DAY. format returned 30, MONTH. format returned 12 and YEAR. format returned 2016. In addition, we have used DOWNAME. format to extract weekday (Friday).  

Other Popular Formats  

Some of the commonly used date formats are listed below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/aeacfe94-dd29-4747-8761-46c311448033)  

Endnotes

Hope you have a better understanding of the difference between SAS Date Formats and Informats and how they are used after completing this tutorial.   


## SAS : PROC FORMAT WITH EXAMPLES  

This tutorial explains the uses of PROC FORMAT in data analysis tasks. It includes several examples to help understand the practical application of PROC FORMAT.

### Sample Data  

In this tutorial, we will be using the dataset sashelp.cars for demonstration purpose. See the sample data shown in the image below.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/66764f6b-8ccc-4188-b0f3-32df716f724c)  

Example 1 : Suppose you are asked to group MSRP variable based on the following conditions and check the number of observations falling in each groups.

Values greater than 40,000 should be labeled as 'High'  

Values between 26,000 and 40,000 should be labeled as 'Medium'  

Otherwise, label them as 'Low'  

__Solution__ 

```sas
proc format;
value range
40000-high='High'
26000-< 40000='Medium'
other ='Low';
run;

proc freq data = sashelp.cars;
table msrp;
format msrp range.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/4840f8d6-6339-49fa-b5d6-2ba74bcb4c57)  

Example 2 : Same as with example 1. Here we are creating a new variable called TSRP based on the conditions applied on the MSRP variable.

__Solution :__  

```sas
proc format;
value range
40000-high='High'
26000-< 40000='Medium'
other ='Low';
run;

data temp;
set sashelp.cars;
TSRP = put(msrp, range.);
run;
```

The put() function is used to apply the format. The line TSRP = put(msrp, range.); applies the custom format range to the msrp variable and stores the formatted values in a new variable named TSRP.

Example 3 : Subset Data - You can also filter data using PROC FORMAT.  

The following code filters the dataset to only include observations where the formatted value is either 'High' or 'Medium'.  

__Method 1 :__  

```sas
data temp;
set sashelp.cars;
where put(msrp, range.) IN ('High' 'Medium');
run;  
```

__Method 2 :__  

```sas
data temp (where = (tsrp IN ('High' 'Medium')));
set sashelp.cars;
tsrp = put(msrp, range.);
run;
```

__Method 3 :__

```sas
proc sql;
select *,
put(msrp, range.) as tsrp
from sashelp.cars
where calculated tsrp in ('High', 'Medium');
quit;
```

## SAS : DELETE EMPTY ROWS IN SAS  

Suppose you want to delete empty rows from a dataset in SAS. It generally happens when we import data from external sources such as excel / csv files. It loads additional rows that are totally blank. Sometimes blank observations also affect the desired output so it's necessary to check missing cases and treat them.  

### Sample Dataset  

The sample dataset looks like below. In the dataset, we have four variables - 1 character and 3 numeric. It would be used further in the example to demonstrate how to remove empty rows.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/bd62a8fc-ad9b-4de2-8db6-9da7368c84fa)  

Create a SAS dataset

The following program creates a sample dataset in SAS.  

```sas
data outdata;
length Name $12.;
input Name $ Score1 Score2 Score3 ;
infile datalines missover;
datalines;
Sam 77 68 66
Deepanshu 50 . 89
Shane 55 78 89
Roger 50 97 86
Priya 88 68 93
;
run;
```

Method I : Remove rows where all variables having missing / blank values  

```sas
options missing = ' ';
data readin;
   set outdata;
   if missing(cats(of _all_)) then delete;
run;
```

Notes :  

1. The MISSING= system option is used to display the missing values as a single space rather than as the default period (.) options missing = ' ';  

2. The CATS function concatenates the values. It also removes leading and trailing blanks. cats(of _all_) - Concatenate all the variables  

3.  missing(cats(of _all_)) - Identifies all the rows in which missing values exist in all the variables.

Output

In the output dataset, we have 5 rows. One row is deleted from the original dataset.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d179e853-8073-483c-81e0-d0e7fc9faa34)  

Method 2   

In this program, NMISS function checks the numeric of missing numeric values and CMISS checks the number of missing character values. In this code, we are telling SAS to delete records wherein both the character and numeric values are missing.  

```sas
data readin;
set outdata;
if nmiss( of _numeric_ ) and cmiss(of _character_) then delete ;
run;
```

Method 3

In the code below, we are using COALESCE and COALESCEC functions to return non-empty rows. These functions return first non-missing value. If all values are missing, it returns missing. Later we are checking whether these functions return missing or not.  

```sas
data readin;
set outdata;
if missing(coalescec(of _character_)) and missing(coalesce(of _numeric_)) then delete;
run;
```

Example : Delete rows where any variable has missing values  

```sas
data readin;
set outdata;
if nmiss(of _numeric_) OR  cmiss(of _character_) > 0 then delete;
run;
```

In this case, we are using OR operator to check if any of the variable has missing values. It returns 4 observations. Check out the output below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/46211c07-bdfc-4ae3-adb3-7ac3630498de)  

### Practice Questions - Try it yourself

Q1. Remove records wherein all numeric columns having empty rows.  

Q2. Remove records wherein all character variables having empty rows.  


## SAS : FIRST. AND LAST. VARIABLES

This tutorial explains how to identify first and last observations within a group. It is a common data cleaning challenge to remove duplicates or store unique values. In SQL, we use window functions such as rank over() to generate serial numbers among a group of rows. In SAS, we can create first. and last. variables to achieve this task.

### First. and Last. Variables  

FIRST.VARIABLE assigns the value of 1 for the first observation in a BY group and the value of 0 for all other observations in the BY group.  

LAST.VARIABLE assigns the value of 1 for the last observation in a BY group and the value of 0 for all other observations in the BY group.  

Note : Data set must be sorted BY group before applying FIRST. and LAST. Variables.  

SAMPLE DATA SET  

Suppose you have a dataset consisting 3 variables and 12 observations. The variables are ID, Name and Score. The variable ID is a grouping variable and it contains duplicates.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f9fbc91d-1de6-4271-b544-589da550a642)  
  
Create this data set in SAS  

The program below creates the dataset in SAS. Copy the program below and paste it into SAS program editor and run/submit it.  

```sas
data readin;
input ID Name $ Score;
cards;
1     David   45
1     David   74
2     Sam     45
2     Ram     54
3     Bane    87
3     Mary    92
3     Bane    87
4     Dane    23
5     Jenny   87
5     Ken     87
6     Simran  63
8     Priya   72
;
run;
```

Use PROC SORT to sort the data set by ID. It is required to sort the data before using first. and last. variables.  

```sas
PROC SORT DATA = READIN;
BY ID;
RUN;
DATA READIN1;
SET READIN;
BY ID;
First_ID= First.ID;
Last_ID= Last.ID;
RUN;
```

Note : FIRST./LAST. variables are temporary variables. That means they are not visible in the newly created data set. To make them visible, we need to create two new variables. In the program above, i have created First_ID and Last_ID variables.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/6832bebf-0897-4b49-8020-43fef1c367ee)  

How it works  

FIRST.variable = 1 when an observation is the first observation in each group values of variable ID.  

FIRST.variable = 0 when an observation is not the first observation in each group values of variable ID.  

LAST.variable = 1 when an observation is the last observation in each group values of variable ID.  

LAST.variable = 0 when an observation is not the last observation in each group values of variable ID.  

When FIRST.variable = 1 and LAST.VARIABLE = 1, it means there is only a single value in the group. (See ID = 4 in the above data for reference)  

### Selecting First Observation within a Group  

Suppose you need to select only the first observation among a group of observations. It is very easy to do it with IF statement. The IF statement subsets data when IF is not used in conjunction with THEN or ELSE statements.  

```sas
PROC SORT DATA = READIN;
BY ID;
RUN;
```

```sas
DATA READIN1;
SET READIN;
BY ID;
IF FIRST.ID;
PROC PRINT;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3a3b714d-4145-4e13-9878-fc294525bc97)  

Note : It returns first observation among values of a group (total 7 observations).  

### Selecting Last Observation within a Group  

Suppose you are asked to include only last observation from a group. Like the previous example, we can use last. variable to subset data.  

```sas
PROC SORT DATA = READIN;
BY ID;
RUN;
```
```sas
DATA READIN1;
SET READIN;
BY ID;
IF LAST.ID;
PROC PRINT;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/76cc79eb-97b1-462b-86c0-feb9733a6751)  

### Can we use WHERE instead of IF with First. and Last. Variables?  

No. WHERE statement cannot be used with First. and Last. Variables. It is because WHERE statement requires variables already be created in the dataset before processing.  

How to generate serial number in a group?  

Suppose you need to create serial numbers among a group of observations. See the snapshot below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/91d654d8-5890-425c-83de-786c6da6cb77)  

```sas
Data temp;
set readin;
by ID;
if first.id then N = 1;
else N +1;
proc print;
run;
```

In the above program, we are setting N=1 when it is the first value of a group i.e. ID. Otherwise adding 1 to N. The N+1 implies N = N + 1 in BY group processing. When there is a second observation in a group, N+1 adds 1 to N=1 so N becomes 2. It further increments by 1 when there is third observation in the group and so on.

### Calculate Cumulative Score by Group  

Suppose you need to calculate running cumulative score by variable ID.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/39d74468-599b-4568-a73d-2a6eb98444fe)  

```sas
Data temp;
set readin;
by ID;
if first.id then CumScore = Score;
else CumScore + Score;
proc print;
run;
```

In the above program, we are setting Cumscore = Score when it is the first value of a group i.e. ID. Otherwise adding Score to Cumscore. The Cumscore + Score implies CumScore = CumScore + Score in BY group processing.

How to store Unique and Duplicate Values  

```sas
data unique duplicates;
set readin;
by id;
if first.id = 1 and last.id = 1 then output unique;
else output duplicates;
run;
```
 
The DATA statement creates two temporary SAS data sets: DUPLICATES AND UNIQUE.  

The SET statement reads observations from data set READIN.  

The BY statement tells SAS to process observations by ID. Variables FIRST.ID and LAST.ID are created.  

If the first and last observation have the same value, it implies it is a unique value; otherwise, the value is a duplicate.  
 
### Case Studies  

1. Identify and select only records having maximum Score among a group of observations of variable ID

3. Select unique observations plus second observation from duplicate observations of variable ID

### Solution 1  

First we need to build a logic how we can select records having max score within variable ID. We can do it via PROC SORT. In this case, we need to sort data by 2 variables - first sorting on variable ID and then next sorting on Score by descending order. The DESCENDING keyword is used in PROC SORT to arrange data from largest to smallest. Sorting on descending order is used to place the max value at first observation in each group of ID.  

```sas
proc sort data= readin;
by ID descending score;
run;
data readin1;
set readin;
by ID;
if first.id;
run;
```

After sorting, we retain records having maximum value by using FIRST. and IF statement. The IF FIRST.ID keeps the first record among a group of values of variable ID. The output is shown in the image below.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b282a5c9-6fda-4fc7-9345-69705bb3b78e)  

Solve second case study yourself and post your answer in the comment box below. Make sure it should be solved in one data step code. Hint : BOTH FIRST. and LAST. variables would be used.  

## SAS PROC SORT: LEARN WITH EXAMPLES

This tutorial explains the PROC SORT SAS procedure in detail, along with examples.  

In SAS, the PROC SORT procedure is used to sort datasets based on one or more variables.  

### Syntax of PROC SORT

The syntax of the PROC SORT procedure in SAS is as follows:  

```sas
PROC SORT DATA=input_dataset OUT=output_dataset;
  BY variable(s);
RUN;
```

DATA: Specifies the input dataset that needs to be sorted.  

OUT: Specifies the output dataset where the sorted data will be stored.  

BY statement: Used to specify the variable(s) by which the dataset should be sorted. You can list multiple variables separated by spaces to perform sorting based on multiple criteria.  


### Sample Dataset  

Let's create a sample dataset for the examples in this tutorial. Here we have 3 columns and 10 rows.  

```sas
data mydata;
input product $ transactions sale;
datalines;
A 84 158
A 75 118
A 64 421
A 12 592
B 75 206
B 17 855
B 46 360
C 87 650
C 96 922
C 40 860
;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/50156de6-4b69-4e3d-8fe0-4f8d78e54fa8)  

### Example 1: Sort Data in Ascending Order

The following code sorts data in ascending order (smallest to largest) based on a column named transactions. The sorted data will be stored in the dataset named "newdata".  

```sas
proc sort data=mydata out=newdata;
by transactions;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2631c51b-dd1f-4db4-8493-bb71264b0ad1)  

### Example 2: Sort Data in Descending Order  

To sort the dataset in descending order, we can use the DESCENDING keyword before the variable name in the BY statement in PROC SORT procedure. The following code sorts the data from largest to smallest based on a column named transactions. The sorted data will be stored in the dataset named "newdata".  

```sas
proc sort data=mydata out=newdata;
by descending transactions;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c571e99c-be93-4b1d-8abf-8eeebbb0917d)  

### Example 3: Filter and Sort Data  

If you want to filter the data before sorting, you can use WHERE= option in PROC SORT. The following code selects data for product A only and then sorts the filtered data based on "transactions" column.  

```sas
proc sort data=mydata (where=(product = 'A')) out=newdata;
by transactions;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ee810859-6e6b-4f4c-90d0-e46e96ded4a9)  

### Example 4: FIRSTOBS= AND OBS= Options in PROC SORT  

The FIRSTOBS= option tells SAS to start reading from a specified observation. Whereas, the OBS= option specifies the observation at which SAS processing ends. In the code below, we are reading data from 5th row till 8th row (inclusive).  

```sas
proc sort data=mydata (firstobs= 5 obs=8) out=newdata;
by transactions;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/7ca80eb6-73c8-4f4f-a5d5-146986e07076)  

### Example 5: Format in PROC SORT  

In the code below, a format named $PRODUCT is defined using the proc format procedure. This format labels the values 'A', 'B', and 'C' to their corresponding labels 'Product A', 'Product B', and 'Product C'.  

```sas
proc format;
value $PRODUCT 'A'='Product A' 'B'='Product B' 'C'='Product C';
run;

proc sort data=mydata out=newdata;
format product $PRODUCT.;
by transactions;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3d05e8e1-a50f-4f74-b8c8-a1303c00a54e)  

### Example 6: Sort Data by multiple columns  

Here the sorting is performed based on two columns - "product" and "transactions".  

```sas
proc sort data=mydata out=newdata;
by product transactions;
run;
```
 
### Example 7: NODUP AND NODUPKEY in PROC SORT  

In PROC SORT, the NODUP and NODUPKEY options are used to remove duplicate observations from the dataset.  

The NODUPKEY option is used to remove duplicates based on the variable(s) specified in BY statement. Whereas the NODUP option is used to remove duplicates based on values of all variables in a dataset.  

In the code below, 7 observations with duplicates based on "product" column were deleted.  

```sas
proc sort data=mydata nodupkey out=newdata;
by product;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a6246a07-adf3-4e2c-a4e1-8deb2378793a)

In the code below, 0 duplicate observations were deleted as there is no duplicate rows in the dataset.

```sas
proc sort data=mydata nodup out=newdata;
by product;
run;
```

## SAS : IDENTIFYING AND STORING UNIQUE AND DUPLICATE VALUES  

This post demonstrates techniques to find unique and duplicate values in a SAS data set. It is one of the most common interview questions as it is commonly used in day-to-day data management activities. SAS has some easy inbuilt options to handle duplicate records.  

Below is a sample data set that can be used for demonstration.  

SAMPLE DATA SET  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5dbd5fd5-54ac-4ae5-bb5d-8ca0fae3f88c)  

__Create this data set in SAS__

```sas
data readin;
input ID Name $ Score;
cards;
1     David   45
1     David   74
2     Sam     45
2     Ram     54
3     Bane    87
3     Mary    92
3     Bane    87
4     Dane    23
5     Jenny   87
5     Ken     87
6     Simran  63
8     Priya   72
;
run;
```

There are several ways to identify unique and duplicate values:  

### 1. PROC SORT  

In PROC SORT, there are two options by which we can remove duplicates.

1) NODUPKEY Option
2) NODUP Option

The NODUPKEY option removes duplicate observations where value of a variable listed in BY statement is repeated while NODUP option removes duplicate observations where values in all the variables are repeated (identical observations).  

The difference between these two options are explained in detail below with SAS codes-  


PROC SORT DATA = readin NODUPKEY;
BY ID;
RUN;	

PROC SORT DATA = readin NODUP;
BY ID;
RUN;

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/bfd14da7-86fe-493c-95d3-20684543b485)  

The NODUPKEY has deleted 5 observations with duplicate values whereas NODUP has not deleted any observations.  

__Why no value has been deleted when NODUP option is used?__  

Although ID 3 has two identical records (See observation 5 and 7), NODUP option has not removed them. It is because they are not next to one another in the dataset and SAS only looks at one record back.  

To fix this issue, sort on all the variables in the dataset READIN.  

To sort by all the variables without having to list them all in the program, you can use the keyword ‘_ALL_’ in the BY statement (see below).

```sas
PROC SORT DATA = readin NODUP;
BY _all_;
RUN;
```

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3d1280f3-6661-49cf-8d78-06c816e16d1e)  

__STORING DUPLICATES__

Use the DUPOUT= option with NODUPKEY (or NODUP) to output duplicates to the specified SAS data set:  

```sas
PROC SORT DATA = readin NODUPKEY DUPOUT= readin1;
BY ID;
RUN;
```

The output is shown below :  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c6acb9d0-47dd-4a8f-a218-8071424d9bdb)  

### FIRST. and LAST. VARIABLES  

FIRST.VARIABLE assigns the value of 1 for the first observation in a BY group and the value of 0 for all other observations in the BY group.  

LAST.VARIABLE assigns the value of 1 for the last observation in a BY group and the value of 0 for all other observations in the BY group.  

Data set must be in sort order.  

Use PROC SORT to sort the data set by ID.  

```sas
PROC SORT DATA = READIN;
BY ID;
RUN;

DATA READIN1;
SET READIN;
BY ID;
First_ID= First.ID;
Last_ID= Last.ID;
RUN;
```

__Note__ : FIRST./LAST. variables are temporary variables. That means they are not visible in the newly created data set. To make them visible, we need to create two new variables. In the program above, i have created First_ID and Last_ID variables.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/4cd5d180-006d-4ad1-a1c8-bbd4af2f7400)  

__How to store unique and duplicate values?__  

```sas
DATA DUPLICATES UNIQUE;
SET READIN;
BY ID;
First_ID= First.ID;
Last_ID= Last.ID;
IF NOT (First_ID = 1 and Last_ID = 1) THEN OUTPUT DUPLICATES;
ELSE OUTPUT UNIQUE;
RUN;
```

__Explanation__ 

The DATA statement creates two temporary SAS data sets: DUPLICATES AND UNIQUE.  

The SET statement reads observations from data set READIN  

The BY statement tells SAS to process observations by ID. Variables FIRST.ID and LAST.ID are created.  

The observations where both First_ID and Last_ID do not equal to 1 go to the newly created data set DUPLICATES.  

The ELSE statement outputs all other observations (i.e., where First_ID and Last_ID equal to 1) to data set UNIQUE.  


## SAS : DETAILED EXPLANATION OF PROC MEANS

PROC MEANS is one of the most common SAS procedure used for analyzing data. It is mainly used to calculate descriptive statistics such as mean, median, count, sum etc. It can also be used to calculate several other metrics such as percentiles, quartiles, standard deviation, variance and sample t-test.  

### Uses of PROC MEANS  

1) Analyze numeric or continuous variables  

2) Analyze numeric variables by group(s)  

3) Identifies outlier or extreme values  

4) Hypothesis Testing with Sample T-test

### PROC MEANS Syntax  

The syntax of PROC MEANS is shown below.  

```sas
PROC MEANS DATA=dataset-name ;
  BY  variables;
  CLASS variable(s) / ;
  VAR variables;  
  OUTPUT OUT=SAS-data-set ;
RUN;
```

The explanation of statements of PROC MEANS is as follows :  

PROC MEANS - Calculate descriptive statistics for variables  

BY - Calculate separate statistics for each BY group  

CLASS - Group the analysis  

VAR - Numeric variables you want to analyze  

OUTPUT - Create an output data set  

### Dataset Description

The data includes seven variables and 499 observations. It comprises of survey responses from variables Q1 through Q5 and two demographics - Age and BU (Business Unit). The survey responses lie between 1 to 6.  

To use the dataset in SAS, you can use PROC IMPORT to read data into SAS. See the code below -  

```
proc import datafile='C:\Users\Deepanshu\Downloads\test.xls'
out=test
dbms = xls;
run;
```

### Simple Example of PROC MEANS  

In the DATA= option, you need to specify the dataset you want to use. In the VAR statement, you need to refer the numeric variables you want to analyze. You cannot refer character variables in the VAR statement.  

```sas
Proc Means Data = test;
Var q1 - q5;
Run;
```

The output of PROC MEANS is shown in the image below.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/073f7f55-1282-4d5c-9fee-04b87b844a0a)  

By default, PROC MEANS generates N, Mean, Standard Deviation, Minimum and Maximum statistics.  

### Common Statistical Options of PROC MEANS  

The most frequent statistical options used in PROC MEANS are listed below against their description.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9a64d4e3-f2d8-461f-9de8-4f24dfb0fb34)  

### Other Statistical Options  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/72fd13d5-9e20-4e76-8233-7cddeda4d18c)  

### How to limit Descriptive Statistics  

Suppose you want to see only two statistics - number of non-missing values and number of missing values.  

```sas
Proc Means Data = test N NMISS;
Var q1 - q5 ;
Run;
```

N refers to number of non-missing values and NMISS implies number of missing values.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/57eb0471-7acf-4363-9f8d-cb2460c29528)  

__Tips__ : Add NOLABELS option to delete Label column in the PROC MEAN table.  

```sas
Proc Means data = test N NMISS NOLABELS;
Var q1 - q5;
Run;
```

### Group the analysis using PROC MEANS  

Suppose you want to group or classify the analysis by Age. You can use the CLASS statement to accomplish this task. It is equivalent to GROUP BY in SQL.  

```sas
Proc Means data = test N NMISS NOLABELS;
Class Age;
Var q1 - q5;
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/38990341-235a-421c-8f10-a57611b3ee3a)  

You can use NONOBS option to delete N Obs column from the Proc Means table.  

```sas
Proc Means data = test N NMISS NOLABELS NONOBS;
Class Age;
Var q1 - q5;
Run;
```
 
### How to use Format in Proc Means  

First, you need to create an user defined format.  

```sas
Proc Format;
Value Age
1 = 'Less than 25'
2 = '25-34'
3 = '35-43'
4 = '44-50'
5 = '51-59'
6 = '60 or more';
Run;
```

Add FORMAT statement to use user defined format in PROC MEANS.  

```sas
Proc Means data = test N MEAN;
Class Age;
Format Age Age.;
Var q1 - q5;
Run;
```

### How to change Sorting Order  

The DESCENDING option to the right of the slash in the first CLASS statement instructs PROC MEANS to analyze the data in DESCENDING order of the values of Age.  

```sas
Proc Means Data = test;
Class Age / descending;
Var q1 - q5 ;
Run;
```

Instead of displaying the results in “sort order” of the values of the Classification Variable (s) you specified in the CLASS Statement, order the results by frequency order using the ORDER=FREQ option in the CLASS Statement.  

```sas
Proc Means Data = test N;
Class Age / Order = FREQ;
Var q1 - q5 ;
Run;
```

You can order the results by user defined format of a variable specified in the CLASS statement using the ORDER=FORMATTED option in the CLASS Statement.  

```sas
Proc Means data = test N MEAN;
Class Age / Order = formatted;
Format Age Age.;
Var q1 - q5;
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/81e0d987-26cf-4c51-bc7e-573d60a751cb)  

Note : If you specify CLASS statement without VAR statement, it classifies the analysis by all numeric variables in your data set.

### Grouping and Output in Separate Tables  

Suppose you want to analyze variables Q1 - Q5 by variable AGE and want the output of each levels of AGE in separate tables. You can use BY statement to accomplish this task. See the example below-  

Make sure you sort the data before using BY statement.  

```sas
proc sort data= test;
by age;
run;
```

```sas
proc means data = test;
by age;
var q1 - q5 ;
run;
```

### Difference between CLASS and BY statement  

The CLASS statement returns analysis for a grouping (classification) variable in a single table whereas BY statement returns the analysis for a grouping variable in separate tables. Another difference is CLASS statement does not require the classification variable to be pre-sorted whereas BY statement demands sorting.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2f7b4f42-45cd-48ac-8c93-4f5df7d11f84)  

### Save output in a data set  

You can use NOPRINT option to tell SAS not to print output in output window.  

```sas
Proc Means data = test NOPRINT;
Class Age / Order = formatted;
Format Age Age.;
Var q1 - q5;
Output out = readin mean= median = /autoname;Run;
```

In the above code, readin is a data set in which output will be stored. The MEAN= MEDIAN= options tells SAS to generate mean and median in the output dataset. The AUTONAME Option automatically assigns unique variable names in the Output Data Set “holding” the statistics requested in the OUTPUT statement.  

You can use AUTOLABEL option to automatically assigns unique label names in the Output Data Set “holding” the statistics requested in the OUTPUT statement.  

```sas
Proc Means Data = test noprint;
Class Age ;
Var q1 q2;
Output out=F1 mean= / autoname autolabel;
Run;
```

You can specify variables for which you want summary statistics to be saved in a output data set.  

```sas
Proc Means Data = test noprint;
Class Age ;
Var q1 q2;
Output out=F1 mean(q1)= median(q2)= / autoname;
Run;
```

You can give custom names to variables stored in a output data set.  

```sas
Proc Means Data = test noprint;
Class Age;
Var q1 - q5 ;
Output out=F1 mean=_mean1-_mean5 median=_median1-_median5;Run;
```

### DROP = , KEEP = option

We can use DROP and KEEP options to remove or keep some specific variables.  

```sas
Proc Means Data = test noprint;
Class Age;
Var q1 - q5 ;
Output out=F1 (drop = _type_ _freq_) mean=_mean1-_mean5 median=_median1-_median5;
Run;
```

### WHERE Statement

The WHERE statement is used to filter or subset data. In the code below, we are filtering on variable Q1 and telling SAS to keep only those observations in which value of Q1 is greater than 1. 

```sas
Proc Means Data = test noprint;
Where Q1 > 1;Class Age;
Var q1 - q5 ;
Output out=F1(drop= _FREQ_) mean= median= / autoname;
Run;
```

Like WHERE statement, we can use WHERE= OPTION to filter data. See the following program -  

```sas
Proc Means Data = test (Where=( Q1 > 1)) noprint;
Class Age;
Var q1 - q5 ;
Output out=F1(drop= _FREQ_) mean= median= / autoname;
Run;
```

### GROUPING on 2 (or more) Variables  

When two ore more variables are included in the CLASS statement, PROC MEANS returns 3 levels of classification which is shown in the _TYPE_ variable. Suppose we are specifying variables AGE BU in the CLASS statement. SAS first returns mean and median of variables Q1-Q5 by BU. It is the first level of classification which can be filtered by using WHERE = ( _TYPE_ = 1). The same analysis by AGE is shown against _TYPE_ = 2. When _TYPE_ = 3, SAS returns analysis by both the variables AGE and BU.  

```sas
Proc Means Data = test noprint;
Class Age BU;
Var q1 - q5 ;
Output out=F1 (where=(_type_=1) drop= AGE _FREQ_) mean= median= / autoname;
Output out=F2 (where=(_type_=2) drop= BU _FREQ_) mean= median= / autoname;
Output out=F3 (where=(_type_=3) drop= _FREQ_) mean= median= / autoname;
Run;
```

Using the NWAY option instructs PROC MEANS to output only observations with the highest value of _TYPE_ to the new data set it is creating. 

```sas
Proc Means Data = test nway noprint;
Class Age;
Var q1 - q5 ;
Output out=F1 mean=_mean1-_mean5 median=_median1-_median5;
Run;
```

 By default, PROC MEANS will analyze the numeric analysis variables at all possible combinations of the values of the classification variables. With the TYPES statement, only the analyses specified in it are carried out by PROC MEANS.  

 ```sas
Proc Means Data = test noprint;
Class Age BU Q1;
Types()
Age * BU
Age * BU * Q1;
Var q1 - q5;
Output out=F1 mean=_mean1-_mean5 max=_median1-_median5;
Run;
```

DESCENDTYPES Option : Orders rows/observations in the output data set by descending value of _TYPE_.  

```sas
Proc Means Data = test DESCENDTYPES noprint;
Class Age;
Var q1 - q5 ;
Output out=F1 mean=_mean1-_mean5 median=_median1-_median5;
Run;
```

### Multiple CLASS Statements  

Multiple CLASS statement permit user control over how the levels of the classification variables are portrayed or written out to new data sets created by PROC MEANS. It means any one of the classification variable can be displayed in descending order.  

```sas
Proc Means Data = test noprint;
Class Age / descending;
Class BU;Var q1 - q5 ;
Output out=F1 mean=_mean1-_mean5 max=_median1-_median5;
Run;
```

### Identifying Extreme Values of Analysis Variables using the IDGROUP Option  

```sas
proc means data=electric.electricity noprint nway;
class transformer;
var total_revenue ;
output out= F1
idgroup (max(total_revenue) out[2] (total_revenue)=maxrev) idgroup (min(total_revenue) out[2] (total_revenue)=minrev) sum= mean= /autoname;
run;
```

### Sample T-Test using PROC MEANS  

With PROC MEANS, we can perform hypothesis testing using sample t-test.  

Null Hypothesis - Population Mean of Q1 is equal to 0  

Alternative Hypothesis - Population Mean of Q1 is not equal to 0.  

```sas
proc means data = test t prt;
var Q1;
run;
```

The PRT option returns p-value which implies lowest level of significance at which we can reject null hypothesis. Since p-value is less than 0.05, we can reject the null hypothesis and concludes that mean is significantly different from zero.  

### Difference between PROC MEANS and PROC FREQ  

PROC MEANS is used to calculate summary statistics such as mean, count etc of numeric variables. It requires at least one numeric variable whereas Proc Freq does not have such limitation. In other words, if you have only one character variable to analyse, PROC FREQ is your friend and procedure to use.  

## PROC SUMMARY IN SAS: LEARN WITH EXAMPLES

This tutorial explains how to use PROC SUMMARY in SAS, along with examples.  

PROC SUMMARY is a powerful SAS procedure that can be used to calculate descriptive statistics for variables either across all observations or within specific groups of observations.  

### How to use PROC SUMMARY?  

Below is the syntax of PROC SUMMARY.  

```sas
PROC SUMMARY DATA=input_dataset;
   BY variable;
   CLASS variable(s) </ options>;
   VAR variable(s);
   OUTPUT OUT=output_dataset </ options>;
RUN;
```

Please refer to the explanation of the PROC SUMMARY statements below.  

DATA=input_dataset: Specifies the input dataset containing the variables you want to summarize.  

BY=variable: Specifies the classification variable. It calculates separate statistics for each BY group and returns the analysis for the variable in separate tables.  

CLASS variable(s): Specifies the list of classification variables. It calculates summary statistics for a variable grouped by the variable specified in this statement and returns analysis for the variable in a single table.  

VAR variable(s): Specifies the list of variables for which you want to calculate summary statistics. You can include multiple variables separated by spaces.  

OUTPUT OUT=output_dataset: Specifies the output dataset where the summarized results will be stored. You can choose a name for the output dataset.  

We are using SAS built-in dataset named CARS, which contains information about various cars, including their specifications and attributes.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9c0ec603-e963-4843-b2b1-08e06dbdb6e9)  

In the code below, we are summarising three numeric variables MSRP, INVOICE and LENGTH. The variable "MSRP" refers to the Manufacturer's suggested retail price of the car. The variable "INVOICE" refers to the invoice price of the car. The variable "LENGTH" refers to the length of the car.  

```sas
PROC SUMMARY DATA = SASHELP.CARS PRINT;
VAR MSRP INVOICE LENGTH;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c9dc9f25-a693-4764-9567-b488d8158ecb)  

By default, PROC SUMMARY produces N, Mean, Standard Deviation, Minimum and Maximum statistics.  

The PRINT option is used to print results in the output window. By default, PROC SUMMARY does not print results, hence it is required to include PRINT option to view results.  

### Common Statistical Options of PROC SUMMARY  

Below is a list of common statistical options of PROC SUMMARY.  

N: Number of observations  

MEAN: Mean  

STD: Standard Deviation  

MIN: Minimum value  

MAX: Maximum value  

NMISS: Number of missing observations  

SUM: Sum of observations  

MEDIAN: Middle value (50th percentile)  

P1: 1st percentile  

P5: 5th percentile  

P10: 10th percentile  

P90: 90th percentile  

P95: 95th percentile  

P99: 99th percentile  

Q1: First Quartile  

Q3: Third Quartile  

In the SAS program below, we are only showing 3 descriptive statistics - Number of missing observations, Mean and Median.  

```sas
PROC SUMMARY DATA = SASHELP.CARS NMISS MEAN MEDIAN PRINT;
VAR MSRP INVOICE LENGTH;
RUN;
```

Since the dataset does not have missing values, it is showing 0 against the variables under "NMISS" column.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d263caf6-6695-42ba-9572-58107c090459)  

To remove label column in PROC SUMMARY, you can use the option NOLABELS.  

```sas
PROC SUMMARY DATA = SASHELP.CARS NMISS MEAN MEDIAN PRINT NOLABELS;
VAR MSRP INVOICE LENGTH;
RUN;
```

### How to group rows using PROC SUMMARY?  

To group numeric variable by categorical variable, you can use the CLASS statement. It is similar to GROUP BY in SQL.  

```sas
PROC SUMMARY DATA = SASHELP.CARS MEAN PRINT NOLABELS;
CLASS TYPE;
VAR MSRP INVOICE;
RUN;
```

In the code above, we are calculating mean for "MSRP" and "INVOICE" by variable "TYPE".  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f69a325f-2ee0-4c28-9dcb-2e13734effa5)  

To remove "N Obs" column from the output, we can use NONOBS option.  

```sas
PROC SUMMARY DATA = SASHELP.CARS MEAN PRINT NOLABELS NONOBS;
CLASS TYPE;
VAR MSRP INVOICE;
RUN;
```

### How to change order of categorical variable?  

By default, PROC SUMMARY returns result in ascending order of classification variable. You can use DESCENDING option in the CLASS statement to arrange it in descending order.  

```sas
PROC SUMMARY DATA = SASHELP.CARS MEAN PRINT NOLABELS NONOBS;
CLASS TYPE  / DESCENDING;
VAR MSRP INVOICE;
RUN;
```

### How to save output of PROC SUMMARY in a dataset?  

You can use OUTPUT OUT=output_dataset to save output of PROC SUMMARY in a SAS Dataset. In the code below, output will be stored in the dataset named READIN. Here we are saving MEAN and MEDIAN of each of the 3 variables - MSRP, INVOICE and LENGTH. The AUTONAME option automatically assigns variable names in the output dataset.  

```sas
PROC SUMMARY DATA = SASHELP.CARS;
VAR MSRP INVOICE LENGTH;
OUTPUT OUT = READIN MEAN= MEDIAN = /AUTONAME;
RUN;
```

We can use AUTOLABEL option to automatically assigns label names in the variables in the output dataset.  

```sas
PROC SUMMARY DATA = SASHELP.CARS;
VAR MSRP INVOICE LENGTH;
OUTPUT OUT = READIN MEAN= MEDIAN = /AUTONAME AUTOLABEL;
RUN;
```

To assign custom variable names of your choice, you can use syntax -MEAN(original_variable)=new_variable_name.  

```sas
PROC SUMMARY DATA = SASHELP.CARS;
VAR MSRP INVOICE;
OUTPUT OUT = READIN MEAN(MSRP)=Avg_MSRP MEAN(INVOICE)=Avg_INVOICE;
RUN;
```

### How to interpret _TYPE_ column?  

By Default SAS creates two variables named _TYPE_ and _FREQ_ in the output dataset.  

```sas
PROC SUMMARY DATA = SASHELP.CARS;
CLASS TYPE;
VAR MSRP INVOICE;
OUTPUT OUT = READIN MEAN(MSRP)=Avg_MSRP MEAN(INVOICE)=Avg_INVOICE;
RUN;
```

_TYPE_=0 refers to the entire dataset which means descriptive statistics like frequency, mean are calculated based on the entire dataset.  

_TYPE_=1 refers to descriptive statistics of unique categories of a classification variable named TYPE. Similarly, if you have more than 1 classification variable in the CLASS statement, _TYPE_ will be incremented accordingly.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8ff21342-ca28-4dfa-a810-a865ff261fa5)  

The _FREQ_ variable contains the number of rows (frequency).  


### How to select or remove variables in PROC SUMMMARY?  

We can use DROP option to remove the variables _TYPE_ and _FREQ_. Similarly we can also use KEEP option to retain the specific variables.  

```sas
PROC SUMMARY DATA = SASHELP.CARS;
VAR MSRP INVOICE;
OUTPUT OUT = READIN (DROP = _TYPE_ _FREQ_) MEAN(MSRP)=AVG_MSRP MEAN(INVOICE)=AVG_INVOICE;
RUN;
```

### How to format and summarise using PROC SUMMARY?  

Suppose you need to categorise MSRP column into the following bands and then calculates average horsepower by the cohorts.  

Values from 0 to 20,000: Displayed as 'Up to 20K'  

Values from 20,000 to 50,000: Displayed as '20K-50K'  

Values from 50,000 to 100,000: Displayed as '50K-100K'  

Values greater than 100,000: Displayed as '100K or more'  

FORMAT statement in PROC SUMMARY tells SAS to apply user-defined formats before producing summary table.  

```sas
proc format;
value MSRP
0-20000 = 'Up to 20K'
20000-50000 = '20K-50K'
50000-100000 = '50K-100K'
100000-high = '100K or more';
run;

PROC SUMMARY DATA = SASHELP.CARS MEAN PRINT NOLABELS;
CLASS MSRP;
FORMAT MSRP MSRP.;
VAR HORSEPOWER;
RUN;
```

### Difference between PROC SUMMARY and PROC MEANS  

PROC SUMMARY and PROC MEANS are very similar, but they have a few differences. Here are the main differences between PROC SUMMARY and PROC MEANS.  

Proc MEANS by default produces printed output in the OUTPUT window whereas Proc SUMMARY does not. PROC SUMMARY requires PRINT option to print results in the output window.  

If you don't include the VAR statement in PROC MEANS, it analyses all the numeric variable whereas if you exclude the VAR statement in PROC SUMMARY, it produces a simple count of observations.  

Compare results of PROC MEANS and PROC SUMMARY when we are not using the VAR statement.  

```sas
PROC MEANS DATA=SASHELP.CARS;
CLASS MSRP;
RUN;

PROC SUMMARY DATA=SASHELP.CARS PRINT;
CLASS MSRP;
RUN;
```

## COMPLETE GUIDE TO PROC UNIVARIATE  

This tutorial explains how to explore data with PROC UNIVARIATE. It is one of the most powerful SAS procedure for running descriptive statistics as well as checking important assumptions of various statistical techniques such as normality, detecting outliers. Despite various powerful features supported by PROC UNIVARIATE, its popularity is low as compared to PROC MEANS. Most of the SAS Analysts are comfortable running PROC MEANS to run summary statistics such as count, mean, median, missing values etc, In reality, PROC UNIVARIATE surpass PROC MEANS in terms of options supported in the procedure. See the main difference between the two procedures.  

### PROC UNIVARIATE vs. PROC MEANS

1. PROC MEANS can calculate various percentile points such as 1st, 5th, 10th, 25th, 50th, 75th, 90th, 95th, 99th percentiles but it cannot calculate custom percentiles such as 20th, 80th, 97.5th, 99.5th percentiles. Whereas, PROC UNIVARIATE can run custom percentiles.

2. PROC UNIVARIATE can calculate extreme observations - the five lowest and five highest values. Whereas, PROC MEANS can only calculate MAX value.

3. PROC UNIVARIATE supports normality tests to check normal distribution. Whereas, PROC MEANS does not support normality tests.

4. PROC UNIVARIATE generates multiple plots such as histogram, box-plot, steam leaf diagrams whereas PROC MEANS does not support graphics.

### Basic PROC UNIVARIATE Code

In the example below. we would use sashelp.shoes dataset. SALES is the numeric (or measured) variable.  

```sas
proc univariate data = sashelp.shoes;
var sales;
run;
```

Default Output of PROC UNIVARIATE

1. Moments : Count, Mean, Standard Deviation, SUM etc  

2. Basic Statistics : Mean, Median, Mode etc

3. Tests for Location : one-sample t-test, Signed Rank test.

4. Percentiles (Quantiles)

5. Extreme Observations - first smallest and largest values against their row position.

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9c914768-1521-4d35-86fa-9d3e0facabe5)  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/feea22e5-33f9-44da-88ad-667505498ee2)  

### Example 1 : Analysis of Sales by Region

Suppose you are asked to calculate basic statistics of sales by region. In this case, region is a grouping (or categorical) variable. The CLASS statement is used to define categorical variable.  

```sas
proc univariate data = sashelp.shoes;
var sales;
class region;
run;
```

See the output shown below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/6e9de2f4-f9d9-45ac-9f2d-a63f7a7cc0ae)  

The similar output was generated for other regions - Asia, Canada, Eastern Europe, Middle East etc.  

### 2. Generating only Percentiles in Output

Suppose you want only percentiles to be appeared in output window. By default, PROC UNIVARIATE creates five output tables : Moments, BasicMeasures, TestsForLocation, Quantiles, and ExtremeObs. The ODS SELECT can be used to select only one of the table. The Quantiles is the standard table name of PROC UNIVARIATE for percentiles which we want. ODS stands for Output Delivery System.  

```sas
ods select Quantiles;
proc univariate data = sashelp.shoes;
var sales;
class region;
run;
```

### How to know the table names generated by SAS procedure

The ODS TRACE ON produces name and label of tables that SAS Procedures generates in the log window.  

```sas
ods trace on;
proc univariate data = sashelp.shoes;
var sales;
run;
ods trace off;
```

### How to write Percentile Information in SAS Dataset

The ODS OUTPUT statement is used to write output in results window to a SAS dataset. In the code below, temp would be the name of the dataset in which all the percentile information exists.  

```sas
ods output Quantiles = temp;
proc univariate data = sashelp.shoes;
var sales;
class region;
run;
ods output close;
```

### 3. Calculating Extreme Values

Like we generated percentiles in the previous example, we can generate extreme values with extremeobs option. The ODS OUTPUT tells SAS to write the extreme values information to a dataset named outlier. The "extremeobs" is the standard table name of PROC UNIVARIATE for extreme values.   

```sas
ods output extremeobs = outlier;
proc univariate data = sashelp.shoes;
var sales;
class region;
run;
ods output close;
```

### 4. Checking Normality

Most of the statistical techniques assumes data should be normally distributed. It is important to check this assumption before running a model.  

There are multiple ways to check Normality :  

Plot Histogram and see the distribution    
Calculate Skewness  
Normality Tests  

### I. Plot Histogram

Histogram shows visually whether data is normally distributed.  

```sas
proc univariate data=sashelp.shoes NOPRINT;
var sales;
HISTOGRAM / NORMAL (COLOR=RED);
run;
```

It also helps to check whether there is an outlier or not.  

### II. Skewness

Skewness is a measure of the degree of asymmetry of a distribution. If skewness is close to 0, it means data is normal.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/fb67c760-c8bf-412d-8c9d-7c22e7693939)  

A positive skewed data means that there are a few extreme large values which turns its mean to skew positively. It is also called right skewed.  

Positive Skewness : If skewness > 0, data is positively skewed. Another way to see positive skewness : Mean is greater than median and median is greater than mode.   

A negative skewed data means that there are a few extreme small values which turns its mean to skew negatively. It is also called left skewed.  

Negative Skewness : If skewness < 0, data is negatively skewed. Another way to see negative skewness : Mean is less than median and median is less  than mode.  

__Rule :__

If skewness < −1 or > +1, the distribution is highly skewed.  

If skewness is between −1 and −0.5 or between 0.5 and +1, the distribution is moderately skewed.  

If skewness > −0.5 and  <  0.5, the distribution is approximately symmetric or normal.  

```sas
ods select Moments;
proc univariate data = sashelp.shoes;
var sales;
run;
 ```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/442dd3f8-0b02-42af-9316-bc0b995b0d81)  

Since Skewness is greater than 1, it means data is highly skewed and non-normal.  

### III. Normality Tests

The NORMAL keyword tells SAS to generate normality tests.  

```sas
ods select TestsforNormality;
proc univariate data = sashelp.shoes normal;
var sales;
run;
  ```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/91629999-8f7a-4e83-83fe-ee2f92fd016a)  

The two main tests for normality are as follows :

### 1. Shapiro Wilk Test [Sample Size <= 2000]  

It states that the null hypothesis - distribution is normal.  

In the example above, p value is less that 0.05 so we reject the null hypothesis. It implies distribution is not normal. If p-value > 0.05, it implies distribution is normal.  

This test performs well in small sample size up to 2000.  

### 2. Kolmogorov-Smirnov Test [Sample Size > 2000]

In this test, the null hypothesis states the data is normally distributed.  

If p-value > 0.05, data is normal. In the example above, p-value is less than 0.05, it means data is not normal.  

This test can handle larger sample size greater than 2000.  

### 5. Calculate Custom Percentiles

With PCTLPTS= option, we can calculate custom percentiles. Suppose you need to generate 10, 20, 30, 40, 50, 60, 70, 80, 90, 100 percentiles.  

```sas
proc univariate data = sashelp.shoes noprint;
var sales;
output out = temp
pctlpts = 10 to 100 by 10 pctlpre = p_;
run;
```

The OUTPUT OUT= statement is used to tell SAS to save the percentile information in TEMP dataset. The PCTLPRE= is used to add prefix in the variable names for the variable that contains the PCTLPTS= percentile.  

Suppose you want to calculate 97.5 and 99.5 percentiles.  

```sas
proc univariate data = sashelp.shoes noprint;
var sales;
output out = temp
pctlpts = 97.5,99.5 pctlpre = p_;
run;
```

### 6.  Calculate Winsorized and Trimmed Means  

The Winsorized and Trimmed Means are insensitive to Outliers. They should be reported rather than mean when the data is highly skewed.  

Trimmed Mean : Removing extreme values and then calculate mean after filtering out the extreme values. 10% Trimmed Mean means calculating 10th and 90th percentile values and removing values above these percentile values.  

Winsorized Mean : Capping extreme values and then calculate mean after capping extreme values at kth percentile level. It is same as trimmed mean except removing the extreme values, we are capping at kth percentile level.  

Winsorized Mean

In the example below, we are calculating 20% Winsorized Mean.  

```sas
ods select winsorizedmeans;
ods output winsorizedmeans=means;
proc univariate winsorized = 0.2 data=sashelp.shoes;
var sales;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/15208b09-61cb-482f-aaf4-2684dffcd379)  

Percent Winsorized in Tail : 20% of values winsorized from each tail (upper and lower side)  

Number Winsorized in Tail : 79 values winsorized from each tail  

Trimmed Mean

In the example below, we are calculating 20% trimmed Mean.  

```sas
ods select trimmedmeans;
ods output trimmedmeans=means;
proc univariate trimmed = 0.2 data=sashelp.shoes;
var sales;
run;
```

### 7. Calculate Sample T-test  

It tests the null hypothesis that mean of the variable is equal to 0. The alternative hypothesis is that mean is not equal to 0. When you run PROC UNIVARIATE, it defaults generates sample t-test in 'Tests for Location' section of output.  

```sas
ods select TestsForLocation;
proc univariate data=sashelp.shoes;
var sales;
run;
```

Since p-value is less than 0.05. we reject the null hypothesis. It concludes the mean value of the variable is significantly different from zero.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/6df82dc8-28d7-46d8-bd07-a1f34fe55d2b)  

### 8. Generate Plots

PROC UNIVARIATE generates the following plots :  

Histogram  
Box Plot  
Normal Probability Plot  

The PLOT keyword is used to generate plots.  

```sas
proc univariate data=sashelp.shoes PLOT;
var sales;
run;
```

## SAS PROC CONTENTS: LEARN WITH EXAMPLES

In this tutorial, we will cover how to use PROC CONTENTS in SAS, along with examples.

### What does PROC CONTENTS do?  

The PROC CONTENTS procedure provides a summary of a dataset's contents, including details such as variable names, types, and attributes (such as formats, informats, and labels). It also tells you the number of observations and variables present in the dataset, as well as the creation date of the dataset.  

Below is the syntax for PROC CONTENTS  

```sas
PROC CONTENTS DATA= dataset_name;
RUN;
```

Here, we are using the built-in SAS dataset named CARS from the SASHELP library. Our goal is to explore this dataset using the PROC CONTENTS procedure.  

```sas
PROC CONTENTS DATA = SASHELP.CARS;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c136c894-ec9f-4943-bcd8-a4d3169cbb36)  

__1 Observations__ : The number of rows in the dataset. The dataset "CARS" from the SASHELP library contains 428 observations.  

__2 Variables__ : The number of columns in the dataset. The dataset "CARS" from the SASHELP library contains 15 variables.  

__3 Created__ : The dataset's creation date and time.  

### Variables Summary  

Here is the summary of variables in the dataset provided by PROC CONTENTS.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a094b989-8067-42a3-b413-fb9df449fed9)  

#: Represents the original order of the variable in the dataset. PROC CONTENTS displays variables in alphabetical order by name, rather than their original order of appearance in the dataset.  

Type: Indicates whether the variable is numeric (Num) or character (Char).  

Len: Refers to length of variables.  

Format: Displays the format applied to the variables' values when printed on the output window.  

Informat: Represents the format used to read the variables' data in SAS.  

Label: Displays the labels of variables. Please note that these are not value labels.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f3718445-cf3c-442b-96ad-4f9d56096e3e)  

Sortedby: Displays the variable(s) by which the dataset is sorted.  

Validated: It shows YES if PROC SORT/SQL sorted the dataset. Else NO.  

Character Set: The character set used to sort the data, can be ASCII, EBCDIC, or PASCII.  

### VARNUM Option  

By default, PROC CONTENTS lists variables in alphabetical order. However, when using the VARNUM option, SAS displays the variables in the order they appear in the dataset.  

```sas
proc contents data=sashelp.cars varnum;
run;
```

### How to display only Variable Names using PROC CONTENTS  

To display only the variable names using PROC CONTENTS, you can specify the SHORT option. This option restricts the output to only the variable names.  

```sas
proc contents data=sashelp.cars short varnum;
run;
```

### How to run PROC CONTENTS on the entire library  

To run PROC CONTENTS on all the datasets in a SAS library, we can use the keyword _ALL_.  

```sas
proc contents data=work._all_;
run;
```

### How to save output of PROC CONTENTS in a dataset   

We can use the NOPRINT option to disable the printing of output. The OUT= option is used to create a new dataset and save the output in that dataset.  

```sas
proc contents data=sashelp.cars noprint out=readin;
run;
```

## SAS : PROC TRANSPOSE WITH EXAMPLES

This tutorial explains how to use the PROC TRANSPOSE procedure in SAS, along with examples.  

### What does PROC TRANSPOSE do?   

PROC TRANSPOSE in SAS is useful when you want to reshape your data. For example, if your data is in a vertical format but you want to convert it into a wide/horizontal format, PROC TRANSPOSE can do this task easily.  

You can transpose data through data step technique but it would require writing complex code that can be time consuming to develop and test. Hence it is recommended to use the TRANSPOSE procedure to transpose your data in SAS.  

### Sample Data Set  

Let's create sample data which is used for explaining the TRANSPOSE procedure.
Suppose you have data for students with their marks in respective subjects. In the data set, you have three variables 'Name', 'Subject' and 'Marks'. See the table below showing this data.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8e654cea-9ac1-4d2f-8f20-36792f5b2364)  

### Create data set in SAS  

To see this data in SAS data set format, run the following code -  

```sas
data transp;
input Name $ Subject $ Marks;
cards;
Samma Maths 96
Sandy English 76
Devesh German 76
Rakesh Maths 50
Priya English 62
Kranti Maths 92
William German 87
;
run;
```

It creates a data set named 'TRANSP' which is stored in WORK library.  

### Simplest Form of PROC TRANSPOSE  

```sas
proc transpose data = transp out= outdata;
run; 
```

The above code creates a data set called outdata which contains values of variable 'Marks' stored in horizontal (wide) format. In other words, it transposes only variable i.e. Marks (which is numeric). It is because by default, PROC TRANSPOSE transposes all numeric variables in the data set.  

Output Data Set  

The output of the data set looks like below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f0bec167-dd55-496e-82a8-d6db8e562e61)  

### Options in PROC TRANSPOSE  

The NAME= option allows you to change the name of the _NAME_ variable. It is the name of the variable that is transposed.  

The PREFIX= option allows you to change the prefix "COL". It is prefix to the transposed values.  

```sas
proc transpose data = transp name=VarName prefix=Student out= outdata;
run;
```

Observe the above code with the previous section code - There are two changes in the code above that are : specifying name 'VarName' to the variable Name. The other change is adding a prefix 'Student' to the transposed marks.  

Output Data Set  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/56d8fb3a-1cdd-4d3c-814e-d87057328bc9)  

### Statements in PROC TRANSPOSE  

ID -[Move to Column Name] It allows you to include the values of a variable as variable names in the output data set. In other words, it tells SAS to give the variable names in the output file which were observations (rows) values in a variable in the input data set. If the variable in the ID statement is numeric, an underscore will be put by default at the beginning of the variable name. Instead of a default '_', you can use PREFIX= option to give a specific prefix which can be any character value.For example, you want to add 'Height' as a prefix which would create variables like 'Height20' 'Height30'.  

BY -It allows you to transpose data within the combination of the BY variables. The BY variables themselves aren’t transposed. The variables need to be sorted before running PROC TRANSPOSE. You can sort the variables with PROC SORT.  

VAR -[Transpose Column] It lists the actual data that needs to be transposed. If you do not include a VAR statement, the procedure will transpose all numeric variables that are not included in a BY statement or a ID statement. If youwant to transpose a character variable, a VAR statement is required.  

Example 2 : Give name to transposed columns  

Suppose you want to have actual students' name instead of 'Student1 Student2 etc' in the variable names. You can use ID statement to accomplish this task. Check out the code below -  

```sas
proc transpose data = transp name=VarName out= outdata;
id name;
run;
```

Output Data Set  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2cd72c81-fdc0-4ba5-927d-7d07cd663166)  

In this case, the variable 'name' is used for naming variables.  

Example 3 : Restructure Data  

Suppose you want to change the structure of data in the manner in which the row values of the variable 'Subjects' come at top i.e. heading / variable names and marks under the respective column in the output dataset.  

In this case, we need to sort the data as we are going to use BY processing in PROC TRANSPOSE.  

```sas
proc sort data = transp;
by Name;
run;

proc transpose data = transp out= outdata;
by Name;
id Subject;
var Marks;
run;
```

In this example, we are specifying variable Name in the BY option which means we do not want to transpose this variable.. The variable Marks specified in the VAR option implies this variable is actually transposed and shape of the data format would be changed in the output data set.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1ac94277-217e-4c8e-a247-fa7053ce044d)  

If you look at the output above, everything looks perfect except the variable '_NAME' which is not relevant. We can eliminate this variable with DROP= option.  

```sas
proc transpose data = transp out= outdata (drop=_name_);
by Name;
id Subject;
var Marks;
run;
```

Is SORTING required when i use BY statement?  

Answer is No. The NOTSORTED option tells SAS that data is not sorted and it is not required to sort it. If you don't specify NOTSORTED option, you need to sort the variable that is listed in BY statement.  

```sas
proc transpose data = transp out= outdata (drop=_name_) ;
by Name NOTSORTED;
id Subject;
var Marks;
run;
```

Output Data Set  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8a3bc907-4c30-418c-9bae-a4f0a16df64e)  

See the above output. You must have observed the names are not sorted in the output data set.  

How to use Two Variables in ID Statement  

We can use DELIMITER= option to separate values of two variables specified in the ID statements. In this example, we have used underscore ( _ ) as a delimiter.    
```sas
proc transpose data = transp delimiter=_ name=VarName out= outdata;
id name subject;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b3c9a07f-cb05-4c42-8007-2cef7cca8344)  

### How to label the Output Variables with PROC TRANSPOSE  

The ID statement tells SAS to provide variable names to the variables after the transpose. But if you want to label these variables, you can use IDLABEL statement which picks labels from a variable from the input file.  

```sas
proc transpose data=temp out=outdata prefix=height;
by id;
var scores;
id height;
idlabel heightl;
run;
```
 
Practice Example  

Suppose you have monthly financial data. You need to convert long formatted data to wide format.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/6d3db2f2-4d23-498c-b601-e57439b2b366)  

SAS Code

```sas
data example;
input ID Months Revenue Balance;
cards;
101 1 3 90
101 2 33 68
101 3 22 51
102 1 100 18
102 2 58 62
102 3 95 97
;
```

Output  

The final output should like the following table.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/219e0821-f656-4afa-8e63-ddfb4e9719dd)  

Solution :  

```sas
proc transpose data=example out= Output1 (drop = _NAME_) prefix=balance_;
id months;
var balance;
by ID;
run;
```

In this case, the variable 'Month' specified in ID statement is a numeric variable. Hence, we have added prefix 'balance_' to make it to the desired output.  

If you want to see your output looks like the data shown in the image below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5546b73a-ed2a-43f9-8ecf-799c344f2d6a)  

```sas
proc transpose data=example out=out1 name=variable prefix=x;
by id months;
run;
```

In this case, the information of the 'Revenue' and 'Balance' variables are stacked to one variable. And the variable 'x1' refers to the values corresponding to it.  

Exercise : Try yourself!  

Suppose you have three columns - ID, Date and Flag. ID refers to unique value assigned to customers. Flag refers to status of customer as on date whether it is active or not. Input Dataset looks like the image shown below.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/fed80ad1-a5dc-4ceb-b4e4-17c20ac1a870)  

```sas
data readin;
   input ID date ddmmyy8. Flag$;
   format date ddmmyy8.;
   cards;
1 30-12-16 Y
1 30-08-17  N
1 31-08-18  N
2 30-06-16 Y
2 31-12-18 N
;
run;
```

Desired Output should be appeared like the table below. Post your solution in the comment box below.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f48d069e-246b-43ce-ad87-b5a06cc32c2a)  

## SAS : PROC RANK

This tutorial explains how to calculate rank for one or more numeric variables with PROC RANK. In SAS, there are multiple ways to calculate rank overall or by a grouping variable. In data step, it can be done via retain statement. SAS made it easy to compute rank with PROC RANK.  

### Create Sample Data  

```sas
data temp;
input ID Gender $ Score;
cards;
1 M 33
2 M 94
3 M 66
4 M 46
5 F 92
6 F 95
7 F 18
8 F 11
;
run;
```

### Compute rank of numeric variable - "Score"   

```sas
proc rank data= temp out = result;
var Score;
ranks ranking;
run;
```
 
Notes :   

The OUT option is used to store output of the rank procedure.  

The VAR option is used to specify numeric variable (s) for which you want to calculate rank  

The RANKS option tells SAS to name the rank variable  

By default, it calculates rank in ascending order.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f291b19a-96bc-46b2-a374-470fa7e5f4c2)  

### Reverse order of ranking (Descending)

Suppose you need to assign the largest value of a variable as rank 1 and the last rank to the lowest value. The descending keyword tells SAS to sort the data in descending order and assign rank to the variable accordingly.  

```sas
proc rank data= temp descending out = result;
var Score;
ranks ranking;
run;
```

### Percentile Ranking (Quartile Rank)

Suppose you need to split the variable into four parts, you can use the groups option in PROC RANK. It means you are telling SAS to assign only 4 ranks to a variable.  

```sas
proc rank data= temp descending groups = 4 out = result;
var Score;
ranks ranking;
run;
```

Note :   

GROUPS=4 for quartile ranks, and GROUPS=10 for decile ranks, GROUPS = 100 for percentile ranks.  

### Ranking within BY group (Gender)

Suppose you need to calculate rank by a grouping variable. To accomplish this task, you can use the by statement in proc rank. It is required to sort the data before using by statement.  

```sas
proc sort data = temp;
by gender;
run;
proc rank data= temp descending out = result;
var Score;
ranks ranking;
by Gender;
run;
```

### How to compute rank for same values

Let's create a sample dataset. See the variable score having same values (33 appearing twice).  

```sas
data temp2;
input ID Gender $ Score;
cards;
1 M 33
2 M 33
3 M 66
4 M 46
;
run;
```

Specify option TIES = HIGH | LOW | MEAN | DENSE in PROC RANK.  

```sas
proc rank data= temp2 ties = dense out = result;
var Score;
ranks rank_dense;
run;
```

LOW - assigns the smallest of the corresponding ranks.  

HIGH - assigns the largest of the corresponding ranks.  

MEAN - assigns the mean of the corresponding ranks (Default Option).  

DENSE - assigns the smallest of the corresponding rank and add +1 to the next rank (don't break sequence)  

See the comparison between these options in the image below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5deb353d-db49-47c5-b1eb-b6ac1d0fb7ea)  

## PROC DATASETS IN SAS: LEARN WITH EXAMPLES  

This tutorial shows how to use PROC DATASETS in SAS, along with examples.  

The PROC DATASETS statement in SAS is used to manipulate SAS datasets. It can be used to perform a variety of operations on datasets, such as copying, renaming, deleting, and modifying datasets.  

### Syntax of PROC DATASETS  

The syntax of PROC DATASETS is as follows:  

```sas
proc datasets library=mylibrary;
run;
quit;
```

If you don't use the library= option, SAS will consider the WORK library as the default library for managing datasets in the PROC DATASETS.  

### Sample Datasets  

Let's create two datasets in the WORK library from the SASHELP library. These datasets will be used in further examples.  

```sas
data cars;
set sashelp.cars;
run;

data class;
set sashelp.class;
run;
```

### Display a list of all the datasets in a library  

To view a list of all the datasets in a specific library, you can use PROC DATASETS. Here we are looking in the WORK library.  

```sas
proc datasets library=work;
run;
quit;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/de09f98d-f4de-475e-91b1-a5c92c8b4d4a)  

In the image above, the first two highlighted ones are datasets. Others are item store and catalogs. Item store is a binary system file created by the SAS. Catalogs are SAS files that can contain macros, formats, and other SAS objects.  

To display only datasets in the results window, you can use memtype=data.  

```sas
proc datasets library=work memtype=data;
run;
quit;
```

### How to copy all the datasets in a library  

Suppose you have a library named mylib and you want to copy all the datasets from the WORK library to "mylib" library.  

Create library if you already don't have. Specify location in the library as per your location.  

```sas
libname mylib '/home/deepanshu88us0/';
```

```sas
proc datasets;
copy in=work out=mylib;
run;
quit;
```

### How to copy all the datasets from a library  

Suppose you have a library named mylib and you want to copy all the datasets from the WORK library to "mylib" library.  

Create library if you already don't have. Specify location in the library as per your location.  

```sas
libname mylib '/home/deepanshu88us0/';
```

```sas
proc datasets;
copy in=work out=mylib;
run;
quit;
```

### How to copy some datasets from a library  

Suppose you want to copy only specific datasets from the WORK library to "mylib" library. You can mention them in the SELECT statement.  

```sas
proc datasets;
copy in=work out=mylib;
select cars class;
run;
quit;
```

### How to move datasets from a library  

We can use the MOVE option in the COPY statement to move a dataset from one library to another. HERE "CARS" dataset has been moved to the "mylib" library from the "work" library.  

```sas
proc datasets;
copy in=work out=mylib move;
select cars;
run;
quit;
```

To check if the moved dataset is available in the WORK library, we can run the command below. We can see that CARS dataset is no more available in the WORK library. "MOVE" option is like cut-paste from a old libarry to a new library.  

```sas
proc datasets library=work memtype=data;
run;
quit;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2cdc7024-436c-4ff7-89ef-15595958a89f)  

### How to delete the whole library in SAS  

We can use the KILL option in PROC DATASETS to delete the whole SAS library. Here we are removing the library named "mylib".  

```sas
proc datasets lib=mylib kill;
run;
quit;
```

### How to delete datasets from a library  

We can use the DELETE statement in the PROC DATASETS to delete specific datasets from a SAS library. Here we are deleting "CLASS" dataset from the "WORK" library.  

```sas
proc datasets lib=work memtype=data;
delete class;
run;
quit;
```

### How to rename SAS dataset  

We can use the CHANGE old-dataset-name = new-dataset-name statement in the PROC DATASETS procedure to rename a SAS dataset. In the code below, we are renaming "cars" dataset to "automobiles".  

```sas
data cars;
set sashelp.cars;
run;

proc datasets lib=work nolist;
change cars = automobiles;
quit;
run;
```

### How to combine SAS dataset  

In the code below, we are combining CARS dataset to itself (doubling it). You can follow the same approach if you have two datasets with the same variables and you need to combine them.  
  
Appended the file WORK.CARS to itself.  

There were 428 observations read from the data set WORK.CARS.  

Added 428 observations.  
  
The data set WORK.CARS now has 856 observations.  

```sas
data cars;
set sashelp.cars;
run;

proc datasets lib=work;
append out=cars data=cars;
run;
quit;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f68bf524-e1fe-4717-8034-0aba45df584a)  


## HOW TO USE PROC COMPARE IN SAS (WITH EXAMPLES)

In this tutorial, we will cover how to use PROC COMPARE in SAS, along with examples.  

### Introduction : PROC COMPARE  

PROC COMPARE in SAS is used to compare the contents and structure of two datasets. It returns a summary of both the similarities and differences found between two datasets.  

### Syntax of PROC COMPARE  

The syntax of PROC COMPARE is as follows:  

```sas
proc compare
 base = data1
 compare = data2;
run;
```

This compares the datasets data1 and data2 and displays the differences between them. By default, PROC COMPARE compares all the variables in the datasets.  

Let's compare two built-in SAS datasets: sashelp.class and sashelp.classfit.  

```sas
proc compare
 base = sashelp.class
 compare = sashelp.classfit;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/7e4cace8-bd34-46ef-92d0-5086889842fa)  

### Dataset Summary  

In the dataset summary section, it shows the comparison of the structure of both the datasets and returns the following analysis.  

Dataset Creation Dates  

Dataset Modification Dates  

Number of Variables  

Number of Observations   

Labels  

### Variable Summary  

In the Variable Summary section, it shows how many variables which are common in both the datasets and how many variables are in one dataset but not in the other dataset.  

### Observation Summary  

In the Observation Summary section, it displays how many observations are in both the datasets and how many of them have equal or unequal values in some or all of the variables.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/56158e30-5b6b-43c8-9f34-952c246571a5)  

### Values Comparison Summary  

In the "Values Comparison summary" section, it displays summary about the variables that either have all values exactly equal or contain some unequal values.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/57e9883c-def9-401c-8833-aa6a1932f925)  

### How to Compare Specific Variables  

You can use the VAR statement in PROC COMPARE to compare specific variables of both the datasets. Please note that the initial summary about dataset and variables remain unchanged. You should focus on the Value Comparison Results. In the code below, we are comparing "name" variable in both the datasets.  

```sas
proc compare
 base = sashelp.class
 compare = sashelp.classfit;
 var name;
run;
```

### How to Compare Only Structure of Datasets  

By using NOVALUES option in PROC COMPARE, we can tell SAS not to compare values between the two datasets. In short it returns only the similarities and difference in the variables, not values. The LISTVAR option is used to list the variables which are in one dataset but not in the other dataset.  

```sas
proc compare
 base = sashelp.class
 compare = sashelp.classfit
 novalues listvar;
run;
```

## SAS : COMBINING AND APPENDING DATASETS  

This tutorial explains how to combine / append two data sets in SAS. In SAS, there are various method to append data sets. It can be done with data step method, PROC SQL as well as procedure called PROC APPEND to accomplish it. It is one of the most frequently data manipulation task in analytics work. For example, you have multiple human records files from various departments of your company and you are asked to join them so that there would be a single file containing information of all the departments.  

### 1. Concatenate two data sets vertically / Appending Data Sets  

Let's create two data sets - Data Set I and Data Set II  

```sas
Data Dataset1;
Input Name $ Score;
cards;
David 30
Ram 25
Sam 74
Sandy 36
;
run;

Data Dataset2;
Input Name $ Score;
cards;
Ken 36
Obama 74
Raj 30
Shyam 25
;
run;
```

__Append / Concatenate two data sets__  

```sas
Data Stack;
Set Dataset1 Dataset2;
Run;
```

__Output__  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/341207a9-908f-432a-8c26-5037c465449e)  

__Note__ : The stacked data set is not sorted because we have not used BY statement.  

### 2. Interleaving SAS Data Sets (Sorted Stacked Data Set)  

Interleaving combines individual sorted SAS data sets into one sorted data set. You interleave data sets using a SET statement and a BY statement in a DATA step.  

Make sure data sets are sorted before appending datasets. Datasets can be sorted with PROC SORT.  

```sas
proc sort data = dataset1;
by name;
run;
proc sort data = dataset2;
by name;
run;
```

```sas
Data Stack1;
Set Dataset1 Dataset2;
By Name;
Run;
```

__Output__

![image](https://github.com/Deepak2k20/SAS/assets/65231118/e4356cc6-d069-4809-8dd1-eaa817595727)  

### 3. PROC SQL for concatenating two data sets  

OUTER UNION CORR keyword is used in PROC SQL to concatenate two data sets. The CORR tells SAS to append data sets by name (not by column position).  

```sas
PROC SQL;
CREATE TABLE stackk AS
SELECT *
FROM Dataset1
OUTER UNION CORR 
SELECT *
FROM Dataset2
ORDER BY Name;
QUIT;
```

The output of PROC SQL is same as the output of previous example.  

### 4. PROC APPEND to concatenate data sets  

In PROC APPEND, the data set specified in BASE= option refers to a data set in which other data set would be added or appended. In log, it writes 'Appending Dataset2 to Dataset1' for our example. After running this code, the dataset1 contains 8 records ( 4 from the original 'dataset1' file and 4 from the dataset2)  

```sas
proc append base=dataset1 data=dataset2;
run;
```

 If you want to append data and store it to another dataset, you can run PROC APPEND twice to do it. In the first PROC APPEND, it would create a base table ALLDATA (as specfied in the code below).  If the dataset ALLDATA does not already exist, it would be automatically created by SAS.  

 ```sas
proc append base=alldata data=dataset1;
run;
proc append base=alldata data=dataset2;
run;
```
 
### Is PROC APPEND faster?  

PROC APPEND is faster than SET statement or PROC SQL UNION because it only reads in the data set being appended (i.e. the dataset identified by the syntax ‘DATA=’).  

### Application of PROC APPEND  

PROC APPEND is most useful when you use it in a macro. For example, you create a macro in which there is a loop for calculation of some metrics of multiple variables. In each iteration, it returns a data set which needs to be appended with the output of subsequent iterations so that once loop completes all the iterations, we would have complete data set.  

### Important Point  

Suppose you have two datasets having same variable names but the length of the common variable is different, It would throw a warning and it would not append datasets. To workaround this issue, we can use FORCE option to append the data sets.  

```sas
proc append base=dataset1 data=dataset2 force;
run;
```
  
### 5. Usage of Multiple Set Statement  

Instead of specifying multiple data sets in a single SET statement, we can also multiple SET statements but the result /output would be totally different. See the output shown below -  

```sas
Data Stack3;
Set Dataset1;
Set Dataset2;
Run;
```

__Warning__ : It overwrites data.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/80f9c792-870a-4398-9fa1-c9ec042f1cc1)  

The question arises " why do we use multiple set statement if it overwrites data". The next topic describes the application of multiple set statement.  

### Application of Multiple Set Statement  

It combines data sets by adding column from the other dataset. Unlike INNER/LEFT Joins, it does not require any primary or unique key to join two datasets.  

Lets create a new data set - Data Set 3  

```sas
Data Dataset3;
Input Section $;
cards;
A
B
C
D
;
run;
```

```sas
Data Stack3;
Set Dataset1;
Set Dataset3;
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/25a38fb2-99b9-4eb5-8710-3c2061ce7cca)  

### Append Data : Many to Many Relationship  

Multiple SET statement can also produce cartesian product of two tables. It can be done with POINT= option.  

```sas
Data Stack2;
set Dataset1;
do i=1 to num;
set Dataset3 nobs=num point=i;
if i=i then output;
end;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/de038ab2-a0dc-4e3b-b804-4df52fbfb569)  

## SAS PROC REPORT: LEARN WITH EXAMPLES  

In this tutorial, we will cover how to use PROC REPORT in SAS, along with examples.   

### What does PROC REPORT do?  

PROC REPORT is a powerful procedure in SAS used for creating highly customizable tabular reports. It allows you to summarize, analyze, and present data in a structured format.  

Here are some key benefits of using PROC REPORT:

Tabular Reporting: PROC REPORT enables you to create tabular reports that organize data in rows and columns.  

Grouping and Breaks: You can group data based on one or more variables and create break lines that visually separate the groups. This helps in organizing and summarizing data by different categories.  

Calculated Columns: PROC REPORT allows you to create new columns in the report that are calculated based on expressions or computations involving existing variables.  

Summary Statistics: You can calculate summary statistics such as sums, means, counts, minimums, maximums, and more for specific variables or groups using PROC REPORT.  

Conditional Formatting: PROC REPORT supports conditional formatting, allowing you to highlight specific cells, rows, or columns based on certain conditions.  

Customization and Formatting: PROC REPORT provides a wide range of options for customizing the appearance and layout of your report. You can control fonts, colors, borders, spacing, alignment, and other formatting aspects to create visually appealing reports.  

### Syntax of PROC REPORT  

The basic syntax of PROC REPORT is as follows.  

```sas
proc report data=dataset-name;
column variable1 variable2 variable3;
run;
```

data=dataset-name: Specify the dataset that contains the data you want to include in the report.  

column: The COLUMN statement specifies the order and variables to be displayed in the report.  

### Sample Dataset  

Let's create a sample dataset for the examples in this tutorial.  

```sas
data mydata;
input product$ country$ transactions country;
cards;
Electric USA 35 3650
Electric UK 25 2450
Electric France 16 680
Electric India 29 3150
Cosmetic USA 15 3350
Cosmetic UK 31 2750
Cosmetic France 26 990
Cosmetic India 41 3050
Garments USA 125 4350
Garments UK 121 2150
;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/44e9f645-8f2b-4ed2-8737-346a981647ea)  

### Print Data  

The basic syntax of PROC REPORT prints data like PROC PRINT procedure. In the code below, we are using the PROC REPORT procedure to create a tabular report with three columns: "product", "country" and "sales"  

```sas
proc report data=mydata;
column product country sales;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/80f888c1-ebd9-467d-9843-860f4173b545)  

### How to Customize Columns in a Report  

You can change the headers of the columns using the display option in the define statement. This will change how the column names appear in the report without modifying the actual variable names. In this example, "Revenue" is the new header label assigning to the "sales" column.  

You can format the values in a column using the format option in the define statement. In the code below, dollar format is being applied.  

```sas
proc report data=mydata;
column product country sales;
define sales / display "Revenue" format=dollar8.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d25fd191-2444-435a-a3ae-bd08821a99bb)  

### How to Group Data in a Report  

group: This option specifies that the "product" variable should be used for grouping the data in the report. "Categories" is the new header label assigned to the "product" column.   

```sas
proc report data=mydata;
column product country sales;
define sales / display "Revenue" format=dollar8.;
define product / group "Categories";
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8ab4da0c-4e62-42d3-838d-1dabf386cfc5)  

### How to Summarize Data in a Report  

By using PROC REPORT, you can produce descriptive statistics such as sum, mean, min, max etc. In this example, we are calculating sum of sales by countries.  

```sas
proc report data=mydata;
column country sales;
define country / group "Locations";
define sales / analysis sum "Sum of Sales" format=dollar8.;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b4bd8f8e-cb45-4f33-91dc-81b7cc212110)  

### How to Transpose a Variable in a Report  

across: This option specifies that the "country" variable should be used for creating a separate header above the data. "Location" is the new header label assigned to the "country" column.  

```sas
proc report data=mydata;
column product country sales;
define sales / display "Revenue" format=dollar8.;
define product / group "Categories";
define country / across "Location";
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8e98c976-8d3d-4b3f-b9a6-32e548b2ebe7)  

### How to Create Grouped Columns in a Report  

(transactions sales): The "transactions" and "sales" variables will be nested under the "country" column.  

```sas
proc report data=mydata;
column product country, (transactions sales);
define product / group "Categories";
define country / across "Location";
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/abd988af-8a6f-477e-95dc-baf3214b3e4e)  

### How to add Grand Total in PROC REPORT   

```sas
proc report data=mydata;
column product country, (transactions sales);
define product / group "Categories";
define country / across "Location";
compute after;
product = 'Total';
endcomp;
rbreak after /summarize;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/96dc5c12-f05d-4f0c-80a4-a38bc3941e4a)  

compute after: The COMPUTE AFTER block is used to insert a custom computation after each group of data.  

product = 'Total';: This line assigns the value "Total" to the "product" variable. It will display "Total" as a row label after each group of data.  

rbreak after: The RBREAK statement is used to create a row break after each group of data.  

/summarize: The SUMMARIZE option in the RBREAK statement indicates that summary statistics, such as sums, will be displayed for the numeric variables in the report.  

### Conditional Formatting in PROC REPORT  

The following code defines a custom format named "mycolor" using PROC FORMAT and then uses it to format the background color of the "transactions" column in the PROC REPORT. If number of transactions are below 30, they will be formatted with a "lightred" background color, else with a "lightgreen" background color.  

```sas
proc format;
value mycolor
Low-30 = 'lightred'
30-High = 'lightgreen';
run;

proc report data=mydata;
column product country, (transactions sales);
define product / group "Categories";
define country / across "Location";
compute after;
product = 'Total';
endcomp;
rbreak after /summarize;
compute transactions;
call define
(_col_,'style',"STYLE=[BACKGROUND=mycolor.]");
endcomp;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c2c5b637-c5ca-4d6e-957c-2f7d9655e770)  

### How to Style PROC REPORT  

```sas
proc report data=mydata
style(column)=[background=lightgrey]
style(header)=[background=grey color=white];
column product country, (transactions sales);
define product / group "Categories";
define country / across "Location";
compute after;
product = 'Total';
endcomp;
rbreak after /summarize;
compute transactions;
call define
(_col_,'style',"STYLE=[BACKGROUND=mycolor.]");
endcomp;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/634c7645-cc26-401c-882b-5bee83b0c21f)  

style(column): This style option applies to all data cells in the columns of the report.  

[background=lightgrey]: This specifies the background color for the data cells in all columns. In this case, the background color will be "lightgrey."  

style(header): This style option applies to all header cells in the report.  

[background=grey color=white]: This specifies the background color for the header cells and also changes the font color to "white." In this case, the background color of the headers will be "grey," and the text color will be "white."  

## SAS : PROC TABULATE EXPLAINED  

### What does Proc Tabulate do?  
  
Proc Tabulate is mainly used to create a professional looking table.  

__Terminologies__  

VAR : The Var statement tells SAS that these variables are analysis variables. They must be numeric. They are used to create summary statistics.  

CLASS : The Class statement tells SAS that these variables are categorical variable  

TABLE : The Table statement tells SAS which variables are row expressions, which are column expressions.  

Table Salary; -  If there are no commas in the TABLE statement, SAS assumes you are only defining the column expression.   
 
Table Gender, Salary; -  If there is one comma, then it is a row expression before comma and column expression after comma.  

### Create a dataset  

```sas
Data test;
Input T1 T2 T3 T4 T5 Age BU;
Cards;
1 5 2 3 4 3 3
4 5 2 1 2 1 3
3 4 4 3 2 3 2
4 3 2 5 3 3 3
1 2 4 2 1 2 2
;
Run;
```

### Simple Table  

```sas
Proc tabulate data = test;
Var T1;                                                                                          
Table T1;          
Run;
```

The output is shown in the image below -

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5a5386f3-cc03-46fa-86bd-3117d93b8a5d)  

By default, it calculates SUM for variables.  

### How to add different Statistics Options

The asterisk * is used to add statistical keywords.  
 
Suppose you want to calculate COUNT for T1 variable :  

```sas
Proc tabulate data = test;
Var T1;
Table T1 * N;
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/95d56a73-a1f9-4b02-8214-4101460ac587)  

Suppose you want to calculate both COUNT and SUM for T1 variable :  

```sas
Proc tabulate data = test;
Var T1;
Table T1 * (N SUM);
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a15abe85-e020-4118-87cb-0713eecba32e)  

### Statistics Options  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9303887f-b75a-4860-83e3-a1dfd1ddbd0d)  

### Cross Tab

In the TABLE statement, row expression is specified first then followed by comma and then column expression.  

```sas
Proc Tabulate Data = test;
Class Age;
Var T1;
Table Age, T1 * (N COLPCTN);
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/834f5434-c258-4f18-88ad-04dc4d2f1204)  

### Transposed Format

```sas
Proc Tabulate Data = test;
Class Age;
Var T1;
Table T1, Age * (N ROWPCTN);
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/39c12a51-e2e2-4aff-81e1-5c0356330af7)  

### Label Variables and Statistics

The "=" equal sign is an operator most commonly used for formatting.  

```sas
Proc Tabulate Data = test;
Class Age;
Var T1;
Table Age, T1 = "Group I" * (N="Count" COLPCTN="%");
Run;
```

The above SAS program can be written as follows :  

```sas
Proc Tabulate Data = test;
Class Age;
Var T1;                                                                              
Keylabel N="Count" COLPCTN="%";
Table Age, T1 = "Group I" * (N COLPCTN);
Run;
```

The Keylabel statement will change the label of keywords. Both the above programs produce same output.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5a4fc36b-ddcf-4786-8be4-3c0b3572a6dd)  

### Shift the row header up

In order to hide variable or labels, you leave the label specification blank (i.e. =‘ ‘ ).  

```sas
Proc Tabulate Data = test;
Class Age;
Var T1;
Table Age=" ", T1 = "Group I" * (N="Count" COLPCTN="%") / box="Age";
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5ee3c69e-b5fe-4495-a9ec-508dcf4cb737)  

### Adding total rows and columns 

The ALL keyword is used to generate a sum total for rows or columns.  

```sas
Proc Tabulate Data = test;
Class Age;
Var T1;
Table Age ALL = "Grand Total" , T1 = "Group I" * (N="Count" COLPCTN="%");
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9bc018c3-694d-460a-a135-b6c027a3b4ee)  

### Two level data cuts

```sas
Proc tabulate data = test;
Class Age BU;
Var T1;
Table T1="Group I",(Age * BU="Business Unit") * (N="Count" ROWPCTN="%");
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/318c8561-ee0b-4d9f-89d2-66964d71f21e)  

In order to hide variable or statistic labels, you leave the label specification blank (i.e. =‘ ‘ ).   

```sas
Proc tabulate data = test;
Class Age BU;
Var T1;
Table T1="Group I",(Age=" " * BU="Business Unit") * (N="Count" ROWPCTN="%");
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ab88a7c5-120c-419e-a7b8-6d69d77a8a1f)  

### Cell Formats

You can use the asterisk *  to associate the format modifier “F=” to the summary statistic.  

```sas
Proc tabulate data = test;
Class Age BU;
Var T1;
Keylabel N="Count" ROWPCTN="%";
Table T1="Group I",(Age * BU="Business Unit") * (N ROWPCTN * F=6.0);
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/47cb732d-b2b4-44ef-8d85-98892f8535a8)  

### Format Statement with Proc Tabulate  

```sas
Proc format;                                                                                                                          
value agefmt                                                                                                                          
1 = 'Under 18'                                                                                                                      
2 = '18 - 25'                                                                                                                        
3 = 'Over 25';                                                                                                                      
Run;                                                                                                                                  
                                                                                                                                     
Proc format;                                                                                                                          
value bufmt                                                                                                                          
1 = 'Analytics'                                                                                                                      
2 = 'Technology'                                                                                                                    
3 = 'Others';                                                                                                                        
Run;
                                                                                 
Proc tabulate data = test;
Format Age agefmt. BU bufmt.;
Class Age BU;
Var T1;                                                                                                                    
Keylabel N="Count" ROWPCTN="%";
Table T1="Group I",(Age * BU="Business Unit") * (N ROWPCTN * F=6.0);
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/e4792ca2-6521-41c1-851a-7fce60f73e72)  

### Three Dimensional Table  

```sas
Data test;
length BU $18.;
Input Location$ BU$ Gender$ Income;
Cards;
Delhi Analytics Male 5000
Mumbai Tech Female 45000
Delhi Analytics Male 37000
Chennai Tech Male 33000
Delhi Tech Male 5000
Chennai Analytics Male 15000
Mumbai Analytics Female 440000
Delhi Analytics Female 5000
Mumbai Tech Male 45000
Delhi Analytics Female 37000
Chennai Tech Female 33000
Delhi Tech Female 5000
Chennai Analytics Male 15000
;                                                                                                                                    
Run;
```

```sas
Proc tabulate data = test F=6.0;
Class Location BU Gender;
Var Income;
Table Location=" "*BU=" ", Gender * Income=" "*(N="Count" ROWPCTN="%") / Box="Location BU";
Run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c84c9ded-1d42-4af0-893b-c3aa0ced9e72)  

### Save output in a dataset  

```sas
Proc tabulate data = test out=test1;
Format Age agefmt. BU bufmt.;
Class Age BU;
Var T1;
Keylabel N="Count" ROWPCTN="%";
Table T1="Group I",(Age * BU="Business Unit") * (N ROWPCTN * F=6.0);
Run;
```

## SAS : USE OF MULTIPLE SET STATEMENTS  

In SAS, you can perform one-to-one reading with the help of multiple SET statements. It combines observations from two or more data sets into a single observation in a new data set.  

Suppose you have two very big datasets. You have IDs column in both the datasets. Each ID in the first dataset has a matching ID in the second one and they are in the same order. Your task is to merge these datasets but the usual method of data step merging doesn't work because it uses a lot of memory. Instead you can use the MULTIPLE SET Statements for merging them.  

```sas
DATA dat1;
INPUT id v1 v2;
CARDS;
1 10 100
2 15 150
3 20 200
;

DATA dat2;
INPUT id v3 v4;
CARDS;
1 1000 10000
2 1500 15000
3 2000 20000
4 800 30000
;
RUN;
```

```sas
DATA dat3;
set dat1;
set dat2;
RUN;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/60f17acc-b96d-4fc9-a092-174845a82cc9)  

The observations are combined based on their relative position in the data set.  

## SAS MERGING TUTORIAL (WITH EXAMPLES) 

This tutorial explains how to merge datasets in SAS. It explains the different types of joins with MERGE statement. Also it includes some special topics related to merging.  

### Introduction: Data Step Merge  

Data step merge is used to merge two or more datasets based on one or more common variables. It is performed using the MERGE statement within DATA step in SAS. It is similar to SQL joins.  

__Create 2 Sample Datasets__ 

The following SAS code is used to create two sample SAS datasets that will be used to demonstrate merging in SAS.    

```sas
Data A;
Input ID Name$ Height;
cards;
1 A 1
3 B 2
5 C 2
7 D 2
9 E 2
;
run;
```

```sas
Data B;
Input ID Name$ Weight;
cards;
2 A 2
4 B 3
5 C 4
7 D 5
;
run;
```

### Important Steps when using MERGE Statement in SAS  

Step 1 : Both the data sets must be SORTED by the variable you want to use for merging.  

Step 2 : The variable you want to use for merging must have same name in both the datasets.  

__Let's merge dataset A and B__ 

First, Sort both the datasets with PROC SORT. See the code below -  

```sas
proc sort data = a;
by id;
run;
proc sort data = b;
by id;
run;
```

__Next Step__ : Use MERGE statement to merge the datasets by the variable ID.

```sas
data dummy;
merge a (in=x) b(in=y);
by id;
a = x;
b = y;
run;
```

__What is IN= option in Data Step Merge?__  

The IN= option tells SAS to create a flag that has either the value 0 or 1. If the observation does not come from the dataset, then the flag returns 0. If the observation comes from the data set, then the flag returns 1.  

Since the IN= option creates temporary variables, we need to create permanent variables so that we can see the flag in the dataset. With this lines of code "a = x; b = y;", we tell SAS to create two variables named a, b and put the same values as stored in variables x and y. You can assign any name you want, not just a.b. See the Output shown in the image below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3192c2a2-10d7-41a2-835b-8fb2d3835691)  

In the above image, the highlighted yellow rows are the rows that are common in both the datasets. Hence, the values are 1 in variables A and B. The value 1 in variable A implies these rows come from dataset A and 0 implies these rows do not come from dataset A. The same logic holds for variable B. When variable B has 1, it means these rows come from dataset B.  

### What Happens If You Don't Include 'BY' Statement in Merging Data?  

The BY Statement tells SAS to match records based on the common variable you specify. Without the 'BY' statement, it does not perform matching of records. What would happen? Observations are combined based on their relative position in each data set. For example, observation one from the first data set combines with observation one of the second data set, the second observation from the first data set combines with the second observation from the second data set, and so on.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/75d53069-a9bd-4b29-9c9c-04bea1c92988)  

If there is a common variable in the two datasets, the value is overwritten by the value in the right dataset. Since ID and Name are the common variables, the values are overwritten by dataset B.  

The number of observations in the combined dataset is equal to the number of observations in the dataset with largest number of observations. For example, dataset A has 5 observations and dataset B has 4 observations so final data would have 5 observations.  

In this section, we cover different types of joins using the MERGE statement in SAS.  

### SAS : INNER JOIN  

Inner Join : It returns rows common to both tables (data sets). In the final merged file, number of columns would be (Common columns in both the data sets + uncommon columns from data set A + uncommon columns from data set B).  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/964da551-e2b5-44a1-afe1-899366327c05)  

```sas
proc sort data = a;
by id;
run;

proc sort data = b;
by id;
run;

Data dummy;
Merge A (IN = X) B (IN=Y);
by ID;
If X and Y;
run;
```

Note : When using IN= option, SAS considers "If X and Y" equivalent to "If X=1 and Y=1".  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3e754d50-ae39-48f7-8dd3-ca0a97a07300)  

Explanation  

Since the above case is of INNER JOIN, Data Step Merge returns values 5 and 7 which are common in variable ID of both the datasets.  

### SAS : LEFT JOIN  

Left Join : It returns all rows from the left table and the matched rows from the right table.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d4e8eea4-9927-4db3-8df2-36b37d5f73e5)  

```sas
proc sort data = a;
by id;
run;

proc sort data = b;
by id;
run;

Data dummy;
Merge A (IN = X) B (IN=Y);
by ID;
If X ;
run;
```

Note : When you use IN= option, SAS considers "If X" equivalent to "If X=1". We can use either of the If statement.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/57ca38a4-a8a3-4522-a7fe-2eb0ebc6a034)  

Explanation  

Since the above case is of LEFT JOIN, Data Step Merge returns all observations from dataset A with matching rows from dataset B.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1d818aca-8c0a-4579-b5e1-a5411ff7da2d)  

```sas
proc sort data = a;
by id;
run;

proc sort data = b;
by id;
run;

Data dummy;
Merge A (IN = X) B (IN=Y);
by ID;
If Y ;
run;
```

Explanation  

Since the above case is of RIGHT JOIN, Data Step Merge returns all observations from dataset B with matching rows from dataset A.  

### SAS : FULL JOIN   

Full Join: It returns all rows from the left table and from the right table.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/fe28c2fb-a13e-4310-914e-2e587d955bf0)  

```sas
proc sort data = a;
by id;
run;

proc sort data = b;
by id;
run;

Data dummy;
Merge A B;
by ID;
run;
```

Note : Since the FULL JOIN is the default type of JOIN in MERGE Statement, it does not require temporary variables with IN option.  

Explanation  

Since the above case is of FULL JOIN, Data Step Merge returns all observations from dataset A and B.  

### What happens when the BY variable in Data Step Merge has different length?  

When we merge datasets with BY variable having different lengths, the length of the BY variable used during matching is determined by the left-hand side dataset in the merge. If length of dataset A is shorter than B, it may return zero records.  

Solution - Include bigger length of the common variable with LENGTH Statement before MERGE statement.  

```sas
data dummy;
length ID 8;
merge a b;
by id;
run;
```

### Special Cases  

If both the tables (data sets) have similar variable name (other than primary key), Data Step MERGE statement would take values of the common variable exist in the TABLE2 (Right table).  

If primary key in both the tables (data sets) have duplicate values, Data Step MERGE statement would return a maximum number of values in both the tables. For example, Table 1 has 3 1's and Table 2 has 2 1's, Data Step Merge would return 3 1's. It is called 'One-to-Many Merge'.  

### See the special case shown in the image below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9ad63c41-6666-4b55-9031-8487dbdcc6e0)  

In this case, dataset A contains two 5s and dataset B contains three 5s. When we merged these two tables, it returns three 5s which is maximum number of 5s in both the dataset A and B.  

__Important Point__ - Did you notice the variable "name" exists in both the datasets A and B? In this example, the variable "name" is NOT a primary key to merge the tables. It is the variable "id" which is the primary key to merge these tables. When we merged the tables, DATA STEP MERGE takes values of variable "name" from dataset B.  

SAS Code for the above special case  

```sas
data a;
input id name$ height;
cards;
1 a 1
3 b 2
5 a 2
5 b 3
7 d 2
9 e 2
;
run;
data b;
input id name$ weight;
cards;
2 a 2
4 b 3
5 d 4
5 e 5
5 f 6
7 f 5
;
run;
```

```sas
data c;
merge a (in=x) b(in=y);
by id;
if x;
proc print;
run;
```

### Q. Do the "Special Cases" explained above hold true for all types of joins?  

Answer is YES. It holds true for all the types of joins.  

### How to check if merge was done correctly?  

Before merging, ask yourself whether the variable type and length of the BY variable is same.  

First check the number of observations in the input files and estimate the number of observations should come in the final merged data set.  

Check the number of variables in the input files and estimate the number of variables should appear in the final merged data set.  

If there are duplicates in the BY variable of the input files, how data step merge has considered these cases? Whether you are getting the desired output?  

## SAS : MANY TO MANY MERGE  

In SAS, many-to-many merges are handled very differently via Data Step MERGE and PROC SQL JOIN.  

Let's take an example -  

Suppose you have two data sets. You want to merge both the data sets but there are duplicate values in the common variable (ie. primary key) of any or both of the datasets.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/74c4ea16-2157-4696-a602-4cc6b4b07df4)  

### Data Step : Many to Many Merge  

The DATA step Merge does not handle many-to-many matching very well. When we perform many to many merges. the result should be a cartesian (cross) product of matching observations. For example, if there are three records that match from one contributing data set to two records from the other, the resulting data set should have 3 × 2 = 6 records.  

Data Step MERGE does not create a cartesian product in case of a many-to-many relationship. It will return number of records for a duplicate value equal to maximum number of the duplicate value in both the table.  

__SAS Code -__   

```sas
data dat1;
input ID Info;
cards ;
1 3123
1 1234
2 7482
2 8912
3 1284
;
run;

data dat2;
input ID Info2;
cards ;
1 4444
1 5555
1 8989
2 9099
2 8888
3 8989
;
run;

data combined;
merge dat1 dat2 ;
by ID;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/fb675c5f-68af-4b45-8a10-bbf8a5a93052)  

__Note :__

In this example, we have 2 1s in dat1 and 3 1s in dat2. The maximum number of 1s in both the tables is 3. So it would return 3 1s in the merged dataset.  

### PROC SQL JOIN : Many to Many Merge  

PROC SQL JOIN creates all possible combinations of matching observations in case of a many-to-many relationship. Cartesian product is a collection of all pairs of two given sets. For example, In ID variable, there are 2 1's in dat1 dataset and 3 1's in dat2 dataset, the cartesian product would be (3*2 = 6 Observations) in the final result.  

```sas
proc sql noprint;
create table combined2 as
select * from dat1 a
join dat2 b
on a.ID = b.ID;
quit;
```

See the output shown in the image below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f6738eae-e252-4f5a-a215-2f8dee7376bb)  

## RETAIN STATEMENT IN SAS (WITH EXAMPLES)  
  
This tutorial explains how to use the RETAIN statement in SAS, with examples. In SAS, it's a very easy and useful way to retain values with RETAIN statement.  

### Create Sample Data  

The following program creates sample data for demonstration -  

```sas
data abcd;
input x y;
cards;
1 25
1 28
1 27
2 23
2 35
2 34
3 25
3 29
;
run;
```

### Uses of RETAIN Statement  

The RETAIN statement simply copies retaining values by telling the SAS not to reset the variables to missing at the beginning of each iteration of the DATA step. If you would not use retain statement then SAS would return missing at the beginning of each iteration.  

The retain statement keeps the value once assigned.  

### Generate Serial Number  

Suppose you need to generate a serial number (or row index number) with data step.  

```sas
data aaa;
set abcd;
retain z 0;
z = z + 1;
run;
```

__Output Dataset__  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/478b88d8-b3af-462b-93f8-f0943b9f2eef)  

The above SAS code initializes a variable "z" to 0 and increments it by 1 for each observation in the "aaa" data set. The result is a new data set with an additional variable "z" that has row numbers.  

__We can retain implicitly by using the +1 notation.__  

```sas
data aaa;
set abcd;
z + 1;
run;
```

z + 1; is a simplified way to increment the variable "z" by 1 for each observation. It returns row numbers starting from 1.  

### Cumulative Score  

Suppose you need to calculate cumulative score. In financial data, we generally need to calculate cumulative score year to date.  

```sas
data aaa;
set abcd;
retain z 0;
z = z + y;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/20565c47-aac8-4581-8b19-3638394d3c07)  

### Generate Serial Number by Group  

Suppose you have a grouping variable say "region" and you need to generate a row index number by region.  

```sas
proc sort data = abcd;
by x;
run;

data aaa;
set abcd;
retain z;
if first.x then z = 1;
else z = z + 1;
by x;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a6f60c8c-d336-42e8-ab0c-d02ba0029d9b)  

### Cumulative Score by Group  

Suppose you need to calculate cumulative sale by product categories.  

```sas
data aaa1;
set aaa;
retain z1;
if first.x then z1 = y;
else z1 = z1 + y;
by x;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c156bfe3-dec4-49ee-914c-a7ea574ab1df)  

The variable "z1" constitutes cumulative values of variable y by grouping variable x.  

### Number of Unique Observations  

The number of unique rows by a group can easily be calculated with PROC FREQ and PROC MEANS. The following program explains how we can calculate number of observations in a categorical variable with Data Step.  
```sas
data aaa2;
set abcd (drop = y);
retain z;
if first.x then z = 1;
else z = z + 1;
by x;
if last.x then output;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5ab77f18-5669-4295-8e5b-85ac9f1ebe90)  

__Suppose you have more than 1 grouping variable__

In the dataset below, we have two grouping (categorical) variables : "ID" and "ID1".  

```sas
data temp;
input ID ID1 Score;
cards;
1 1 25
1 1 26
1 2 27
1 2 29
2 1 28
2 1 29
2 2 31
;
run;
```

When you have more than 1 grouping variable, we can use multiple FIRST. statements with OR operator to generate serial numbers.  

```sas
data temp2;
set temp;
by ID ID1;
if first.ID or first.ID1 then N = 1;
else N+1;
proc print;
run;
```

### CALCULATING PERCENTILES WITH SAS  

In SAS, you can calculate percentiles using PROC UNIVARIATE procedure.  

Important options used for calculating percentile in PROC UNIVARIATE  

PCTLPTS : Specifies percentile levels  

PCTLPRE : Specifies one or more prefixes to create the variable names for the variables that contain the PCTLPTS= percentiles.  

PCTLNAME : Specifies one or more suffixes to create the variable names for the variables that contain the PCTLPTS= percentiles.  

Example 1 :   
 
Percentile calculation for a variable  

```sas
proc univariate data = abcd noprint;
var a;
output out=outdata PCTLPTS = 99.5 PCTLPRE = a;
run;
```

Example 2 : 

Percentile calculation for multiple variables  

```sas
proc univariate data = abcd noprint;
var a b c;
output out=outdata PCTLPTS = 99 PCTLPRE = a b c PCTLNAME = _P99;
run;
```


![image](https://github.com/Deepak2k20/SAS/assets/65231118/7b6d40f1-d530-4447-a21f-c6c6436e1dbe)  

2 Important Points : 

If you specify 3 variables in var statement (var a b c) and only 1 prefix in PCTPRE, SAS will create percentile for only 1 variable that is mentioned first in the var statement.  

If the number of PCTLNAME= values is fewer than the number of percentiles or if you omit PCTLNAME=, PROC UNIVARIATE uses the percentile as the suffix to create the name of the variable that contains the percentile.  

Example 3 : 

Series of percentile levels  

```sas
proc univariate data = abcd noprint;
var c;
output out=outdata PCTLPTS = 0 to 5 by 0.5 , 95 to 100 by 0.5 PCTLPRE = P;
run;
```

## SAS ARRAYS AND DO LOOP MADE EASY  

### SAS Arrays : Introduction  

SAS arrays provides a simple, efficient way to process a list of variables in a SAS DATA step. In other words, arrays are useful when you need to perform similar operations on multiple variables or when you want to avoid writing similar code for multiple variables.  

### Syntax of SAS Arrays  

The syntax of SAS arrays is as follows:  

Array array-name {number-of-elements} list-of-variables;  

Note: You can use [ ] or { } or ( ) for defining number of elements in the ARRAY statement.  

ARRAY ABC[5] a b c d e;: ABC is an array-name, 5 implies the number of variables in the array, and "a b c d e" are the fields that make up the array.  

ARRAY ABC[*] a b c d e;: In this example, SAS would automatically calculate the number of variables in the array.   

ARRAY ABC[*] X1-X10;: Where the X1 variable contains the X1 value, X2 contains the X2 value, etc.  

ARRAY ABC[*] $ X1-X10;: If the variables are of character type then use $ sign before specifying list of variables.  

### SAS DO Loop : Introduction  

The DO loop allows you to perform iterative processing. You can use the DO loop to repeat a set of statements for a specific number of iterations or for a particular range of values.  

### Syntax of SAS DO Loop  

The syntax of SAS DO Loop is as follows:
```sas
DO index-variable = start-value TO end-value;
  /* Statements to be executed inside the loop */
END;
```

index-variable: This is a temporary variable used to keep track of the loop iterations. It is usually a numeric variable.  

start-value: This is the initial value for the index variable.  

end-value: This is the final value for the index variable.  

### Sample Dataset  

Let's create a sample SAS dataset for demonstration purposes.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/297f647e-fa86-424b-8bc1-fb8963a499ee)  

```sas
data temp;
input x1 x2 x3 x4$ x5$;
cards;
1 2 3 AA BB
2 3 4 AB CC
3 4 5 AC DD
4 5 6 AD EE
5 6 7 AE FF
6 7 8 AF GG
;
run;
```

### Example 1 : Replace values greater than 3 in numeric variables with missing data  

The following code reads data from the "temp" dataset and then goes through each observation and checks if the values of the variables "x1," "x2," and "x3" are greater than 3. If any of these values are greater than 3, the value is replaced with a missing value. It stores the updated values in a new dataset "test".  

```sas
data test;
set temp;
array nvars {3} x1-x3;
do i = 1 to 3;
if nvars{i} > 3 then nvars{i} =.;
end;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8480bdb1-b9ed-4535-9d2b-a7447a5531f3)  

### Why i is 4 in the output data set?  

The first time the loop processes, the value of "i" is 1; the second time, 2; and the third time, 3. At the beginning of the fourth iteration, the value of "i" is 4, which is found to be greater than the stop value of 3 so the loop stops. The value of i is now 4 and not 3, the last value before it would be greater than 3 as the stop value.  

Note : We can drop variable "i" with drop statement or drop data set option.  

### Efficient version of the above code  

```sas
data test;
set temp;
array nvars (*) _numeric_;
do i = 1 to dim(nvars);
if nvars{i} > 3 then nvars{i} =.;
end;
drop i;
run;
```
  
__Notes -__ 

The "_numeric_" is used to specify all the numeric variables.  

The DIM function returns the number of elements (variables).  

### Example 2 : Extract first letter of all the character variables  

The following code reads data from the "temp" dataset and then goes through each character variable and keeps only the first letter, discarding the rest. The result is a new dataset "test" with character variables truncated to their first letters.  

```sas
data test;
set temp;
array cvars (*) _character_;
do i = 1 to dim(cvars);
cvars{i} = substr(cvars{i},1,1);
end;
drop i;
run;
```
 
Note - The "_character_" is used to specify all the character variables.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/658bee8c-814b-4c43-8130-fe25ddfa36b7)  

### Example 3 : Extract first letter and assign to new variables  

The following code reads data from the "temp" dataset and then goes through each character variable and extracts the first letter from each variable, and assigns it to the corresponding "X6" or "X7" variable in the "test" dataset. The result is a new dataset "test" with the first letter of each character variable stored in "X6" and "X7" variables.  

```sas
data test;
set temp;
array cvars (*) _character_;
array dvars (*) $ X6 X7;
do i = 1 to dim(cvars);
dvars{i} = substr(cvars{i},1,1) ;
end;
drop i;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/857cc690-6184-4ef2-8dea-75f1a11f0821)  

### Example 4 : Assign Initial Values in a SAS Array  

The following code reads data from the "temp" dataset and then goes through each numeric variable in "temp" and multiplies it by a corresponding percentage increase factor from the temporary "pctinc" array. The results are assigned to the "px1", "px2", and "px3" variables in the "abcd" dataset. The temporary array "pctinc" is used for the calculation but is not included in the final dataset.  

```sas
data abcd;
set temp;
array nvars (*) _numeric_;
array pvars (*) px1 px2 px3;
array pctinc {3} _temporary_ (1.1 , 1.2 ,1.3); 
do i = 1 to dim(nvars);
pvars{i} = nvars{i} * pctinc{i};
end;
drop i;
run;
```

__Notes -__  

In the above example, we are multiplying values of variables with different numbers.  

When the key word _TEMPORARY_ is used in a ARRAY statement, data elements are created but are not stored in the data file.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/790483a0-40fd-4b32-a1ec-a66d1461fe3b)  

### Example 5 : Calculate Percentage Growth  

The following code reads data from the "temp" dataset and then calculates the difference and percentage difference between consecutive numeric variables in "temp" and stores the results in the temporary "diff" and "percent" arrays. The final "abcd" dataset will not include the temporary "diff" array but will have the percentage differences stored in the "percent" array.  

```sas
data abcd;
set temp;
array nvars(*) _numeric_;
array diff{2} _temporary_;
array percent{2};
do i = 1 to 2;
diff{i} = nvars{i +1} - nvars{i};
percent{i} = diff{i} / nvars{i} ;
end;
drop i;
run;
```

### Using the OF Operator in a SAS Array  

The following two codes are equivalent :  

```sas
array gnp (*) x y z;
sumgnp = sum(of gnp(*));
```
OR

```sas
sumgnp = sum(x,y,z);
```

Calculate the mean : mean_score = mean(of gnp(*));  

Calculate the minimum : min_score = min(of gnp(*));

Suppose you are asked to create a flag in cases wherein sum of variables x1,x2 and x3 is greater than 10.  

```sas
data test;
set temp;
array nvars (*) x1-x3;
if sum(of nvars(*)) > 10 then flag =1;
else flag=0;
run;
```

### DO OVER LOOP  

The DO OVER loop is one of the most useful DO loops. It can be used with an array when indexing of the array is not needed.  

In the example below, the "do over" statement iterates over each numeric variable in the array "nvars". For each variable, the code checks if its value is greater than 3. If it is, then the value is set to missing (represented by a dot "."). This effectively replaces any numeric value greater than 3 with a missing value.  

```sas
data test;
set temp;
array nvars _numeric_;
do over nvars;
if nvars > 3 then nvars = .;
end;
run;
```

## SAS : LENGTH OF NUMERIC VARIABLES  

This tutorial describes how SAS treats length of numeric variables in data sets. It is often asked in interviews if default length of numeric variable is 8, how would you store a numeric variable having value more than 8 digits (for example, 123456789). It seems to be a simple question but confusing. Hence, it is required to pay attention how SAS stores numeric variables.  

### Solution :

In SAS, the default length of a numeric variable is 8 bytes. Pay attention to bytes. The limit is NOT 8 digits but 8 bytes. 8 bytes means we can store up to 16 digits for a numeric variable in SAS. In other words, the default length of numeric variable is 16 digits. It is important to note that the minimum length of a numeric is 3 bytes. It does not mean it cannot store a numeric value lower than 3 digits. It can store values of 1 or 2 digits. See the table below what bytes mean in terms of digits.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/4c53a4e0-1a96-4f0a-a37c-9206200f6afc)  

The length of a numeric variable lies between 3 and 8 bytes. It means SAS can store a numeric value from 1 to 16 digits.   

See the example below -  

Run the following program and see log. It would give you how SAS keeps numeric values.  

```sas
data temp;
x = 1234567890;
x1 = 1234567890123456;
put x= x1=;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/750c2b0b-4672-4e1e-958f-ff3dbc48c3d5)  

If you look at the image above, SAS stores variables x and x1 without any issue. But the format of the variable x1 is in E notation. See how it works -  

1.23456789E15 is equivalent to 1.23456789 𝗑 10¹⁵  

__Rule -__

If the the value of numeric variable is less than or equal to 12 digits it is displayed normally which means the format of the numeric value does not change to E notation. If it is more than 12 digits, the format changes to E notation. To avoid E notation, we can use best16. format which prevents to change the format of the larger values.  

```sas
data temp;
x = 1234567890;
x1 = 1234567890123456;
format x1 best16.;
put x= x1=;
run;
```

### SAS: HOW TO CHECK NUMBER OF OBSERVATIONS IN A DATASET  

This post explains how to determine the number of observations in a SAS dataset. Most of the times we need to check whether a SAS dataset is empty or not. In macro, we generally tell SAS to go to the next iteration only when SAS dataset is non-empty. In this post, we will see various methods to count number of rows (records) in SAS table.  

### Method I : Proc SQL Count (Not Efficient)  

In the example below, we will use CARS dataset from SASHELP library. This dataset contains 428 observations and 15 columns.  

The easiest method is to use count(*) in Proc SQL. It returns all rows (missing plus non-missing rows) in a dataset.  

```sas
proc sql;
select count(*) as N from sashelp.cars;
quit;
```

Result : 428
 
In case you want to store it in a macro variable, you can use INTO : keyword.  

```sas
proc sql noprint;
select count(*) into :N from sashelp.cars;
quit;

%put &N;
```

This will print the number of records in SAS log. Check log after running the above program.  

### Is it an efficient method?  

No, it is not efficient at all. It does not use metadata information of SAS dataset. Instead it reads through each record (row) of your SAS dataset. It takes a long time to do it in big SAS tables. However, it is a simple and handy trick to calculate the number of rows in a SAS dataset.  

### Method 2 : Descriptor Portion (Efficient)  

Before getting into detail, we need to understand the descriptor portion and how it works -  

__SAS dataset consists of the following two portion -__

__Descriptor portion__. It constitutes information about name of dataset, number of observations and variables, creation date, engine type.  

__Data portion__. It stores values of data.  

This method is one of the most efficient way to count observations in a SAS table as it uses metadata information and does not search in dataset.  

```sas
data _NULL_;
if 0 then set sashelp.cars nobs=n;
put "no. of observations =" n;
stop;
run;
```

__Explanation__  

The 'if 0' statement does not process at execution time because IF statement does not hold TRUE. The whole IF THEN statement is used to pull the header information of the data set and later hand over to the compiler to adjust it to the PDV.  

NOBS is a SAS automatic variable which contains the number of rows in a dataset i.e. SASHELP.CARS dataset.  

NOBS = N puts the returns count of records in the variable n.  

The STOP statement is used to stop an endless loop.  

Like the first method, we can keep it in a macro variable. See the implementation below -  

```sas
data _NULL_;
if 0 then set sashelp.cars nobs=n;
call symputx('totobs',n);
stop;
run;
%put no. of observations = &totobs;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9178216d-28ae-4830-b6d5-76c885f55572)  

CALL SYMPUT is one of the method to create a SAS macro variable in data step. In this case, we have used a newer function i.e. CALL SYMPUTX which left justifies and trims trailing blanks from a numeric value. If you want to stick to the old style CALL SYMPUT, you can write like below -  

```sas
call symput('totobs',left(n));
```

### 3. Proc SQL Dictionary Method (Efficient)  

Like second method, we can use metadata information of a dataset with PROC SQL Dictionary.Tables.  

```sas
proc sql noprint;
select nobs into :totobs separated by ' ' from dictionary.tables
where libname='SASHELP' and memname='CARS';
quit;
%put total records = &totobs.;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f724c0f3-a41f-414c-88e7-793bf98415d6)  

It is an efficient method as it does not look into each values of a dataset to determine the count. The LIBNAME= refers to the name of the library in which data is stored. The MEMNAME= refers to SAS table (dataset). The separated by ' ' is used in this case to left align the numeric value.  

### 4. Macro Language Method (Efficient)  

This method also uses metadata information but it is via the macro language using DATA step functions. The OPEN function is used to open a data. The ATTRN function returns the value of a numeric attribute for a SAS data set. When it is used with the NOBS argument, it returns the number of observations. Later we are closing the opened dataset using CLOSE function.  

```sas
%macro totobs(mydata);
%let mydataID=%sysfunc(OPEN(&mydata.,IN));
%let NOBS=%sysfunc(ATTRN(&mydataID,NOBS));
%let RC=%sysfunc(CLOSE(&mydataID));
&NOBS
%mend;
%put %totobs(sashelp.cars);
```

### SAS : Check if it is empty table

Suppose you only need to check whether a table is empty or not. You can use the same logic as explained above. And if the returned value is 0, write 'Empty Data' in log. Otherwise, count the number of records.  
```sas
data _NULL_;
if 0 then set sashelp.cars nobs=n;
if n = 0 then put 'empty dataset';
else put 'Not empty. Total records=' n;
stop;
run;
```

Result : Not Empty. Total records = 428  

Let's create a blank dataset to check the above code. The following program returns empty dataset as 1=2 condition does not meet.  

```sas
proc sql noprint;
create table temp as
select * from sashelp.cars
where 1 = 2;
quit;
```

Try it yourself!  

### Let's wrap the above code in a SAS macro  

```sas
%macro emptydataset (inputdata=);
data _NULL_;
if 0 then set &inputdata. nobs=n;
call symputx('totobs',n);
stop;
run;
%if &totobs. = 0 %then %put Empty dataset;
%else %do;
%put TotalObs=&totobs;
%end;
%mend;
```

%emptydataset(inputdata=sashelp.cars);  
Result : TotalObs=428  

%emptydataset(inputdata=work.temp);  
Result : Empty dataset  

If you think it's difficult to memorize sas code of descriptor portion method, you can use the code below.  

```sas
data _NULL_;
set sashelp.cars nobs=N;
if _N_ = 2 then stop;
put N;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5362fe77-d858-43e2-ad9c-eb01c909948a)  

It reads only first two observations from the dataset. See log above.  

## SEND SAS OUTPUT TO EXCEL  

This tutorial explains how to send SAS results (output) to Excel.

### Example 1 :

Create a new sheet for each unique value in the grouping variable (By Group)  

```sas
ods tagsets.excelxp file="C:\Users\Deepanshu\test.xls"
options(embedded_titles="yes"
autofilter="1-3"
frozen_headers="3"
frozen_rowheaders="1"
absolute_column_width="8.5,11,7,9,8,8"
autofit_height="yes"
sheet_interval="bygroup"sheet_label=" "
suppress_bylines="yes") style=normal;

proc print data=sashelp.shoes noobs;
title "Detail of Region #byval(region)";
by region;
run;

ods tagsets.excelxp close;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/11bc5cff-cd7c-4017-a14a-1c528c122f9a)  

The SHEET_INTERVAL= option is used to define the interval in which to create new worksheets.  

### Example 2 :

Define names of sheets manually   

```sas
ods tagsets.excelxp file='C:\Users\Deepanshu\Documents\multitable.xls' style=STATISTICAL
options(sheet_name='Summary' skip_space='1,0,0,0,1' EMBEDDED_TITLES='yes' sheet_interval='none');

Title " First File";
proc freq data = sashelp.class;
table sex;
run;

Title " Second File";
proc print data = sashelp.cars;
run;

ods tagsets.excelxp options(sheet_name='FREQ' skip_space='1,0,0,0,1' EMBEDDED_TITLES='yes' sheet_interval='none');
Title " Third File";

proc freq data = sashelp.cars;
table make;
run;

ods tagsets.excelxp close;
```

### Example 3 :

Apply Custom Format of Excel  

```sas
data temp;
pct= 0.75;
number= -45;
run;

ods tagsets.excelxp file="C:\Users\Deepanshu\temp.xls";

proc print data=temp noobs;
var pct;
var number / style(data)={tagattr="format:$#,##0_);[Red]($#,##0)"};
format pct percent5.2;
run;

ods tagsets.excelxp close;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/114ac6d2-0ed6-4b7b-a4c7-f6bfe33005c3)  

### Important Note  

ODS TAGSETS.EXCELXP does not support graphs (charts). From SAS 9.4, SAS added new ODS called ODS EXCEL that supports both graphs and tables.  

### ODS EXCEL  

```sas
ods excel file="c:\test.xlsx"
options(start_at="B5“
tab_color="red"
absolute_row_height="15"
embedded_titles="yes");

ods text="Sales report for company X";
proc print data=sashelp.orsales;
title "Sample title showing new
features";
run;

ods excel close;
```

### ODS Excel- PROC MSChart  

```sas
proc sql;
create table summary as
select(region), sum(sales) format=dollar14.2 as sales
from sashelp.shoes
group by region;
run;
quit;
```

```sas
ods excel file="c:\temp.xlsx";
title "Sales by Region";
proc mschart data=work.summary category=region width=4in position="$D$1";
where region in("Africa","Asia","Canada","Pacific","United States");
vcolumn sales;
run;
ods excel close;
```

## SAS : VARIABLE NAME HAVING SPACES OR SPECIAL CHARACTERS  

This article may be an eye-opener for you if you think a variable name cannot contain blanks or special characters except for the underscore in SAS. In this article, we would learn how we can read a variable whose name having spaces or special characters. Also, how to deal a variable name starts with a number. It also covers the same case with a dataset (table).  

### Why do we need to have spaces in a variable name?

If you use teradata or any other database, you would encounter this problem very soon if you have not encountered it yet. Many times, database column contains blanks or special characters. To read them in SAS, we need to know how to read variables having spaces in their names.  

It is also required when we transpose our variables and the variable whose values name the transposed variables in the output data set contains special characters.  

### Let's create a sample data  

```sas
data temp;
input var1;
cards;
1
2
;
run;
```

### Rename the variable 'var1'  to 'variable one';  

```sas
options validvarname=any;
data temp2;
set temp;
rename var1 = 'variable one'n;
run;
```

The options validvarname=any; tells SAS to allow you to have variable name begin with or contain spaces, special characters or numbers.  

Additionally, we need to put variable name having spaces in quotes followed by the letter n.  

Q. If i don't use VALIDVARNAME=ANY option and use only 'variable one'n , how SAS would take it?  

Sol : SAS would return an error "variable name is not valid" as SAS by default cannot contain blanks or special characters.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a491c799-54cb-483f-8f19-394615d62051)  

### Can variable name starts with a number?
  
Yes, follow the code below -  

```sas
options validvarname=any;
data temp2;
set temp;
rename var1 = '1variable'n;
run;
```

### How about reading a dataset whose name having spaces?  

The option VALIDMEMNAME= EXTEND allows you to read or access dataset (table) whose name having spaces or special characters. In addition, we also need to put name of variable in quotes followed by the lettern. 

```sas
options VALIDMEMNAME=EXTEND;
proc print data= 'price data'n;
run;
```

### SPEED UP SAS CODE WITH INDEX

This tutorial demonstrates how to speed up SAS code with Indexes.  

### What is Index?  

Indexes are not something technical or related to SAS programming. It is something we use everyday to make our life easy. For example, every employee in an organization has an employee ID which is unique. It's easy for HR /Admin team to find information about a particular employee. First Name or Last Name of employees are not unique so it's better to record information by unique ID. So, employee information is indexed by employee ID. Let's take few more examples - dictionary is alphabetically sorted. So alphabets are index in this case. There can be multiple indexes to find information. For example, books in a library are sorted by topics (Science) and sub-topics (Physics /Chemistry / Bio / Statistics).  

In SAS, Index is used to store observations in an ascending order and later access them quickly from a variable. In simple words, it minimizes some steps of searching a particular value by telling SAS the nearest /exact location of the value you are searching for. Confused? Read the next section.  

### How Index works?  

When Index is used, SAS runs a binary search algorithm on the data set.  

Binary search is a performance improvement algorithm for searching a particular observation from a sorted variable. It works by continuously dividing in half of the total number of observations and search the value in the half of the list, until you got the value that you were looking for.  

__Example__  

Let's assume you have a variable CustomerID :   

15, 20, 3, 16, 9, 17, 13

You are finding the information of customer having CustomerID equals to 17. See the steps below to find the value -  

First, sort the CustomerID variable. We will have these values - {3,9,13,15,16,17,20}  

Calculate the median (middle value) of the list i.e. 15.  

We would check whether search_value = median? Is 17 =15? No. 17 > 15.  

Ignore all the values that are less than or equal to 15 as 17 is a higher number than 15.  

Now, we need to search in the remaining list i.e. 16, 17, 20. The middle value is 17.  

Is 17 = 17? Yes. the value found.  

If you do not create an index SAS would search 17 sequentially in the whole list. The above is a simple example of a few values. If you have millions of observations, it would take a hell lot of time to search a particular value sequentially in the variable.  

### When to Use Index ?

1. Size of Subset Records

You should only use Index if you need to pull a small subset from a large SAS data set. See the definition of 'small' and 'large' in the table below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/19a70d4b-3417-4d73-bafb-a3462230d0b4)  

2. Variable Consideration

It is recommended to index only those variables that have a high number of distinct values. For example, Customer ID as it is unique at customer level so it would have a high number of unique records.  But the variable 'sex' would have only two distinct values so it would not be a good choice to index.  

3. Usage Level

If you use a variable frequently that is indexed, it makes sense as it improves the performance in terms of CPU time. But if you are creating an index for just a single usage, it's not a sensible idea to do it as  it takes resources (CPU time, I/0 etc) to initially create an index. Hence, it's required to anticipate the usage of  dataset with Index before creating it.  

### How to create Index with SAS

In SAS, there are several ways to create an index. It can be implemented with either of the following three options -  

1) PROC DATASETS  

2) INDEX = Data Step Option  

3) PROC SQL

### 1. PROC DATASETS : Index

A simple Index can be created like below -  

```sas
proc datasets library=work nolist;
modify mydata;
index create custid;
quit;
```

__Explanation :__  

LIBRARY=WORK refers to the SAS temporary library that contains SAS data set 'mydata'  

NOLIST option hides the printing of the directory of SAS files in the SAS log and output window.  

MODIFY tells SAS we are creating an index in data set 'mydata'  

CUSTID in the 'Index Create' statement is the name of the variable for which we want to create an Index.  

### Index of two or more variables

It's called composite index when we create an index for two or more variables. In composite index, values of multiple variables are concatenated and form a single value which would be used for search specific values. The variables can be character or numeric or mixed (one character and the other one is numeric).  

```sas
proc datasets library=mylibrary;
modify customermart;
index create names = (first last);
run;
```

In this case, 'names' is an index-name and it's created for two variables - first and last.  

### Only Unique Values

If you want to set condition that values for a variable must be unique, you can use UNIQUE option. For example, you know the customer ID would always be unique. When you use UNIQUE option, SAS would make sure there would not be any duplicate in simple or composite index. In composite index, it would check the uniqueness in combination of multiple variables. If someone would try to update the file with duplicates, it would throw an error.  

```sas
proc datasets library=work nolist;
modify mydata;
index create custid / unique nomiss;
quit;
```

NOMISS Option : It does not mean the missing values cannot be added to the data set. It implies the missing values cannot be added to the index.  

### 2. INDEX = Data Set Option

We can create an index with dataset option. See the code below -  

```sas
data mydata (index=(custid / unique));
set mydata;
run;
```

An composite index can be created like code below -  

```sas
data mydata (index=(names=(first last)));
set mydata;
run;
```

### 3. PROC SQL : Index  

The syntax for creating a simple index with PROC SQL is as follows -  

```sas
proc sql;
create index custid
on mydata;
quit;
```

### Performance Comparison

In this section of post, we are making comparison of filtering with and without Index to check the performance.  

Let's create a sample for demonstration :  

The following code would create three variables - k, custid, demog. The variable 'k' constitutes values ranging from 1 through 20 millions and the variable 'custid' would  have same values as 'k' (just added 1) and the variable 'demog' is a categorical variable having 4 levels.  

```sas
data temp;
length demog $12.;
do k =1 to 20000000;
custid = k+1;
if mod(k,8)=0 then demog ='category i';
if mod(k,8)=1 then demog ='category ii';
if mod(k,8)=2 then demog ='category iii';
output;
end;
run;
```

### Filtering without Index  

We are simply subsetting rows by few values in the variable 'custid'.  

```sas
data testing;
set temp;
where custid in (5467620,225,2671899, 18000000);
run;
```

NOTE: The data set WORK.TESTING has 4 observations and 3 variables.
NOTE: DATA statement used (Total process time):
real time 3.47 seconds
cpu time 3.43 seconds

### Filtering with Index

First, we are creating index with PROC DATASETS and subsetting data in the second section of the code.  

```sas
proc datasets library=work;
modify temp;
index create custid;
quit;

data testing2;
set temp;
where custid in (5467620,225,2671899, 18000000);
run;
```

NOTE: The data set WORK.TESTING2 has 4 observations and 3 variables.
NOTE: DATA statement used (Total process time):
      real time           0.09 seconds
      cpu time            0.03 seconds  

__Result :__  

Compare CPU time of both the codes and see Indexing resulted to more than 100 times faster code than without using Index.  

### Does Index always speed up SAS code?  

Answer is NO. It may even slow down the code if we have a variable that has a very few distinct/unique values. For example, there is a variable called 'Age Group' that contains only 5 distinct values ranging from 1 to 5. 1 refers to the smallest age-group (<18 years old) and 5 refers to the highest age-group (>55 years old). Suppose you need to search 2 in the variable 'AgeGroup'. If we perform indexing on the variable, it would run binary search algorithm which would calculate the middle value and compare it with the searching value. It works iteratively (repetitively). It would take more time than that of sequentially searching '2' in the variable. See the live example below -  

Example : We are extracting 'category i' from the variable 'demog'.  

__Without Index__  

```sas
data testing;
set temp;
where lowcase(demog) = 'category i';
run;
```

NOTE: The data set WORK.TESTING2 has 2500000 observations and 3 variables.
NOTE: DATA statement used (Total process time):
      real time           13.12 seconds
      cpu time            13.07 seconds  

__With Index__  

```sas
proc datasets library=work;
modify temp;
index delete custid;
index create demog;
quit;

data testing2;
set temp;
where lowcase(demog) = 'category i';
run;
```

NOTE: The data set WORK.TESTING has 2500000 observations and 3 variables.
NOTE: DATA statement used (Total process time):
      real time           19.99 seconds
      cpu time            13.71 seconds  

In this case, creating an index on a variable took more time than without having index on the variable.  

__Uses of Indexing__  

1. Filtering rows with WHERE statement results in better performance of SAS Code when index is already created on the variable.  

Important Point : SAS by default checks whether to use an index or not when you use WHERE statement.  

2. Data need not to be prior sorted before running BY processing if index is turned on. For example,  two datasets need to be sorted before using MERGE statement. But if index is already created on the datasets, you need to sort the data sets before MERGING. See the example below -

```sas
data a_index (index=(id));
set a;
run;
data b_index (index=(id));
    set b;
 run;
```

```sas
data final;
merge a_index(in=a) b_index(in=b);
by id;
if a=b;
run;
```

CAUTION : If you are creating index just for merging, it's not a good idea as Index increase resources which means increasing CPU processing time.  

Important Point : Merging and Indexing  

If you are merging/joining a small table with the large indexed table, the indexing would result a good performance. By 'small' table, it means at most 15% of the large indexed table. If you are merging two large indexed table, it might reduce the performance as it takes resources to create an index.  

3. The KEY= option in the SET statements allows you to perform efficient merging.

### Key Points

1. IF statement does not use an index. Whereas WHERE statement makes use of it.  

2. You can run PROC CONTENTS to see the names of the variables which are used for indexing.  

3.  You can delete indexes by the following ways :

PROC DATASETS : Use command 'index delete index-name;'  

PROC SQL : Use command 'drop index index-name from dataset-name;'  

### Endnotes  

SAS indexing capabilities can increase the performance of your SAS code which leads to a significant time saving. But we also need to consider the points listed above wherein it can reduce the performance or might not improve it. It's important to remember the point that indexing increases in the size of the data and it takes time to create an Index. Hence, we should create an index only if the usage of the key variable on dataset is very high.  

# SAS Functions  

Here is a valuable collection of comprehensive tutorials on various functions in SAS. These functions make it easier for you to work with data and perform various operations.  

## SAS : CHARACTER FUNCTIONS  

This tutorial covers the most frequently used SAS character functions with examples. Dealing with character strings can be a little tricky compared to numeric values. Therefore, it is necessary to understand the practical usage of character functions.  
  
### 1. COMPBL Function  

The COMPBL function compresses multiple blanks to a single blank.  

In the example below, the Name variable contains a record "Sandy   David". It has multiple spaces between the first and last name.  

### Create a dummy data  

```sas
Data char;
Input Name $ 1-50 ;
Cards;
Sandy    David
Annie Watson
Hello ladies and gentlemen
Hi, I am good
;
Run;
```

### Use COMPBL Function  

```sas
Data char1;
Set char;
char1 = compbl(Name);
run;
```

Output  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a12f451a-730e-4319-af33-fd7064de63a2)  

### 2. STRIP Function  

The STRIP function removes leading and trailing spaces.  

```sas
Data char1;
Set char;
char1 = strip(Name);
run;
```

### 3. COMPRESS Function  

The COMPRESS function removes leading, between and trailing spaces.  

SYNTAX
COMPRESS(String, characters to be removed, Modifier)

```sas
Data char1;
Set char;
char1 = compress(Name);
run;
```

Output  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/92da731c-3e42-4577-b8fc-338eaa6216ac)  

__Remove specific characters__

```sas
data _null_;
x='ABCDEF-!1.234';
string=compress(x,'!4');
put string=;
run;
```

It returns ABCDEF-1.23.  

In SAS 9.1.3, the additional parameter called MODIFIER was added to the function.  

The following keywords can be used as modifiers-  

a – Remove all upper and lower case characters from String.  

ak - Keep only alphabets from String.  

kd - Keeps only numeric values  

d – Remove numerical values from String.  

i – Remove specified characters both upper and lower case from String.  

k – keeps the specified characters in the string instead of removing them.  

l – Remove lowercase characters from String.  

p – Remove Punctuation characters from String.  

s – Remove spaces from String. This is default.  

u – Remove uppercase characters from String.  

### Example 1 : Keep only alphabets from alphanumeric values  

```sas
data _null_;
x='ABCDEF-!1234';
string=compress(x,'','ak');
put string=;
run;
```
 
It returns ABCDEF  

Example 2 : Keep only numeric from alphanumeric  

```sas
data _null_;
x='ABCDEF-!1234';
string=compress(x,'','kd');
put string=;
run;
```

It returns 1234  

Example 3 : Remove all punctuation from string    

```sas
data _null_;
x='ABCDEF-!1234';
string=compress(x,'','p');
put string=;
run;
```

It returns ABCDEF1234   

Example 4 : Keep Integer Values from String  

```sas
data _null_;
x='ABCDEF-!1.234';
string=compress(x,'0123456789.','k');
put string=;
run;
```

It returns 1.234  

### 4. LEFT Function  

The LEFT function moves leading blanks to the end of the value. The length of the string does not change.  

```sas
Data char1;
Set char;
char1 = left(Name);
run;
```

### 5. TRIM Function   

The TRIM function removes trailing spaces.  

```sas
Data char1;
Set char;
char1 = trim(Name);
run;
```

### 6. TRIM(LEFT(string))  

It is equivalent to STRIP function. It first removes leading spaces and then trailing spaces.  

### 7. CAT Function  

The CAT function concatenates character strings. It is equivalent to || sign.  

```sas
data _null_;
a = 'abc';
b = 'xyz';
c= a || b;
d= cat(a,b);
put c= d =;
run;
```

Both c and d returns "abcxyz".  

Concatenate String and Numeric Value  

```sas
data _null_;
x = "Temp";
y = 22;
z = x||y;
z1 = cats(x,y);
z2 = catx("",x,y);
put z = z1= z2 =;
run;
```

z = Temp   22  

z1=Temp22  

z2=Temp 22  

__Note__ -  

The || keyword inserts multiple spaces when numeric and text values are concatenated.  

CATS strips both leading and trailing blanks, and does not insert separators.  

CATX strips both leading and trailing blanks, and inserts separators. The first argument to CATX specifies the separator.  
 
### 8. SCAN Function  

The SCAN Function extracts words within a value that is marked by delimiters.  

SCAN( text, nth word, <delimiters>)  

For example :  

We wish to extract first word in a sentence 'Hi, How are you doing?'. In this case, delimiter is a blank.  

```sas
data _null_;
string='Hi, How are you doing?';
first_word=scan(string, 1, ' ' );
put first_word =;
run;
```

first_word returns 'Hi,' since it is the first word in the above sentence using blank as a delimiter.
We wish to extract last word in a sentence 'Hi, How are you doing?'. In this case, delimiter is a blank.  

```sas
data _null_;
string='Hi, How are you doing?';
last_word=scan(string, -1, ' ' );
put last_word =;
run;
```

last_word returns 'doing?' since it is the last word in the above sentence.   
Let's make it a little complicated.  
Suppose, delimiter is a character instead of blank or special sign.  

```sas
string='Hello SAS community people';
beginning= scan( string, 1, 'S' ); ** returns "Hello ";
middle = scan( string, 2, 'S' ); ** returns "A";
end= scan( string, 3, 'S' ); **returns " community people";
```

### 9. SUBSTR Function  

The SUBSTR function extracts strings based on character position and length. It is equivalent to MS Excel's MID Function.  

= substr(old_var, starting_position, number of characters to keep);  

__Examples__ :  

```sas
data _null_;
t="AFHood Analytics Group";
new_var=substr(t,8,9);
put new_var =;
run;
```

Result: new_var=Analytics  

### 10. SUBSTR(Left of =) Function  

It replaces a portion of string with new string  

```sas
data _null_;
string='old_variable';
substr(string,1,8) = "new_data";
put string =;
run;
```

Result: string=new_dataable

In this case, SUBSTR replaces the first 8 characters of string with the value "new_data". After this line executes, the value of string will be 'new_dataable'  

### 11. LOWCASE, UPCASE and PROPCASE  

LOWCASE converts the character string to lowercase.  

UPCASE converts the character string to uppercase.  

PROPCASE returns the word having uppercase in the first letter and lowercase in the rest of the letter (sentence format).  

```sas
data _null_;
  name = 'Hello world';
  name_upper = upcase(name);
  name_lower = lowcase(name);
  name_proper = propcase(name);  
  put name_upper=;
  put name_lower=;
  put name_proper=;  
run;
```

__Output:__  

name_upper=HELLO WORLD  

name_lower=hello world  

name_proper=Hello World  

### 12. INDEX Function  

The INDEX function finds characters or words in a character variable  

```sas
data _null_;
string='Hi,How are you doing?';
x = index(string, "How");
put x=;
run;
```

x returns 4 as "How" starts from 4th character.  

To select all the records having 'ian' in their character.  

```sas
if index(name,'ian') > 0;
```

To select all the records having first letter 'H'  
```sas
if name =: 'H';
```

### 13. FIND Function  

The FIND function locates a substring within a string  

FIND (character-value, find-string <,'modifiers'> <,start>)  

STRING1 = "Hello hello goodbye"  

Examples :  

1. FIND(STRING1, "hello") returns 7  

2. FIND("abcxyzabc","abc",4) 7

### 14. TRANWRD Function  

The TRANWRD function replaces all occurrences of a word in a character string. It doesn't replace full phrase (entire value content).  

TRANWRD (variable name, find what , replace with)  

Example : name : Mrs. Joan Smith  

name=tranwrd(name, "Mrs.", "Ms.");  

Result : Ms. Joan Smith  
 
### 15. TRANSLATE Function  

The TRANSLATE function replaces specific characters in a character expression  

TRANSLATE(source, replace with, find what)  

Examples:  

x = translate('XYZW','AB','VW');  

Result : "XYZB"  

### Difference between TRANWRD and TRANSLATE Functions  

The TRANSLATE function converts every occurrence of a user-supplied character to another character. TRANSLATE can scan for more than one character in a single call. In doing this, however, TRANSLATE searches for every occurrence of any of the individual characters within a string. That is, if any letter (or character) in the target string is found in the source string, it is replaced with the corresponding letter (or character) in the replacement string.  

The TRANWRD function differs from TRANSLATE in that it scans for words (or patterns of characters) and replaces those words with a second word (or pattern of characters).  

### 16. PRXMATCH  

The PRXMATCH function can be used for the following cases :  

When you want to identify if there is alphanumeric (has any letter from A to Z) in a variable.  

If you need to search a character variable for multiple different substrings.  

PRXMATCH (perl-regular-expression, source);    

Perl Regular Expression  

^ - start with  
$ - end with  
\D - any non digits  
\d - digits  
? - may or may not have?  
| - or  
* - repeating  
( i:) - turns ON the case insensitive search  
(-i:) - turn OFF the case insensitive search

### 1. Check alphanumeric value  

```sas
DATA test;
INPUT string $ 1-8;
prxmatch=prxmatch("/[a-zA-Z]/",string);
CARDS;
ACBED
11
12
zx
11 2c
abc123
;
run;
```

Note : prxmatch("/[a-zA-Z]/",string) checks first character.  

### 2. Replace multiple words with a new word  

if prxmatch('/Luthir|Luthr|Luther/',name) then name='Luthra' ;  

### 17. INPUT and PUT Function  

The INPUT Function is used to convert character variable to numeric.  

new_num=input(character-variable, 4.);  

Example -  

```sas
data temp;
x = '12345';
new_x = input(x,5.);
run;
```

In the above example, the variable x is a character variable as it is defined in quotes '12345'. The newly created variable new_x is in numeric format.  

The PUT Function is used to convert numeric variable to character.   

```sas
new_char=put(numeric,4.0);
```

```sas
data temp;
x = 12345;
new_x = put(x,5.);
run;
```

In this example, the variable x is originally in numeric format and later converted to character in the new variable new_x.  

### 18. LENGTH  

The LENGTH function returns length of a string.  

```sas
data _null_;
x='ABCDEF-!1.234';
n= length(x);
put n=;
run;
```

It returns 13.  

If you need to calculate the number of digits in a numeric variable -  

First, we need to convert our numeric variable to character to count the number of digits as LENGTH function works only for character variable.  

```sas
data _null_;
x = 12345;
cnt = length(strip(put(x,12.)));
put cnt=;
run;
```

In the above nested function, we first converted the variable x to character and then remove spaces by using STRIP function and then count number of digits by using LENGTH() function.  

Another Method -  

```sas
data _null_;
x = 12345;
cnt = int(log10(x)) + 1;
put cnt=;
run;
```
 
We can also use LOG10 function to solve it. LOG10 has a property which says :  

Number of Digits = Integer value of [LOG10(x)] + 1. For example, LOG10(100) = 2 so Number of digits in 100 = 2 +1. See LOG10(1100) = 3.04 => INT(3.04) = 3 => 3+1 = Number of digits in 1100.  

### 19. IF THEN  

IF THEN replaces the entire phrase in a string.  

```sas
data mydata;
input names $30.;
cards;
Raj Gates
Allen Lee
Dave Sandy
William Gates
Jon Jedi
;
run;

data mydata2;
set mydata;
length new_names $30.;
if find(names, "Raj") then new_names = "Raj Kumar";
else new_names = names;
run;
```

In the above SAS program we are checking if the string "Raj" is found within the variable "names". The FIND function is used to perform this search. If the string "Raj" is found, the if block is executed, and the value "Raj Kumar" is assigned to the "new_names" variable in the mydata2 dataset. If the string "Raj" is not found in the names variable, the else block is executed, and the value of the "names" variable is assigned to the "new_names" variable.  

### 20. COUNT Function  

The COUNT function counts the number of times that a specified substring appears within a character string.  

```sas
data _null_;
name = "DeepAnshu Bhalla";
x = count(name,"a");
x1 = count(name,"a","i");
put x= x1=;
run;
```

Result : x=2 as there are 2 lower case 'a's in the variable name. x1=3 as there are 3 'a's in the variable name (The 'i' modifier ignores case sensitivity)  
 
### 21. COUNTW Function  

The COUNTW function counts the number of words in a character string.  

```sas
data readin;
input name$15.;
cards;
Trait Jhonson
3+3=6
;
run;

data out;
set readin;
x = countw(name);
x1 = countw(name,' ');
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/e4f8eb52-b0d5-4bab-ac39-7d64607d1749)  

If you don't specify delimiter in the second parameter of COUNTW function, the function will use the default delimiter, which is a blank space.  

## INPUT Function  

### SAS: HOW TO CONVERT CHARACTER TO NUMERIC VARIABLE    

In SAS, the INPUT function is used to convert a character variable to a numeric variable. You can specify a informat within the INPUT function to control the conversion. The informat tells SAS how to interpret the data in the character variable.  

Below is the syntax of INPUT function.  
```sas
new_numeric_variable = input(character_variable, comma9.);  
```

### Example: Convert Character to Numeric Variable in SAS   

Here we are creating a sample dataset for demonstration. The dataset consists of a character variable with length 10. The dataset name is example and the character variable name is var1.  

```sas
data example;
  input var1 $10.;
  datalines;
123
456
789
;
run;


data want;
set example;
var2 = input(var1, comma9.);
run;
```

To confirm conversion, we can use PROC CONTENTS to check the data type and length of variable var2.  

```sas
proc contents data=want;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2206c590-cc08-4e9d-a631-4fa91081a800)  
  
As shown in the image above, var2 is a numeric variable whereas var1 is a character variable.    

Note- comma9. also handles character variable having commas or dollar signs.  

In order to use the same variable name after conversion, you can use DROP= option to remove the character variable. Then you can rename the new numeric variable to the old name using RENAME statement.  

```sas
data want (drop = var1);
set example;
var2 = input(var1, comma9.);
rename var2=var1;
run;
```

## PUT Function  

### SAS: HOW TO CONVERT NUMERIC TO CHARACTER VARIABLE  

In SAS, the PUT function is used to convert a numeric variable to a character variable. You can specify a format within the PUT function to control the conversion.  

Below is the syntax of PUT function.  

```sas
new_character_variable = put(numeric_variable, 8.);
```

### Example: Convert Numeric to Character Variable in SAS  

Let's create a sample dataset consisting of a numeric variable. The dataset name is example and the numeric variable name is var1.  

```sas
data example;
  input var1;
  datalines;
10
20
30
40
50
;
run;

data want;
set example;
var2 = put(var1, 8.);
run;
```

To validate conversion, we can use PROC CONTENTS to check the data type and length of variable var2.  

```sas
proc contents data=want;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3e0450ea-88d7-4a42-a6d3-dd4810e9a0f5)  

As shown in the image above, var2 is a character variable whereas var1 is a numeric variable.  

To maintain the same variable name after converting a numeric variable to a character variable in SAS, you can use the DROP= option to exclude the numeric variable from the dataset. Afterwards, you can proceed to rename the newly created character variable to match the original variable name using RENAME statement.  

```sas
data want (drop= var1);
set example;
var2 = put(var1, 8.);
rename var2=var1;
run;
```

## SUBSTR Function  

### SAS SUBSTR FUNCTION: LEARN WITH EXAMPLES   

This tutorial explains how to use SUBSTR function in SAS, along with examples.  

The SUBSTR function in SAS is used to extract a specific part of a string.  

### Syntax of SUBSTR Function  

Below is the syntax of SUBSTR function in SAS.

```sas
SUBSTR(string, start, length)
```
string: String from which you want to extract a substring.  

start: Starting position where the extraction should start.  

length: Number of characters to extract from the string. This is an optional argument. If you don't specify it, SAS would read the number of characters from the starting position to the end of the string.  

### Create Sample Dataset  

Let's create a sample SAS dataset that will be used to demonstrate examples in this tutorial.  

```sas
data readin;
  input name $20.;
  datalines;
John Simpson
Dane Stewart
Deepanshu Bhalla
Jonathan Lee
;
run;
```

### How to extract First N Characters?  

In the example below, we are extracting first name from the full name. We are pulling first 4 characters from the variable name.  

```sas
data readin2;
  set readin;
  firstname = substr(name, 1, 4);
run;

proc print data=readin2;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/120b3c01-0214-4d00-8570-20e79f8926cf)  

Incorrect Method: As shown in the image above, the first names of the last two individuals have a length greater than 4 characters. Hence, this results in an incorrect output.  

Correct Method: We can use the FIND function to find out the position of the first space in the name. The "firstname" variable extracts characters from the beginning of the name until the space. We have modified the SUBSTR function accordingly by combining it with the FIND function to make the code dynamic.  

```sas
data readin2;
  set readin;
  firstname = substr(name, 1, find(name, ' ') - 1);
run;

proc print data=readin2;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b5698445-4d99-4279-b882-1cb9732e6a89)  

### How to extract Last N Characters?  
 
In this example, we are showing how to extract last 3 characters using SUBSTR function in SAS.  

The LENGTH function is used here to determine the length of the variable "name". We have substracted 2 from it to set as starting position so that we can fetch last 3 characters from the variable "name".  

```sas
data readin2;
  set readin;
  last3 = substr(name, length(name)-2,3);
run;

proc print data=readin2;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/c3e0335f-c781-41d9-a1bd-1722366ddde0)  

To extract last name from the variable name, you can use the code below.  

```sas
data readin2;
  set readin;
  lastname1 = substr(name, 6);
  lastname2 = substr(name, find(name, ' ') + 1);
run;

proc print data=readin2;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d2c48c4a-4c2d-489a-aa55-0f93a57b74e5)  

The lastname1 variable is static and always extracts from the 6th character till the end .  

The lastname2 variable extracts characters after the space till the end of the name. Here we are using FIND function like the previous example to determine the position of space.  

__Note__: In the code above, we have not defined the third argument of the SUBSTR function. SAS automatically considers it as extracting characters till the last character by default.  

### How to use SUBSTR in IF-ELSE?  

Suppose you want to create a new variable based on the first letter of the variable "name". If the first letter is 'J' then set new variable as 'pass' else 'fail'.  

```sas
data readin2;
  set readin;
  if substr(name, 1,1) = 'J' then newvar = 'pass';
  else newvar = 'fail';
run;

proc print data=readin2;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a66043be-a054-4271-83df-6d4fdf82748f)  

### How to replace characters using SUBSTR?  

Suppose you have a phone number and you want to change the country code of the number. Here we are replacing the second and third character with '87'.  

```sas
data _null_ ;
phone='(91) 9811-4343' ;
substr(phone, 2, 2)='87' ;
put phone=;
run;
```

Result: phone=(87) 9811-4343  

phone has been changed from (91) 9811-4343 to (87) 9811-4343.  

## INDEX Function  

### SAS INDEX FUNCTION: LEARN WITH EXAMPLES  

This article explains how to use the INDEX function in SAS. It includes several examples that you can practice with to become proficient in using the INDEX function.  

### What does the INDEX Function do?  

The INDEX function in SAS is used to return the position of the first occurrence of a substring within a character string.  

### Syntax: INDEX Function  

The syntax of the INDEX Function is as follows -  
```sas
INDEX(string, substring)
```

string: The string within which you want to find the substring.  

substring: The substring you want to find within the string.  

### Examples: INDEX Function  

Here are some examples that will help you understand how to use the INDEX function in SAS. Let's generate a sample dataset for demonstration purposes.  

```sas
data mydata;
input names $30.;
cards;
Raj Gates
Allen Lee
Dave Sandy
William Gates
Jon Jedi
;
run;
```

In the example below we are using the INDEX function to find the position of the first occurrence of the string "Gates" in each observation of the variable "names".  

```sas
data readin;
set mydata;
position = index(names, "Gates");
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/132ff055-7331-49d0-a324-3ff9213653d3)  

In the above SAS Program, we have created a new variable named position which stores the position of the first occurrence of the string "Gates". The INDEX function returns 0 if the substring does not exist in the string. In this example it returns a value of 0 when the variable "names" does not contain "Gates" in the observation.  

### How to handle case sensitivity in INDEX Function?  

The INDEX function is case-sensitive which means it treats "gates", "Gates" and "GATES" as different substrings.  

```sas
data readin;
set mydata;
position = index(names, "gates");
proc print;
run;
```

__Wrong Output__  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/76b7cb24-c281-4d21-84c9-c5e194326b1a)  

The INDEX function returned 0 because it couldn't find 'gates' in the 'names' variable. 'Gates' does exist in the variable, but the function differentiates between uppercase 'G' and lowercase 'g'.  

To fix this issue, we can convert the variable to lowercase using the LOWCASE function. This will result in "Gates" becoming "gates".  

```sas
data readin;
set mydata;
position = index(lowcase(names), "gates");
proc print;
run;
```

__Correct Output__  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/99a36c0d-ee5a-4732-bc1c-49c66d83ea0b)  

### How to handle spaces in INDEX Function?  

Let's say you have a variable that contains leading spaces. See the sample dataset below. Leading spaces cause a change in the position of a substring within the longer string.  

```sas
data mydata;
input names $char15.;
datalines;
peter smith
  peter doe
 peter johnson
;
run;
```

To fix this, we can use STRIP function to remove leading (and trailing) spaces. Compare the values of two variables named "position" and "position2". The variable "position2" leverages the STRIP function whereas the variable "position" is without the STRIP function.  

```sas
data readin;
set mydata;
position  = index(names, "peter");
position2 = index(strip(names), "peter");
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/21196092-72be-42e3-be3d-ca04136dac39)  

### How to filter data using INDEX Function?  

In this example we are using a dataset named CARS from SASHELP library. It is a built-in SAS dataset that contains information about various car models. We are selecting only those models that contain "convertible" in their names.  

To filter data using the INDEX function in SAS, we added a WHERE statement to specify the condition for filtering. The INDEX function is used within the WHERE statement to check if the substring "convertible" exists in the variable. If the result of the INDEX function is greater than 0, it means the substring is found, and the record is included in the filtered dataset.  

```sas
data readin;
set sashelp.cars;
where index(lowcase(model), 'convertible') > 0;
run;
```

## SCAN Function  

### SAS SCAN FUNCTION: LEARN WITH EXAMPLES  

This article explains how to use the SCAN function in SAS. It includes various examples to practice and master the SCAN function. By the end of the tutorial, you should be able to understand how this function works and its practical use cases.  

### What does the SCAN Function do?  

The SCAN Function in SAS extracts words from a character string. Character string is a variable having text. For example let's say you have a variable which contains this sentence I love SAS and you wish to extract the second word "love" from this sentence.    

### Syntax: SCAN Function  

The syntax of the SCAN Function is as follows -  
```sas
SCAN(text, nth-word, [delimiters], [modifiers])
```

text: The string from which you want to extract the word.  

nth-word: The nth-word is the position of the word you want to extract. A positive value extracts from left to right, and a negative value extracts from right to left.  

delimiters: The delimiter that separate the words within the string. It is optional. By default it takes space as delimiter.  

modifiers: It is an optional argument that can be used to change or expand the default behavior of SCAN Function. For example it can be used to perform a case-insensitive search. See the list of modifiers in the next section of this tutorial.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/f494077b-883a-464d-a096-deaa37fb75e2)  

### Examples: SCAN Function  

Let's take a simple example. We have a string I love SAS Programming and we want to extract second word from the string.  

```sas
data _null_;
text = "I love SAS Programming";
result = scan(text,2);
put result=;
run;
```

__Output__  

As shown in the image below, "love" is the second word extracted from the string. The DATA _NULL_ statement is used when you need to perform some operations or calculations without creating an output dataset. In the above example, we have not created any dataset as we just wanted to show how SCAN function works.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/bf0b59bf-76a4-468c-a9d9-2e19907a9a46)  

### SCAN : Extract the second last word  

There are two ways to scan from right to left in the SCAN function.  

Solution 1  

The SCAN function can also be used to read from right to left. When you specify a negative number in the second argument of the function nth-word, SAS starts scanning from the right. For example -1 means the last word of the string.  

Since we wish to find the second last word in the string, we have mentioned -2 in the second argument of the SCAN function.  

```sas
data _null_;
text = "I love SAS Programming";
result = scan(text,-2);
put result=;
run;
```

Output  

As shown in the image below, the SAS Program returns "SAS" as the second-to-last word.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/35722baa-9535-455a-a698-5764e71291b7)  

Solution 2 : Use Modifier  

We can also scan from right to left using modifier which is the fourth argument of the SCAN Function. The "b" modifier tells SAS to scan backward which means reading string from right to left.  

```sas
data _null_;
text = "I love SAS Programming";
result = scan(text,2," ","b");
put result=;
run;
```

### SCAN : Handle Delimiters  

Let's create a sample dataset for demonstration. In the dataset, we have a variable (column) named 'text' which contains names not in a proper format. Suppose you are asked to pull lastname from the variable. 

Comma (,) is a separator or delimiter in the example below. Hence we will use comma as a third argument in the function to extract last name from the variable 'text'.  

```sas
data readin;
input text $30.;
datalines;
Mrs Serena, Williams
Mr. Dave, Sandy
Rakesh Kumar, Arora
Peter,Sandreas
;
run;

data readin2;
set readin;
lastname=scan(text,2,",");
proc print;
run;
```
 
Output  

In the above SAS program, we have created a new variable named 'lastname' which contains last names.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/64d0da5d-8f58-44e3-866b-06df59cee542)  

### SCAN : Convert a String into Multiple Observations  

Suppose you have a string that consists of multiple substrings delimited by commas, and you wish to transform it into multiple observations (rows).  

```sas
data readin;
input text $30.;
datalines;
live, love, laugh, repeat
;
run;
```

```sas
data readin2(keep=word);
set readin;
  do i = 1 to countw(text, ',');
    word = scan(text, i, ',');
    output;
  end;
proc print;	
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8d97b406-d845-402d-850e-46ab3fa4ea5e)  

Explanation  

A DO loop is initiated with the variable 'i' iterating from 1 to the number of words in the 'text' variable, separated by commas. This is done using the 'COUNTW' function.  

Within the loop, the SCAN function is used to extract each word from the 'text' variable based on the current value of 'i' and the comma delimiter. The extracted word is then assigned to the 'word' variable.  

The 'OUTPUT' statement is used to store each word as a separate observation in the new dataset named 'readin2'. It is run within the loop.  

In the new dataset named 'readin2', we have kept the variable 'word' only. We didn't retain the variables 'i', 'text'.  

### SCAN : Convert a String into Multiple Variables  

In the previous example, we converted a string into multiple rows. Here, we are transforming it into multiple columns (variables). We have used the same sample dataset in this example.  

```sas
data readin;
input text $30.;
datalines;
live, love, laugh, repeat
;
run;
```

```sas
data _null_;
set readin;
call symputx('nWords', countw(text, ","));  
run;

data readin2;
  set readin;
  array word[&nWords] $12 word1-word&nWords;  
  do i = 1 to &nWords;
    word[i] = scan(text, i, ',');
  end;
  drop i;
proc print;  
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b93aa7fe-0655-4813-8481-f08a43bc758b)  

Explanation  

First we count the number of words in the variable "text" using the countw function, with the delimiter as a comma (","). The call symputx statement was used to create a macro variable named "nWords" and assigned the count of words to it.  

We declared an array named "word" with a size equal to the value stored in the macro variable "nWords". Each array element is a character variable of length 12, and the variables are named "word1" to "word4". Then we executed a do-loop that iterates from 1 to the value of "nWords".  

Within the do-loop, we assigned each word from the variable "text" to the corresponding element of the array "word" using the scan function with a comma (",") as the delimiter. In simple words, we created a new variable for each word in the variable "text". Later we removed the variable "i" from the dataset.  

## FIND Function  

### SAS FIND FUNCTION: LEARN WITH EXAMPLES  

In this tutorial, we will show how to use the FIND Function in SAS, along with examples.  

### What does FIND Function do in SAS?  

The FIND function is used in SAS to search for a specific substring within a string. It returns the position of the first occurrence of the substring within the string.  

### Syntax of FIND Function  

Below is the syntax of FIND Function in SAS.  
```sas
FIND( string, substring , [modifier], [start-position])
```

string: The character variable or string that you want to search.  

substring: The character variable or string that you want to find within the string.  

modifier (optional): Specifies the type of search to be performed. It can be any of the following:  

i: Performs a case-insensitive search.
t: Trims trailing blanks from string and substring.  

start-position (optional): Specifies the position in the string where the search should start. It can be a positive or negative integer. A positive value starts the search from the beginning of the string, while a negative value starts the search from the end of the string.  

### Sample Dataset  

Let's create a sample dataset for demonstration purpose.  

```sas
data mydata;
input text $22.;
datalines;
What is your name?
His name sounds cool
He looks sharper
His name is David
Name:What's in a name
;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/34301d53-9a23-4f41-8d38-716661ec98a1)  

### Examples: FIND Function  

In this section, we will cover various examples of the FIND function to gain a better understanding of how it works.  

Find Position of First Occurrence of String  

Here we are using the FIND function to search for the occurrence of "name" within the variable "text".  

```sas
data newdata;
set mydata;
first_name = find(text, "name");
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ada06607-eec8-4331-b47b-305c35c8c894)  

"What is your name?": The first occurrence of "name" is at position 14 in the text.  

"His name sounds cool": The first occurrence of "name" is at position 5 in the text.  

"He looks sharper": The word "name" is not present in this text, so the result is 0, indicating no occurrence.  

"His name is David": The first occurrence of "name" is at position 5 in the text.  

"Name: What's in a name": The first occurrence of "name" is at position 18 in the text. Please note it is case-sensitive.  

The position of the first occurrence is stored in the variable "first_name" in the new dataset "newdata.  

### Find Case-Insensitive First Occurrence Position  

To make the search case-insensitive i.e. treating uppercase and lowercase letters as equal, we can use the modifier i in the FIND function.  

```sas
data newdata;
set mydata;
first_name = find(text, "name", "i");
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/ec0cf938-55b2-4787-9fc9-9ab8d4d79652)  

Look at the last observation - "Name: What's in a name". It has two occurrences of "name". After enabling case-insensitive search, it returns 1 instead of 18.  

### Customize Search with Custom Start Position  

In the code below, the number 6 represents the position in the text string from where the search should start.  

```sas
data newdata;
set mydata;
first_name = find(text, "name", "i", 6);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/984b00d8-779a-4c63-9fc9-290221a278a8)  

It returns 0 for second and fourth row as "name" in these two rows are at position 5.  

## COMPRESS Function  

### SAS COMPRESS FUNCTION: LEARN WITH EXAMPLES  

In this tutorial we will cover how to use the COMPRESS function in SAS, along with examples.  

### What does the COMPRESS Function do?  

The COMPRESS function in SAS is used to remove specific characters from a string.

### Syntax of COMPRESS Function  

The syntax of the COMPRESS function is as follows:  

```sas
COMPRESS(string, characters to be removed, modifier)
```

string: The string from which you want to remove characters.  

characters to be removed: The characters that you want to remove from the original string.  

modifier It is an optional argument. Specify the keyword for the action you want to perform.  

### List of Modifiers  

Here is a list of modifiers in the COMPRESS function in SAS.  

a – Remove all alphabetical characters from String.
ak - Keep only alphabets from String.
kd - Keep only numeric values from String.
d – Remove numerical values from String.
i – Remove specified characters (both upper and lower case) from String.
k – Keep the specified characters in the String instead of removing them.
l – Remove lowercase characters from String.
p – Remove punctuation characters from String.
s – Remove spaces from String. This is the default.
u – Remove uppercase characters from String.  

### Sample Dataset  

The following code creates a sample SAS Dataset that will be used to demonstrate examples of the COMPRESS function.  

```sas
data mydata;
input name $20.;
cards;
Sandy David 123.
Sam Andreas@14
123Sahil Arora
#Deeps Bhalla
;
run;
```

### 1. Remove All Spaces from String  

By default, the COMPRESS function removes leading, between and trailing spaces from a string.  

```sas
data mydata2;
  set mydata;
  name2 = compress(name);
run;
 ```

 ![image](https://github.com/Deepak2k20/SAS/assets/65231118/16cba23b-e812-42cf-bc6b-f229c7b6c1c1)  

 The above code takes the existing dataset "mydata" and creates a new dataset "mydata2" with an additional variable "name2", where the values in "name2" have spaces removed using the COMPRESS function.  

 ### 2. Remove Specific Characters from String  
 
Here we are deleting characters - at sign (@) and hash sign (#) from the "name" column.  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '@#');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/4013c90e-d4d0-4b2b-b489-91032fd53507)  

### 3. Remove all alphabets from string  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'a');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/7416d25e-3199-4c18-bfa8-e8c477026a74)  

### 4. Keep only alphabets from string  

Here we are keeping all alphabetical characters from a string and removing everything else.  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'ak');
run;
 ```

 ![image](https://github.com/Deepak2k20/SAS/assets/65231118/69edccae-cfcc-4693-8f86-1de5a5ebf95a)  

 ### 5. Keep only numeric values from string  

 ```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'kd');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/b399dd90-8791-4594-ab49-a582e4f8034b)  

### 6. Remove numerical values from string  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'd');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/de3ba96d-b1a0-410f-bf0a-c69f8505e6bc)  

### 7. Remove specified characters both upper and lower case from string

To remove specified characters from a string while ignoring case sensitivity, you can use the COMPRESS function in SAS with the 'i' modifier.  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, 's', 'i');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d850d18a-1609-43cd-8cf9-75cc5753912e)  

If you look at the second observation, both the capital and small letter 'S' or 's' were removed from name.  

### 8. Keep the specified characters in the string  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, 's', 'k');
run;
```

### 9. Remove lowercase characters from string  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'l');
run;
```

### 10. Remove uppercase characters from string  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'u');
run;
```

### 11. Remove punctuation characters from string  

```sas
data mydata2;
  set mydata;
  name2 = compress(name, '', 'p');
run;
```

## COUNTW Function  

### HOW TO USE COUNTW FUNCTION IN SAS (WITH EXAMPLES)  

In this tutorial, we will show how to use the COUNTW Function in SAS, along with examples.  

### What does COUNTW Function do in SAS?  

The COUNTW function is used in SAS to count the number of words in a character string.  

### Syntax of COUNTW Function  

Below is the syntax of COUNTW Function in SAS.  

```sas
COUNTW(string, [character(s)] , [modifier(s)])
```

string: The character variable or string.  

character(s) (optional): Delimiters that separate words.  

modifier(s) (optional): Keywords that can change how the COUNTW function works.  

### Sample Dataset  

Let's create a sample dataset for demonstration purpose.  

```sas
data example;
input string $60.;
datalines;
It's a pleasant day today
I_am yet to receive payment
352+20+2=374
Send to my address xyz_a@gmail
;
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/82bfae14-a522-4fc2-bdd7-f799859b09d6)  

Here we are using the COUNTW function to count the number of words in the variable "string".  

```sas
data newdata;
set example;
count_words=countw(string);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3ad0c9ba-bec8-4a9c-9cd6-22f69864b054)  

By default SAS consider the followings as default delimiters:  

blank ! $ % & ( ) * + , - . / ; < ^ |  

In the example above it considered blank and + as delimiters to count the number of words.  

### How to define delimiters in the COUNTW Function  

In the COUNTW function, we can specify a delimiter which makes it to count the number of words based on the specified delimiter rather than the default one. In the example below, we are using blank space and underscore (_) sign as separators.  

```sas
data newdata;
set example;
count_words=countw(string, ' ');
count_words_=countw(string, '_');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/5796e16d-9d7c-4041-836c-137b6e26d1b9)  

### How to use modifiers in the COUNTW Function  

Below is an example where we are using the COUNTW function with the 'd' modifier. The 'd' modifier refers to digits. Here we are counting the number of words separated by digits.  

```sas
data newdata;
set example;
count_words_digits=countw(string, , 'd');
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/80d3bb79-1986-4ffe-93f8-22eab673174c)  

Important Note: You don't need to specify anything in the second argument when using the modifier.  

Here is a list of modifiers that can be used in the COUNTW Function in SAS.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d6991158-b3a7-4555-b8ca-8f99c0909866)  

## STRIP Function  

### STRIP FUNCTION IN SAS : REMOVE SPACES FROM STRING  

In SAS, the STRIP function removes both the leading and trailing spaces from a string or character variable. It is equivalent to MS Excel's TRIM Function.

Please note that the STRIP function does not remove spaces between words. Use COMPRESS function instead if you want to remove spaces between words.

The syntax of STRIP function is as follows:

```sas
new_variable = strip(variable)
```

### Sample Dataset  

Let's create a sample SAS dataset for demonstration purpose.  

```sas
data example;
input name $char20.;
cards;
    David Sandy 
   Sam Andrews
;
run;
```

The following code creates "result" dataset that stores the same observations as the "example" dataset, but with an additional variable called "name_clean" that stores the cleaned version of the "name" variable, removing any leading or trailing spaces.

```sas
data result;
set example;
name_clean = strip(name);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/0e8a71b3-1ca0-4f47-b0bf-9db3d3c2e77a)  

## TRANWRD and TRANSLATE Functions  

### SAS: TRANWRD AND TRANSLATE FUNCTIONS (WITH EXAMPLES)  

In this tutorial, we will show how to use the TRANWRD and TRANSLATE functions in SAS, along with examples.  

### Difference between TRANWRD and TRANSLATE Functions  

The TRANWRD replaces specific words within a character string with other words, whereas the TRANSLATE function replaces specific characters within a character string with other characters.  

To remember the TRANWRD function, you can focus on the last three characters "WRD" which can stand for "Word Replacement"  

### Syntax of TRANWRD and TRANSLATE Functions  

__TRANWRD__

The syntax of the TRANWRD Function in SAS is as follows:  

```sas
TRANWRD(string, find_what , replace_with)
```

__TRANSLATE__

Below is the syntax of TRANSLATE Function in SAS.  

```sas
TRANSLATE(string, replace_with, find_what)
```

string: The character variable or string.  

find_what : The character or word to be replaced within the string.  

replace_with : The character or word that will replace the old word within the string.  

### Sample Dataset  

Let's create a sample dataset for demonstration purpose.  

```sas
data have;
input phrase $45.;
cards;
Hello, How are you doing?
The brown cat jumps over the hairy dog
XYYXYYY
;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3a6a9821-0d84-4bba-87fc-071516fb5ba0)  

Here we are replacing characters XY with AB in the character variable named "phrase".  

```sas
data want;
set have;
phrase_tranwrd = tranwrd(phrase, "XY", "AB");
phrase_translate = translate(phrase, "AB", "XY");
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/eb0b5dd8-4037-4cbc-baf9-be906f339066)  

"XYYXYYY" becomes "ABYABYY" because TRANWRD replaces the pattern "XY" with "AB" whereas TRANSLATE returns ABBABBB as it replaces each occurrence of "X" with "A" and each occurence of "Y" with "B".  

### How to replace words in SAS?  

In this example, we are going to replace the word Hello with Hey.  

```sas
data want;
set have;
new_phrase = tranwrd(phrase, "Hello", "Hey");
new_phrase2= translate(phrase, "Hey", "Hello");
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2482df4a-8122-4464-a67c-db0bcb9821f1)  

When we used the TRANSLATE function with the input string "Hello, How are you doing?" and replaced "Hello" with "Hey", the resulting string is "Heyy , H w are y u d ing?".  

Since the TRANSLATE function replaces individual characters, it doesn't recognize the entire "Hello" and "Hey" as a single unit. Instead, it replaces each occurrence of "H" with "H", "e" with "e", and "l" with "y" and "o" with blank.  

## Convert Strings to Lowercase, Uppercase & Proper Case  

### SAS: LOWERCASE, UPPERCASE & PROPER CASE  

This tutorial explains how to convert a string to lowercase, uppercase and proper case in SAS, along with examples.  

The descriptions and syntax of LOWCASE, UPCASE, PROPCASE, ANYLOWER, and ANYUPPER functions are as follows:  

LOWCASE: Converts a string to lowercase.  

Syntax: lowercase_string = lowcase(original_string);  

UPCASE: Converts a string to uppercase.  

Syntax: uppercase_string = upcase(original_string);  

PROPCASE: Converts a string to proper case.  

Syntax: propercase_string = propcase(original_string);  

ANYLOWER: Returns position of first lowercase character.  

Syntax: position = anylower(original_string);  

ANYUPPER: Returns position of first uppercase character.  

Syntax: position = anyupper(original_string);  
 
### Sample Dataset  

Let's create a sample SAS dataset that will be used in the examples of this tutorial.  

```sasdata mydata;
input company $ 1-20;
cards;
google
gooGle
Microsoft
APPLE
;
run;
```

### How to Convert Strings to Uppercase  

The following code uses the upcase() function to convert the values in the "company" variable to uppercase, and the result is stored in the new variable "company_new".  

```sas
data example;
set mydata;
company_new = upcase(company);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/90e7fdbe-d0f1-40ae-866d-b405825bf549)  

### How to Convert Strings to Lowercase  

The following code uses the lowcase() function to convert the values in the "company" variable to lowercase, and the result is stored in the new variable "company_new".  

```sas
data example;
set mydata;
company_new = lowcase(company);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/e9f612e6-5cd2-48c0-87a2-bd2227b1ae26)  

### How to Convert Strings to Proper Case  

The following code uses the propcase() function to convert the values in the "company" variable to proper case, and the result is stored in the new variable "company_new".  

Proper case refers to a style where the first letter of each word is in uppercase, while the remaining letters are in lowercase. For example, consider the sentence: "hello world". In proper case, it would be written as: "Hello World".  

```sas
data example;
set mydata;
company_new = propcase(company);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/183d4740-caf4-4cd3-87c2-ba781cb26140)  

### How to Detect Lowercase and Uppercase Letters  

The following code calculates the positions of the first lowercase and uppercase characters in the "company" variable using the ANYLOWER and ANYUPPER functions. The results are stored in the "lower_position" and "upper_position" variables.  

```sas
data example;
set mydata;
lower_position = ANYLOWER(company);
upper_position= ANYUPPER(company);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/cd42de1f-f053-4af4-b08d-196a991ad72a)  

## Concatenate Functions - CAT, CATT, CATS, CATX  

### SAS: CONCATENATE STRINGS WITH CAT, CATT, CATS & CATX  

This tutorial explains five different ways to quickly concatenate strings (character values) in SAS.  

### Concatenate Strings using Concatenation Operator (||)  

combined_variable = variable1 || variable2  

### CAT Function: Concatenate Strings  

combined_variable = CAT(variable1, variable2)  

### CATT Function: Concatenate Strings with No Trailing Space  

combined_variable = CATT(variable1, variable2)  

### CATS Function: Concatenate Strings with No Space  

combined_variable = CATS(variable1, variable2)  

### CATX Function: Concatenate Strings with a Delimiter and No Space  

combined_variable = CATX(delimiter, variable1, variable2)   

### Sample Dataset  

Let's create a sample dataset for demonstration purpose. This dataset will be used in the examples below.  

```sas
data have;
length first_name $9.;
input first_name $ last_name $ sales;
cards;
Joe Dan 25
Jason Roy 22
Deeps Arora 31
Deepanshu Bhalla 27
;
run;
```

### Method 1: Concatenate Strings using Concatenation Operator (||)  

In SAS, the double vertical bar (||) joins strings. It's the oldest method in SAS to combine strings.  

```sas
data want;
set have;
name = first_name ||  last_name;
run;
 ```

The double vertical bar (||) has a limitation of adding unnecessary spaces when concatenating strings. Refer to the image below. The variable first_name has a length of 9 characters so it adds spaces in all the strings where length is less than 9. It doesn't add a space against name 'Deepanshu' because it has a length of 9 characters. Hence this method is not recommended.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8734e775-702b-4f4b-8813-64038a942c0b)  

To fix the unnecessary spaces between the text, we can use the STRIP function to remove leading and trailing spaces before concatenating. Here we are adding one space between the first and last name to create a full name.  

```sas
data want;
set have;
name = strip(first_name) || " " || strip(last_name);
run;

proc print data=want;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/76f441f9-9ebb-45a2-8d9b-3f11dc08d15c)  

### Method 2: Concatenate Strings using CAT Function  

The CAT function combines strings without removing any spaces at the beginning or end. Please note that if any of the variable is numeric, it will be converted to a character string, and any leading or trailing spaces will be removed.  

```sas
data want;
set have;
name = cat(first_name, last_name);
run;
```

The CAT Function also has a limitation of having spaces at the end which makes spacing between two strings inconsistent when concatenating the strings.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/0daeca26-8613-44c9-ad67-cd1d80d99d50)  

### Method 3: Concatenate Strings using CATT Function  

The CATT function combines strings and removes trailing spaces when concatenating. The extra "T" in "CATT" refers to TRIM function in SAS which removes the trailing blanks.  

```sas
data want;
set have;
name = catt(first_name, last_name);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9970f717-7740-49bd-b34a-2784a3ceba73)  

### Method 4: Concatenate Strings using CATS Function  

The CATS function combines strings and removes both leading and trailing spaces when concatenating. The "S" in "CATS" refers to the STRIP function which removes both leading and trailing blanks.  

```sas
data want;
set have;
name = cats(first_name, last_name);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/8faadd60-6e22-49fe-95e2-ee26f37bce60)  

### Method 5: Concatenate Strings using CATX Function  

The CATX function combines strings and separates them with a delimiter. The CATX function also removes leading and trailing spaces when concatenating.  

You can specify any delimiter you want in the first argument of CATX function. In the code below, we are showing two different examples wherein we are using one space and "-" as delimiters.  

```sas
data want;
set have;
name  = catx(" ", first_name, last_name);
name2 = catx("-", first_name, last_name);
run;

proc print data=want;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/dbd4aecc-ef37-4779-8bb8-8d03c1c962f5)  

### Compare Methods of Concatenation in SAS  

In the table below, we have a comparison of five different methods of concatenation in SAS. It is recommended to use the CATX function.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/e22a62aa-f884-4c4d-8238-ca515d61bbe1)  

## Pattern Matching - PRXMATCH and PRXCHANGE Functions  

### PATTERN MATCHING WITH SAS  

This tutorial explains how to use regular expression language (pattern matching) with SAS.  

### Sample Data  

```sas
data x;
infile datalines truncover;
input name $100.;
datalines;
Deepanshu
How are you, deepanshu
dipanshu
deepanshu is a good boy
My name is deepanshu
Deepanshu Bhalla
Deepanshuuu
DeepanshuBhalla
Bhalla Deepanshu
;
run;
```

### Important Functions for Pattern Matching  

### 1. PRXMATCH

Searches for a pattern match and returns the position at which the pattern is found.  

```sas
PRXMATCH (perl-regular-expression, variable_name)  
```

It returns the position at which the string begins. If there is no match, PRXMATCH returns a zero.  

Example 1 :  

```sas
data xx;
set x;
if prxmatch("/Deepanshu/", name) > 0 then flag = 1;
if prxmatch("/Deepanshu/i", name) > 0 then flag1 = 1;
if prxmatch("/^Deepanshu/i", name) > 0 then flag2 = 1;
if prxmatch("/\bDeepanshu\b/i", name) > 0 then flag3 = 1;
if prxmatch("/D[ai]panshu/i", name) > 0 then flag4 = 1;
if prxmatch("/D.panshu/i", name) > 0 then flag5 = 1;
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/9810c687-318d-49bf-9af7-4a18a77bf3d3)  

### Important Points

The /i in the regular expression makes search case-insensitive.  

The ^ in the regular expression tells SAS to search for the strings that starts with the search-string.  

The \b in the regular expression tells SAS to match word boundary.  

The \B in the regular expression tells SAS to match non-word boundary.  

The [ai] in the regular expression searches any of the characters within the string.  

The . in the regular expression tells SAS to take any of the characters within the string.  

### Example 2 : Search Multiple Sub Strings  

```sas
data temp;
Input company $30.;
cards;
Tata
tata
Tataz
TataM Jan
Tata Motor
Reliance World
Reliance Ltd
Reliance Petro
Reliance Global
Vanucoverltd Company
;
run;
```

```sas
data temp1;
set temp;
if prxmatch("/\b(Tata|Reliance)\b/i",company) > 0;run;
```
 
### Example 3 : Find Pattern  

Suppose you are asked to find strings that contain length of 4 characters. The first character must contain a letter and the remaining characters must contain numeric.  

```sas
data _null_;
x =  'A345';
x2 = 'A55A';
y =  prxmatch("/^[a-zA-Z][0-9]{3}$/", x);
y2 = prxmatch("/^[a-zA-Z][0-9]{3}$/", x2);
put y= y2=;
run;
```

### 2. PRXCHANGE Function

It performs a pattern-matching replacement.  

```sas
PRXCHANGE(regular-expression, -1, variable) 
```

Suppose you are asked to replace 'Tata' with 'Tata Group'.  

```sas
data temp2;
set temp;
Company0 = PrxChange('s/\b(Tata)\b/Tata Group/i' , -1 , strip(company));
proc print;
run;
```

__Note__ : The 's keyword indicates substitution.  

### Remove a list of keywords such as Jan, Ltd, Company  

Company1 = PrxChange('s/\b(Jan|ltd|Company)\b//i' , -1 , strip(company));  

## Fuzzy Matching - COMPGED Function  

### FUZZY MATCHING WITH SAS  

This tutorial explains how to perform fuzzy matching (string matching) with SAS.  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/0bd5aba1-4fb4-4ff4-90df-6cebbcf2d6c8)  

### Sample Datasets  

```sas
Data temp ;
Input company $30.;
cards;
Vanucover
Reliance
Tata
Tata Motors
;
run;
```

```sas
data temp2;
Input company $30.;
cards;
Tata
tata
Tataz
TataM Jan2015
Tata Motor
Reliance World
Reliance Ltd
Reliance #Petro
Reliance Global
Vanucoverltd 12 Company
;
run;
```

### Steps

### 1. Remove punctuations, special characters, numeric values, dates.

Company1 = compress(company, '',"ak");
Company2 = compbl(PrxChange('s/\b(?:Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\b//i' , -1 , strip(company1)));  

- COMPRESS with modifier ak removes punctuations, special characters and numeric values.  

- PRXCHANGE performs a pattern-matching replacement. It is an alternative to TRANWRD which can only replace a single keyword at a time. However, PRXCHANGE can replace multiple keywords at one run.

### Detailed Explanation - PRXCHANGE  

The 's tells SAS that we want to substitute or replace some keywords.   

The /\b(?: tells SAS to use these keywords when they are not grouped with other keywords. For example, It differentiate between 'Smith Jan' and 'JanSmith'. It would replace 'Jan' from 'Smith Jan' but not from 'Jan Smith'.  

The //i  tells SAS to substitute keywords with blank. If you want to substitute with a keyword 'blank', change //i  to  /blank/i.    

### 2. Setting Stopwords such as Corporation, Corp,Ltd, Limited, Inc etc,  

Company3 = compbl(PrxChange('s/\b(?:Corporation|Corp|Ltd|Limited|Inc|Incorporated|Company|Co|LTD|LLC|PLLC)\b//i' , -1 ,Strip(Company2)));  

### 3. Apply fuzzy matching using COMPGED function.  

COMPGED(String1, String2, 400, 'LN')  

The COMPGED function returns the generalized edit distance between two strings. In the code, 400 is the cut off. If the actual generalized edit distance is greater than the value of cutoff, the value that is returned is equal to the value of cutoff.  

The 'LN' modifier tells SAS to consider the following points before comparing the values  

remove leading blanks in string-1 and string-2  

remove quotations and ignore case sensitivity.  

### Important Point

The value that is returned by COMPGED(string1, string2) is not always equal to the value that is returned by COMPGED(string2, string1) .  

```sas
data _null_;
x = compged('Tata', 'TataM');
y = compged('TataM', 'Tata');
put x y;
run;
```

### Full SAS Code : Fuzzy Matching  

```sas
data temp3 (drop = company1 company2);
set temp2;
company1 = compress(company, '',"ak"); /** Keeping only characters**/;
/**Stopwords**/;
Company2 = compbl(PrxChange('s/\b(?:Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\b//i' , -1 , strip(company1)));
Company3 = compbl(PrxChange('s/\b(?:Corporation|Corp|Ltd|Limited|Inc|Incorporated|Company|Co|LTD|LLC|PLLC)\b//i' , -1 ,Strip(Company2)));
run;
```

```sas
proc sql noprint;
create table matrix as
select a.Company , a.company3 as cleaned_text, b.Company as Company2, COMPGED(a.Company3, b.Company, 400, 'LN') as GEDSCORE
from temp3 a left join temp b
on compged(a.company3, b.company, 'LN') < 400
group by a.company
having GEDSCORE= min(GEDSCORE)
order by a.company;
quit;
```

### Method 2 : Improve Performance of Fuzzy Matching  

Since COMPGED on 2 tables returns cartesian product of the two tables, it is a very memory extensive process. Suppose you have two tables - first table contains 100 cases and other table contains 1 million cases, it would return 100 million cases.  

Tip : Improve Performance of Fuzzy Matching on large table  

The quick tip to improve performance is to select exact matches outside COMPGED function and excludes these exact match cases when you apply COMPGED function.  

```sas
proc sql noprint;
**Selecting exact matches;
create table matrix as
select a.company, a.company3 as cleaned_text, b.company as company2
from temp3 a inner join temp b
on UPCASE(a.company3) = UPCASE(b.company);

**Run compged on non-exact matches;
create table matrix2 as
select a.Company , a.company3 as cleaned_text, b.Company as Company2,
COMPGED(a.Company3, b.Company, 400, 'LN') as GEDSCORE
from temp3 a left join temp b
on compged(a.company3, b.company, 'LN') < 400
where a.company NOT IN (Select company from matrix)
group by a.company
having GEDSCORE= min(GEDSCORE)
order by a.company;

**Joining exact and non-exact matches;
create table matrix3 (drop = GEDSCORE2) as
select *,
case when GEDSCORE2 = . then 0 ELSE GEDSCORE2 END AS GEDSCORE
from
(select * from matrix
union
select * from matrix2 (rename = (GEDSCORE = GEDSCORE2)));
quit;
```

### Fuzzy Matching with Multiple Criteria  

Suppose you have multiple primary keys to match with the other tables. For example, you have Company Name, Address and PIN.  

Sample Datasets  

```sas
Data xx ;
Input company $1-12 PIN 13-30;
cards;
Vanucover    110051
Reliance     112345
Tata         140000
Tata Motors  125432
;
run;
data xx2;
Input company $15. PIN 16-30;
cards;
Tata           140000
tata           140000
Tataz          125433
TataM Jan2015  125432
Tata Motor     125432
Reliance World 112345
Reliance Ltd   113345
Reliance #Petro 113007
Reliance Global 113600
Vanucoverltd 12 110051
;
run;
```

### SAS Code : Fuzzy Matching with Multiple Criteria  

```sas
data example2 (drop = company1 company2);
set xx2;
company1 = compress(company, '',"ak"); /** Keeping only characters**/;
/**Stopwords**/;
Company2 = compbl(PrxChange('s/\b(?:Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)\b//i' , -1 , strip(company1)));
Company3 = compbl(PrxChange('s/\b(?:Corporation|Corp|Ltd|Limited|Inc|Incorporated|Company|Co|LTD|LLC|PLLC)\b//i' , -1 ,Strip(Company2)));
run;
```

```sas
proc sql noprint;
create table matrix2 as
select a.Company , a.company3 as cleaned_name, b.Company as Company2, a.PIN, b.PIN as PIN2,
COMPGED(a.Company3, b.Company, 'LN') as GEDSCORE_Co,
COMPGED(PUT(a.PIN,10.), PUT(b.PIN,10.)) as GEDSCORE_PIN,
calculated GEDSCORE_Co + calculated GEDSCORE_PIN as GEDSCORE
from example2 a left join xx b
on COMPGED(a.Company3, b.Company, 'LN') <= 400 OR COMPGED(PUT(a.PIN,10.), PUT(b.PIN,10.)) <=200
group by a.company
having GEDSCORE = MIN(GEDSCORE)
order by a.company;
quit;
```

### Important Tips 

Stopwords for Addresses  
 
Addresses = PrxChange('s/\b(?:(NORTH|SOUTH|EAST|WEST|STREET|ST|AVENUE|AVE|LANE|LN|PARKWAY|PKWY|WAY|ROAD|RD|DRIVE|DR|
PLACE|PL|CIRCLE|CIR|COURT|CT|PIKE|TERRACE|TER|TRAIL|TRL|TL|BOULEVARD|BLVD)\b//i',-1 ,Strip(_Addresses));  

## SAS: Date Functions   

This tutorial explains the various date functions in SAS. It also includes ways to handle date values with SAS.  

### Syntax of Date Functions in SAS  

date1 = date(): Returns today's date as a SAS date value.  

date1 = today(): Returns today's date as a SAS date value.  

date1 = day(date): Returns the day of month from the variable date.  

date1 = month(date): Extracts the month component from the variable date.  

date1 = year(date): Extracts the year component from the variable date.  

date1 = qtr(date): Extracts the quarter component from the variable date.  

date1 = weekday(date): Returns the day of week from the variable date.  

retirement = intnx('year', date, 60): Calculates the date of retirement by adding 60 years to the date.  

date1 = intck('day', date, date()): Calculates the number of days between date and the current date.  

date1 = datdif(date, date(), 'ACT/ACT'): Calculates the difference between date and the current date using the ACT/ACT method.  

dt = datepart(datetime): Returns the date from a SAS datetime value.  

dt = timepart(datetime): Returns the time from a SAS datetime value.  

### System Dates (Current Date)  

```sas
data _null_;
a = date();
b = today();
c = "&sysdate"d;
put 'Without Format: ' a = b = c =;
run;
```

See Log  

Without Format: a=20480 b=20480 c=19749  

### Make Date Values Formatted  

```sas
data _null_;
a = date();
b = today();
c = "&sysdate"d;
format a b c ddmmyy10.;
put 'With Format: ' a = b = c = ;
run;
```

See Log  

With Format: a=27/01/2016 b=27/01/2016 c=26/01/2014  

### SAS Date Formats  

```sas
data dates;
date1 = put(date(),mmddyy8.);
date2 = put(date(),WORDDATE.);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/aacc2fbb-5e26-405a-99e3-189154c258ad)  

### Date Functions  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2f2c4330-bf1d-4972-9cd7-162addc78549)  

```sas
data _null_;
birthdt = '22oct91'd;
date1 = day(birthdt);
date2 = month(birthdt);
date3 = year(birthdt);
date4 = qtr(birthdt);
date5 = weekday(birthdt);
put date1 date2 date3 date4 date5;
run;
```

### Date Calculations

Task -Number of intervals (Years /Months / Days) from birth date to today's date  

### Functions - DATDIF and INTCK  

```sas
data _null_;
birthdt = '22oct91'd;
date5 = datdif(birthdt, date(), 'ACT/ACT');
date55 = intck('day',birthdt, date());
date6 = intck('year',birthdt, date());
date7 = intck('qtr',birthdt, date());
date8 = intck('week',birthdt, date());
put date5 date55 date6 date7 date8;
run;
```

Note : 'ACT' refers to the actual number of days between dates. Each month is considered to have the actual number of calendar days in that month, and each year is considered to have the actual number of calendar days in that year.  

Task -When customer will retire (60 years old)  

The INTNX function advances a date value by a given interval and returns a date value.  

```sas
data _null_;
birthdt = '22oct91'd;
retirement = intnx('year',birthdt, 60);
put retirement date9.;
run;
```

### Additional Parameter in INTNX Option  

```sas
date10 = intnx('month',date(), 5, 'sameday');
date11 = intnx('month',date(), 5, 'end');
```

### Important Points  

1. January 1, 1960 is the zero point for SAS. Any day before 1/1/1960 is a negative number, and any day after that is a positive number.  

Old dates can be subject to producing incorrect dates in SAS. You may not get a missing value, butmake sure that you check your century. The YEARCUTOFF option gives you the capability to define a 100-year range for two-digit year values. The default value for the YEARCUTOFF option is 1920, giving you a range of 1920- 2019.  

```sas
options yearcutoff = 1890;
data _null_;
birthdt = '22oct91'd;
currdt = '22oct51'd;
diff = intck('year',birthdt, currdt);
put diff;
run;
```

In the code above, yearcutoff = 1890 takes century from 1890 to 1989.

### 2. Subsetting Date Formatted Data  

```sas
data temp2;
set temp;
where date >= '1jan1991'd;
run;
```

### DATEPART and TIMEPART Functions  
 
DATEPART returns the date from a SAS datetime value. Whereas, TIMEPART returns the time from a SAS datetime value.  

```sas
data _null_;
x='21oct16:8:45'dt;
xx=datepart(x);
xxx=timepart(x);
put xx worddate.;
put xxx time.;
run;
```

## INTNX Function  

This tutorial explains how SAS INTNX function works. It includes explanation of INTNX function with practical examples which would help you to understand it.  
  
### What does the INTNX Function do?  

SAS function INTNX is used to increment SAS date by a specified number of intervals. It helps to answer the following questions.  

### Examples  

Here are some real-world examples of how the INTNX function can be used.  

When is next Monday?  

When was last Friday?  

What would be date after 21 weeks?  

Subtract 2 quarters from the current date  

### Syntax : INTNX Function  

The first three parameters of the INTNX function is mandatory and the fourth one is optional.  

```sas
INTNX(interval, start-from, increment, [alignment])
```

Interval is the unit of measurement. The intervals can be days, weeks, months, quarters, years.  

Start-from is a SAS date value which would be incremented.  

Increment is number of intervals by which date is incremented. It can be zero, positive or negative. Negative value refers to previous dates.  

Alignment [Optional Parameter] is where datevalue is aligned within interval prior to being incremented. The values you can specify - 'beginning', 'middle', 'end', 'sameday'. Default value - 'beginning'.  

### INTNX Function: Examples  

Below is a list of some examples in which we have demonstrated the INTNX function in SAS.  

### 1. Add 7 days to a specific date  

In the following code, we are adding seven days to 02 January 2017.  

```sas
data temp;
mydate = '02JAN2017'd;
day=intnx('day', mydate , 7);
format mydate day date9.;
run;
```

Result : day = 09JAN2017  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/bc32d3e5-964f-40ee-ba1e-a309011fe6e3)  

If you are wondering how INTNX is different to 'simply adding 7 to mydate variable' like code below. You would get answer to this question in the next example.

```sas
day = mydate + 7;
```

### 2. Find Next Sunday  

In this case, we need to find answer of the question 'when is next sunday?'. The 02January,2017 is Monday.  

```sas
data temp;
mydate = '02JAN2017'd;
nextsunday=intnx('week', mydate , 1);
format mydate nextsunday date9.;
run;
```

Result : nextsunday = 08JAN2017  

It returns 08JAN2017 as it aligns to the 'beginning' period. The 'beginning' alignment is default in INTNX function. In other words, if you change the mydate to '04JAN2017'd, it still returns '08JAN2017' as the next sunday would be same within this week interval. If you want to add exactly 1 week to the date, you can use the 'sameday' in the fourth parameter of this function. See the statement below -

```sas
nextsunday=intnx('week', mydate , 1, 'sameday'); returns 09JAN2017  
```

### 3. Get First Date  

Suppose you need to find out the first day of a specific date. For example, today is 09January, 2017 and the first day of this date is 01January,2017.  

```sas
data temp;
set sashelp.citiday;
firstday=intnx('month', date , 0);
format firstday date9.;
proc print data = temp;
var date firstday;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/3f0e3749-a65b-4a4a-b03e-e7ea0f51dd3b)  

By specifying 0 in the third parameter of INTNX function, we can calculate the first day of the dates.  

### 4. When was Last Tuesday?  

It is tricky to figure out the date when it was last tuesday. 13January,2017 is Friday. In real world dataset, we don't have the exact days of a list of dates when we need to code to get the last tuesday.  

### Incorrect Method  

```sas
data temp;
mydate = '13JAN2017'd;
lasttuesday = intnx('week.3', mydate , 0);
format mydate lasttuesday date9.;
proc print;
run;
```

It returns 10JAN2017. In this case, week.3 refers to tuesday within week as a unit of measurement. Similarly, week.2 refers to monday.  

It doesn't work when input date is current tuesday. For example, run the above code with mydate ='10JAN2017'd.10JAN2017 is tuesday. In this case, it returns '10JAN2017' which is not a previous tuesday. It should have returned '03JAN2017'.  

### Correct Method  

```sas
data temp;
mydate = '10JAN2017'd;
lasttuesday = intnx('week.4', mydate , -1, 'end');
format mydate lasttuesday date9.;
proc print;
run;
```

It returns 03JAN2017 which is previous tuesday. See the changes we have made in this program -

-1 instead of 0 as increment value  

'end' instead of 'beginning' as date alignment  

'week.4' instead of 'week.3' to figure out the last tuesday  

### 5. Adjustment within the Interval  

This program explains how INTNX function adjusts / align dates within the interval specified.  

```sas
data temp;
mydate = '31JAN2017'd;
beginning=intnx('year ', mydate , 1, 'b');
middle=intnx('year ', mydate , 1, 'm'); 
end=intnx('year ', mydate , 1, 'e');
sameday=intnx('year ', mydate , 1, 's');
format mydate beginning middle end sameday date9.;
proc print;
run;
```

The abbreviation 'b' refers to beginning, 'm' - middle, 'e' - end, 's' - sameday. The default value is 'b' if you don't specify anything in the fourth parameter.  

Result  

beginning = 01JAN2018  

middle = 02JUL2018  

end = 31DEC2018  

sameday = 31JAN2018  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2f0d7bb1-54ee-459e-a64f-48874745cb43)  

### 6. Datetime Formats  

Like date formats, we can use time and datetime formats in INTNX function to increment time (seconds / minutes / hours).  

```sas
data temp;
mydt = '29JAN2017:08:34:00'dt;
seconds=intnx('second', mydt , 1);
minutes=intnx('minute', mydt , 1);
hours=intnx('hour', mydt , 1);
days=intnx('dtDay', mydt , 1);
weeks=intnx('dtWeek', mydt , 1);
format mydt seconds minutes hours days weeks datetime20.;
proc print NOOBS;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d5707e61-c497-4355-b7dd-38b22cd77f7b)  

### Difference between INTNX and INTCK Functions  

The INTCK function calculates the difference between two dates or times, whereas the INTNX function adds days or times to a date.  

To remember the difference between these two functions easily, focus on the first three letters and the last two letters separately.  

INTCK - INT= Interval CK= Check difference  

INTNX - INT= Interval NX= Next days  

## INTCK Function  

The INTCK function is one of the most important date function in SAS that is used to calculate the difference between two dates, two times or two datetime values.  

Here are some real-world examples of how the INTCK function is used in SAS.    

__Calculation of individual's age__ :

The INTCK function is used to calculate the number of years between date of birth and today's date.  

__Tenure of an employee with company__ :

The INTCK function is used to find out the number of months between date of joining and today's date.  

__Customer Retention Duration__ :  

The marketing department wants to know the length of time that customers remain engaged with and continue their relationship with us so that they can provide offers to tenured customers. The INTCK function can be used in calculating the longevity of customer relationships.  

__Number of quarterly payments paid__  

__Number of working days__  

__Number of hours spent on a particular course__  

### INTCK Function - Syntax  

The syntax of INTCK is defined below -  

```sas
INTCK(date-or-time-interval, start-date-or-time, end-date-or-time, [method])
```

date-or-time-interval : Date or time period needs to be defined in the first parameter. For eg. MONTH, YEAR, QTR, WEEK, HOUR, MINUTE etc. Specify period in single quotes  

start-date-or-time : Starting date or time to calculate the number of periods.  

end-date-or-time : End date or time to calculate the number of periods.  

method : Optional Parameter. Method to calculate the difference. Methods are 'CONTINUOUS' or 'DISCRETE'. By default, it is DISCRETE.  

### Simple Example of INTCK Function  

Calculate the number of years between two dates. In this case, two dates are 01JAN2015 and 01JAN2017.  

```sas
data temp;
date1 = '01JAN2015'd;
date2 = '01JAN2017'd;
no_of_years = intck ('YEAR', date1, date2);
format date1 date2 date9.;
proc print data = temp;
run;
```

The 'YEAR' keyword tells SAS to calculate the number of intervals between dates in terms of year. Since 01JAN2015 is a starting date, it is specified in the INTCK function before 01JAN2017. The FORMAT statement is used to display datevalues in date format when we print our results.  

The output is shown below -  

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d0223626-0b43-430f-956a-97b56d9ecd2e)  

Other alias of year - 'YEARS' and 'YR'-  

no_of_years = intck ('YEARS', date1, date2)  

no_of_years = intck ('YR', date1, date2)  

### SAS INTCK Examples

Like calculation of years, we can use other intervals such as semiyear, quarter, month, week, day. The examples of these intervals are displayed below -  

```sas
data temp;
date1 = '01JAN2015'd;
date2 = '01JAN2017'd;
no_of_years = intck ('YEAR', date1, date2);
no_of_semiyears = intck ('SEMIYEAR', date1, date2);
no_of_quarters = intck ('QUARTER', date1, date2);
no_of_months = intck ('MONTH', date1, date2);
no_of_weeks = intck ('WEEK', date1, date2);
no_of_days = intck ('DAY', date1, date2);
format date1 date2 date9.;
proc print data = temp noobs;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/32dced41-51a3-45ec-a03d-9a144fe04ad9)  
 
### Custom Intervals using INTCK Function  

Suppose you are asked to calculate the number of 4 months interval between two dates -  

```sas
data temp;
date1 = '01JAN2015'd;
date2 = '01JAN2017'd;
no_of_4months = intck ('MONTH4', date1, date2);
run;
```

The MONTH4 interval implies interval is of 4 months. It is equal to the number of months divided by 4. Don't confuse it with QUARTERS. QUARTERS is equal to interval of 3 months. Remember 4 Quarters in an year.

Result : no_of_4months = 6  
Similarly, we can use the custom intervals in YEAR, QUARTER and other periods. For example, 'YEAR2' tells SAS the interval is of 2 years. It would return 1 for the above mentioned dates.  

### Set Starting Point for Calculation  

Let's compare YEAR and YEAR.3 by calculating the number of years between two dates using the INTCK function.  

```sas
data temp;
date1 = '31JAN2015'd;
date2 = '31DEC2016'd;
diff = intck ('YEAR', date1, date2);
diff2 = intck ('YEAR.3', date1, date2);
format date1 date2 date9.;
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/2d41b934-378f-4844-a593-c5a03d3e294f)  

How it works :  

intck ('YEAR', date1, date2) - It checks the number of times first of January appears as first of january is set as a starting point by default. The variable diff returns 1 as it includes only 01JAN 2016.  

intck ('YEAR.3', date1, date2) - It checks the number of times first of March appears as YEAR.3 refers to the period starting from 1st of March to end of February next year. The variable diff2 returns 2 as it includes 01 March 2015 and 01March 2016.  
  
Is it a month difference?  

INTCK function says there is a month difference between 25OCT2016 and 03NOV2016. But there is no month difference between 01OCT2016 and 31OCT2016. How?  

```sas
data temp;
month1= intck('month', '25OCT2016'd, '03NOV2016'd);
month2= intck('month', '01OCT2016'd, '31OCT2016'd);
proc print;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/1659af93-3034-4564-b45b-fd4e5f9a0dcf)  

INTCK checks whether the first day of the month lies with in the range. In the first case, 01 November falls between October 25 and November 03 so it returns 1. In the second case, it returns 0 as 01 November does not fall between 01OCT2016 and 31OCT2016.    

How to correct it?  

Add one more parameter at end of INTCK function. In the parameter, specify 'C' which refers to continuous method for calculation.  

```sas
data temp;
month1= intck('month', '25OCT2016'd, '03NOV2016'd, 'C');
proc print;
run;
```

The above function returns 0.  

The CONTINUOUS method calculates continuous time from the start-of-period date specified in the second parameter of INTCK function.  

### Calculating Weekdays with INTCK Function  

Suppose you are asked to calculate the number of weekdays -  

```sas
data eg;
weekdays = intck('WEEKDAY', '11DEC2016'd ,'18DEC2016'd);
proc print;
run;
```

It returns 5. In this case, saturday and sunday are considered weekends and excluding from the calculation.  
  
Define 6 days working  

If you need to calculate number of working days between 2 dates considering 6 weekdays -  

```sas
data eg;
weekdays = intck('WEEKDAY1W', '11DEC2016'd ,'18DEC2016'd);
proc print;
run;
```

WEEKDAY1W implies sunday as weekend (1=Sunday, 2= MONDAY... 7=Saturday)  

Set Custom Weekends  

```sas
data eg;
weekdays = intck('WEEKDAY24W', '11DEC2016'd ,'16DEC2016'd);
proc print;
run;
```

WEEKDAY24W means MONDAY and WEDNESDAY are weekends. The above function returns 3  

### Calculate between Datetime values  

Suppose you need to calculate hours, minutes and seconds between two datetime values.  

```sas
data temp2;
hours=intck('hour','01jan2016:10:50:00'dt,'01jan2016:11:55:00'dt);
minutes=intck('minute','01jan2016:10:50:00'dt,'01jan2016:11:55:00'dt);
seconds=intck('second','01jan2016:10:50:00'dt,'01jan2016:11:55:00'dt);
proc print noobs;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/caa5ae8c-d863-4538-9b77-10c7e197b98a)  

Result - 1 hour, 65 minutes and 3900 seconds  

### Time Difference using INTCK Function  

To calculate the time difference between two times using the INTCK function, you need to specify the time interval you want to measure. Here's the syntax of the INTCK function:  

```sas
data temp3;
hours=intck('hour','12:00:00't, '23:05:00't);
minutes=intck('minute','12:00:00't,'23:05:00't);
seconds=intck('second','12:00:00't,'23:05:00't);
proc print noobs;
run;
```

Result : 11 hours 665 minutes 39900 seconds  

## Extract Week, Day, Month and Year from Date  

This tutorial explains how to extract the week, day, month and year from a date in SAS, along with examples.  

### Sample SAS Dataset  

Let's create a sample SAS dataset that will be used in the examples of this article.  

```sas
data mydata;
    input date_var date9.;
    format date_var date9.;
    datalines;
01JAN2023
10JAN2023
15JAN2023
20JAN2023
25JAN2023
01FEB2023
10FEB2023
15FEB2023
20FEB2023
25AUG2023
;
run;
```

### How to Calculate Week Number of Year  

In SAS, the WEEK function calculates the week number of the year.  

```sas
data want;
set mydata;
weeknumber = week(date_var); 
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/34f8c5fd-d380-4586-9e7a-f5103f7f3dee)  

### How to Calculate Week Number of Month  

The following code uses the intck function to calculate the number of weeks between the beginning of the month and the given date. The intnx function is used to find the first day of the month ('B' option stands for 'beginning'). Adding 1 to the result accounts for the week number starting from 1.  

```sas
data want;
set mydata;
weeknumber = intck('week', intnx('month', date_var, 0, 'B'), date_var) + 1;
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/d263df1e-4657-48cf-8af9-b233a6b53f02)  

### How to Extract Month from Date  

In SAS, the month function is used to extract month from a date.  

```sas
data want;
set mydata;
monthnumber = month(date_var);
run;
```

![image](https://github.com/Deepak2k20/SAS/assets/65231118/a4b82564-f574-4f09-b613-6fcd87b863a8)  

### How to Extract Day from Date  

In SAS, the day function is used to extract day from a date.  

```sas
data want;
set mydata;
daynumber = day(date_var);
run;
```

### How to Extract Year from Date  

In SAS, the year function is used to extract year from a date.  

```sas
data want;
set mydata;
yearnumber = year(date_var);
run;
```


















 



 












 















































 
























































  










 













 


























