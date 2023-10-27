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
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/80da7ab7-2943-4678-931b-72f22b1af7c0)

2.Navigate to stories and Click on Composites
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/13b90686-9d1c-4e4d-958a-bb9bfbd5517f)

3. Composites Page displays the recently viewed files and click on Create New Composite 
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/2bc7807f-fb57-4bd5-b023-0f9fa8033dcc)

4. You will be landed into New Composite designer page. In this example you will create a composite with Header with default title and description. 

   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/cf4725ad-cc02-4bab-bc0c-73608fbfdc31)

5. Drag and Drop Panel widget to the page.
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/d3b4e084-4f9d-4271-853e-833acc01a378)

6. Re-size the panel to full page

   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/0faefc06-f8fc-4015-8181-257df3c4702e)

   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/fbae1f62-80f2-410c-a810-5398be93f9ae)

7. Open the Right side Panel :
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/a20f4b0a-f2cd-402a-b3aa-7b7192280aa4)

8. Change the background colour
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/819566b4-e4b2-46ce-b688-9c0532ff2191)

9.Insert Text Box: 
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/fabeca7d-6e09-49c5-98a9-17a9afb60331)
10. Change the Font Colour to whiteand add Text as **Title**
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/c17802af-268d-4642-8e5a-50c9a10abc2c)

11. Add Two more Text Boxes as Subtitle abd Descritpion
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/e6854c5d-ae86-486d-b2a2-568895997058)

12. Change the font text colour as white and adjust the font size accordingly.
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/3c642d2e-9e0c-4de9-b26e-ac1f2b2eff36)

13. Open the Left Side Panel --> Outline --> interface
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/5e952f45-51da-41df-8cb5-7b4207ace5e9)

14. Create following interfaces (Title, Subtitle, Description):

   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/e9d0fdbc-29a1-4e34-943e-bff61caf1a40)

  1. SetDescription and Create New Arguments as **Text**
     ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/f96aec60-6828-48ad-8e98-087d779fd60f)
     Add formula 
  2. SetDescription and Create New Arguments as **Text**
     ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/b3ec2692-60a9-40fc-bc29-88010e9f6eae)
  3. SetTitle and Create New Arguments as **Text**
  4. ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/cc1ec454-2349-4966-b076-fb2410954f38)

15. Save the Composite
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/3417463e-9a6f-45f1-a0b5-801148122c8d)

16. In DA161 Folder:
    ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/fa9b6571-13a0-4472-9c9c-68662693ff1e)

17. Now you can use this composite in Stories. Open the Exercise 4 story and click on edit
    ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/1bd487c1-a490-42c6-860d-e22ef77c88b8)

18. Expand the left side Panel, click on composites and click on Import Icon

    ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/e0703be6-dcc4-4bf3-9d7c-d5a4dcb3bf40)


19. Import the newly created composite : Header – composite 
   ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/dd87ce23-ee04-472c-8551-3ffa62ff7a63)

20. Composite is imported sucessfully :
![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/cd44a546-d0e3-4d23-9c32-d64137c04fea)

21. Drag and Drop the composite :
![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/99c87b3f-6826-4861-bfa1-f166aa15b3d3)
![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/f77470f7-9e88-42ce-ba80-e8e5fd437916)

22. Resize the coposite header to the top of the page.
![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/3fbbe2dc-1e6d-40e4-b6a5-bc7df5c983c9)

23. CLick on Outline :
 ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/0bc6e64d-79f5-4def-a2ec-f5c06b0cdafb)

24. Click on Formula of Page_1 and select Oninitialization 
 ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/116448c4-3672-4ade-8b5d-576d9ffe18ed)

25. Add the formula
 ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/574220fe-4c51-49c6-83a2-9303a729cc96)

26. Save the Story
 ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/85b47775-97ce-46a7-8ed5-ceabb9aa2e5c)

27. Open the Story in New tab:
 ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/36d6eed4-ef3d-4132-87ad-d0ca929b7416)

28. Now you can see the Title, Subtitle and Description is updated.
  ![image](https://github.com/SAP-samples/teched2023-DA161/assets/146338540/607f198f-4f9b-415d-afc4-e5ba3e9c4841)

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
