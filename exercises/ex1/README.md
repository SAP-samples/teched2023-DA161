# Exercise 1 – Understanding the Basics of SAP Analytics Cloud Stories

**Objective:** You should develop a basic understanding on how to create visualizations within SAP Analytics Cloud. 

**Estimated Time:** 35 mins

**Exercise Description:** You and a colleague are building a dashboard for the upcoming board meeting. As a starting point, your colleague has incorporated some Financial Planning Data into the dashboard. You want to further enhance the dashboard to better represent some KPIs while including HR data to get a better understanding on the end-to-end business operations as TCS Technologies. 

**Key Features:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the Builder Panel vs. Styling Panel 
- Learn how to create some calculations

⚠️**Disclaimer**
When completing exercises, some data values or screenshots may not match what you see on your screen. It is because the current exercise is based on a feature that is currently in BETA. 

----------------------------------------------------------------------------------------------------------------------------------------

🚩As a Business Analyst for TCS Technologies, we are interested in creating a dashboard that incorporates Business Intelligence, Planning, and Scripting. As a starting point, you want to enhance the dashboard that your colleague has started by incorporating HR data. 
 
Lets start by editing the dashboard!

1. Click **Edit**

![image](https://user-images.githubusercontent.com/112718519/200538027-765c8858-2bcc-4fac-a052-d27f2551a795.png)

🚩 We can see that based on the current design of the dashboard, the Table and Reporting Currency (Measure Input Control) takes up the entire dashboard. Let's resize a few widgets to make room for some additional visualizations that we want to create.

2. Scroll to the **bottom of the dashboard**

![image](https://user-images.githubusercontent.com/112718519/200538367-9cd58388-c2d6-44cd-bd82-21b6c27263c0.png)

3. Click and **hold** the resize icon in the bottom right of the Table 

![image](https://user-images.githubusercontent.com/112718519/200538473-244c56b6-6bd2-4b4e-988e-55fc4cd3bace.png)

4. Resize the Table until it just fits all the Accounts

![image](https://user-images.githubusercontent.com/112718519/200539009-e09d794e-c16e-443c-8c36-42cc837fe559.png)

5. Click and hold the resize icon in the bottom right of the Reporting Currency Input Control

![image](https://user-images.githubusercontent.com/112718519/200688313-e5bf582a-6eb6-49be-a931-4816ea637f4e.png)

6. Resize the Reporting Currency Input Control so that it has the same height as the Table

![image](https://user-images.githubusercontent.com/112718519/200538867-bbd46e3d-84e3-4845-90de-1c72d418c0c2.png)

⚠️**Quality Check!**
Does your Table and Reporting Currency Input Control look like this?

![image](https://user-images.githubusercontent.com/112718519/199618487-073b1a5f-fa3c-48de-ba9f-a3106ade61fe.png)

🚩 Now that we have room on our dashboards, let's create our first visualization. We want to provide our colleagues a better understanding of the Gross Profit per Product.
 
Let's insert a Chart to visualize this information.

7. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/197619063-09705a2c-7aad-4a19-8639-ff374c068cbc.png)

ℹ️ Welcome to the Builder Panel!

The Builder Panel is a place where you can create your visualizations by specifying elements of a visualization such as accounts, measures, dimensions, filters and so on. The Builder Panel will dynamically update depending on the Data Model and the type of visualization that you are creating. 
 
For this Chart, we want to use SAP_XPA_FINANCE as our data model, which is a New Model type. The Chart requires at least one Account and at least one Measure to be selected from the Builder Panel. 

![image](https://user-images.githubusercontent.com/112718519/200542883-18b2c9fd-ff46-416c-9575-e9ad0dc44ed9.png)

🚩 In the Builder Panel, we can see that the current data model that is being used in the Chart is SAP_XPA_HEADCOUNT. In order to incorporate financial data into the Chart, you will need to change the Data Model for this Chart.

8. Click on the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/200542938-d167e56a-4426-4b96-a32b-51b6ad75d08f.png)

9. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199082639-86f8f983-4107-42cf-a3ad-34a40bd749e9.png)

10. Click **SAP_XPA_FINANCE**

![image](https://user-images.githubusercontent.com/112718519/199082690-5b325dbd-9107-4323-86ef-a39a0fae62a2.png)

11. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/199082747-349edbdf-3949-43d1-b108-0826d238ae80.png)

🚩 After selecting the Finance Data Model, the Builder Panel automatically updates the name of the Data Model.

12. Click **+ At least 1 Account required**

![image](https://user-images.githubusercontent.com/112718519/199083035-638c0472-f146-4ad8-8ff3-4b39f12501f8.png)

13. Click on the arrow beside Finance to expand the Account
14. Click on the arrow beside Operating Income to expand the Account
15. Click on **Gross Profit**
16. Click anywhere outside the Account selection dropdown menu to collapse it 

![image](https://user-images.githubusercontent.com/112718519/199083860-4b4fe42e-e30c-4d16-ba7a-89e54192ae0a.png)

17. Click **+ At least 1 Measure required**

![image](https://user-images.githubusercontent.com/112718519/199084027-73fb187b-2b7a-4c81-8bc3-b02479031688.png)

18. Click **Reporting Currency**
19. Click on a spot outside the Measures selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199084112-834e7f1f-84d8-4d26-9080-7501e08238c4.png)

🚩 We can now see data for our Gross Profit as we've successfully met the minimum conditions to view data for our Bar / Column Chart. Let's now add our Product dimension to see the breakdown per Product.

![image](https://user-images.githubusercontent.com/112718519/199619015-fe52f2f1-c50f-43c6-b5da-605a8291f900.png)

20. Click **+ Add Dimension**

![image](https://user-images.githubusercontent.com/112718519/199084155-488f00af-059f-43d5-a316-77fccd115369.png)

21. Click **SAP_XPA_PRODUCT**
22. Click anywhere outside the Dimension selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199084307-0511fa19-fbed-4aac-b785-436c935ab24c.png)

🚩 However, as Product is a hierarchial dimension, we want to drill down into the Product Dimension so that we can see a more detailed view of our Gross Profit.

23. Let's try drilling via the Builder Panel. Click the **Drill** icon in the SAP_XPA_Product Dimension. 
24. Click on **Level 2**
 
![image](https://user-images.githubusercontent.com/112718519/200914833-0ece700b-cae3-473b-83e4-317bdf2acdd4.png)

🚩 We can now see data for our Gross Profit per Product. Based on this breakdown, we can see that Youth Bikes bring us the most Gross Profit in comparison to any other product that we offer.

Let's resize and reposition the visualization for better readability.

25. Scroll to the right of the dashboard
26. Click and hold the border of the Chart to move the Chart to align it with the top of the Table

![image](https://user-images.githubusercontent.com/112718519/199610647-8bd43648-27e6-4df0-8c26-a02ca87a6cf2.png)

27. Click and hold the bottom right resize icon for the Chart. Resize the Chart to align it with the table and the edge of the shape header.

![image](https://user-images.githubusercontent.com/112718519/199610701-5adc12e5-a6b7-4a00-b8ba-67fa26a7ebf2.png)

⚠️**Quality Check!** Does your Table look like this?

![image](https://user-images.githubusercontent.com/112718519/199611034-2a0e24e6-acc4-492c-904f-909828d13b64.png)

🚩 Now, the Chart only shows actual Gross Profit. We want the Chart to show actual Gross Profit versus planned Gross Profit. We will add planned Gross Profit into the Chart by adding an additional Dimension. 

28. Scroll to the bottom of the Builder Panel
29. Click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/200915978-7e33105c-5b6b-49d3-9a36-b8e56ef4f383.png)

30. Click **Version** 

![image](https://user-images.githubusercontent.com/112718519/199611186-bf29c876-3372-478e-ba58-aa5d53d3fbb5.png)

Note: if the chart is in blue then uncheck color by Account

<br>![](/exercises/ex1/images/30_1.png)<br><br><br>

ℹ️ International Business Communication Standards (IBCS)

The color of the Chart is now changed to black for actual Gross Profit. This is because SAP Analytics Cloud is following International Business Communication Standards (IBCS), so we are coloring the bars based on the color of the Version that is added to the Chart. Now that we have actual Gross Profit in our Chart, we want to add planned Gross Profit.

![image](https://user-images.githubusercontent.com/112718519/199611592-218dd603-191e-4e64-bd67-f84fb7920da2.png)

31. Click **+ Add Version**

![image](https://user-images.githubusercontent.com/112718519/199611769-3603796a-8c95-4f41-a52a-15a7cc9f3bbb.png)

32. Click **22 Plan**
33. Click on a spot outside the Version selection dropdown menu to collapse it

![image](https://user-images.githubusercontent.com/112718519/199611789-a6021b16-19f8-46c7-a289-3137e4ba6d70.png)

🚩 We can see the difference between our Plan 22 and Actuals. However, we want a better visual representation of this data. Hence, lets add a variance to show the difference between Actual and 22 Plan.

34. Click the **expand** icon for Chart Add-ons
35. Scroll to the bottom of the Builder Panel
36. Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/199611830-72d07bdc-3f46-4640-ad7a-8d007dce9172.png)

37. Click **+ Add Version/Time** 

![image](https://user-images.githubusercontent.com/112718519/199611840-e89e3e4d-132b-40cf-b466-6a297795e7b6.png)

38. Click **Version** 

![image](https://user-images.githubusercontent.com/112718519/199611875-5bacc75b-bbd6-4ca9-9863-8d6f97f91d49.png)

39. For Compare (A), click the expand icon for Version
40. Click **Actual**

![image](https://user-images.githubusercontent.com/112718519/199611913-6f722657-7b05-46b5-8f4c-98be4b3e700c.png)

41. For To (B), click the expand icon for Version
42. Click **22 Plan**

![image](https://user-images.githubusercontent.com/112718519/199611942-1a3b4aef-23b8-4cfc-ba23-c306cd977115.png)

43. Click **Data Label**
44. Scroll to the bottom of the Variance Panel
45. Click **Both**
46. Click  the **expand** icon for Number
47. Select **1** to set the decimal precision for the numeric variance

![image](https://user-images.githubusercontent.com/112718519/200696880-ec4cfdf2-c9b4-4b67-9696-c1b54156ab3a.png)

48.	Click the **expand** icon for Percentage
49.	Select **1** to set the decimal precision for the percentage variance
50.	Click **Done**

![image](https://user-images.githubusercontent.com/112718519/199612015-08d7730e-df42-4c2b-b402-1395e3569de7.png)

⚠️**Quality Check!** Does your Chart look like this? 

![image](https://user-images.githubusercontent.com/112718519/199612802-bc96fc93-3d8c-4c0f-82ce-bd5ea9c15fe9.png)

🚩 Press CTRL + S to save your story. 
Select keep Model as below

![image](https://github.com/SAP-samples/teched2023-DA161/assets/146422837/cc4af490-56e0-4127-ac01-583bc8b075bb)


🚩 To ensure that we are comparing 22 Plan with 22 Actual instead of Actual financial data for all years, let's add a filter so that we are setting a date range for current year (2022) values through the current period.

51. Click **+ Add Filters**

![image](https://user-images.githubusercontent.com/112718519/199613739-f4aa042a-37f7-4841-8192-d405b182ef80.png)

52. Click **Date (Range)**

![image](https://user-images.githubusercontent.com/112718519/199613815-1e779afb-46ac-4cde-b43b-449690b65bc2.png)

53. Click the **toggle** to enable the ability to include range up to the current period and select 1 under look back

![image](https://github.com/SAP-samples/teched2023-DA161/assets/146422837/dc6df592-413f-4f4f-86e5-57f030c24754)


54. Click **OK**

![image](https://github.com/SAP-samples/teched2023-DA161/assets/146422837/6e3bfa71-fa17-4be2-9c5b-735611f994b3)


⚠️**Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/199614205-174b6132-a506-4b77-a4ff-8260d5710428.png)

🚩 We now have a good representation of some key figures when it comes to our financial data. Now, let's incorporate some Headcount data into our dashboard to provide our management team a holistic view of the business. 

55. In the toolbar, click on the **Chart** icon

![image](https://user-images.githubusercontent.com/112718519/199614384-e0f4ff42-2531-44f8-836c-fc8db412f5fa.png)

56. Click and hold the border of the chart to move the object and position it to align with the Reporting Currency Input Control.

![image](https://user-images.githubusercontent.com/112718519/200699710-282d1e17-2c87-4432-b4fb-9a46285cd6c2.png)

57. Click and hold the bottom right resize icon of the Chart

![image](https://user-images.githubusercontent.com/112718519/200699722-7cb0d815-140f-4a03-9787-576b0d56daf2.png)

58. Resize the Chart so that its width is slightly smaller than the Table above

![image](https://user-images.githubusercontent.com/112718519/200699738-6cb8cc4f-abd2-4798-8c1e-ed5a1e233211.png)

🚩 We can see that the current data model that is being used in the Chart is SAP_XPA_FINANCE. In order to incorporate Headcount data into the Chart, you will need to change the Data Model for this Chart. 

59. Click the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/200699758-b5317fae-3d28-46ca-b163-a68c7135ab0c.png)

60. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/200700057-0536d294-dada-4f65-93a5-8352daf6445c.png)

61. Click on the arrow

![image](https://user-images.githubusercontent.com/112718519/200700064-93cb9fb6-177a-4cd4-8720-0ced99f2fe0c.png)

62. Click **SAP_XPA_HEADCOUNT**

![image](https://user-images.githubusercontent.com/112718519/200699859-8a11a22a-5fe6-44c0-82bc-e74949cd3945.png)

63. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/200699882-f0e7f7c1-15a5-40d6-9f31-61e2ce09dedb.png)

🚩 After selecting the Headcount Data Model, the Builder Panel automatically updates the name of the Data Model. For the Headcount Data Model, it is a Classic Account Model instead of a New Model that we saw for the Finance Data Model. Therefore, the Builder Panel is updated to reflect how Account is the only requirement for the Classic Account Model. 

You are not too familiar with the Headcount Data Model and you want to see a list of Accounts and Dimensions that are available to insert into the Chart. In the top right of the Builder Panel, click Available Objects.

64. Click **Available Objects** in the Builder Panel

![image](https://user-images.githubusercontent.com/112718519/200700090-22438f86-66af-41c7-84e4-d496de2d410d.png)

ℹ️ Welcome to the Available Objects!

It provides you a holistic view of all the data-related objects that are associated to the data model. It provides you with an ability to quickly drag and drop objects into the Builder Panel or use any of the quick action menus to bind the data.

![image](https://user-images.githubusercontent.com/112718519/200700120-2ad4f526-afb5-4c8c-b726-5b713ee866f3.png)

🚩 Based on the data that is available within this data model, we are interested in building a trend over time that represents our headcount.

65. Click on the **More** action icon ("...") for **Headcount**
66. Click Add to Accounts

![image](https://user-images.githubusercontent.com/112718519/200700132-1213585c-7c8e-4fc7-9015-ad1a72dc94c6.png)

67. Click on the search bar and type **Hire**
68. Click on the **More** action icon ("...") for **SAP_XPA_HIRE_DATE**
69. Click on **Add to Dimensions**

![image](https://user-images.githubusercontent.com/112718519/200700147-e65c20e5-d574-4c03-b6fd-b009ce5b753c.png)

⚠️ **Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/200700169-20a980c5-150b-4b23-bbc8-110fc1ce29d7.png)

70. Click on the bar that represents (all)
71. Click on the **Drill Down** icon

![image](https://user-images.githubusercontent.com/112718519/200700193-6f596a1d-51b4-4453-8f4e-4312fdbf377e.png)

72. Within the Builder Panel, click on the **Drill icon** for SAP_XPA_HIRE_DATE
73. Click **Level 3**

![image](https://user-images.githubusercontent.com/112718519/200700256-83084804-f666-4508-ac67-921b456c9c78.png)
 
⚠️ **Quality Check!** Does your Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/200700287-dc7d40cd-b370-4d91-930a-845dd85f9a66.png)

74. Scroll to the bottom of the Builder Panel
75. Click **expand** for the Chart Add-ons
76. Click **Variance**

![image](https://user-images.githubusercontent.com/112718519/200700399-e565f6d1-5b99-4566-897e-22cfff24e9b8.png)

77. Click **+ Add Version/Time**

![image](https://user-images.githubusercontent.com/112718519/200700414-d0fe9d59-9c32-4728-a109-2726c70fce2e.png)

78. Click **SAP_XPA_HIRE_DATE** 

![image](https://user-images.githubusercontent.com/112718519/200700427-5b4e7ef8-109f-4985-a43b-cdeed429a3eb.png)

79. Click **Integrated**
80. Click **Done**

![image](https://user-images.githubusercontent.com/112718519/200700455-f2a649c5-95fa-46b6-ad60-6d2fc7b251a6.png)

81. Click **X** to close the Available Objects List

![image](https://user-images.githubusercontent.com/112718519/200700471-5b0e705c-0597-4f93-a905-3570d6702cd0.png)

⚠️Quality Check! Does you Chart look like this?

![image](https://user-images.githubusercontent.com/112718519/200700499-53054f60-e22f-4b51-ac73-4b1e9c29ea1d.png)

🚩 We now want to add a Geographical representation of where the hires are per location. It would also be a good idea for us to better understand the various career levels that we have by headcount per location.

82. Click the **Add** icon
83. Click **Geo Map** in the Others section

![image](https://user-images.githubusercontent.com/112718519/201235170-205d0ced-a278-4a14-a8bc-c75dc4e79420.png)

84. Click and hold the border of the Geo Widget to move the object

![image](https://user-images.githubusercontent.com/112718519/200700537-1900a278-ec0b-4e4d-888e-f018867ffab0.png)

85. Move the Geo Widget to align it with the top of the Chart

![image](https://user-images.githubusercontent.com/112718519/200700550-85845114-dfee-4711-8d86-b80bbe0b3cd3.png)

86. Resize the Geo to align it with the Chart above and the edge of the shape header

![image](https://user-images.githubusercontent.com/112718519/200700578-4e4149d0-0a69-4eb7-b040-dcf1033ef36b.png)

🚩 We want to change the Base Layer Style to better match the theme of the rest of the dashboard.

87. Click Light Gray to open the dropdown menu to see other Base Layer Styles
88. Click **Transparent Dark Gray**

![image](https://user-images.githubusercontent.com/112718519/200700597-e06d014c-be7d-40c4-88fc-678864d9c700.png)

89. Click **+ Add Layer**

![image](https://user-images.githubusercontent.com/112718519/200700607-0e230137-473a-4dc7-87db-4d821051f7ee.png)

90. Click **+ Location Dimension required** 

![image](https://user-images.githubusercontent.com/112718519/200700627-c6c4b7fd-5aa0-48c3-8d1d-1e9d72fb06c1.png)

91. Click **Hire_Location**

![image](https://user-images.githubusercontent.com/112718519/200700636-208ac5b3-fe52-4fd9-930e-2aeb528eea83.png)

ℹ️ Location Clustering in Geo Visualization! Adding a Location Dimension will determine whether or not Location Clustering in the Builder Panel will continue to be turned on or automatically turned off. It will be turned off if you have less than 5000 data points. In this example, Location Clustering is automatically turned off in the Builder Panel. 

![image](https://user-images.githubusercontent.com/112718519/199616164-63424461-3b29-435d-a609-215330b2ea1d.png)

🚩 We can now see data points for all our hire locations in the Geo Map. Let's add Headcount and Career Level as the size and color respectively to further drill down into our data.

92. Under Bubble Size, click **+ Add Account**

![image](https://user-images.githubusercontent.com/112718519/200700669-11678090-2f2e-4f64-8a93-64182b9c2825.png)

93. Click **Headcount**

![image](https://user-images.githubusercontent.com/112718519/200700686-26f00d73-690f-4094-983c-76c15a30990a.png)

94. Under Bubble Color, click **+ Add Dimension/Account**

![image](https://user-images.githubusercontent.com/112718519/200700694-f1a16543-1414-4109-adcc-e888aeff1d50.png)

95. Click **SAP_XPA_CAREER_LEVEL**

![image](https://user-images.githubusercontent.com/112718519/200700716-165d1e12-ffe4-4474-afe0-75e9499ac3cf.png)

96. Rename the Layer Name to **Headcount by Career Level**
97. Click **Done**

![image](https://user-images.githubusercontent.com/112718519/200700737-629fd6c3-9101-414f-8e3e-58d0ac247487.png)

⚠️ **Quality Check!** Does your Geo Visualization look like this?

![image](https://user-images.githubusercontent.com/112718519/199100172-356e447d-7660-4e5f-a8d8-255e0b4da34c.png)

🚩 Press CTRL + S to save your story. 

🚩 We are now interested in adding another KPI to summarize the Average Salary that we are paying our employees. To make it easier, let's duplicate the existing KPI so that we don't need to worry much about the formatting of the object.

98. Click on the Numeric Point Chart for Operating Income for 2022
99. Click the **More** Action icon
100. Hover over **Copy** and select **Duplicate**

![image](https://user-images.githubusercontent.com/112718519/201237616-896118a2-4bf9-4d6b-bd1d-19db67557dbe.png)

101. Move the object besides Operating Income for 2022
102. Click on the **Data Model** icon

![image](https://user-images.githubusercontent.com/112718519/200700864-ff74b30b-f570-406f-9689-5eaf1a063ea8.png)

103. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/200701179-9bd190cc-d300-4ecf-88cf-50454928b682.png)

104. Click **SAP_XPA_HEADCOUNT**

![image](https://user-images.githubusercontent.com/112718519/200701184-dc46e43c-5315-480b-82d5-df4fc5ff91be.png)

105. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/200701193-5245d5d0-0312-45d4-9570-1d7c621328ef.png)

106. Click **+ At least 1 Account required** 

![image](https://user-images.githubusercontent.com/112718519/200701208-4235146c-2923-47a3-b4bb-a9cbec469d3f.png)

107. Click **Salary** 

![image](https://user-images.githubusercontent.com/112718519/200701215-9e0394ef-c673-4987-9bb7-a3f4c444803b.png)

🚩 After clicking Salary, we realize that the KPI shows the total salary that was ever paid to employees. This KPI doesn't show Average Salary per Employee, which is what we want to see in the KPI.

Hence, we will have to create a calculation to reflect this metric.

108. Deselect **Salary** 
109. Click **Add Calculation** 

![image](https://user-images.githubusercontent.com/112718519/200701241-f7e16f77-bdab-451e-a406-3dad76b0b5be.png)

110. Click **Aggregation**

![image](https://user-images.githubusercontent.com/112718519/200701339-93b98629-56a3-4d59-bf7f-cd396a5f6ce8.png)

111. Click the **Expand** icon for Operation
112. Scroll down till you see **Average**
113. Click **Average**

![image](https://user-images.githubusercontent.com/112718519/200703351-672fc08a-5b22-4fcd-ab64-88ee1ef9d55b.png)

114. Click the **Expand** icon for Account
115. Click **Salary** 

![image](https://user-images.githubusercontent.com/112718519/200701364-cf59044f-5f0c-4f5d-960c-ddf7fddf923c.png)

116. Click the **Expand** icon for Aggregation Dimensions
117. Click **SAP_XPA_EMPLOYEE**

![image](https://user-images.githubusercontent.com/112718519/201236671-6079eef2-6a0a-483a-931e-9471a9d93c4b.png)

118. Rename the calculation to **Average Salary**
119. Click **OK**

![image](https://user-images.githubusercontent.com/112718519/200701424-1654a3c4-bf09-4e88-89af-b6e34f2bed7e.png)

120. Rename the Title to **Average Salary**

![image](https://user-images.githubusercontent.com/112718519/200701482-05859c5d-e093-4f1a-aa74-f6add6ef9eae.png)

121. Click the **More** Action icon
122. Hover over Show / Hide and deselect **Primary Value Labels**

![image](https://user-images.githubusercontent.com/112718519/200702329-03a8e9da-6f88-4a06-86d7-d29d006f4d00.png)

⚠️Quality Check! Does your KPI look like this?

![image](https://user-images.githubusercontent.com/112718519/200701969-72f72fba-8a2d-468b-a0cf-62818c48dd3c.png)

🚩 Press CTRL + S to save your story. 



## Summary

**You have completed the entire Understanding the Basics of SAP Analytics Cloud Stories section!**

**You are now able to:**
- Create a set of visualizations (i.e. Chart, Geo, and Table) to illustrate key relationships within your data
- Understand the difference between the Builder Panel vs. Styling Panel 
- Create a set of basic calculations
- Include Chart Add-ons, such as a Variance

Continue to - [Exercise 2 - Expand the Dashboard with Core Add-ons](../ex2/README.md)

