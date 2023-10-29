# Exercise 2 - Expand the Dashboard with Core Add-ons





## Exercise 2.1 View Time Toolbar Customization


Objective: You should develop a basic understanding on how to create Customize your toolbar for various experiences of SAP Analytics Cloud Stories.

Estimated Time: 5 mins

Exercise Description: You as a Dashabord designer want to control the toolbar experience for your end users, and having all the toolbar features is not really required for end users.

Key Features:

Define what view mode of the story you need to control for your end users view vs embed mode of your stories.
Learn you to control the toolbar features via story settings.




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
