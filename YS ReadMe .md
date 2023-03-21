# College Dropout Prediction
Yue Shen  March 21,2023

## Dataset Description
As part of the Bill & Melinda Gates Foundation’s Postsecondary Success Strategy, the Frontier Set initiative brings together a set of institutions/systems (Sites) that are transforming their higher education models to create a community of peers with the purpose of helping more students. especially low-income, first-generation, and students of color – graduate at higher rates, with high- quality credentials, and at affordable prices.

Frontier Set Sites are asked to submit longitudinal student-level data each academic year to allow for tracking of students’ progress over time. The purpose of the Frontier Set data collection is to support analyses that examine the outcomes of students as related to their academic preparation, progress through their academics, financial aid policies and practices, and eventual success in completing their program of study.

## Type of Data
Different types of data are collected: institutional characteristics and institution-level data such as course information, and student-unit-record (SUR) data. Student demographics and previous education, academic progress, and National Student Clearinghouse data (to identify students’ prior and subsequent enrollments and credentials) are collected at the student level. General data collection information follows; details about file structures, data submission methods, and specific data definitions are included in the Data Dictionary and File Creation section of this document.
## Data Fields
|Variable|Description| 
|----|-----|
|ReferDevMath|whether the student is referred to developmental Math according to the completion of the mathematics course. 1 means complete, 0 means incomplete. |
|----|-----| 
|FinishDevMath|whether the student complete the developmental English. 1 means finish, 0 means not finish. |
|----|-----|
|DoubleDegre|whether the student is double majoring. 1 means double, 0 means not double. | 
|----|-----|  
|AwarReceived|whether to the reward has been received.1 means Yes, 0 means No. |
|----|-----|
|LastTermGPA|student’s average GPA earned for the last term. |
|----|-----|
|LastCumGPA|student’s cumulative GPA earned for last term.|
|----|-----|
|avgTermGPA|student’s cumulative grade point average earned for all terms, up to and including the current term. Based on credits used toward student’s credential and reported on a 4-point scale.|
|----|-----|
|LastCumGPA|student’s cumulative grade point average earned for all terms, up to and including the current term. Based on credits used toward student’s credential and reported on a 4-point scale. And we merge all above variables into one data frame.|     
## Data Volume
1000*35variables
## Data Cleanning
Since we have many files of data and all data are messy and hard to read. Firstly, we should clean these data and summarize the key information. For the progress data set，we substitute the data which less than zero to NA and keep the original data which is equal or greater than 0. 
## Dataset Use
The dataset is public and it is accessible to everyone.

## Data Source
Kaggle link：https://www.kaggle.com/competitions/hud4050studentdropoutfall22/data

### Additional Questions
#### Which metadata standard did you choose and why?
I choose The Data Documentation Initiative (DDI) standard
The Data Documentation Initiative (DDI) standard is a metadata specification for documenting social science data. There are several reasons why I choose to use the DDI standard for a dataset:

Enhance data discoverability: The DDI standard includes information about the study design, sampling methods, data collection procedures, and variable definitions. This information can help indiviuals find and use the data more easily.

Improve data quality: The DDI standard provides a structured framework for documenting data, which can help ensure consistency and accuracy in data documentation. This can help prevent errors and misunderstandings when using the data.

Facilitate data sharing: The DDI standard is widely recognized and used by social science data archives and repositories. By using the DDI standard, data producers can make their data more easily shareable and discoverable by others.

Increase transparency: By providing detailed documentation of the data collection and processing procedures, researchers using the DDI standard can increase transparency in their research. This can help others understand and replicate the research more easily.

Adhere to funding agency requirements: Some funding agencies require the use of specific metadata standards, including the DDI standard. Adhering to these requirements can help ensure funding compliance and increase the chances of successful grant applications.
#### Which template/software did you use?
I will mainly use R to deal with dataset and draw plots，and use Matlab to build models.

#### What was the most challenging part of creating a ReadME file? How did you overcome these obstacles?
The most significant challenge is deciding what information to include and how to present it in a clear and concise manner. It can be tricky to strike a balance between providing enough detail to be helpful and avoid overwhelming the reader with unnecessary information. To overcome this hurdle, I first went through all the files of the data source and selected the important parts in the data dictionary, then filtered for text that I thought would present my dataset concisely and clearly. I also collected feedback from others and iterated on the content until it was both comprehensive and understandable.
