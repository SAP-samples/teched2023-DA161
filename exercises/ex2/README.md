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


⚠️Exercise check! Does your dashboard look like this screenshot in Edit mode? 

![8-11](https://user-images.githubusercontent.com/92877810/141006673-3826b6bd-9bf0-4d51-8424-7612626c6275.png)

🚩When working with your data in SAP Analytics Cloud, you may find that you want to look at additional components to your data that are currently not captured by the existing measures and dimensions in the model. Luckily, story designers can extend the data models with additional calculated measures and dimensions. This enables the story creator to delve into further insights from their data. Let us start by creating a calculated dimension that divides the Store dimension in our data into Studios and Non-Studios. 

13. Click **Gross Margin % for Actual** Chart

![8-12](https://user-images.githubusercontent.com/92877810/141006677-0d6bbe2e-d1bf-43bb-9974-32056994bc67.png)

14. Click **Designer**

15. Click **+ Add Dimension**

![8-13](https://user-images.githubusercontent.com/92877810/141006679-c4ddfcc8-ad52-4ed0-acf1-f4c75a6b601d.png)

16. Scroll and Click **+ Create Calcluated Dimension...**

![8-14](https://user-images.githubusercontent.com/92877810/141006681-e1068697-44ba-4718-99b7-83fb9ee468da.png)

ℹ️Welcome to Calculated Dimensions!  
  
Calculated Dimensions are useful when you want to enrich your dimension if your model does not have the needed format. 
 
You can choose to combine existing dimensions to create your own dimensions. There are two calculated dimensions that can be created: 
  
**Calculated Dimension:** Use formulas to create new dimension members 
  
**Measure Based Dimension:** Use ranges within an existing measure to determine how to group 
dimension members together 

![8-15](https://user-images.githubusercontent.com/92877810/141006683-1dac0f5e-40f5-42b1-9448-84903c584235.png)

🚩As we want to identify the stores that are studios, we will use the regular calculated dimension. 

17. Click **Calculated DImension**

![8-16](https://user-images.githubusercontent.com/92877810/141006684-629e5566-31ab-4431-afcd-6fc004c70b94.png)

🚩The formula field for Calculated Dimensions uses conditional logic and function formulas to create the Dimension rules. This offers the business analyst great flexibility in defining new calculated dimensions. 

18. Press **Ctrl + Space** on the Keyboard

![8-17](https://user-images.githubusercontent.com/92877810/141006687-22d5b394-0876-4870-a982-91d0838a5f94.png)

19. Click IF

🚩Our IF statement has three fields. The first field is used as a condition that evaluates to true or false. The second field is the Dimension value if True and the third field is the Dimension value if False. 

![8-18](https://user-images.githubusercontent.com/92877810/141006690-43289132-1d4a-4003-9185-c48ed9272b85.png)

20. Click the **Condition (First Field)** in the IF Formula

![8-19](https://user-images.githubusercontent.com/92877810/141006691-5ff882ef-e972-42a5-8b2b-df41ecf3f497.png)

21. Press **Ctrl + Space** on the Keyboard
  
💡Using Ctrl + Space is a great way to learn how to use the Calculation Editor. Using this hotkey combination will always bring up all possible functions and measures/dimensions that can be typed into the according field for the ease of the user. 

![8-20](https://user-images.githubusercontent.com/92877810/141006692-1b3a8569-4491-4d14-b203-2fc7918a041b.png)

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

22. Scroll till **RIGHT** is **Visible**

23. Click **RIGHT**

![8-21](https://user-images.githubusercontent.com/92877810/141006695-8a2018bd-3e34-455f-a47c-e8fd45b3c6dd.png)

🚩Here we are specifying the Dimension we are reading our string from

24. Type **St** in the **First Input Field** for **RIGHT**

25. Click **Store**

![8-22](https://user-images.githubusercontent.com/92877810/141006697-d73c223a-8627-4d41-a7a0-3a9ce1a7198a.png)

ℹ️Since Dimensions often have an ID and 
Description, it is important to clarify that we are looking to parse the Store name from description here. 

26. Type in a **Period "."**

27. Press **Ctrl + Space** on the keyboard

28. Click **Description**

![8-23](https://user-images.githubusercontent.com/92877810/141006698-bc5592b2-9763-471b-980f-fd1b0530659f.png)

🚩We know we are trying to divide our Store dimension into Studios and Non-Studio. Since we are looking for "Studio" at the end of store name, we know we should filter on 6 characters using our RIGHT string function. 

29. Type **"6"** in the **Second Input Field** for the **RIGHT** Function

![8-24](https://user-images.githubusercontent.com/92877810/141006700-9275c240-e159-478e-b613-2334cb849a77.png)

🚩Let us compare the last 6 letters of our store name with Studio to group them into two Store Groups. 

30. Type in =**"Studio"** following the RIGHT formula

31. Type in **"Studio"** in the **TRUE** Field for the IF Function

32. Type in **"Non-Studio"** in the **FALSE** Field for the  IF Function

![8-25](https://user-images.githubusercontent.com/92877810/141006702-74aad9f1-5737-44d0-81ed-cb6481387cdc.png)

⚠️Quality Check! Does the end of your formula look like this? 

![8-26](https://user-images.githubusercontent.com/92877810/141006703-ac58bbb8-b21d-4bdd-8e61-bc4147c337ea.png)

🚩Format will parse your Formula and identify if there are any problems with the input parameters. 

33. Click **Format** to Validate the Formula
  
🚩Great! Our formula is valid and good for use in defining a new Calculated Dimension. Let us name this Dimension and use it in our charts. 

![8-27](https://user-images.githubusercontent.com/92877810/141006705-223073c3-2bf1-4b4e-801a-4a3b5d499aee.png)

34. Name the Calculated Dimension as **Store Group**

35. Click **OK**

![8-28](https://user-images.githubusercontent.com/92877810/141006707-c60f5381-be9e-463d-9a82-5e7b37d045dc.png)

⚠️Quality check! Does your chart look like this after including your Calculated Dimension? 

🚩By creating a Calculated Dimension, we are able extract further insights from our data. We can now see that Gross Margin % is higher for Studios than other stores. This could be of interest to us for further financial analysis and investments. 

![8-29](https://user-images.githubusercontent.com/92877810/141006708-2ba13a1f-b302-4b12-b4f3-1ba783cbf162.png)

🚩Let us use our new Calculated Dimension to find out the split of Average Sales Revenue by Store Group. 

36. Click Avg Sales Revenue for Actual Chart

![8-30](https://user-images.githubusercontent.com/92877810/141006711-b0215de9-3334-4faa-93ce-1087c3755f0b.png)

37. Click **+ Add Dimension** 

![8-31](https://user-images.githubusercontent.com/92877810/141006713-6fc3679d-96a2-4405-b87e-2f0bc6de0f0d.png)

38. Scroll and Click **Store Group**

39. Click Inside the Builder Panel to Collapse the Dimension Selection Drop Down Menu 

![8-32](https://user-images.githubusercontent.com/92877810/141006714-7dfdceba-e915-40a4-99f5-bd6b0c3de334.png)

⚠️Quality check! Do your charts look like this screenshot? 
  
🚩We can now see that Avg Sales Revenue is also higher for Studio Stores. It could be a good business decision to change our contract structure with our Studio Stores! 

![8-33](https://user-images.githubusercontent.com/92877810/141006715-991c052d-6d0b-4758-9789-ae58619b8d1e.png)



## Exercise 2.2 Create a Variance within a Story

Objective: Up to this point, we have created a lot of visualizations. For us to easily draw conclusions and highlight key insights, we should add variances and thresholds on our charts in our dashboard so we can draw attention to changes and outliers. 

Estimated Time: 5 mins

Exercise Description: You as a Dashboard Designer will be able to create previuos period comparisons for being able to highlight the charts with critical points.

Key Features:

Define variances in our charts


![3-21](https://user-images.githubusercontent.com/92877810/138261811-ccb46f24-2b2e-44cd-bc9f-65e5babceb12.png)

🚩First, let us add a variance to our KPI for average sales revenue in stores so we can compare if average sales revenue has dropped this year relative to our previous year's performance. If you can recall, our KPIs currently have a 2021 time filter applied on them. 

1. Right Click on the Avg Sales Revenue Chart to Open the Context Menu

2. Click Compare To

3. Click Previous Period

🚩We want to compare our data in 2021 year to date with the calculation for the previous year. By comparing to previous period, SAC will automatically calculate this variance for us. 

![3-22](https://user-images.githubusercontent.com/92877810/138261815-181434bd-67c1-4f37-b97e-b6319df2c378.png)

🚩After creating our variance, the absolute value may still be hard to contextually understand. We want to know the percentage difference so let us edit this variance. 

![3-23](https://user-images.githubusercontent.com/92877810/138261816-7eaefbe5-59b2-4fe0-b0ae-aa4dd3d848a3.png)

4. Click **1 Variance**

5. Click **Edit All Measures in Use**

![3-24](https://user-images.githubusercontent.com/92877810/138261817-c5304eab-976e-4c15-b1dc-fcd2913ff093.png)

🚩In this panel, users can choose how they want to format their variances to best fit their data. We are comparing a KPI across two periods using a single number. In this instance, a percentage would be easier to understand for an end user. 

6. Click **Percentage**

7. Deselect **Numbers**

8. Click on **Avg Sales Revenue for Actual** to Collapse the Variance Panel

![3-25](https://user-images.githubusercontent.com/92877810/138261818-9c84e36a-6eeb-45ff-a5db-4a508521d031.png)

🚩The new variance looks great! We can now clearly see that average sales revenue in our stores has experienced a 3.7% drop from the last period. 

![3-26](https://user-images.githubusercontent.com/92877810/138261820-4d487ce7-79be-4bd8-ab9a-53445779ee16.png)

🚩Now let’s add more variances to our chart. A good candidate to track change in data over time is our chart using a time dimension. SAC offers recommended comparisons in the builder panel as a suggestion for easy creation of variances. 

9. Select your **Gross Margin per Order Date for Actual** Chart

🚩We want to select Previous Period because it will dynamically change the variance based on the granularity in the chart. 

10. Expand **Recommened Comparisons**

11. Click **Previous Period**

![3-27](https://user-images.githubusercontent.com/92877810/138261821-154f9835-dac8-4f7a-9d40-d52f19f718a8.png)

🚩Our variances show the delta to the period before, in this case the last month's gross margin. We want to know the percentage difference instead of absolute difference. Let us change the formatting of our variance values. 

![3-28](https://user-images.githubusercontent.com/92877810/138261822-434fb259-be1f-43b8-8ddf-a193366b87f5.png)

12. Scroll to the Bottom of the Builder Panel

13 Click **Edit** for the Variance **All Measure in Use (Previous Period)**

![3-29](https://user-images.githubusercontent.com/92877810/138261823-27ca40d7-c623-4e1e-abe8-c71544e5991d.png)

14. Expand **Display Options**

15. Scroll to the Bottom of the Builder Panel

16. Click **Percentage**

17. Deselect **Numeric**

18. Click **OK**

![3-30](https://user-images.githubusercontent.com/92877810/138261824-2f15a39e-296d-4582-9601-a83dc45fb56f.png)

⚠️Quality check! Have your variances in the chart updated to percentage values? Please note your data will look different due to the dynamic time filter on the chart

![3-31](https://user-images.githubusercontent.com/92877810/138261825-3b5fffe4-a935-4968-b6ff-e73fe5248003.png)



## Exercise 2.3 Create a threshold

Objective: Welcome to the Thresholds panel. 

Estimated Time: 5 mins

Exercise Description: You as a Dashboard Designer will be able to create Within Thresholds, you can create a threshold based on a number range or against another measure. In our case, we are interested in a number range.

Key Features:

Define thresholds in our charts
 

1. In Threshold Panel, Click **Add Range**

![3-39](https://user-images.githubusercontent.com/92877810/138261836-4316999f-d492-4fdc-9ff9-9484a2f432d8.png)

2. Enter 0 for the OK (Green) Min Range

3. Enter 0 for the Warning (Yellow) Max Range

![3-40](https://user-images.githubusercontent.com/92877810/138261837-a00d7b3c-1e41-4827-876d-eca788fb49c9.png)

4. Expand the **Orange Indicator**

5. Choose the **Red Indicator**

6. Click **Apply**

![3-41](https://user-images.githubusercontent.com/92877810/138261839-55e6ab20-3a6d-4dba-9587-d14462d58392.png)

🚩Users can see by scrolling through the table that an appropriate indicator has been given to values in each threshold in the Delta column. 
  
We would like to change how this value is displayed to only highlight the number rather than adding an indicator. 

![3-42](https://user-images.githubusercontent.com/92877810/138261840-30de12bd-f485-4d8d-99e6-b9915487e5e4.png)

7. Click **Designer** to Open Builder Panel (in case not already open)

8. Click **Styling**

![3-43](https://user-images.githubusercontent.com/92877810/138261841-a745789d-f862-43a1-ba58-03c933ce00f0.png)

ℹ️Welcome to the Styling Panel! 
  
The Styling Panel displays options available for the selected tile type. Some options may not be available to all users.  
  
For widget, you see only the styling options for the specific area that you have highlighted. The heading in the Styling Panel identifies the area. For example, it may show Title, Data Cell, Axis Labels, and so on. Selecting a different part of the widget changes the heading and the styling options. 

![3-44](https://user-images.githubusercontent.com/92877810/138261842-9bb75e2e-26fb-4c78-87b7-622c4102c5b9.png)

9. Expand **Threshold Style**

10. Click **Color Values**

![3-r](https://user-images.githubusercontent.com/92877810/140990851-e292bf04-dc4d-4420-8f0a-1cd29842ce50.png)

🚩Thresholds in the table are now color coded instead of representation by a symbol indicator. 

![3-46](https://user-images.githubusercontent.com/92877810/138261844-ccf89b5c-0321-4451-aeed-29d15cd5418b.png)

⚠️Quality Check! Does your dashboard with thresholds and variances look like this screenshot? 

🚩Please save your story by pressing **Ctrl + S** on your keyboard! 

![3-47](https://user-images.githubusercontent.com/92877810/138261847-1706de9d-af06-4c1b-8774-3a19f90ef649.png)


## Summary

**You have completed Thresholds, and Variances section!**

**You are now able to:**

- Use recommended comparison to quickly add variances to a chart
- Add a threshold to a table

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
