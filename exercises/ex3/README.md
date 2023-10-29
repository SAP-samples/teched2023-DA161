# Exercise 3 - Customize the View Time Experience with No Code Features and Formatting


## Exercise 3.1 View Time Toolbar Customization


Objective: You should develop a basic understanding on how to create Customize your toolbar for various experiences of SAP Analytics Cloud Stories.

Estimated Time: 5 mins

Exercise Description: You as a Dashabord designer want to control the toolbar experience for your end users, and having all the toolbar features is not really required for end users.

Key Features:

Define what view mode of the story you need to control for your end users view vs embed mode of your stories.
Learn you to control the toolbar features via story settings.

## Summary

Now that you have ... 

## Exercise 3.2 Create a Theme (or Edit)


Objective: Theme a dashboard for easier and a better look and feel.

Estimated Time: 5 mins

Exercise Description: You have created an analytics dashboard with visualizations that show variances and thresholds, you added interaction for our viewers, but before you share the dashboard with your colleagues at BestRun, you need to make sure your dashboard is not only insightful but also looks visually appealing.

Key Features:

- Learn about the styling panel and how to format your visualizations
- Learn how to simplify your visualisations by hiding unnecessary information 
- Learn how to add an image or a logo to your dashboard
- Use Device Preview to preview your analytical content across various devices and screen sizes (i.e. Laptop, Tablet, Phone)

ℹ️Exercise check! Does your dashboard look like this screenshot?  

In this section we will cover theme and styling options in SAP Analytics Cloud to tweak your story into a professional dashboard. 

![4-1](https://user-images.githubusercontent.com/92877810/138502901-ddc92961-1536-4d94-9d3e-90061044aa91.png)

🚩Story creators can quickly change styling options for an entire story in the story preferences. This enables users to quickly apply corporate themes and sync their styling across different dashboards. We will first apply color and table preferences in this menu. 

1. Click **File**

2. Click **Edit Story**

3. Click **Preferences**

![4-2](https://user-images.githubusercontent.com/92877810/138502906-29891dc3-b417-49b2-8e4c-fc2a9f314796.png)

ℹ️Welcome to Story Preferences! 
  
In story preferences, story creators can choose to set standard theme and styling options for their entire story. This enables the business user with ease in quickly styling their entire story. Creators can choose to apply story preference changes to all pages, lanes, and tiles or only to newly created pages, lanes, and tiles. 

![4-3](https://user-images.githubusercontent.com/92877810/138502911-4c22720b-3d64-4b1f-9997-ed14c1461a7c.png)


🚩We want to apply this color palette to everything on our story, so we change the option to All. 

4. Click **All pages, lanes, and titles**

![4-8](https://user-images.githubusercontent.com/92877810/138502923-cf9f2e30-0719-4a74-b50a-b7d594a1a01b.png)

5. Scroll untill **Default Styling Template** is **Visible**

🚩We can choose different styling templates for our charts and tables based on dashboard needs. In this instance, we want our tables to appear in report-styling. 

6. Expand **Default Styling Template**

7. Click **Report Styling**

![4-9](https://user-images.githubusercontent.com/92877810/138502925-fc77e77c-b050-433b-81f5-76878444922f.png)



## Summary

Now that you have ... 

## Exercise 3.3 Customize the Dashboard for a Mobile Device


Objective: You should develop a basic understanding on how to design stories for mobile devices

Estimated Time: 5 mins

Exercise Description: As part of the exercise you would be able to use the mobile design features which helps to translate the dashboard to be nicely consumed in mobile devices.

Key Features:

- Learn how to use device preview to check how the story looks like on different devices
- Add responsive lanes to group widgets
- Adjust widgets position and size to specific devices
- Hide widgets from a small devide


ℹ️Exercise check! Creating responsive rules

In this section we will learn more about how a story designer defines responsive rules so that the story can be adapted to different devices.

You have already created a story and added widgets to a responsive page. Now you can use responsive rule to adjust their size and position to the device.

You can create a copy of the story TBD and Open in Edit Mode

1. To add a lane , Right click or Select ... and Add lane Below
   <img width="1674" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/9c252959-2ca6-4e48-8543-abbf38568ee7">

2. you should be able to see the lane created below
   <img width="1664" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/6da476a7-c0f3-4518-905d-1207fa2090d7">

🚩Let's group few widgets into this lane, 

3. Move "Gross Margin per Sales Manager" and "Gross Margin per Product, Workout Usage"
   <img width="1671" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/6e088f08-146c-4e45-96a7-2e766459525a">

🚩We will see how the current story looks like one smaller devices

4. Open the device list at the bottom and choose iOS Tablet
   <img width="1669" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/2320cd12-29d9-4e2a-bbc1-af095e8006a6">
   <img width="1669" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/d04637bd-6497-4651-9fee-b554b9a6232f">

A message appears to notify you about the unnsupported features on the device, some features aren't supported for specific iOS and Android devices.

  <img width="1652" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/7789d6fe-3f04-49f1-8eec-5bc92c2f3e08">

🚩We will now see how responsive rules can be set for the charts

5. Select the lane for which you want to set the responsive rules, in our example its the newly added lane
  <img width="1643" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/b592bca8-c605-4015-b8b3-7236f1b36295">
  
6. Click on the top icon to open the Builder panel which will show the Responsive Rule Configuration where you can set the position, size, and visibility of all the widgets in the lane for a specific device.
   <img width="1670" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/417d76fe-e1ac-430c-9d99-510e298e4c6b">

7. Activate the responsive rules configuration by toggling on the Activate button as below.
   <img width="1670" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/631f71da-0056-4e3a-be84-d30ab112c9fd">

8. Choose Widget Position as Free, which means widgets can be freely moved and stay in a specific position, irrespective of others and device types.
   <img width="1669" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/fcaf0c90-9ac3-470e-8593-01f2d9454e06">

9. Choose Add Widget
  <img width="1671" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/a829f93d-7cef-41b0-8296-4497cdc4a92a">

10. Open the Set the widget width list and select Chart_1, set the grid position from top to 9 and press enter, change will be reflected.
    <img width="1667" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/6a4bffd5-f227-4b1e-9529-f3efb0eb47f7">

    <img width="1660" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/81f04a88-e70c-472d-9418-494ab7353512">


11. Now change the device to small tablet
    <img width="1677" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/53222eee-e009-488e-9749-0d23bd1cb91d">

The responsive rules cascade down from larger to smaller devices. As there is no rule defined for small tablet, it now follows the one just defined for large tablet.

12. To overide and define a different rule for small tablet, switch on _Activate_.

    <img width="1671" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/a5425ab5-d31a-42ba-8a67-c6f9dce1b9df">

    
13. For small tablet, you'd like to display the charts in an auto type of layout, choose _Auto-Flow_ , which means the widgets will be placed sequentiually.
    <img width="1667" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/2b6af6a6-31f0-47cb-8b9b-b4066103d7ba">

14. Choose Add Widget
    <img width="1667" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/2af9a5e3-e5ad-4bfd-a0a1-2cb4d9187410">

15. Open the Set the widget width list and select Chart_1, set the widget width to 25 and press enter, change will be reflected and the widget will be pushed to fill the widhth and other widget will be pushed down.
    <img width="1661" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/f323b0f9-4a24-4fa6-8e36-80b743717fc0">

16. Set the Widget width for each widget to 25 so other widgets in the lane also occupy the same width when added.
    <img width="1666" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/42553867-33cb-41e7-8fec-49039ed91df4">

17. Choose the right panel button to close it.
    <img width="1660" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/5c3bd63b-2908-4616-8da9-0cc63d329ce8">

18. You can also the do the same for a Large Phone scenario, where Each Widget is already defined with a responsive rule to occupy the full screen width.
    <img width="1664" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/cf7b38e7-e875-48a6-b334-e3ed437febba">

You can scroll down on the phone screen to check the presense of the other designed widgets being displayed sequentially and full screen width.

🚩We will now see how to hide a widget when consuming over mobile devices

19. Table is not a great use case of mobile screens so let's try to hide it for small phones.
    <img width="1661" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/b0eb2c4f-a1cd-4393-9e0d-3545dcecbbf5">

20. Select Lane in which we see the table, in our case it is Lane_3, Open the Builder panel with the button to enable the right panel.
    <img width="1663" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/94202fe2-af96-48ff-908b-f07328eda9ef">

21. You can now set the widget visibility for Table widget and say hide the widget by adding it from the list
    <img width="1663" alt="image" src="https://github.com/SAP-samples/teched2023-DA161/assets/146448346/302fb2a7-9f13-466a-9daa-a1af481f441c">

    You can see that the table is hidden from the display screen of small phone.

    
## Summary

Now with this exercise you would be able to get an understanding of applying responsive configurations when designing content for mobile devivces successfully.

Continue to - [Exercise 4 - Exercise 4 Description](../ex4/README.md)
