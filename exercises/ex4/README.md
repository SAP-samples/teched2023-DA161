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
 composites ready to be used in stories, story designers and developers spend less time building stories, and they can do further actions and customizations on the 
 composite as a whole as well, such as changing styling and adding scripts.
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
 
10. Change the Font Colour to whiteand add Text as **Title**
  <br>![](/exercises/ex4/Images/4img11.png)<br><br><br>

11. Add Two more Text Boxes as Subtitle abd Descritpion
 <br>![](/exercises/ex4/Images/4img12.png)<br><br><br>

12. Change the font text colour as white and adjust the font size accordingly.
  <br>![](/exercises/ex4/Images/4img13.png)<br><br><br>

13. Open the Left Side Panel --> Outline --> interface
  <br>![](/exercises/ex4/Images/4img14.png)<br><br><br>

14. Create following interfaces (Title, Subtitle, Description):

   <br>![](/exercises/ex4/Images/4img15.png)<br><br><br>

  1. SetDescription and Create New Arguments as **Text**
    <br>![](/exercises/ex4/Images/4img16.png)<br><br><br>
     Add formula 
  2. SetDescription and Create New Arguments as **Text**
     <br>![](/exercises/ex4/Images/4img17.png)<br><br><br>
  3. SetTitle and Create New Arguments as **Text**
     <br>![](/exercises/ex4/Images/4img18.png)<br><br><br>

15. Save the Composite
  <br>![](/exercises/ex4/Images/4img19.png)<br><br><br>

16. In DA161 Folder:
   <br>![](/exercises/ex4/Images/4img20.png)<br><br><br>

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
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/0c79cc18-8293-462e-80cb-e5738965b305)
  
2.  Add a custom widget – Echarts Sankey styling V1.0.0:
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/49e38d49-863b-41ae-b180-41581ea384de)

3. Click on Right Panel :
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/618dd3a0-7804-46c9-aae6-b4b3238b9a71)

4. Navigate to Builder Panel :
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/a0a5d959-b7e2-4df4-b7d7-fb4b95e713b9)

5. Click on Select model:
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/85398aa7-3d4f-4802-a466-27299ac637b1)

6. Choose BestRunJuice_Sample Model:
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/2bc1cb70-7dde-4343-ace2-dd923d40d01a)
   
7. Add Gross Margin as Measure and Location in Dimension  
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/85fe6e77-c925-48cb-9d1c-a0bfc5dc2c85)
 
8.Sankey chart is displayed for Gross Margin for different locations :
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/7b1c577c-19c4-4865-8c73-db50e63f5e2a)


## Summary
**You have completed the Creation of Custom Widget!**
**You are now able to:**
* Understand how to Create and add custom widgets in a dashboard

  Continue to - [Exercise 5 - Extend the Dashboard with Scripting](../ex5/README.md)
