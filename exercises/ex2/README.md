# Exercise 2 - Expand the Dashboard with Core Add-ons



## Exercise 2.1 Create Basic Calculations within Stories


Objective: Use the latest calculations available in SAP Analytics Cloud to expose additional information that was not available in your original data model. Understand the potential and workflow of creating calculations in our story.

Estimated Time: 5 mins

Exercise Description: You have access to shipping information and financial sales data that with some common dimensions, including Order Number and Store Name. You need to create various calculated 
dimensions, statistical aggregations to understand the effects of shipping times and impact of delivery delays on sales revenue..

Key Features:
- Create calculated dimensions with string functions to enhance your data
- Employ statistical calculations in aggregations of your data
- Integrate calculation input controls to simulate values in your visualizations

🚩Please make a copy of the dashboard "Exercise 2.1 Create Basic Calculations within Stories"

⚠️Exercise check! Does your dashboard look like this screenshot in Edit mode? 

![8-11](https://user-images.githubusercontent.com/92877810/141006673-3826b6bd-9bf0-4d51-8424-7612626c6275.png)

🚩When working with your data in SAP Analytics Cloud, you may find that you want to look at additional components to your data that are currently not captured by the existing measures and dimensions in the model. Luckily, story designers can extend the data models with additional calculated measures and dimensions. This enables the story creator to delve into further insights from their data. Let us start by creating a calculated dimension that divides the Store dimension in our data into Studios and Non-Studios. 

1. Click **Gross Margin % for Actual** Chart

  <br>![](/exercises/ex2/images/image1.png)<br><br><br>

2. Click **Edit** and Open **Right Panel**

3. Click **+ Add Dimension**

  <br>![](/exercises/ex2/images/ex2_3.png)<br><br><br>

4. Scroll and Click **+ Create Calcluated Dimension...**

<br>![](/exercises/ex2/images/ex2_4.png)<br><br><br>


ℹ️Welcome to Calculated Dimensions!  
  
Calculated Dimensions are useful when you want to enrich your dimension if your model does not have the needed format. 
 
You can choose to combine existing dimensions to create your own dimensions. There are two calculated dimensions that can be created: 
  
**Calculated Dimension:** Use formulas to create new dimension members 
  
**Account Based Dimension:** Use ranges within an existing measure to determine how to group dimension members together 

<img width="1281" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/9b675538-547b-4b99-9eea-a68786211f43">


🚩As we want to identify the stores that are studios, we will use the regular calculated dimension. 

5. Click **Calculated DImension**

<br>![](/exercises/ex2/images/ex2_5.png)<br><br><br>

🚩The formula field for Calculated Dimensions uses conditional logic and function formulas to create the Dimension rules. This offers the business analyst great flexibility in defining new calculated dimensions. 

6. Press **Ctrl + Space** on the Keyboard

<br>![](/exercises/ex2/images/ex2_6.png)<br><br><br>


7. Click IF

🚩Our IF statement has three fields. The first field is used as a condition that evaluates to true or false. The second field is the Dimension value if True and the third field is the Dimension value if False. 

<br>![](/exercises/ex2/images/ex2_7.png)<br><br><br>

8. Click the **Condition (First Field)** in the IF Formula

<br>![](/exercises/ex2/images/ex2_8.png)<br><br><br>


9. Press **Ctrl + Space** on the Keyboard
  
💡Using Ctrl + Space is a great way to learn how to use the Calculation Editor. Using this hotkey combination will always bring up all possible functions and measures/dimensions that can be typed into the according field for the ease of the user. 

<br>![](/exercises/ex2/images/ex2_8.png)<br><br><br>

ℹ️Welcome to String Functions in the Calculation Editor! There are a variety of different String Functions that can be used to transform the Dimension values to a specific use case. 
  
**FINDINDEX:** Search for a substring and return its 0 based index 
**ENDSWITH:** Returns True if given string ends with user given substring 
**TRIM:** Removes unwanted leading and trailing spaces 
**REPLACE:** Replace characters in a string with a specified replacement 
**SPLIT:** Returns substring from a string using a specified divider 
**UPPERCASE/LOWERCASE:** Convert a string to all Lower or all Upper case 
**CONCAT:** Combine two strings together 
**LEFT/RIGHT:** Returns the specified number of characters from the beginning or end of a string 
  
Let us use RIGHT function to categorize Stores by if they are a Studio. 

10. Scroll till **RIGHT** is **Visible**

11. Click **RIGHT**

<br>![](/exercises/ex2/images/ex2_11.png)<br><br><br>

🚩Here we are specifying the Dimension we are reading our string from

12. Type **St** in the **First Input Field** for **RIGHT**

13. Click **Store**

<br>![](/exercises/ex2/images/ex2_13.png)<br><br><br>

ℹ️Since Dimensions often have an ID and Description, it is important to clarify that we are looking to parse the Store name from description here. 

14. Type in a **Period "."**

15. Press **Ctrl + Space** on the keyboard

16. Click **Description**

<br>![](/exercises/ex2/images/ex2_16.png)<br><br><br>

🚩We know we are trying to divide our Store dimension into Studios and Non-Studio. Since we are looking for "Studio" at the end of store name, we know we should filter on 6 characters using our RIGHT string function. 

17. Type **"6"** in the **Second Input Field** for the **RIGHT** Function

<br>![](/exercises/ex2/images/ex2_17.png)<br><br><br>

🚩Let us compare the last 6 letters of our store name with Studio to group them into two Store Groups. 

18. Type in =**"Studio"** following the RIGHT formula

19. Type in **"Studio"** in the **TRUE** Field for the IF Function

20. Type in **"Non-Studio"** in the **FALSE** Field for the  IF Function

<br>![](/exercises/ex2/images/ex2_20.png)<br><br><br>

⚠️Quality Check! Does the end of your formula look like this? 

<br>![](/exercises/ex2/images/ex2_20_2.png)<br><br><br>


🚩Format will parse your Formula and identify if there are any problems with the input parameters. 

21. Click **Format** to Validate the Formula
  
🚩Great! Our formula is valid and good for use in defining a new Calculated Dimension. Let us name this Dimension and use it in our charts. 

<br>![](/exercises/ex2/images/ex2_21.png)<br><br><br>

22. Name the Calculated Dimension as **Store Group**

23. Click **OK**

<br>![](/exercises/ex2/images/ex2_23.png)<br><br><br>


⚠️Quality check! Does your chart look like this after including your Calculated Dimension? 

🚩By creating a Calculated Dimension, we are able extract further insights from our data. We can now see that Gross Margin % is higher for Studios than other stores. This could be of interest to us for further financial analysis and investments. 

<br>![](/exercises/ex2/images/ex2_23_2.png)<br><br><br>


🚩Let us use our new Calculated Dimension to find out the split of Average Sales Revenue by Store Group. 

24. Click Avg Sales Revenue for Actual Chart

<br>![](/exercises/ex2/images/ex2_24.png)<br><br><br>

25. Click **+ Add Dimension** 

<br>![](/exercises/ex2/images/ex2_25.png)<br><br><br>


26. Scroll and Click **Store Group**

27. Click Inside the Builder Panel to Collapse the Dimension Selection Drop Down Menu 

<br>![](/exercises/ex2/images/ex2_27.png)<br><br><br>


⚠️Quality check! Do your charts look like this screenshot? 
  
🚩We can now see that Avg Sales Revenue is also higher for Studio Stores. It could be a good business decision to change our contract structure with our Studio Stores! 

<br>![](/exercises/ex2/images/ex2_27_2.png)<br><br><br>




## Exercise 2.2 Create a Variance within a Story

Objective: Up to this point, we have created a lot of visualizations. For us to easily draw conclusions and highlight key insights, we should add variances and thresholds on our charts in our dashboard so we can draw attention to changes and outliers. 

Estimated Time: 5 mins

Exercise Description: You as a Dashboard Designer will be able to create previuos period comparisons for being able to highlight the charts with critical points.

Key Features:

Define variances in our charts

🚩Please make a copy of the dashboard "Exercise 2.2 and 2.3 - Thresholds and Variances"


<br>![](/exercises/ex2/images/ex22_a.png)<br><br><br>

Goto **EDIT** and **Open the right builder panel** using the icon

<br>![](/exercises/ex2/images/ex22_b.png)<br><br><br>


🚩First, let us add a variance to our KPI for average sales revenue in stores so we can compare if average sales revenue has dropped this year relative to our previous year's performance. If you can recall, our KPIs currently have a 2021 time filter applied on them. 

1. Click on the Avg Sales Revenue Chart

2. Click _Add Variance_ as below or from Chart Add-Ons

<br>![](/exercises/ex2/images/ex22_2.png)<br><br><br>

<br>![](/exercises/ex2/images/ex22_3.png)<br><br><br>


4. Click _Add Version/Time_ and choose _Order Date_
<br>![](/exercises/ex2/images/ex22_4.png)<br><br><br>



🚩We want to compare our data in 2021 year to date with the calculation for the previous year. By comparing to previous period, SAC will automatically calculate this variance for us. 

<br>![](/exercises/ex2/images/ex22_4_2.png)<br><br><br>


🚩After creating our variance, the absolute value may still be hard to contextually understand. We want to know the percentage difference so let us apply _Percentage Display Optio_n to  this variance. 

5. From the builder panel under display options choose _Percentage_ and uncheck _numeric_


<br>![](/exercises/ex2/images/ex22_5.png)<br><br><br>


Our chart is now enhanced to show variance display to previuos period.

6. Click _Done_ to close the Variance Edit panel.

<br>![](/exercises/ex2/images/ex22_6.png)<br><br><br>

7. Close the Builder Panel _Save_ your story

<br>![](/exercises/ex2/images/ex22_7.png)<br><br><br>


⚠️Quality check! Have your variances in the chart updated to percentage values? Please note your data will look different due to the dynamic time filter on the chart

<br>![](/exercises/ex2/images/ex22_7_2.png)<br><br><br>




## Exercise 2.3 Create a threshold

Objective: To be able to create thresholds based on ranges in our SAC story 

Estimated Time: 5 mins

Exercise Description: You as a Dashboard Designer will be able to create Within Thresholds, you can create a threshold based on a number range or against another measure. In our case, we are interested in a number range.

Key Features:

- Define thresholds in our charts

  
 
🚩Please make a copy of the dashboard "Exercise 2.2 and 2.3 - Thresholds and Variances"

🚩Open Story in Edit mode

<br>![](/exercises/ex2/images/ex23_a.png)<br><br><br>

🚩We would like to create threshold for the Table as highlighted


1. Click on the Right panel Icon to open the Builder panel

<br>![](/exercises/ex2/images/ex23_1.png)<br><br><br>


2. Click on the Account under the **Columns** and Select Thresholds -> New Threshold

   <br>![](/exercises/ex2/images/ex23_2.png)<br><br><br>

  <br>![](/exercises/ex2/images/ex23_2_1.png)<br><br><br>


3. In the _Threshold_ Panel Select _Measure_ as _Gross Margin %_

<br>![](/exercises/ex2/images/ex23_3.png)<br><br><br>

4. We can now define the _threshold_ as a _Number Range_ for _Gross Margin %_ .

5. Add the Value 30 for _Gross Margin %_ >= scenario so that its indicated as green in the table cells.

<br>![](/exercises/ex2/images/ex23_5.png)<br><br><br>

6. Click _Apply_.

   <br>![](/exercises/ex2/images/ex23_6.png)<br><br><br>


  
7. Save your Story and see that Gross Margin% is now shown in green for % >=30%

   <br>![](/exercises/ex2/images/ex23_7.png)<br><br><br>



🚩Thresholds in the table are now color coded based on number range. 



⚠️Quality Check! Does your dashboard with thresholds look like this screenshot? 

<br>![](/exercises/ex2/images/ex23_7_2.png)<br><br><br>

## Summary

**You have completed Thresholds, and Variances section!**

**You are now able to:**

- Use recommended comparison to quickly add variances to a chart
- Add a threshold to a table

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
