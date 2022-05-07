
# **Lab 09- Creating and Using Dataflows**

**The estimated time to complete the lab is 45 minutes**



In this lab, you will 
1. Create ane configure dataflow and
2. Create report (/s) where-in you will connect to this dataflow

### Task 1: Create Dataflow 

1.	Login to PowerBI.com

2.	Select the workspace

3.	Click on New |Dataflow 
![14-CreateDataFlow_image1.png](.\Linked_image_Files\14-CreateDataFlow_image1.png)
\
and it will appear as follows
![14-CreateDataFlow_image2.png](.\Linked_image_Files\14-CreateDataFlow_image2.png)

4.	Click on Add new tables from Define new tables, and it will appear as follows
![14-CreateDataFlow_image3.png](.\Linked_image_Files\14-CreateDataFlow_image3.png)
\
Select SQL Server database 

5.	And enter the details
![14-CreateDataFlow_image4.png](.\Linked_image_Files\14-CreateDataFlow_image4.png)
\
[Make sure that Gateway is up and runniing] 
\
Click on Next button
![14-CreateDataFlow_image5.png](.\Linked_image_Files\14-CreateDataFlow_image5.png)
 6.	Select the tables, 
\
DimCustomer, DimDate, DimProduct, DimProductCategory,DimProductSubCategory, FactInternetSales and FactResellerSales
\
and it will show the screen as follows
![14-CreateDataFlow_image6.png](.\Linked_image_Files\14-CreateDataFlow_image6.png)

7.	Click on Transform Data, and it will show the screen as follows
![14-CreateDataFlow_image7.png](.\Linked_image_Files\14-CreateDataFlow_image7.png)
 
Click on Save & close, and it will show the screen as follows
\
 ![14-CreateDataFlow_image8.png](.\Linked_image_Files\14-CreateDataFlow_image8.png)
\
And thereafter will show the screen to save the dataflow as follows
 ![14-CreateDataFlow_image9.png](.\Linked_image_Files\14-CreateDataFlow_image9.png)
\
Give it a name ‘AdventureWorks-Dataflow’, and click on Save button and it will show the screen as follows
\
 ![14-CreateDataFlow_image10.png](.\Linked_image_Files\14-CreateDataFlow_image10.png)
\
10. Click on Workspace, and then click on Datasets + Dataflows, and newly create dataflow  will be available as follows
 ![14-CreateDataFlow_image11.png](.\Linked_image_Files\14-CreateDataFlow_image11.png)

11.	Click on | Settings , next to dataflow, and it will show the screen as follows
![14-CreateDataFlow_image12.png](.\Linked_image_Files\14-CreateDataFlow_image12.png)

12.	Click on Scheduled Refresh, and we can set the frequency as to when it should be refreshed
\
![14-CreateDataFlow_image13.png](.\Linked_image_Files\14-CreateDataFlow_image13.png)

### Task 2: Use Dataflow

**2	Power BI Desktop**
1.	Open Power BI Desktop, and save the solution as ‘Sales Analysis Using Dataflow’


**2.1	Utilize Existing Dataflow**
\
2.	Click on Get Data | Power BI dataflows, and it will show the screen as follows
![14-CreateDataFlow_image14.png](.\Linked_image_Files\14-CreateDataFlow_image14.png)

3.	Sign-in with the credentials and it will show the screen as follows
![14-CreateDataFlow_image15.png](.\Linked_image_Files\14-CreateDataFlow_image15.png)
 
4.	Select the required tables 
![14-CreateDataFlow_image16.png](.\Linked_image_Files\14-CreateDataFlow_image16.png)
5. Click on 'Load Data' and tables will be loaded
\
![14-CreateDataFlow_image17.png](.\Linked_image_Files\14-CreateDataFlow_image17.png)

\
6. Create the report and publish it
