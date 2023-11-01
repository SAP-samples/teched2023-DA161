# Exercise 4 - Extend the Dashboard with No Code Features

**Objective:** You should develop a dashboard with No code Features in SAP Analytics Cloud.

**Estimated Time:** 20 mins

**Exercise Description:** Story designers can leverage a variety of no-code features coming from analytical applications, such as Custom widgets, composite and Custom widget Add-on. 

 **Custom Widgtes:**
 Story designer can now integrate custom widgets into story, to extend the varieties of visualizations and functionalities. With the data binding capability of 
 custom widget, story designer can configure custom widgets like configure a standard SAP Analytics Cloud chart without any coding or scripting knowledge. 

 **Composites:**
 A composite is a combination of widgets with configured data and scripting elements, which can be reused across optimized stories. It can be a unified corporate  
 header or footer, page navigation panel, collapsible section with visualizations, or chart with a button to switch to another chart type or table view. With 
 composites ready to be used in stories, story designers and developers spend less time building stories, and they can do further actions and customizations on 
 the composite as a whole as well, such as changing styling and adding scripts.
 You can create a composite and then import and directly use it in your optimized story as other SAP Analytics Cloud built-in widgets.

**Key Features:**
* Create a composite
* Create a custom widget
----------------------------------------------------------------------------------------------------------------------------------------
Create **Composites** 

1. Navigate to SAC **HomePage**
 <br>![](/exercises/ex4/Images/4img1.png)<br><br><br>

2.Navigate to stories and Click on Composites
 <br>![](/exercises/ex4/Images/4img2.png)<br><br><br>
3. Composites Page displays the recently viewed files and click on Create New Composite 
 <br>![](/exercises/ex4/Images/4img3.png)<br><br><br>

4. You will be landed into New Composite designer page. In this example you will create a composite with Header with default title and description. 

   <br>![](/exercises/ex4/Images/4img4.png)<br><br><br>

5. Drag and Drop Panel widget to the page.

   <br>![](/exercises/ex4/Images/4img5.png)<br><br><br>

6. Re-size the panel to full page

   <br>![](/exercises/ex4/Images/4img6.png)<br><br><br>

   <br>![](/exercises/ex4/Images/4img7.png)<br><br><br>

7. Open the Right side Panel :

   <br>![](/exercises/ex4/Images/4img8.png)<br><br><br>

8. Change the background colour

   <br>![](/exercises/ex4/Images/4img9.png)<br><br><br>
9.Insert Text Box: 
   <br>![](/exercises/ex4/Images/4img10.png)<br><br><br>

10.Change the Font Colour to white and add Text as **Title** and rename the ID as **Title**
 
  <br>![](/exercises/ex4/Images/4img11.png)<br><br><br>
  
  <br>![](/exercises/ex4/Images/Title.png)<br><br><br>

11. Add Two more Text Boxes as Subtitle and Descritpion. Rename the ID as **Subtitle** and **Description**
 <br>![](/exercises/ex4/Images/4img12.png)<br><br><br>

 <br>![](/exercises/ex4/Images/subtitle.png)<br><br><br>
 
 <br>![](/exercises/ex4/Images/Description.png)<br><br><br>

12. Change the font text colour as white and adjust the font size accordingly.
  <br>![](/exercises/ex4/Images/4img13.png)<br><br><br>

13. Open the Left Side Panel --> **Outline** --> interface --> Functions
  <br>![](/exercises/ex4/Images/4img14.png)<br><br><br>

  using Add Script function option, create three Script functions 
  <br>![](/exercises/ex4/Images/interface.png)<br><br><br>

  <br>![](/exercises/ex4/Images/Addscriptfunction.png)<br><br><br>

15. Click on fx for function1 to edit scripts:
   
   <br>![](/exercises/ex4/Images/4img15.png)<br><br><br>


15.1 Edit the Name of Scriptfunction function1 as setTitle

<br>![](/exercises/ex4/SetTitle.png)<br><br><br>

   15.2 Create a new Arguments  

   <br>![](/exercises/ex4/Argument.png)<br><br><br>

   15.3 Name the argument as **Text**

   <br>![](/exercises/ex4/argumentText.png)<br><br><br>

  15.4 similarly edit other two Scriptfunctions function2 and function3 as SetDescription and SetsubTitle with New Arguments as **Text**

   <br>![](/exercises/ex4/Images/Allscriptfunctions.png)<br><br><br> 

  15.5 click on formula fx for SetDescription :

  <br>![](/exercises/ex4/Images/setDesFunc.png)<br><br><br> 

  Add the below script:
 
  **Description.applyText(Text);**
 
  **Description.setVisible(true);**
  
   <br>![](/exercises/ex4/Images/setDesFormula.png)<br><br><br> 
  
  15.6 click on formula fx for Setsubtitle :

  <br>![](/exercises/ex4/Images/setsubtitleFunc.png)<br><br><br> 

   Add the below script:
  
   **Subtitle.applyText(Text);**
   
   **Subtitle.setVisible(true);**

   <br>![](/exercises/ex4/Images/setsubtitleFormula.png)<br><br><br> 
  

  15.7 click on formula fx for SetTitle :

  <br>![](/exercises/ex4/Images/settitleFunc.png)<br><br><br> 

   Add the below script:
   
  **Title.applyText(Text);**
  
  **Title.setVisible(true);**

   <br>![](/exercises/ex4/Images/settitleFormula.png)<br><br><br> 

  

15. Save the Composite
  <br>![](/exercises/ex4/Images/4img19.png)<br><br><br>

16. In **MyFiles/Starting Dashboards** Folder:
   <br>![](/exercises/ex4/Images/savecomp.png)<br><br><br>

17. Now you can use this composite in Stories. Open the Exercise 4 story and click on edit
   <br>![](/exercises/ex4/Images/4img21.png)<br><br><br>

18. Expand the left side Panel, click on composites and click on Import Icon

  <br>![](/exercises/ex4/Images/4img22.png)<br><br><br>

19. Import the newly created composite : Header – composite 
  <br>![](/exercises/ex4/Images/4img23.png)<br><br><br>

20. Composite is imported sucessfully :
  <br>![](/exercises/ex4/Images/4img24.png)<br><br><br>

21. Drag and Drop the composite :
  <br>![](/exercises/ex4/Images/4img25.png)<br><br><br>
  <br>![](/exercises/ex4/Images/4img26.png)<br><br><br>

22. Resize the coposite header to the top of the page.
  <br>![](/exercises/ex4/Images/4img27.png)<br><br><br>

23. CLick on Outline :
  <br>![](/exercises/ex4/Images/4img28.png)<br><br><br>

24. Click on Formula of Page_1 and select Oninitialization 
  <br>![](/exercises/ex4/Images/4img29.png)<br><br><br>

25. Add the formula
  <br>![](/exercises/ex4/Images/4img30.png)<br><br><br>

26. Save the Story
  <br>![](/exercises/ex4/Images/4img31.png)<br><br><br>

27. Open the Story in New tab:
  <br>![](/exercises/ex4/Images/4img32.png)<br><br><br>

28. Now you can see the Title, Subtitle and Description is updated.
   <br>![](/exercises/ex4/Images/4img33.png)<br><br><br>

## Summary
**You have completed the Creation of Composite section!**
**You are now able to:**
* Understand how to Create and add Composites in a dashboard

Create **Custom widget** 
1. Click on the Custom widget Page:
    <br>![](/exercises/ex4/Images/CW1.png)<br><br><br>
  
2.  Add a custom widget – Echarts Sankey styling V1.0.0:
   <br>![](/exercises/ex4/Images/CW2.png)<br><br><br>

3. Click on Right Panel :
   <br>![](/exercises/ex4/Images/CW3.png)<br><br><br>

4. Navigate to Builder Panel :
  <br>![](/exercises/ex4/Images/CW4.png)<br><br><br>

5. Click on Select model:
  <br>![](/exercises/ex4/Images/CW5.png)<br><br><br>

6. Choose BestRunJuice_Sample Model:
   <br>![](/exercises/ex4/Images/CW6.png)<br><br><br>
   
7. Add Gross Margin as Measure and Location in Dimension  
   <br>![](/exercises/ex4/Images/CW7.png)<br><br><br>
 
8.Sankey chart is displayed for Gross Margin for different locations :
  <br>![](/exercises/ex4/Images/CW8.png)<br><br><br>


## Summary
**You have completed the Creation of Custom Widget!**
**You are now able to:**
* Understand how to Create and add custom widgets in a dashboard

  Continue to - [Exercise 5 - Extend the Dashboard with Scripting](../ex5/README.md)
