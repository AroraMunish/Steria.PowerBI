---
lab:
    title: 'Use Parameter Table To Display Amount In Selected Units'
    module: 'Design a Data Model in Power BI'
---


# **Lab 03- Use Parameter Table To Display Amount In Selected Units**

**The estimated time to complete the lab is 45 minutes**

In this lab you will learn to use Parameter Table to display the (sale /any other field) values in 
* Real Value
* Thousands
* Millions
* Billions

**Steps**

1. To open the Power BI Desktop, on the taskbar, click the Microsoft Power BI Desktop shortcut.

 	![Picture 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)

1. To close the getting started window, at the top-left of the window, click **X**.

 	![Picture 7](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image2.png)

1. To open the starter Power BI Desktop file, click the **File** ribbon tab to open the backstage view.

1. Select **Open Report**.

 	![Picture 6](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image3.png)

1. Click **Browse Reports**.

 	![Picture 5](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image4.png)

1. In the **Open** window, navigate to the **C:\PowerBI\Labs\03.Using-Parameter-Table-To-Display-In-Specified-Units\Starter** folder.

1. Select the **Sales Analysis** file.

1. Click **Open**.

 	![Picture 4](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image5.png)

1. Close any informational windows that may open.

1. To create a copy of the file, click the **File** ribbon tab to open the backstage view.

1. Select **Save As**.

 	![Picture 3](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image6.png)

1. If prompted to apply changes, click **Apply**.

 	![Picture 15](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image7.png)

1. In the **Save As** window, navigate to the **C:\PowerBI\MySolution** folder, and save the file as **03.Sales Analysis.pbix** as Click **Save**..

 	![Picture 2](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image8.png)

Importing The Data

1. Click on Get Data | Text/CSV
Select Scale.csv, from the folder 'C:\PowerBI\Resources',  and it will display the screen as follows
![04.1.SelectParameterTable.png](Linked_image_Files/04.1.SelectParameterTable.png)
2. Click on Load button, and it will create a Scale table and it will display the screen as follows 
![04.2.LoadParameterTable.png](Linked_image_Files/04.2.LoadParameterTable.png)

**Creating Measures**
1. Click on Data Pane, and then click on 'Create Table' in the ribbon
![04.3.CreateMyMeasures.png](Linked_image_Files/04.3.CreateMyMeasures.png)
and it will appear as follows
![04.4.CreatingTable.png](Linked_image_Files/04.4.CreatingTable.png)
Change the expression to be
```
MyMeasures = 
```
and it will appear as follows
![04.5.CreatingMyMeasures.png](Linked_image_Files/04.5.CreatingMyMeasures.png)
Click on Enter Key and table will be created

2. Right Click on My Measures | New Measure, and enter the formula as follows
and enter the formula as follows
```
Scaled Sales = if(
                    HASONEVALUE(Scale[ShowValueAs]),
                    DIVIDE(SUM(Sales[Sales]),SELECTEDVALUE(Scale[DivideBy])),
                    SUM(Sales[Sales])
                )
```
\
3. Select the measure 'Scaled Sales' and Click on Format pane, and specify the currency to be '$ English (United States)' and format to 0 decimal places.
![04.6.Formatting.png](Linked_image_Files/04.6.Formatting.png)

4. Now click on Report pane, and add Matrix visualization 
![04.7.MatrixVisualzation.png](Linked_image_Files/04.7.MatrixVisualzation.png)

5. Add the following fields to Matrix Visualization\
a. Rows: Region | Group\
b. Values: Sales | Sales\
c. Values: MyMeasures | Scaled Sales\
and it will appear as follows
![04.9.Report.png](Linked_image_Files/04.9.Report.png)

6. Now add a slicer to the report, and add field 'ShowValueAs' to the slicer\
![04.10.Slicer.png](Linked_image_Files/04.10.Slicer.png)

7. Click on 'ShowValueAs' field, and from Column Tools, set sort by as 'DivideBy' field\
![04.11.ShowValueAs.png](Linked_image_Files/04.11.ShowValueAs.png)
and slicer will appear as sorted on the basis on Divide By as follows
![04.12.SlicerChange.png](Linked_image_Files/04.12.SlicerChange.png)

8. Now, when we make any selection in slicer, according Scaled Sales Amount gets updated in Matrix Report.
![04.13.ScaledValues.png](Linked_image_Files/04.13.ScaledValues.png)

9. Right click on MyMeasures | New Measure
![04.14.NewMeasure.png](Linked_image_Files\04.14.NewMeasure.png)
and enter the formula as follows
```
Display Unit = "Scaled Sales Unit: " & SELECTEDVALUE(Scale[ShowValueAs]," Real Value")
```
and it will appear as follows\
![04.16.DisplayUnit.png](.\Linked_image_Files\04.16.DisplayUnit.png)

10. Add a Card visualization, and add Display Unit to it
![04.17.CardVisualization.png](.\Linked_image_Files\04.17.CardVisualization.png)

11. Click on Format icon and hide Category Label 

![04.19.CategoryLabel.png](.\Linked_image_Files\04.19.CategoryLabel.png)

and specify the size
![04.18.DisplayUnits.png](.\Linked_image_Files\04.18.DisplayUnits.png)
and it will appear as follows
![04.20.Final.png](.\Linked_image_Files\04.20.Final.png)

12. Now, if you change the unit, and same will be reflected, as execpected
![04.21.FinalOutput.png](.\Linked_image_Files\04.21.FinalOutput.png)


