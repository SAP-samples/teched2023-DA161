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

  <img width="1669" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/6cd84b04-00ab-425f-a14e-1a6240429539">


4. Scroll and Click **+ Create Calcluated Dimension...**

<img width="1665" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/c933d62a-2bf8-45c3-8545-cfed47bea050">


ℹ️Welcome to Calculated Dimensions!  
  
Calculated Dimensions are useful when you want to enrich your dimension if your model does not have the needed format. 
 
You can choose to combine existing dimensions to create your own dimensions. There are two calculated dimensions that can be created: 
  
**Calculated Dimension:** Use formulas to create new dimension members 
  
**Account Based Dimension:** Use ranges within an existing measure to determine how to group dimension members together 

<img width="1281" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/9b675538-547b-4b99-9eea-a68786211f43">


🚩As we want to identify the stores that are studios, we will use the regular calculated dimension. 

5. Click **Calculated DImension**

<img width="1667" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/6d3fcb05-392a-4612-9c0f-2a12055b3f5a">


🚩The formula field for Calculated Dimensions uses conditional logic and function formulas to create the Dimension rules. This offers the business analyst great flexibility in defining new calculated dimensions. 

6. Press **Ctrl + Space** on the Keyboard

<img width="1273" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/86fb099e-99c5-466b-a682-650f926aca66">


7. Click IF

🚩Our IF statement has three fields. The first field is used as a condition that evaluates to true or false. The second field is the Dimension value if True and the third field is the Dimension value if False. 

<img width="1669" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/1eaecb10-b8e5-4187-9429-29027548be0a">


8. Click the **Condition (First Field)** in the IF Formula

<img width="1128" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/799294db-4800-4c6a-9aff-22b36e2eeca8">


9. Press **Ctrl + Space** on the Keyboard
  
💡Using Ctrl + Space is a great way to learn how to use the Calculation Editor. Using this hotkey combination will always bring up all possible functions and measures/dimensions that can be typed into the according field for the ease of the user. 

<img width="1278" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/756eeeba-5395-4c95-8479-18445931052e">


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

<img width="1277" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/3931b154-fe26-451c-b877-f3ad96268ee9">


🚩Here we are specifying the Dimension we are reading our string from

12. Type **St** in the **First Input Field** for **RIGHT**

13. Click **Store**

<img width="1280" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/2925d9b0-cb35-4a4c-8af3-1618e1371427">


ℹ️Since Dimensions often have an ID and Description, it is important to clarify that we are looking to parse the Store name from description here. 

14. Type in a **Period "."**

15. Press **Ctrl + Space** on the keyboard

16. Click **Description**

<img width="1266" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/f4ffc6b6-1ba3-4283-9374-294ad3bed17c">


🚩We know we are trying to divide our Store dimension into Studios and Non-Studio. Since we are looking for "Studio" at the end of store name, we know we should filter on 6 characters using our RIGHT string function. 

17. Type **"6"** in the **Second Input Field** for the **RIGHT** Function

<img width="1668" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/d46c3074-b235-418c-8ce7-d95134c8abfc">


🚩Let us compare the last 6 letters of our store name with Studio to group them into two Store Groups. 

18. Type in =**"Studio"** following the RIGHT formula

19. Type in **"Studio"** in the **TRUE** Field for the IF Function

20. Type in **"Non-Studio"** in the **FALSE** Field for the  IF Function

<img width="1657" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/e60305b9-d77c-425f-afb0-e6dbd33675f8">


⚠️Quality Check! Does the end of your formula look like this? 

<img width="1657" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/40d4a3d5-2ebb-46d7-9e4c-3cf29597f7ce">


🚩Format will parse your Formula and identify if there are any problems with the input parameters. 

21. Click **Format** to Validate the Formula
  
🚩Great! Our formula is valid and good for use in defining a new Calculated Dimension. Let us name this Dimension and use it in our charts. 

<img width="1662" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/edb7bdf4-7196-4062-8a77-e75aed219529">


22. Name the Calculated Dimension as **Store Group**

23. Click **OK**

<img width="1660" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/3d1de24c-6aa8-4036-b79c-57005c422959">


⚠️Quality check! Does your chart look like this after including your Calculated Dimension? 

🚩By creating a Calculated Dimension, we are able extract further insights from our data. We can now see that Gross Margin % is higher for Studios than other stores. This could be of interest to us for further financial analysis and investments. 

<img width="1670" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/57b8f62c-60b2-4f55-8eb1-559aa19285c7">


🚩Let us use our new Calculated Dimension to find out the split of Average Sales Revenue by Store Group. 

24. Click Avg Sales Revenue for Actual Chart

<img width="1668" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/c2b445a4-5ad5-4df7-a1c8-57f979c7462d">


25. Click **+ Add Dimension** 

<img width="1664" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/9ab32975-4d60-400c-b8e0-d9faceabf0dd">


26. Scroll and Click **Store Group**

27. Click Inside the Builder Panel to Collapse the Dimension Selection Drop Down Menu 

<img width="1663" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/45b46a66-cc4a-4e27-8ec7-a7a620e67bba">


⚠️Quality check! Do your charts look like this screenshot? 
  
🚩We can now see that Avg Sales Revenue is also higher for Studio Stores. It could be a good business decision to change our contract structure with our Studio Stores! 

<img width="868" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/65b4c53b-9eef-48e4-83fe-a3e1c623cf14">




## Exercise 2.2 Create a Variance within a Story

Objective: Up to this point, we have created a lot of visualizations. For us to easily draw conclusions and highlight key insights, we should add variances and thresholds on our charts in our dashboard so we can draw attention to changes and outliers. 

Estimated Time: 5 mins

Exercise Description: You as a Dashboard Designer will be able to create previuos period comparisons for being able to highlight the charts with critical points.

Key Features:

Define variances in our charts

🚩Please make a copy of the dashboard "Exercise 2.2 and 2.3 - Thresholds and Variances"


<img width="1668" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/a04bd5f5-c39b-499a-aadf-bec105b785d0">

Goto **EDIT** and **Open the right builder panel** using the icon

<img width="1676" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/521476d7-71f2-424f-9980-8ecf974b94e3">


🚩First, let us add a variance to our KPI for average sales revenue in stores so we can compare if average sales revenue has dropped this year relative to our previous year's performance. If you can recall, our KPIs currently have a 2021 time filter applied on them. 

1. Click on the Avg Sales Revenue Chart

2. Click _Add Variance_ as below or from Chart Add-Ons

  <img width="1665" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/a43be9b8-9e69-4d65-8add-3f0069dec656">

  <img width="1663" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/64341f48-1c0e-4520-83db-0429c5422855">


4. Click _Add Version/Time_ and choose _Order Date_
  <img width="1280" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/e065e8dc-c699-4041-a9cf-65d63a758553">



🚩We want to compare our data in 2021 year to date with the calculation for the previous year. By comparing to previous period, SAC will automatically calculate this variance for us. 

<img width="1667" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/5f9684ce-be8c-4af7-8463-eaadd95f9d07">


🚩After creating our variance, the absolute value may still be hard to contextually understand. We want to know the percentage difference so let us apply _Percentage Display Optio_n to  this variance. 

5. From the builder panel under display options choose _Percentage_ and uncheck _numeric_


<img width="1677" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/1d7b5490-26a1-4abb-911f-f3509445ab61">


Our chart is now enhanced to show variance display to previuos period.

6. Click _Done_ to close the Variance Edit panel.

<img width="1677" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/19d36de5-09fc-4434-b79b-0caf4c6ba96b">

7. Close the Builder Panel _Save_ your story

   <img width="1665" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/a09df8a2-8925-4c04-b5f2-a4aae229117d">


⚠️Quality check! Have your variances in the chart updated to percentage values? Please note your data will look different due to the dynamic time filter on the chart

<img width="1706" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/b6c538e5-27f3-4c3d-a477-40392bfd31cb">




## Exercise 2.3 Create a threshold

Objective: To be able to create thresholds based on ranges in our SAC story 

Estimated Time: 5 mins

Exercise Description: You as a Dashboard Designer will be able to create Within Thresholds, you can create a threshold based on a number range or against another measure. In our case, we are interested in a number range.

Key Features:

- Define thresholds in our charts

  
 
🚩Please make a copy of the dashboard "Exercise 2.2 and 2.3 - Thresholds and Variances"

🚩Open Story in Edit mode

<img width="1662" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/4669b512-19bf-492e-b43b-8eed9eb36087">

🚩We would like to create threshold for the Table as highlighted


1. Click on the Right panel Icon to open the Builder panel
<img width="1657" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/8c036706-c1a3-4ef7-a922-3be8891d832b">


2. Click on the Account under the **Columns** and Select Thresholds -> New Threshold

   <img width="1276" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/eda4e63f-9b96-4584-9cd5-6335a9dc6b88">

  <img width="1280" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/6b5c547d-f4d0-4779-890e-83f766499610">


3. In the _Threshold_ Panel Select _Measure_ as _Gross Margin %_
  <img width="1267" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/75d6b5e0-0315-4061-a9fc-b4a492d68fcd">

4. We can now define the _threshold_ as a _Number Range_ for _Gross Margin %_ .

5. Add the Value 30 for _Gross Margin %_ >= scenario so that its indicated as green in the table cells.
  <img width="1675" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/ce82095f-6f69-47b9-9a0a-c9df734783d1">

6. Click _Apply_.

   <img width="1675" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/a4bd39cf-4a67-4c0d-9b7c-1cff90199324">


  
8. Save your Story and see that Gross Margin% is now shown in green for % >=30%

   <img width="244" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/3a837e22-7dae-4caa-ad13-9606a907e528">



🚩Thresholds in the table are now color coded based on number range. 



⚠️Quality Check! Does your dashboard with thresholds look like this screenshot? 

<img width="1706" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/8005b3d2-b67a-4509-8154-2c15a99c1dbb">


## Summary

**You have completed Thresholds, and Variances section!**

**You are now able to:**

- Use recommended comparison to quickly add variances to a chart
- Add a threshold to a table

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
